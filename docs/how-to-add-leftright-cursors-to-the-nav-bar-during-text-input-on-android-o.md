# 如何在 Android O 上输入文本时在导航条上添加左/右光标

> 原文：<https://www.xda-developers.com/how-to-add-leftright-cursors-to-the-nav-bar-during-text-input-on-android-o/>

自定义 rom 中最古老的功能之一是手动移动文本输入光标的能力，这一功能尚未进入 Android 的正式版本。根据您的 ROM，您可以使用音量按钮或按导航条上的虚拟按钮来移动文本输入光标。如果你在打字时经常回去修改，这个功能是必不可少的，但是如果没有定制的 ROM，你将无法享受它。

然而，如果你运行的是 Android O 开发者预览版，它在 SystemUI Tuner 下隐藏了一个新的[导航条定制器](https://www.xda-developers.com/android-o-preview-brings-nav-bar-customization-under-system-ui-tuner/)，那么你可以在导航条上添加左/右键盘光标。你所需要做的就是将左边的导航条键设置为[键码 _ DPAD _ 左](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_DPAD_LEFT) (#21)，将右边的导航条键设置为[键码 _ DPAD _ 右](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_DPAD_RIGHT) (#22)。至于图标，使用默认的左/右箭头图标最有意义。正如 *Android Police* ，**指出的那样，[这种方法肯定是有效的，但它有缺陷，因为它要求这些键被永久地*放置在*导航条上。](http://www.androidpolice.com/2017/03/22/add-permanent-leftright-cursor-buttons-nav-bar-android-o/)**

如果[你已经](https://www.xda-developers.com/how-to-display-a-picture-in-picture-mode-toggle-while-using-youtube-on-android-o/)[跟随](https://www.xda-developers.com/add-forward-backward-keys-to-android-o-nav-bar-quickly-read-emails/)我的[之前的](https://www.xda-developers.com/how-to-add-page-scroll-keys-to-the-navigation-bar-while-using-chrome-in-android-o/) [教程](https://www.xda-developers.com/how-to-add-custom-icons-to-the-navigation-bar-in-android-o/)上了 Android O 导航条定制器，那么你就会知道，可以根据我们想要的任何标准来改变两个导航条键。因此，为了使我们的新文本输入/键盘光标更具上下文意识，我们可以使用 Tasker**仅在 Android O 上显示文本输入时显示键盘光标按钮。**我们将在本教程中提供逐步说明，但您也可以跳到底部下载配置文件以导入它。

*感谢 Eli Irvin 测试我的 Tasker 个人资料并捕获此屏幕记录！*

* * *

## 文本输入过程中在导航条中显示左/右光标

Tasker 是必要的，因为它是我们正在使用的自动化应用程序，当 AutoInput 检测到文本字段时，将通过 SecureTask 插件发送命令来更改我们的导航栏。安装完这些应用程序后，我们需要对它们进行设置。

虽然没有任何直接的方法来检测键盘何时显示，但我们可以监视的一件事是文本字段何时成为焦点。通过观察文本框中闪烁的光标，您将知道文本输入字段何时处于焦点上。我们可以通过使用刚刚发布的 AutoInput 的最新测试版来监控这些，这使我们能够实现这一点。为了让 AutoInput 监视文本字段，我们需要启用它的可访问性服务。

这样做非常快，只需进入设置->辅助功能，并在服务列表中寻找“自动输入”。启用辅助功能服务。

接下来，我们需要授予 SecureTask 修改设备上的系统设置的能力。为此，我们必须授予 SecureTask 一个称为 WRITE_SECURE_SETTINGS 的特殊权限，通常常规应用程序无法访问该权限，但用户可以通过 ADB 手动授予该权限。因此，您需要在您的机器上安装并运行 ADB 来使其工作。幸运的是，授予这种许可只是一次性的事情，所以如果你打算遵循我们的其他 Android O 相关指南，你最终将需要这样做。

### 建立亚洲开发银行

你需要做的第一件事是为你的操作系统下载 ADB 二进制文件。你可以在这里这样做。一旦你下载了它们，如果你用的是 Windows，你需要确保你有合适的[驱动程序](https://developer.android.com/studio/run/win-usb.html)。

一旦你将二进制文件解压到一个单独的文件夹并安装了驱动程序，我们接下来需要在智能手机上启用 USB 调试。为此，请打开“设置”,然后进入“关于手机”。点击 7 次 Build Number 直到你得到一个对话框告诉你你已经解锁了开发者选项。您现在可以在“设置”中访问开发人员选项。显然在 Android O 中，你必须输入你的 pin/密码才能打开开发者选项。这样做，并寻找 USB 调试，然后启用它。

现在插上你的手机，在你解压 ADB 二进制文件的同一个目录下打开一个命令提示符。(Windows 用户，按住 shift 键并右键单击该文件夹，然后选择“在此打开命令提示符”)在命令提示符下键入`adb devices`。你会看到一条消息，说亚行服务器正在启动，然后在你的手机上，你会看到一个提示，要求你授予你的计算机亚行访问。接受吧。现在，当您在命令提示符下输入`adb devices`时，您应该会看到您的设备的序列号，如果是这样，那么您就成功了。

### 向 SecureTask 授予 WRITE_SECURE_SETTINGS

打开 ADB 命令提示符后，输入以下命令授予 SecureTask 必需的权限。

```
 adb shell pm grant com.balda.securetask android.permission.WRITE_SECURE_SETTINGS 
```

SecureTask 现在将能够在没有 root 访问权限的情况下修改系统设置！现在我们准备向 Tasker 前进。

### 设置任务者配置文件

打开 Tasker，按+按钮创建一个新的配置文件。将其命名为**键盘光标**并选择**事件**上下文。转到**插件- >自动输入- > UI 动作**。对于动作类型，选择**输入元素聚焦**和**输入元素聚焦丢失**。将元素文本留空。添加这个 AutoInput 上下文将启动 AutoInput 的 monitor 服务，以检测文本输入字段何时获得或失去焦点，并将其作为我们可以读取的布尔值(真/假)存储在一个变量中。

一旦你完成了个人资料，Tasker 会要求你添加一个任务。选择创建一个新的任务，但是不要麻烦给它一个名字。进入任务编辑屏幕后，添加以下操作:

1.  **A1** : *任务- > If* 。将其设置为 if %aifocus ~ true。这将是 AutoInput 检测到文本输入字段处于焦点时的条件。接下来的两个动作会将导航条键设置为 DPAD 左和 DPAD 右。
2.  **A2** : *插件- >安全任务- >安全设置*。动作:**写**。设置:`secure sysui_nav_bar_left`。值:`key(21:com.android/systemui/2131230907)`。
3.  **A3** : *插件- >安全任务- >安全设置*。动作:**写**。设置:`secure sysui_nav_bar_right`。值:`key(22:com.android/systemui/2131231004)`。
4.  **A4** : *任务- >其他*。当%aifocus 设置为 false 时，文本输入字段将失去焦点。然后我们将清除导航条键。
5.  **A5** : *插件- >安全任务- >安全设置*。动作:**写**。设置:`secure sysui_nav_bar_left`。值:`null`。
6.  **A6** : *插件- >安全任务- >安全设置*。动作:**写**。设置:`secure sysui_nav_bar_right`。值:`null`。
7.  **A7** : *任务- >结束如果*。

您已经完成了这个 Tasker 脚本。现在，每当 AutoInput 检测到文本输入字段处于焦点时(这与您的键盘何时显示相关)，您将会看到两个新的导航条光标键，当文本输入字段不再处于焦点时，它们将会消失。

* * *

## 下载并导入

与所有 Tasker 相关教程一样，我们将提供 XML 文件供您下载和导入。从下面的 AndroidFileHost 下载. prf.xml 文件，并将其保存到您的内部存储。打开 Tasker，长按顶部的 Profiles 标签，直到你看到一个导入按钮。点击它，找到您刚刚保存的 XML 文件，然后选择它来导入它。请确保您已经启用了 AutoInput 的辅助功能服务，并且已经将 WRITE_SECURE_SETTINGS 授予了我的文章中提到的 SecureTask，否则此配置文件将不会在您的手机上执行任何操作！

[**从 AndroidFileHost** 下载“键盘光标”配置文件](https://www.androidfilehost.com/?fid=817550096634758746)

如果你想知道我们还可以在导航栏中添加哪些有用的按键，让 Android O 成为更愉快的体验，我们将在未来的教程中向你展示另一种设置。