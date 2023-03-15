# 在 Android O 的导航条上添加一个菜单和前进按钮来增强网页浏览

> 原文：<https://www.xda-developers.com/add-menu-forward-button-to-nav-bar-android-o-web-browsing/>

Android O 的[导航条定制器](https://www.xda-developers.com/android-o-preview-brings-nav-bar-customization-under-system-ui-tuner/)可以用于[的各种情况](https://www.xda-developers.com/tag/android-o/)，但当你根据上下文改变导航键时，它尤其有用。在我们的教程中，我们专注于寻找添加新的导航条键可以增强你的应用体验的情况，今天我们将向你展示如何在使用谷歌 Chrome 时向导航条添加**菜单**和**前进**按钮。这些按钮将极大地增强你的网络浏览体验，因为它胜过了一直到达右上角去点击菜单溢出按钮。

感谢 Eli Irvin 成为我的试验品并获得这个截屏。

正如你在上面看到的，两个新的导航条键被添加到了导航条中，但只是在使用谷歌浏览器的时候。左键打开 Chrome 的菜单(使用 [KEYCODE_MENU](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_MENU) )，而右键将触发浏览器中的“前进”功能(使用 [KEYCODE_FORWARD](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_FORWARD) )。不像我们以前的一些教程，我们没有在导航栏中使用任何自定义图标，所以你不需要去下载任何额外的应用程序。

我们将向你展示如何在你自己的设备上复制这个设置，这样你就可以学习如何定制你自己的导航条配置，但是如果你想直接跳到那个，我们也会在文章的最后提供一个下载链接。

*注意:这个教程与我们之前的关于使用 Chrome 浏览器时在导航条上添加滚动键的教程不兼容。您可以根据自己喜好选择要使用的概要文件或这个概要文件，但不能两者都选。*

* * *

Tasker 是必要的，因为它是我们用来检测我们在什么应用程序中的自动化应用程序，并通过 SecureTask 插件发送命令，这将处理我们的导航栏的更改。一旦您安装了这两个应用程序，我们需要设置它们。

为了让 Tasker 检测到我们在哪个应用程序中，我们需要授予它可访问性服务。这样做非常快，只需进入设置->辅助功能，并在服务列表中查找“Tasker”。启用辅助功能服务。

接下来，我们需要授予 SecureTask 修改设备上的系统设置的能力。为此，我们必须授予 SecureTask 一个称为 WRITE_SECURE_SETTINGS 的特殊权限，通常常规应用程序无法访问该权限，但用户可以通过 ADB 手动授予该权限。因此，您需要在您的机器上安装并运行 ADB 来使其工作。幸运的是，授予这个权限只是一次性的事情，如果你想跟随我的其他与 Android O 相关的导航条教程(其中[有许多](https://www.xda-developers.com/category/tutorials/))，你将需要 SecureTask，所以这绝对值得做。

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

打开 Tasker，按下 **+** 创建一个新的配置文件，并将其命名为“切换 Chrome Extra Keys”。选择**应用**上下文。滚动列表并**选择你的浏览器应用**(我选择了 Chrome)。

添加应用程序并返回 Tasker 主屏幕后，Tasker 会要求您附加一个现有任务或创建一个新任务。创建一个新任务，但不要费心给它起名字。进入任务编辑屏幕后，添加以下两个操作:

1.  插件->安全任务->安全设置。动作:**写**。设置:`secure sysui_nav_bar_left`。值:`key(82:com.android.systemui/2131230913)`
2.  插件->安全任务->安全设置。动作:**写**。设置:`secure sysui_nav_bar_right`。值:`key(125:com.android.systemui/2131231004)`

一旦完成，你可以退出回到 Tasker 的主菜单。我们现在将通过添加一个退出任务来结束这个配置文件，当您离开 Chrome 应用程序时将会触发该任务。此退出任务将清除这些图标的导航栏。

通过长按刚刚添加到配置文件的现有任务来添加退出任务。点击“添加退出任务”创建一个新任务，然后添加以下两个操作:

1.  插件->安全任务->安全设置。动作:**写**。设置:`secure sysui_nav_bar_left`。值:`null`
2.  插件->安全任务->安全设置。动作:**写**。设置:`secure sysui_nav_bar_right`。值:`null`

退出回到 Tasker 的主菜单，你就完成了。Tasker 现在会在使用 Chrome 时显示菜单和前进键，不使用 Chrome 时清除。

* * *

## 下载并导入

与所有 Tasker 相关教程一样，我们将提供 XML 文件供您下载和导入。从下面的 AndroidFileHost 下载. prf.xml 文件，并将其保存到您的内部存储。打开 Tasker，长按顶部的 Profiles 标签，直到你看到一个导入按钮。点击它，找到您刚刚保存的 XML 文件，然后选择它来导入它。确保您启用了 Tasker 的可访问性服务，并按照我在文章中提到的那样将 WRITE_SECURE_SETTINGS 授予了 SecureTask，否则此配置文件将不会在您的手机上执行任何操作！

[**从 AndroidFileHost**](https://www.androidfilehost.com/?fid=817550096634758768) 下载“切换 Chrome 额外按键”配置文件

如果你想知道在 Android O 中我们还可以在导航栏中添加哪些更有用的键，请查看我们的其他[教程](https://www.xda-developers.com/category/tutorials/)！