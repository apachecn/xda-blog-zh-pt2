# 如何访问 Android 上的脸书隐藏设置菜单

> 原文：<https://www.xda-developers.com/access-facebook-hidden-settings/>

脸书的应用程序[很像它的对手 Facebook Messenger 应用程序](https://www.xda-developers.com/facebook-messenger-internal-menu/)，也有自己隐藏的内部菜单，供脸书的工程师用于调试和测试。这个脸书隐藏设置菜单**不能**永久启用，不像 Messenger 的内部菜单。很像 Messenger 你**需要 root 权限**或者 XDA 资深会员 [evilwombat](https://forum.xda-developers.com/member.php?u=5029215) 修改的[APK](https://forum.xda-developers.com/android/apps-games/bullshified-version-facebook-okay-to-t3586318)才能进入这个菜单。正如在 Messenger 教程中一样，您还需要使用 Android 调试桥(ADB)或终端应用程序，如 [Termux](https://www.xda-developers.com/termux-the-ultimate-linux-terminal-emulator-for-android-xda-spotlight/) 。如果您使用 ADB，需要启用 USB 调试，这可以在您设备上的开发者选项中找到。

您将需要在您的手机上的 root 访问权限，以遵循本教程。解锁设备的引导程序后，你可以通过闪烁 [Magisk](https://forum.xda-developers.com/apps/magisk) 或 [SuperSU](https://forum.xda-developers.com/apps/supersu) 来获得 root 权限。请注意，使用上面链接的修改后的 APK 需要您卸载任何现有的脸书应用程序，而是使用来自您计划使用的同一开发商的所有修改后的脸书应用程序的*。*

 ** * *

### 使用亚行

下载您选择的亚行工具。这些可以是来自我们论坛的"[最小亚行&快速启动](https://forum.xda-developers.com/showthread.php?t=2317790)或者是谷歌发布的[官方二进制文件](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)。安装或解压后，在包含 ADB 二进制文件的文件夹中，按住 shift +右键并点击“在此打开命令窗口”(如果你在 Windows 上)。如果你在 Mac 或 Linux 上，那么你需要在下面的“adb shell”命令前加上 adb 二进制文件的目录。

将电话连接到计算机，并授予调试访问权限。接下来，在命令提示符下键入以下命令:

```
 adb shell 
```

```
 su 
```

当手机提示时，授予超级用户访问“shell”的权限。

```
 am start -n "com.facebook.katana/com.facebook.katana.internsettingsactivity.InternSettingsActivity" 
```

现在，您将看到手机上的内部菜单打开。

### 使用终端

打开您选择的终端应用程序。我个人使用 Termux，但任何可以访问终端的设备都可以正常工作。键入以下命令。

```
 su 
```

当设备上出现提示时，授予超级用户访问权限。

```
 am start -n "com.facebook.katana/com.facebook.katana.internsettingsactivity.InternSettingsActivity" 
```

内部菜单将在您的设备上打开。

* * *

## 说明

我们使用 adb 或终端来启动`InternSettingsActivity`，它是隐藏的内部菜单活动的名称。这是在 AndroidManifest 文件中定义的未导出的活动；这意味着它不能从第三方应用程序正常访问。这个内部菜单中有一些设置和调整，脸书应用程序的用户可能会从中受益。这个菜单只允许脸书应用的开发者和测试者使用，所以你可以做很多事情。向下滚动查看一些示例。

* * *

### 数据保护程序

这是我在内部设置中最喜欢的功能。您可以启用数据使用监视器，一旦达到特定限制，它将停止应用程序传输数据。这对那些使用计量连接的人来说是件好事，因为脸书的数据非常密集。它充满了视频和图片，所以这并不奇怪。有了这个菜单，你可以简单地设置应用程序允许的最大数据量，如果你想允许自己使用更多的数据，也可以重置计数器。这个限制器适用于 WiFi 或移动数据，所以那些在 WiFi 上使用限制性数据上限的人也可以利用这一点。

### 强制应用更新

另一个有趣的功能是“强制应用程序更新”功能。它似乎下载了最新版本的应用程序和更新，虽然我没有得到一个软件包安装的尝试，即使一个 toast 告诉我它正在下载。这个特性可能被破坏了，但是看起来仍然很有趣。

### 视频统计

在内部菜单中，您可以启用播放视频的视频规格，以便在观看视频时显示元数据(文件信息)。您还可以启用日志记录、静音播放视频和强制自动播放视频。自动播放设置已经在应用程序中了，但在这里看到它们稍微高级一点还是很有趣的。

仅此而已，如果你发现脸书应用程序中隐藏的任何其他有用的功能，请在下面的评论中告诉我们！*