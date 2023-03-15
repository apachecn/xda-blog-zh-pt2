# 装载 ntfs 时装载 ntfs 驱动器

> 原文：<https://www.xda-developers.com/mount-ntfs-drives-with-ntfs-mounter/>

虽然安装 NTFS 可能不是用户在购买 Android 手机时排队购买的第一个功能，但它有时肯定是有用的。对于那些可能会考虑在他们的 Android 设备上安装 NTFS USB key 或硬盘的人来说，你现在实际上已经有了一个应用程序。

XDA 论坛成员 [Kwull](http://forum.xda-developers.com/member.php?u=385298) 已经发布了 NTFS 安装程序，它能做到所说的，并在插入时自动安装 NTFS 驱动器。目前，该应用程序已知支持[三星 Galaxy S II I9100](http://forum.xda-developers.com/forumdisplay.php?f=1055) 、[三星 Galaxy Tab 2](http://forum.xda-developers.com/forumdisplay.php?f=1596) 和[国际 Galaxy Note](http://forum.xda-developers.com/forumdisplay.php?f=1346) 。然而，要在这些设备上工作，用户必须运行带有内核的根 ICS ROM，该内核具有 fuse 驱动程序。对于不喜欢看的人，你可以在 Galaxy S II 上使用 XDA 精英公认开发者 [Chainfire](http://forum.xda-developers.com/member.php?u=631273) 的 [CF-Root 内核](http://forum.xda-developers.com/showthread.php?t=1331784)。Kwull 说:

> 2.如果系统中不存在 ntfs-3g，该应用程序会安装它
> 
> 3.应用程序接收媒体 NOFS 事件，并尝试将所有未装载的/dev/sdXXX 设备装载为 NTFS 卷
> 
> 4.尚未安装 NTFS 格式的 SD 卡

最有趣的计划功能之一是有一天允许用户使用 NTFS 格式化他们的外部 SD 卡。这将消除 FAT32 中的低文件大小限制，在某些情况下甚至可能有助于提高性能。

要开始，请访问[原始线程](http://forum.xda-developers.com/showthread.php?t=1654024)。