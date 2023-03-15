# 在 2012 款 Nexus 7 - XDA 开发者电视上安装 Ubuntu Touch

> 原文：<https://www.xda-developers.com/installing-ubuntu-touch-on-the-2012-nexus-7-xda-developer-tv/>

上周， [XDA 开发者电视](http://www.xda-developers.com/xda-tv/ "XDA Developer TV")制片人乔丹向我们展示了如何在即将发布的 Ubuntu Touch 操作系统中开发应用程序。当然，如果你有测试设备，为设备或操作系统开发一个应用程序总是更容易。幸运的是，谷歌发布了新版本的 Nexus 7，市场上充斥着你能以低价买到的[老款 Nexus 7](http://forum.xda-developers.com/forumdisplay.php?f=1673 "Nexus 7 Forums") 。

在这个视频中，Jordan 向您展示了如何在原始的 Nexus 7 (2012)设备上安装 Ubuntu Touch。这将允许你尝试把 Ubuntu Touch out 作为一个操作系统，或者甚至把应用程序推送到来测试你的开发。所以如果你有一台旧的 Nexus 7 (2012)或者你想试试 Ubuntu Touch，看看这个视频吧！

一定要看看其他伟大的 [XDA 开发者电视](http://www.xda-developers.com/xda-tv/ "XDA Developer TV")视频。

使用的命令:

*   sudo add-apt-repository PPA:phablet-team/tools
*   sudo apt-get 更新
*   sudo apt-get 安装 phablet-tools Android-tools-ADB Android-tools-fast boot

要解锁 bootloader，按住电源按钮+音量增大+音量减小打开电源，然后在设备解锁后运行“sudo fastboot oem unlock”，再次通过 Android 设置，启用 USB 调试，连接，运行“adb devices”以确保连接正确，然后耐心等待“phablet-flash Ubuntu-system-channel devel-no-backup”。这需要很长时间。

查看[乔丹的 YouTube 频道](http://youtube.com/twildottv "Twil.tv")和[乔丹的游戏 YouTube 频道](http://youtube.com/twilplays "TwilPlays")