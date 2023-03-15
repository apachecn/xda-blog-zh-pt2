# Android 7.1+有一个“恐慌检测”模式，可以检测疯狂的后退按钮按压

> 原文：<https://www.xda-developers.com/android-7-1-has-a-panic-detection-mode-that-detects-frantic-back-button-presses/>

虽然像我们这样的以 Android 为中心的网站的许多读者不太可能遇到流氓应用程序危害他们系统的情况，但对于一般人来说可能不是这样。几乎每周我们都会从各种安全研究人员那里听到针对 Android 用户的新恶意软件。大多数这些恶意攻击可以通过检查权限或避免安装外观粗糙的应用程序来避免，尽管我们确实建议我们的读者将手机的安全掌握在自己手中，但谷歌有责任保护每一部 Android 手机。为此，该公司悄悄在 Android 7.1 牛轧糖中引入了一个新的安全功能，名为“**恐慌检测**”，它会连续监听多次后退按钮，然后将用户返回到他们的主屏幕。

很简单，如果一个流氓应用程序试图劫持用户的屏幕并阻止用户离开(也许是通过实现一个可访问性服务来拦截所有的按键事件)，Android 将自己覆盖该应用程序以带回主屏幕。然后，用户可能会从启动器中卸载恶意应用程序。

这一功能没有被发现，这是可以理解的，因为谷歌可能不想向世界宣传他们正在摧毁恶意应用程序的一种方式。但是快速浏览一下 Android 的开源代码就会发现这个简单的功能是如何在支持它的设备上工作的。

* * *

### 检查代码

首先，你的设备运行的是 Android 7.1+并不代表实际上启用了这种恐慌检测行为。确定该功能是否开启的值可以在 SystemUI APK 的`config.xml`文件中找到。

```

0 - Nothing
1 - Go to home

<integer name="config_backPanicBehavior">0</integer> 
```

默认情况下，Android 对紧急按下后退按钮的反应是什么都不做。然而，如果整数值`config_backPanicBehavior`被设置为 1，这就是 Android 新的保护措施发挥作用的地方。

在`PhoneWindowManager.java`中，我们可以看到这个特性是如何实现的。首先，该文件定义了两件事:系统需要按多少次后退按钮才能确定用户“惊慌失措”，然后根据这种状态采取什么行动。

```

static final int PANIC_PRESS_BACK_COUNT = 4;
static final int PANIC_PRESS_BACK_NOTHING = 0;
static final int PANIC_PRESS_BACK_HOME = 1; 
```

默认情况下，系统需要连续按 4 次后退按钮才能进入紧急模式。该函数是否使用整数值`PANIC_PRESS_BACK_NOTHING`或`PANIC_PRESS_BACK_HOME`取决于 SystemUI APK 内配置文件中的值。

无论该值如何，每次多次按下后退按钮都会被检查，以确定是否会被视为紧急按下。首先，系统拦截对 [KEYCODE_BACK](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_BACK) 键事件的按下，并检查系统是否设置为检查该键的多次按下或长时间按下。然后，系统检查是否应该将同一个 KEYCODE_BACK 键事件的向上按压传递给用户应用程序。

在`interceptBackKeyDown()`方法中，如果后退按键计数器在 1 和 3 之间，那么系统跳过多次按键检测超时，因为紧急检测需要至少 4 次按键才能采取任何行动。

接下来，一旦用户将手指从 back 键移开，触发了 up 事件，`interceptBackKeyUp`将 back 键计数器加 1。然后，它将消息排队 300 毫秒。这样做的原因是因为系统在决定后退按钮的按下是否是多次按下事件的一部分时预留了 300 毫秒的延迟时间。如果是，那么用户可能会慌乱地按下按钮，因此系统不应该向用户应用程序发送按键事件。

300 毫秒多次按压超时值存储在安全设置“`multi_press_timeout`”中，如下所示。

```
 /**
* The duration in milliseconds between the first tap's up event and the second tap's
* down event for an interaction to be considered part of the same multi-press.
* @hide
*/
public static final String MULTI_PRESS_TIMEOUT = "multi_press_timeout"; 
```

默认情况下，该值设置为 300 毫秒。

```
 /**
* Defines the default duration in milliseconds between the first tap's up event and the second
* tap's down event for an interaction to be considered part of the same multi-press.
*/
private static final int DEFAULT_MULTI_PRESS_TIMEOUT = 300 
```

然后，如果确实检测到多次按压(在 300 毫秒内超过 1 次后退按钮完成向上/向下按压)，系统调用`backMultiPressAction`方法来确定采取什么动作。最后，返回按钮计数器被重置为 0。

虽然这是一个非常小的、未公开的功能，但仍然很高兴看到谷歌正在幕后做些什么，以使 Android 对普通用户来说更加安全。