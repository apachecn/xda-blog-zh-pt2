# 如何在 Android O 上使用 YouTube 时显示画中画模式切换

> 原文：<https://www.xda-developers.com/how-to-display-a-picture-in-picture-mode-toggle-while-using-youtube-on-android-o/>

在我们的上一篇文章中，我们率先向您展示了如何在智能手机上使用 Android O 的新画中画(PiP)模式。概括地说，该方法包括发送由常数 171 定义的被称为 KEYCODE_WINDOW 的特定密钥。通过启用 SystemUI Tuner 中的[隐藏导航条定制器](https://www.xda-developers.com/android-o-preview-brings-nav-bar-customization-under-system-ui-tuner/)，然后添加一个触发键码的新导航条项目，这个键码最容易发送。

然而，使用这种方法意味着你将在导航栏中有一个永久的图标来切换画中画模式，即使它不适用。PiP 只适用于某些应用程序，即可以全屏显示视频内容的应用程序，因此在所有应用程序中都有一个按钮来切换它是没有意义的。在文章的最后，我们声明我们将向您展示如何基于每个应用程序显示画中画模式。这是如何做到的。

* * *

## 基于每个应用程序显示画中画切换

Tasker 是必要的，因为它是我们用来检测我们在什么应用程序中的自动化应用程序，并通过 SecureTask 插件发送命令，这将处理我们的导航栏的更改。一旦您安装了这两个应用程序，我们需要设置它们。

为了让 Tasker 检测到我们在哪个应用程序中，我们需要授予它可访问性服务。这样做非常快，只需进入设置->辅助功能，并在服务列表中查找“Tasker”。启用辅助功能服务。

接下来，我们需要授予 SecureTask 修改设备上的系统设置的能力。为此，我们必须授予 SecureTask 一个称为 WRITE_SECURE_SETTINGS 的特殊权限，通常常规应用程序无法访问该权限，但用户可以通过 ADB 手动授予该权限。因此，您需要在您的机器上安装并运行 ADB 来使其工作。幸运的是，授予这个权限是一次性的事情，我们将在未来的 Android O 相关教程中使用 SecureTask，所以我绝对建议你现在就这么做。如果你已经遵循了我之前的教程，在那里我告诉你安装自动工具，SecureTask 的功能不太丰富，但它已经足够满足我们的需要了。

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

打开 Tasker 并创建一个新的配置文件。将其命名为“切换画中画”选择**应用**上下文，寻找你想要启用导航键的视频应用(如 YouTube)。选择您想要的应用程序，然后返回到下一个创建任务。

Tasker 会要求您将任务附加到这个新的配置文件。当被询问时创建一个新任务，并给它命名(或者不命名)。当你进入任务创建界面时，进入**插件- >安全任务- >安全设置，添加一个新动作。**按铅笔图标打开 SecureTask 配置。

在动作下，挑**写**。在设置下，放置`secure sysui_nav_bar_right`。在值下面，放`key(171:com.android.systemui/2131230944)`。退出 Tasker 的主菜单。通过长按我们刚刚创建的新任务，然后选择“添加退出任务”，将退出任务添加到此配置文件中重复上面的操作，但是这一次将值设置为 null。

就是这样！当你进入 YouTube 应用程序(或你选择的任何其他应用程序)，你现在会看到一个图标在你的导航栏右侧弹出，允许你切换画中画模式。

* * *

## 下载并导入

与所有 Tasker 相关教程一样，我们将提供 XML 文件供您下载和导入。从下面的 AndroidFileHost 下载. prf.xml 文件，并将其保存到您的内部存储。打开 Tasker，长按顶部的 Profiles 标签，直到你看到一个导入按钮。点击它，找到您刚刚保存的 XML 文件，然后选择它来导入它。请确保您启用了 Tasker 的可访问性服务，并按照我在文章中提到的那样授予了 SecureTask 的 WRITE_SECURE_SETTINGS 权限，否则此配置文件将不会在您的手机上执行任何操作！

[**从 AndroidFileHost**](https://www.androidfilehost.com/?fid=457095661767150001) 下载“切换画中画”模式

如果你想知道我们还能通过 SecureTask 和 Android O 完成什么，请继续关注 XDA 门户网站，因为我们有很多东西可以分享。期待更多关于如何让 Android O 中的导航栏实现许多有用功能的教程！