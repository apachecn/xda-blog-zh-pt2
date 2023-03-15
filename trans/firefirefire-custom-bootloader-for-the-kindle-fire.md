# FireFireFire 为 Kindle Fire 定制的引导程序

> 原文：<https://www.xda-developers.com/firefirefire-custom-bootloader-for-the-kindle-fire/>

Amazin Kindle Fire 已经证明了自己是一款非常受欢迎且功能强大的设备。这款设备的开发肯定不缺乏，其中大部分都列在了由 XDA 资深成员 [stiffmast3r](http://forum.xda-developers.com/member.php?u=3367404) 发布的[非常有用的帖子](http://forum.xda-developers.com/showthread.php?t=1467013)中。

许多人倾向于立即认为定制 rom 和内核是 XDA 开发的全部，而我们设备的引导加载程序经常被忽略。然而，Kindle Fire 部分的情况并非如此。FireFireFire 是一个定制的引导加载程序，最初由 XDA 资深会员 [pokey9000](http://forum.xda-developers.com/member.php?u=466725) 开发，它在 3 个方面提供了比普通引导加载程序更多的功能:

*   它允许您在设备开始启动后，只需再次按下电源按钮即可进入恢复模式，因此不再需要繁琐的按钮组合。
*   当设备通电时，它还会自动启用快速启动，从而消除了对 idme bootmode、特殊电缆或 stock bootloader 在每次运行快速启动时所需的命令的需要。
*   当与[重新点燃](http://forum.xda-developers.com/showthread.php?p=20565446http://forum.xda-developers.com/showthread.php?p=20565446)结合使用时，也可以使用 FireFire 对设备内存进行重新分区并修复阻塞的设备。(不过要注意，这种方法涉及到一些 AdamOutler 风格的对设备内部的修补)

不幸的是，pokey9000 似乎不再对 FireFire 有效了。然而，修改仍在继续，火炬已经传递给了资深成员[金福恩斯](http://forum.xda-developers.com/member.php?u=4422144)。他的版本带来了一些你可能更喜欢的变化，即不同的启动标志和更短的快速启动窗口，这将节省 5 秒的启动时间。

您可以在下面的链接中找到这两个版本: