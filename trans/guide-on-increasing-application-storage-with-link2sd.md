# 使用 Link2SD 增加应用存储的指南

> 原文：<https://www.xda-developers.com/guide-on-increasing-application-storage-with-link2sd/>

如果你日常使用的是旧设备，或者你是一个囤积者，你可能会在某个时候达到你的存储极限。作为一个用谷歌 Nexus One 开始使用安卓系统的人，我太了解这种感觉了。虽然我已经开始使用内置存储空间更大的设备，但并不是每个人都有最新的设备。另外，你永远不知道什么时候你会安装更多的[游戏](https://play.google.com/store/apps/details?id=com.carrotpop.www.smth)。

为了帮助您充分利用可用的存储选项，许多人已经开始使用 [Link2SD](https://play.google.com/store/apps/details?id=com.buak.Link2SD&hl=en) 将他们的应用程序存储扩展到他们的 SD 卡。XDA 论坛成员 [acermedo](http://forum.xda-developers.com/member.php?u=5399496) 已经创建了一个快速指南，引导你完成对你的 SD 卡进行分区并使 Link2SD 正常工作的过程。

这是通过使用基于 PC 的分区工具重新格式化你的物理 micro SD 卡来实现的。然后，应用程序用于将此链接到设备的内部存储。最佳情况下，这是在带有物理 SD 卡的设备上完成的，sd 卡可以通过 USB 大容量存储来访问。当然，这对于只通过媒体传输协议访问 eMMC 内部存储的设备来说是行不通的。这是因为重新分区需要低级别的访问权限。按照这种思路，它可能适用于通过 USB 大容量存储(而不是 MTP)使用单独的内部存储挂载点的设备，但这种方式绝对不会提高速度，只会增加存储空间。

前往[导丝](http://forum.xda-developers.com/showthread.php?t=2412319)开始。