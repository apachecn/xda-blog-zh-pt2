# Scrcpy 1.14 增加了无缝复制粘贴，保持清醒的选项，等等

> 原文：<https://www.xda-developers.com/free-android-mirroring-app-scrcpy-seamless-copy-paste-stay-awake/>

# 免费的 Android 屏幕镜像应用程序“scrcpy”增加了无缝复制粘贴、保持清醒选项等等

一款免费开源的 Android 屏幕镜像应用“scrcpy”现在可以在你的智能手机和个人电脑之间无缝复制粘贴。

在不同操作系统的设备之间工作和交互有时会很痛苦。很少有第三方工具可用于建立多平台连接，其中许多工具要求您拥有同一品牌的设备。幸运的是，有第三方工具来拯救这一天。一个名为 [scrcpy](https://www.xda-developers.com/scrcpy-control-android-on-pc/) 的免费开源项目允许你将 Android 设备的屏幕镜像到个人电脑上，无论它运行的是 Windows、Mac 还是 Linux。它使用 Android Debug Bridge 作为连接隧道，并通过它传输 h.264 编码的视频。就在昨天，该项目的开发人员发布了该工具的新版本，具有一些受欢迎的功能。

**无缝复制粘贴**

这些功能中最重要的一个是能够在手机和电脑之间无缝复制和粘贴，反之亦然。将 UTF 8 编码的文本从电脑复制粘贴到手机上可以在运行 Android 7 及更高版本的 Android 设备上运行。那是因为 Android 7.0 中引入了通过 ADB 注入‘粘贴’键事件的命令。然而，这种新的方法肯定胜过旧的方法，旧的方法涉及从 Android 的剪贴板中抓取复制的文本。

**保持清醒**

另一个伟大的新功能让你强迫设备保持清醒。结合关闭屏幕的命令，您可以在 PC 上与设备进行交互，而实际设备的屏幕是关闭的。

```
 scrcpy -Sw  
```

您也可以使用 Ctrl + Shift + O 快捷键来重新打开屏幕。

scrcpy 1.14 的 changelog 的其余部分包括一些 bug 的常规修复和解决方法。

**下载 scrcpy 1.14**

 <picture>![scrcpy 1.4](img/abe9a9135c36dad9473d5990d0cc8dc5.png)</picture> 

scrcpy 1.14 running on a Windows 10 PC

正如我已经提到的，scrcpy 是一个开源项目。你可以在 GitHub 上看到并贡献给[库](https://github.com/Genymobile/scrcpy)以及[下载工具](https://github.com/Genymobile/scrcpy/releases)。这是一个命令行工具，所以没有花哨的 GUI，所以一定要查看那里的安装和配置说明。如果遇到 bug，请确保创建问题并向存储库发送请求。

* * *

**Via: [OMG！Ubuntu！](https://www.omgubuntu.co.uk/2020/05/scrcpy-1-14-seamless-clipboard)**