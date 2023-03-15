# 使用状态栏下载进度检查下载状态

> 原文：<https://www.xda-developers.com/statusbar-download-progress/>

# 使用状态栏下载进度检查下载状态

状态栏下载进度允许你以一种无障碍的方式检查你的下载进度，在你的状态栏上方显示一个进度线。

大多数下载操作使用标准的 Android 下载管理器，它为开发人员提供了一个强大而可靠的解决方案。利用它的一些流行的例子包括 Play Store、Chrome 和 Xposed Installer。(如果你很好奇，手机上的“下载”应用程序提供了一个界面，用于查看使用 Android 下载管理器下载的文件。)

如果你想查看正在进行的下载的进度，你通常需要拉下通知栏。这可能会分散注意力，并导致当前活动失去焦点(如果您在等待下载完成的同时玩快速游戏，这一点尤其明显)。幸运的是，XDA 公认的贡献者 [C3C076](http://forum.xda-developers.com/member.php?u=5008415) 写了一个 Xposed 模块，允许你以一种非常无障碍的方式快速浏览当前下载的进度。

状态栏下载进度类似于电池栏，您可能很熟悉。它在你的状态栏的顶部显示一条线，随着你的下载进度水平填充它。您还可以选择进度条的颜色、模式(在状态栏的顶部和底部边缘之间选择)和边距。

如果你想尝试一下，确保你已经安装了[exposed Framework](http://forum.xda-developers.com/xposed)，然后访问[状态栏下载进度论坛线程](http://forum.xda-developers.com/xposed/modules/app-statusbar-download-progress-v1-0-t2933867)来试用这个模块。