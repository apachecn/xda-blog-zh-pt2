# 三星 Galaxy Note 3 的 Android 5.0 泄露

> 原文：<https://www.xda-developers.com/android-5-0-leak-galaxy-note-3/>

# 三星 Galaxy Note 3 的 Android 5.0 泄露

三星 Galaxy Note 3 出现了一个泄露的 Android 5.0 固件。学习如何闪现它。

Android Lollipop 仍在向许多新设备进军。摩托罗拉、LG 和三星已经推出了固件更新。这些更新大多已经由这些原始设备制造商正式发布，另一款应该很快就会获得官方更新的设备是[三星 Galaxy Note 3](http://forum.xda-developers.com/galaxy-note-3) ，因为棒棒糖固件版本已经泄露。

Note 3 SM-n 9005(n 9505 xugbnl 8)的更新版本为 1.1 GB，它带来了 Android 5.0 体验和重新设计的 Touchwiz 前端。更新过程非常简单，但 XDA 认可的贡献者 [mithun46](http://forum.xda-developers.com/member.php?u=4922752) 创建了一个很好的指南，展示如何在 Windows 操作系统上刷新泄露的固件。要刷新镜像，需要使用最新版本的 Odin(3.09 版)。在闪存期间，/data 分区将被擦除，因此请确保您已经备份了最重要的数据，以避免令人不快的意外。您还应该备份您的 PIT 分区，Mithun46 提供了正确创建备份所需的相关 ADB 命令。

Android 5.0 使用了新的编译器——ART，使得设备与 Xposed 框架不兼容。第一次启动过程也明显更长，所以如果您的设备需要更长的时间来启动，不要惊慌。如果一切顺利，迎接你的应该是 Android 5.0 的启动向导。

如果你有一台 SM-N9005，并且想在上面使用 Android 5.0，请访问[指南线程](http://forum.xda-developers.com/galaxy-note-3/general/guide-t2983873)了解更多信息。