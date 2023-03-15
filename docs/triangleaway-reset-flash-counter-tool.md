# TriangleAway -重置闪光计数器工具

> 原文：<https://www.xda-developers.com/triangleaway-reset-flash-counter-tool/>

XDA 知名开发者 Chainfire 展示了他的最新应用 TriangleAway。该工具将为您提供重置闪存计数器的选项，并通过对引导程序进行编码来删除黄色三角形。仅在使用 Android 冰激凌三明治作为操作系统的根设备上使用**。**

 ****Chainfire** 评论

闪存计数器和三角状态必须存储在某个地方。每个人都知道。过去有人猜测过它可能在哪里，我个人也比较过不同数量的自定义闪存之间的原始闪存盘内容，没有发现任何差异。您可以转储并比较整个/dev/block/mmcblk0，您不会发现任何差异(尽管您会发现一些未分配和未使用的间隙)。

该解决方案附带了 ICS builds 使用的新内核。闪存盘实际上有两个隐藏的引导分区，/dev/block/mmcblk0boot0 和/dev/block/mmcblk0boot1。过去，用于 Gingerbread 的内核中的 MMC 驱动程序不提供这些分区，ICS 内核中的 MMC 驱动程序提供了这些分区。

随着更多官方 ICS 固件的出现，将会有更多的设备能够使用这个有趣的工具，它应该只供专家使用，因为它可能会破坏你昂贵的玩具。

请将您的反馈反馈给开发者，感谢您的阅读。

原创 [XDA 线程](http://forum.xda-developers.com/showthread.php?p=22463153#post22463153)**