# 如何在 Android O 的导航条上添加前进/后退键来快速阅读邮件

> 原文：<https://www.xda-developers.com/add-forward-backward-keys-to-android-o-nav-bar-quickly-read-emails/>

如果你花在智能手机上的时间包括浏览大量的电子邮件，那么你可能会发现当你试图查看整封电子邮件时，意外地切换消息是很烦人的。得益于 Android O 中新的[导航条定制器，我们可以在导航条中添加新的按键来执行定制动作。在这种情况下，我们将在导航栏中添加两个新键，每当我们使用 Gmail 应用程序时，**将在您的电子邮件列表中向前/向后移动。**](https://www.xda-developers.com/android-o-preview-brings-nav-bar-customization-under-system-ui-tuner/)

*感谢 Eli Irvin(再次)为我测试，并捕捉到上面的屏幕记录。*

如果你一直在关注我们之前的 Android O 教程，你就会知道我们将如何解决这个问题。这个教程和我们的[画中画按钮教程](https://www.xda-developers.com/how-to-display-a-picture-in-picture-mode-toggle-while-using-youtube-on-android-o/)非常相似，所以如果你已经通读过了，那么这个应该很容易。

* * *

## 在 Gmail 中向导航栏添加前进/后退键

Tasker 是必要的，因为它是我们用来检测我们在什么应用程序中的自动化应用程序，并通过 SecureTask 插件发送命令，这将处理我们的导航栏的更改。一旦您安装了这两个应用程序，我们需要设置它们。

为了让 Tasker 检测到我们在哪个应用程序中，我们需要授予它可访问性服务。这样做非常快，只需进入设置->辅助功能，并在服务列表中查找“Tasker”。启用辅助功能服务。

接下来，我们需要授予 SecureTask 修改设备上的系统设置的能力。为此，我们必须授予 SecureTask 一个称为 WRITE_SECURE_SETTINGS 的特殊权限，通常常规应用程序无法访问该权限，但用户可以通过 ADB 手动授予该权限。因此，您需要在您的机器上安装并运行 ADB 来使其工作。幸运的是，授予这种权限只是一次性的，我们将在未来的 Android O 相关教程中使用 SecureTask(还有几个教程)，所以绝对值得这么做。

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

打开 Tasker 并创建一个新的配置文件。将其命名为“Gmail 滚动键”选择**应用**上下文，并查找您想要启用导航栏键的电子邮件应用(如 Gmail)。选择所需的应用程序，然后返回到下一个创建任务。

Tasker 会要求您将任务附加到这个新的配置文件。当被询问时创建一个新任务，并给它命名(或者不命名)。我们将在这个条目任务中创建两个操作，如下所示:

1.  A1: **插件- >安全任务- >安全设置**。动作:**写**。设置:`secure sysui_nav_bar_left`。值:`key(21:com.android.systemui/2131230907)`
2.  A2: **插件- >安全任务- >安全设置。**动作:**写**。设置:`secure sysui_nav_bar_right`。值:`key(22:com.android.systemui/2131231004)`

入口任务(当你进入电子邮件应用程序时运行的任务)就到此为止，现在我们需要添加一个退出任务，以便在我们离开电子邮件应用程序时禁用这两个键。通过长按进入任务并在弹出时选择“添加退出任务”选项来创建退出任务。我们还将在此任务中创建两个操作，如下所示:

1.  A1: **插件- >安全任务- >安全设置**。动作:**写**。设置:`secure sysui_nav_bar_left`。值:`null`
2.  A2: **插件- >安全任务- >安全设置。**动作:**写**。设置:`secure sysui_nav_bar_right`。值:`null`

就是这样！现在，当你进入 Gmail 应用程序(或你选择的任何其他电子邮件应用程序)时，你会看到两个导航键，允许你在电子邮件列表中向前或向后移动。

* * *

## 下载并导入

与所有 Tasker 相关教程一样，我们将提供 XML 文件供您下载和导入。从下面的 AndroidFileHost 下载 prf.xml 文件，并将其保存到您的内部存储。打开 Tasker，长按顶部的 Profiles 标签，直到你看到一个导入按钮。点击它，找到您刚刚保存的 XML 文件，然后选择它来导入它。确保您启用了 Tasker 的可访问性服务，并按照我在文章中提到的那样将 WRITE_SECURE_SETTINGS 授予了 SecureTask，否则此配置文件将不会在您的手机上执行任何操作！

[**从 AndroidFileHost** 下载“Gmail 滚动键”配置文件](https://www.androidfilehost.com/?fid=529152257862715654)

如果你想知道我们还能通过 SecureTask 和 Android O 完成什么，请继续关注 XDA 门户网站，因为我们有更多内容可以分享。期待更多关于如何让 Android O 中的导航栏实现许多有用功能的教程！