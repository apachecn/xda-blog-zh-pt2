# 在 Android O 的手机通话中，在导航条上增加一个联系人快捷方式和一个结束通话按钮

> 原文：<https://www.xda-developers.com/add-contacts-shortcut-and-end-call-button-to-nav-bar-during-phone-calls-android-o/>

如果你一直在关注我们的[教程提要](https://www.xda-developers.com/category/tutorials/)，那么你现在应该知道我们喜欢寻找利用 Android O 的新[导航条定制器](https://www.xda-developers.com/android-o-preview-brings-nav-bar-customization-under-system-ui-tuner/)的方法。通过流行的自动化应用 Tasker 的强大功能，我们可以根据上下文更改导航条，以包含在特定上下文中有用的导航键。在本教程中，我们将演示如何在通话过程中向导航栏添加一个**联系人快捷方式**和一个**结束通话快捷方式**。

感谢 Eli Irvin 成为我的试验品并获得这个截屏。

在上面的视频中，我的测试人员开始与我通话，这导致 Tasker 在导航栏中显示两个新图标。当联系人快捷方式被按下时，调用[键码 _ 联系人](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_CONTACTS)，而结束呼叫按钮调用[键码 _ 结束呼叫](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_ENDCALL)。

我使用的图标不是 Android O 的导航栏定制器中常见的图标，而是我正在使用的自定义图标。你可以点击这里阅读我之前关于如何给 Android O 的导航条添加自定义图标的教程。为了这个教程，你需要根据你设备的 DPI 从[图标数据库](http://www.iconsdb.com/)下载两个图标。第一个是**联系人图标**，你应该保存为/NavIcons/contacts.png，第二个是**结束通话图标**，需要保存为/NavIcons/endcall.png

我们将向你展示如何在你自己的设备上复制这个设置，这样你就可以学习如何定制你自己的导航条配置，但是如果你想直接跳到那个，我们也会在文章的最后提供一个下载链接。

* * *

## 通话时自定义导航条键

Tasker 是必要的，因为它是我们用来检测我们在什么应用程序中的自动化应用程序，并通过 SecureTask 插件发送命令，这将处理我们的导航栏的更改。安装完这两个应用程序后，我们需要设置 SecureTask。

我们需要授予 SecureTask 修改设备上的系统设置的能力。为此，我们必须授予 SecureTask 一个称为 WRITE_SECURE_SETTINGS 的特殊权限，通常常规应用程序无法访问该权限，但用户可以通过 ADB 手动授予该权限。因此，您需要在您的机器上安装并运行 ADB 来使其工作。幸运的是，授予这种权限只是一次性的，我们将在未来的 Android O 相关教程中使用 SecureTask(还有几个教程)，所以绝对值得这么做。

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

我们将需要设置两个不同的 Tasker 配置文件。一个会在你打电话时触发，另一个会在你挂机时触发。前者将显示两个导航条键，后者将禁用它们。非常简单。

对于第一个配置文件，打开 Tasker 并按右下角的+按钮创建它。选择**事件**上下文，进入**电话- >电话摘机**。按 back 返回 Tasker 的主屏幕。将其命名为“启用手机导航条键”

Tasker 将要求您附加一个现有任务或创建一个新任务。创建一个新的，进入任务编辑屏幕后，添加以下操作:

1.  插件->安全任务->安全设置。动作:**写**。设置:`secure sysui_nav_bar_left`。值:`key(207:file:///storage/emulated/0/NavIcons/contacts.png)`
2.  插件->安全任务->安全设置。动作:**写**。设置:`secure sysui_nav_bar_right`。值:`key(6:file:///storage/emulated/0/NavIcons/endcall.png)`

退出回到 Tasker 的主菜单。创建一个新的配置文件并再次选择**事件**上下文，但这次选择**电话- >电话空闲**。命名为“禁用手机导航条键。”

再次创建一个新任务，当您进入任务编辑屏幕时，向它添加以下两个操作:

1.  插件->安全任务->安全设置。动作:**写**。设置:`secure sysui_nav_bar_left`。值:`null`
2.  插件->安全任务->安全设置。动作:**写**。设置:`secure sysui_nav_bar_right`。值:`null`

现在你完成了。当您接受来电，或连接外拨电话，Tasker 将显示一个接触快捷键，以及结束通话键。只要电话还在通话，你就可以在使用任何应用程序时使用这些按键。一旦电话结束，Tasker 将禁用这些导航条键。

* * *

## 下载并导入

与所有 Tasker 相关教程一样，我们将提供 XML 文件供您下载和导入。从下面的 AndroidFileHost 下载. prf.xml 文件，并将其保存到您的内部存储。打开 Tasker，长按顶部的 Profiles 标签，直到你看到一个导入按钮。点击它，查找您刚刚保存的 XML 文件，然后选择它们来导入它们，一次一个。确保你已经将 WRITE_SECURE_SETTINGS 授予了我文章中提到的 SecureTask，否则配置文件将不会在你的手机上做任何事情！

[**从 AndroidFileHost**](https://www.androidfilehost.com/?fid=673368273298943972) 下载“启用手机导航键”配置文件

[**从 AndroidFileHost**](https://www.androidfilehost.com/?fid=673368273298943971) 下载“禁用手机导航键”配置文件

虽然我们没有更多的 Android O 导航栏相关教程来分享，但我们确实还有一个关于 Android O 的教程悬而未决。敬请关注门户网站，获取更多教程！