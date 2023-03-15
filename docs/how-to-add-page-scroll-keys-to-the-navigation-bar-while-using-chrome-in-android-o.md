# 如何在 Android O 中使用 Chrome 时在导航栏中添加页面滚动键

> 原文：<https://www.xda-developers.com/how-to-add-page-scroll-keys-to-the-navigation-bar-while-using-chrome-in-android-o/>

本周，我们在 XDA 与[新的导航条定制者](https://www.xda-developers.com/android-o-preview-brings-nav-bar-customization-under-system-ui-tuner/)一起度过了一段愉快的时光。从自定义键到[控制音乐播放](https://www.xda-developers.com/how-to-enable-media-playback-nav-bar-controls-in-android-o-when-playing-music/)，在使用 YouTube 时切换[画中画模式，最后](https://www.xda-developers.com/how-to-display-a-picture-in-picture-mode-toggle-while-using-youtube-on-android-o/)[添加键来浏览您的电子邮件对话列表](https://www.xda-developers.com/add-forward-backward-keys-to-android-o-nav-bar-quickly-read-emails/)，有许多方法可以利用导航条定制器来增强您最喜爱的应用程序。最近，我们还向您展示了如何[将自定义图标添加到您的导航条键](https://www.xda-developers.com/how-to-add-custom-icons-to-the-navigation-bar-in-android-o/)中，这样您可以更容易地识别您的自定义键在您的 Tasker 个人资料中实际代表的内容。现在，我们将向您展示一个例子，它利用这一点在使用 Google Chrome 时向导航栏添加**页面滚动键。**

*感谢 Eli Irvin 测试了我的脚本并捕获了这段屏幕记录。*

正如你在上面的视频中看到的，当我的测试人员打开谷歌浏览器时，导航条上增加了两个新键，当按下时，可以上下滚动页面。发送的键码是 [KEYCODE_PAGE_DOWN](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_PAGE_DOWN) (#93)和 [KEYCODE_PAGE_UP](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_PAGE_UP) (#92)。弹出的图标很容易解释哪一个代表向下滚动，哪一个代表向上滚动，这要感谢我使用了来自[图标数据库](http://www.iconsdb.com/)的自定义图标。

我们将向你展示如何在你自己的设备上复制这个设置，这样你就可以学习如何定制你自己的导航条配置，但是如果你想直接跳到那个，我们也会在文章的最后提供一个下载链接。

* * *

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

在我们开始使用 Tasker 之前，您需要下载一个向下箭头和一个向上箭头图标，用作滚动键的自定义图标。下载适合您设备屏幕密度的自定义图标，并将其存储在/NavIcons 中。将这些图标命名为 down.png 和 up.png。现在我们准备好制作我们的 Tasker 个人资料了。

打开 Tasker，按右下角的+按钮创建一个新的配置文件。选择**应用**上下文，然后在应用选择屏幕中选择所有您希望滚动键出现的应用(如 Chrome)。

接下来，Tasker 将要求您选择一个现有的任务或创建一个新的任务。创建一个新任务，但不要费心给它起名字。进入任务创建屏幕后，我们需要向其中添加两个操作:

1.  A1: **插件- >安全任务- >安全设置**。动作:**写**。设置:`secure sysui_nav_bar_left`。值:`key(93:file:///storage/emulated/0/NavIcons/down.png)`
2.  A2: **插件- >安全任务- >安全设置**。动作:**写**。设置:`secure sysui_nav_bar_right`。值:`key(92:file:///storage/emulated/0/NavIcons/up.png)`

这两个操作将添加两个导航栏键，分别对应于您从互联网上下载的带有向下箭头和向上箭头图标的 KEYCODE_PAGE_DOWN 和 KEYCODE_PAGE_UP。这些按键只会在你选择的应用程序中出现，在我的例子中是 Chrome，所以我们需要在退出 Chrome 时通过添加退出任务来禁用它们。

您可以通过长按刚刚创建的任务(在 Tasker 的主屏幕上)并在弹出窗口中按“添加退出任务”来添加退出任务。登录后，添加以下两个操作:

1.  A1: **插件- >安全任务- >安全设置**。动作:**写**。设置:`secure sysui_nav_bar_left`。值:`null`
2.  A2: **插件- >安全任务- >安全设置**。动作:**写**。设置:`secure sysui_nav_bar_right`。值:`null`

随着这个退出任务的增加，Tasker 现在会在你退出 Chrome 应用程序时自动删除这些滚动键。这样，你只能在有用的时候看到这些滚动键。

## 下载并导入

与所有 Tasker 相关教程一样，我们将提供 XML 文件供您下载和导入。从下面的 AndroidFileHost 下载. prf.xml 文件，并将其保存到您的内部存储。打开 Tasker，长按顶部的 Profiles 标签，直到你看到一个导入按钮。点击它，找到您刚刚保存的 XML 文件，然后选择它来导入它。确保您启用了 Tasker 的可访问性服务，并按照我在文章中提到的那样将 WRITE_SECURE_SETTINGS 授予了 SecureTask，否则此配置文件将不会在您的手机上执行任何操作！

[**从 AndroidFileHost**](https://www.androidfilehost.com/?fid=529152257862715743) 下载“在 Chrome 中切换滚动键”配置文件

注意:如果您下载了上面的配置文件，您需要确保您已经下载了向上箭头和向下箭头图标，并将它们保存到/NavIcons 中，如 up.png 和 down.png。否则，您需要手动编辑入口任务中的操作，以指向这些新图标。

如果你想知道我们还可以在导航栏中添加什么有用的键来让浏览 Chrome 更愉快，我们将在未来的教程中向你展示一个替代设置。敬请关注门户网站，获取更多教程！