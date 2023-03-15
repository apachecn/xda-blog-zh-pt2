# 如何在文本输入时将左/右键盘光标添加到导航条

> 原文：<https://www.xda-developers.com/how-to-add-leftright-keyboard-cursors-to-the-nav-bar-during-text-input/>

自从谷歌推出搭载 Android 4.0 冰淇淋三明治的 [Galaxy Nexus](https://forum.xda-developers.com/galaxy-nexus) 以来，定制导航栏一直是定制 rom 的主要内容(我们不谈论摩托罗拉 Xoom 和蜂巢围绕这些部分)。虽然一些原始设备制造商在他们的手机上提供了某种软件按键定制，但只有在[第一次 Android O 开发者预览版](https://www.xda-developers.com/google-announces-android-o-developer-preview-1-available-for-supported-devices/)中，谷歌才正式包括[导航条定制](https://www.xda-developers.com/android-o-preview-brings-nav-bar-customization-under-system-ui-tuner/)。然而，我们论坛上的用户发现，自 Android Nougat 以来，谷歌的导航条调谐器实际上[隐藏在 AOSP，但直到本周我们才发现，这个隐藏的导航条调谐器可以通过 shell 命令](https://forum.xda-developers.com/nexus-6p/themes-apps/mod-enable-navbar-tuner-nougat-t3447478)[访问，而不需要 root、自定义 rom 或系统 UI 模块](https://www.xda-developers.com/nav-bar-customization-was-hidden-in-stock-nougat-all-along-and-it-never-needed-root/)。现在可以实现流行的自定义 ROM 功能了吗，比如在导航条上添加键盘光标？

没错，这一发现为无根的导航条定制打开了闸门，站在最前沿的是 XDA 资深会员 [paphonb](https://forum.xda-developers.com/member.php?u=6018897) ，他开发了一个名为[定制导航条](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967)的应用程序，帮助用户修改导航条，而不必运行 shell 命令。他的应用程序功能丰富；例如，它提供了一个[任务器](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm)插件，所以你可以根据上下文改变导航条。由于许多用户不熟悉 Tasker，我写这些教程来帮助用户利用导航条定制。

在本教程中，我将向你展示如何**在键盘显示时将左/右键盘光标添加到导航条(Android 7.0+，不需要 root！)**这个教程类似于我为 [Android O 用户](https://www.xda-developers.com/how-to-add-leftright-cursors-to-the-nav-bar-during-text-input-on-android-o/)写的那个，但是这个教程会更容易理解，因为它在 Android 牛轧糖上工作。

是的，是的，我们知道快捷键和 Gboard 都有内置的键盘光标。然而，并不是每个键盘都这样做，在我看来，使用导航条上的按钮比使用 Swiftkey(占用空间)或 Gboard(需要不精确地滑过空格键或切换到特殊模式)中的按钮更方便。

* * *

**推荐阅读 1** : [如何改变你的导航条图标或者重新排列没有根的按钮](https://www.xda-developers.com/how-to-change-your-nav-bar-icons-or-re-arrange-the-buttons-without-root/)

**推荐阅读 2:** [如何在播放音乐时给导航条添加媒体播放控件](https://www.xda-developers.com/how-to-add-media-playback-controls-to-the-nav-bar-when-playing-music/)

* * *

## 在文本输入过程中向导航条添加左/右键盘光标

### 要求

**系统** **需求**:你需要一个兼容 AOSP 导航条定制器的 Android 7.0+设备。已知谷歌 Nexus、Pixel 和一些索尼/HTC 手机可以工作。大多数接近库存 Android 的设备很可能没有删除 AOSP 导航条定制器，应该可以工作。这意味着它可能无法在你的 LG、三星或华为/Honor 设备上运行。见本帖第一篇[的“兼容性”部分。(注意:您设备的 OEM 可能没有列在该线程中。要确定你的设备是否兼容，唯一的方法就是试用这个应用程序，我们将在下面告诉你怎么做。)](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967)

**App 需求:**

我们需要自定义导航条的原因很明显——这个应用程序允许我们修改导航条来显示这些媒体播放键。(从技术上来说，我们实际上并不需要这个应用程序来进行这些修改，因为我们可以使用 shell 命令或其他 Tasker 插件，但是为了让我们的用户更容易，我们将展示如何使用这个精彩的应用程序进行设置。)AutoInput Beta 是一个 Tasker 插件，它将帮助我们检测键盘何时显示(从技术上讲，该插件将检测文本输入框何时显示，而不是键盘本身何时显示，但这是我们能够获得的最接近的结果)。最后，Tasker 在 AutoInput Beta 和自定义导航栏之间架起了一座桥梁。

### 设置:自定义导航栏

我们需要做的第一件事是确保你可以修改你设备上的导航条。如果你的设备是在[自定义导航栏线程](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967/)中列出的兼容设备之一，那么它很有可能是兼容的。我们可以通过运行这个应用程序附带的简短教程来验证。

从谷歌 Play 商店安装应用[，然后打开应用并继续进入介绍性屏幕。自定义导航栏将要求您授予它一个名为 WRITE_SECURE_SETTINGS 的特定权限，以便继续使用该应用程序。有两种方法可以做到这一点，如申请中所述。](https://play.google.com/store/apps/details?id=xyz.paphonb.systemuituner)

1.  如果您有根设备，自定义导航栏将请求超级用户访问。授予它，应用程序将自动授予自己此权限。
2.  如果您的设备不是根设备，那么您需要通过 ADB 授予许可。在机器上打开命令提示符/终端，然后输入以下命令:`adb shell pm grant xyz.paphonb.systemuituner android.permission.WRITE_SECURE_SETTINGS`

一旦你通过上述两种方法中的任何一种授予应用程序此权限，那么应用程序将继续进行兼容性测试。如果你的导航条没有变化，那么你很不幸的不走运。如果你的导航条变成显示一个右箭头按钮，那么恭喜你的设备是受支持的！我们现在可以继续修改我们的导航栏。

### Setup: AutoInput Beta

为了让 AutoInput Beta 检测文本输入框何时显示，我们必须启用它的辅助功能服务。你只需进入设置->辅助功能(取决于你的设备，它可能在另一个子菜单中)并在服务列表中找到自动输入。点击它，然后点击切换到顶部，以启用辅助功能服务。

* * *

### 辅导的

一旦您确认自定义导航栏与您的设备兼容，并且为 AutoInput Beta 启用了辅助功能服务，就该进行设置了。我们需要做的第一件事是在自定义导航栏中创建一个新的配置文件，当启用时，会将左/右键添加到我们的导航栏中。以下是逐步说明:

1.  打开自定义导航栏应用程序，点击自动化部分下的**个人资料**。
2.  点击右上角的 **+** 图标，添加新的个人资料。
3.  点击刚刚创建的个人资料。
4.  在配置文件部分，点击名称，并将此配置文件命名为**键盘光标**。
5.  在“额外左按钮”下点击**类型**。将类型设置为**键码**。
6.  在“额外的左按钮”下应该有两个新的选项叫做键码和图标。点击**键码**。
7.  向下滚动并选择 **Dpad Left** 。
8.  现在点击“额外左按钮”部分下的**图标**。
9.  选择**人字形左**图标。
10.  对“额外的右按钮”重复步骤 5-9 但是，将键码设置为 **Dpad Right** 并将图标设置为 **chevron right** 。
11.  回到剖面图部分的顶部，点击**启用**来测试该剖面图。如果你看到导航条上弹出一个左右箭头，那么这是正常的。

现在我们已经设置了自定义导航栏配置文件，我们准备设置 Tasker 配置文件，它将在检测到/消失文本输入时启用/禁用此配置文件。所有这些都将在一个概要文件中完成。以下是说明:

1.  打开 Tasker，点击右下角的 **+** 图标创建一个新档案。
2.  选择**事件**上下文。
3.  选择**插件- >自动输入- > UI 动作**。点击铅笔图标打开自动输入配置。
4.  一旦进入自动输入 UI 动作配置，点击**动作类型**。选择**输入元素聚焦**和**输入元素聚焦丢失**。忽略元素文本部分。完成后，点击顶部的勾号图标。
5.  返回 Tasker 的主屏幕，Tasker 会要求您将任务附加到此配置文件。选择创建新任务。不要为任务命名。
6.  点击底部中间的 **+** 图标，为该任务添加一个操作。
7.  如果，则进入**任务- >。如果%aifocus ~ true** ，则设置为**。～是“匹配”**
8.  第二个动作，进入**插件- >自定义导航栏**。点击铅笔图标打开配置。对于该动作，选择**启用配置文件**。在选择配置文件下，选择我们之前制作的**键盘光标**配置文件。
9.  对于第三个动作，转到**任务- >其他**。
10.  第四个动作，进入**插件- >自定义导航栏**。点击铅笔图标打开配置。对于操作，选择**禁用个人资料。**在选择轮廓下，再次选择**键盘光标**轮廓。
11.  对于最后一个动作，转到**任务- >结束 If。**
12.  按 back，退出任务编辑屏幕。

一旦你完成了上面所有的步骤，我们就完成了！继续尝试，打开任何文本输入框，看看你的导航条是否改变，以包括左/右键盘光标。如果它不起作用，请仔细检查 AutoInput 的辅助功能服务是否已启用。

* * *

### 使用 Shell 命令

鉴于使用 XDA 资深会员 [paphonb](https://forum.xda-developers.com/member.php?u=6018897) 的[定制导航栏](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967)应用程序是如此简单，我真的不认为有必要提供详细的分步说明，说明如何使用其他 Tasker 插件，如 [SecureTask](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967) 或[自动工具](https://play.google.com/store/apps/details?id=com.joaomgcd.autotools&hl=en)(或 Tasker 中的 run shell 功能)。然而，这当然是可能的，至少我会提供一个不使用 paphonb 的应用程序复制这个设置所需的命令的摘要。

您需要做的第一件事是安装 SecureTask 或 AutoTools。您将需要授予 WRITE_SECURE_SETTINGS 权限来控制您选择的应用程序，以便控制导航栏调谐器。

对于 SecureTask:

```
 adb shell pm grant com.balda.securetask android.permission.WRITE_SECURE_SETTINGS 
```

对于自动工具:

```
 adb shell pm grant com.joaomgcd.autotools android.permission.WRITE_SECURE_SETTINGS 
```

接下来，您需要下载将用于上一个/下一个键的图标。你将需要 PNG 格式的图标，至于大小，你可以通过在 Material.io 上查找你的[设备的显示密度指标并将其与](https://material.io/devices/)[图标大小参考图表](http://iconhandbook.co.uk/reference/chart/android/)相关联来确定你需要的图标大小。IconsDB.com 是免费图标的好资源。将您将要用作 left.png 和 right.png 的图标保存在存储根目录下的/NavIcons 文件夹中。

最后，您将输入以下命令来显示媒体控制按钮:

```
 settings put secure sysui_nav_bar "key(21:file:///storage/emulated/0/NavIcons/left.png),back;home;recent,key(22:file:///storage/emulated/0/NavIcons/right.png)" 
```

其中键#21 指[键码 _ DPAD _ 左](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_DPAD_LEFT)，键#22 指[键码 _ DPAD _ 右](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_DPAD_RIGHT)。

然后将导航条键恢复到默认布局(即文本输入焦点已丢失)，输入该命令:

```
 settings put secure sysui_nav_bar "space,back;home;recent,menu_ime" 
```

本质上，Tasker 配置文件的设置将与上面的设置完全相同，除了在两个自定义导航栏 Tasker 操作的位置，您将使用 SecureTask/AutoTools/Run Shell。请注意，除非您是 rooted 用户并使用 Tasker 中的“run shell”操作，否则将这些命令导入 SecureTask 或 AutoTools 的过程完全由您决定。这真的不难做到，但许多用户发现只使用 paphonb 的应用程序更容易使用，所以我不会在这里进行更多的细节。

* * *

### 结论

本教程到此为止。当我发现改变你的导航条有更多的实际用途时，我会偶尔发布一些教程，特别是在使用 Tasker 这样的自动化应用程序时。如果你有任何聪明的想法，但不知道如何自己实现，请使用我们的[提示表](https://www.xda-developers.com/tip-us/)给我们发消息，或者直接给我们发电子邮件，我们会尽最大努力解决它！

请尽你所能支持 XDA 开发者！我们最近发现，有几个博客剪切、复制、粘贴了我们的原始教程和我们的用户在论坛上分享的其他内容。这些博客一直试图将我们在编写这些教程中所做的大量努力归功于自己，而不是自己提供高质量的内容。你不会在我们的[教程类别](https://www.xda-developers.com/category/tutorials/)中找到这样的教程，也不会在其他地方找到来自我们论坛的教程。

在推特、[谷歌+](https://plus.google.com/+xda) 、[脸书](https://www.facebook.com/xda.developers/)或 [YouTube](https://www.youtube.com/user/xdadevelopers) 上关注我们。查看我们的 [XDA 实验室](https://www.xda-developers.com/xda-labs/)应用程序，快速浏览我们的论坛(并考虑获得 [XDA 无广告](https://forum.xda-developers.com/ad-free/)！)上，如果你有一台 OnePlus 3 或 OnePlus 3T，请查看我们最近发布的 [XDA Feed](https://www.xda-developers.com/introducing-xda-feed/) 应用程序！谢谢，请继续关注我们的下一个教程！