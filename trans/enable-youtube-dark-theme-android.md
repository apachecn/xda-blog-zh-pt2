# 在没有 root 或修改的 apk 的 Android 上启用 YouTube 黑暗主题

> 原文：<https://www.xda-developers.com/enable-youtube-dark-theme-android/>

早在三月份，谷歌宣布 Android 和 iOS 的 YouTube 移动应用程序[将获得黑暗模式](https://www.xda-developers.com/youtube-app-dark-mode-android/)。这一黑暗主题几乎立即在 iOS 用户中推出，但在 Android 版本中却花了数月时间。事实上，谷歌[最近才开始为少数用户测试](https://www.xda-developers.com/youtube-dark-theme-android/)黑暗主题。对于那些喜欢摆弄你的设备的人，你可能知道 YouTube 的黑暗主题[已经在 Android 上可用了几个月](https://www.xda-developers.com/enable-youtube-dark-mode-android/)——前提是你愿意为你的设备安装 root 或者安装一个修改过的 APK。对于那些不想在你的设备上安装或者下载 YouTube 应用程序的修改版本的人来说，在你的设备上推出这个功能之前，你将会有很长的等待时间。但是如果你不想等待，我们找到了一种方法**在没有 root 和不修改 APK** 的情况下为 Android 的黑暗模式启用 YouTube。

如果你想让 Android 上的 YouTube 应用看起来像这样，那就继续读下去。

就像我们以前的许多教程一样，我们将使用一个叫做“ADB”的便利工具来完成这个小技巧。ADB 或 Android Debug Bridge 是一种计算机工具，开发人员使用它来连接他们的设备。它提供了许多有用的调试工具，其中之一允许用户备份和恢复他们的应用程序数据。我们将利用 ADB 的备份和恢复功能来强制启用 YouTube 的黑暗模式。

启用它是小菜一碟——如果您已经设置了 ADB，这个过程只需几秒钟。如果你还没有建立亚洲开发银行，你必须先完成这个过程，然后才能继续。不过，我们建议你为你的智能手机设置 ADB 访问，因为它打开了一系列隐藏的定制选项，这些选项通常是不可用的(例如 Android 8.0 Oreo 和 Android 8.1 Oreo 上的[全系统无根定制主题](https://www.xda-developers.com/custom-themes-android-oreo-substratum/))。)如果你对此感到满意，并希望获得 Android 黑暗主题的 YouTube，那么这里有一些方法。我们将在一步一步的指导之后解释这是如何工作的。

## 如何在 Android 上启用 YouTube 的黑暗主题

*非常感谢[我们的不和谐服务器](https://www.xda-developers.com/official-xda-developers-discord-server/)* *上的 xfileFIN 与我们分享这个方法。*

1.  请从上面的谷歌 Play 商店下载该应用程序，确保您使用的是该应用程序的最新版本。
2.  如果您还没有，请[下载适用于您的操作系统的最新平台工具，以便您可以使用 ADB](https://www.xda-developers.com/install-adb-windows-macos-linux/) 。
3.  从 [AndroidFileHost](https://www.androidfilehost.com/?fid=5862345805528062570) 下载“[youtubedarkstheme _ xda . zip](https://www.androidfilehost.com/?fid=5862345805528062570)”。
4.  从 zip 文件中提取“YouTubeDarkTheme_XDA.ab”并将其放在 ADB 二进制文件所在的 platform-tools 文件夹中。
5.  在 ADB 所在的目录打开命令提示符或终端窗口**，根据你的操作系统输入以下命令: **Windows 命令提示符:**`adb restore YouTubeDarkTheme_XDA.ab`**Windows Power Shell:**`.\adb restore YouTubeDarkTheme_XDA.ab`**MAC OS 终端:** `./adb restore YouTubeDarkTheme_XDA.ab` **Linux 终端:** `./adb restore YouTubeDarkTheme_XDA.ab`**
6.  您应该会看到一条消息，告诉您解锁手机并确认恢复操作。
7.  在您的智能手机上，您应该会看到一个全屏提示，要求您批准“所有数据的完全恢复”不输入密码就接受(我们做的文件不需要密码)。按“恢复我的数据”不会擦除或替换你手机的任何数据(除了 YouTube 的设置，这是我们在这里的目标)，所以不要担心。
8.  几秒钟后，全屏提示应该会消失。如果你已经在 YouTube 应用程序中，它应该重新载入黑暗主题。如果你还没有在应用程序中，只要打开它，它应该加载主题。YouTube 可能会强制关闭，但只要重新打开应用程序就可以安全地忽略这一点。
9.  恭喜你，你现在应该可以在 YouTube 上看到 Android 的黑暗主题了！你不会在设置中看到切换，所以如果你想关闭黑暗模式，你必须清除 YouTube 的应用数据。

我们不喜欢向我们的读者展示一个很酷的调整而不解释它是如何工作的，所以如果你想知道我们到底在做什么，文章的下一部分就是为你准备的。

## 它是如何工作的

每个 Android 应用程序都将数据存储在一个只有该应用程序才能访问的位置。对于 YouTube，该位置在/data/data/com . Google . Android . YouTube 中。在该位置中是“共享偏好设置”文件夹，其中包含保存应用程序设置的 XML 文件。youtube.xml 文件包含定义应用程序是否应该显示黑暗主题(以及其他内容)的首选项。默认情况下，首选项值为 false。手动将此值修改为真[需要 root 访问权限](https://www.xda-developers.com/enable-youtube-dark-mode-android/)，因为/data 中的所有文件(不包括/data/media，它需要适当的外部存储权限才能读/写)对于没有 root 权限的第三方应用程序都是不可访问的。但是我们可以利用内置的第一方工具来解决这个限制。

“共享首选项”文件夹中的文件可以由 ADB 手动备份，或者在应用程序允许的情况下自动备份到 Google Drive。我们可以利用前一种备份方法，通过准备我们自己的修改后的“备份”文件来进行恢复，该文件包含一个修改后的 youtube.xml，并将“黑暗主题”首选项设置为 value。这正是我们在这里所做的——我们用 YouTube ADB 备份，解包，修改，然后用这个工具重新打包。你可以打开。一个 ab 文件，如果你愿意，我们让你自己去验证它的内容。恢复这个。ab 文件会覆盖原始的 youtube.xml 文件，从而强制将黑暗模式值设置为 true。