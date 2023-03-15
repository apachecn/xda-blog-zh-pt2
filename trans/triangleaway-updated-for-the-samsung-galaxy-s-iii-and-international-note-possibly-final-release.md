# 为三星 Galaxy S III 和国际版 Note 更新了 TriangleAway，可能是最终版本

> 原文：<https://www.xda-developers.com/triangleaway-updated-for-the-samsung-galaxy-s-iii-and-international-note-possibly-final-release/>

那些熟悉由 XDA 精英认可的开发商 [Chainfire](http://forum.xda-developers.com/member.php?u=631273) 开发的 [TriangleAway](http://www.xda-developers.com/android/triangleaway-reset-flash-counter-tool/ "TriangleAway – Reset Flash Counter Tool") 的人会感到欣慰的是，该应用程序已经更新，增加了与[三星 Galaxy S III](http://forum.xda-developers.com/forumdisplay.php?f=1563) 和[国际 Galaxy Note](http://forum.xda-developers.com/forumdisplay.php?f=1346) 的兼容性。对于那些不熟悉这个应用程序的人来说，它就像它的名字暗示的那样，通过移除三角形并重置你设备上的闪光计数器来实现。

让我们回溯一分钟，找出应用程序必须更新的确切原因，以及这次与以前有所不同的原因。在应用程序启动时，内核闪存计数器相对容易管理。简单地重置该值将会删除计数器。然而，随着 Galaxy Note 的发布，三星通过隐藏数据让事情变得更加困难。现在，在三星 Galaxy S III 上，三星使它变得更加困难，这要归功于一种后台服务，它可以搜索根的迹象。

根据 Chainfire 的开发博客:

> 在 Galaxy S II 中，三星引入了自定义内核闪存计数器和自定义内核警告三角形。这就是 Triangle Away 的用武之地——它重置了闪光计数器，并移除了警告三角。
> 
> 在 Galaxy Note 上，三星再次尝试隐藏数据，因此 Triangle Away 不起作用。
> 
> 在 Galaxy S III(以及其他新设备)上，三星更进一步，推出了一种后台服务，可以在你的设备上运行，并检查诸如修改的/系统、以 root 访问权限运行的应用程序等。
> 
> 就目前而言，这项服务并没有恶意，但谁知道未来会带来什么？跟踪 IMEI 的曾经运行根，禁用服务等？

很可怕，不是吗？最后一行应该会引起你的注意，因为不难想象将来的服务版本也可以这样使用。而且通过查看更新日志，可以清楚的看到 Chainfire 和三星的战斗:

> 更新 16.02.2012: 用户已经确认 TriangleAway 对 I9220 SGNote ICS 泄漏的工作！
> 
> 2012 年 5 月 13 日更新: TriangleAway 在最新的 SGNote ICS 官方固件上*不*工作。很快会有一个固定的版本，但它必须等我的笔记从维修中返回，否则我不能测试它
> 
> 2012 年 6 月 4 日更新:1.50 版应该可以再次与 I9220 和 N7000 SGNote 兼容

现在，你可能想知道为什么三星或任何其他 OEM 会觉得有必要密切关注你的订单。人们可以假设这与保修有关，但这真的是三星的一个有效理由吗？毕竟，如果硬件功能正常，[为什么不正确的固件刷新甚至会损坏硬件](http://www.xda-developers.com/android/hard-brick-bug-on-galaxy-s-ii-and-note-leaked-ics-kernels/ "Hard Brick Bug on Galaxy S II and Note Leaked ICS Kernels")？

根据 Chainfire 自己的说法:

> **定制 rom、root、砖块和保修**
> 
> 我不确定三星想要追踪这一切的原因是什么。我想“中断”他们跟踪的原因只有一个:保修。
> 
> 能够在我拥有的设备上运行我想要的软件而不失去硬件保修应该是法律赋予的权利。就我所见，只有两种方法可以真正用 root 权限破解你的设备:
> 
> (1)超频到硬件损坏的地步
> 
> (2)对你的引导程序分区进行无意义的刷新
> 
> 我不确定如何处理(1)。我个人从不超频——而且我也不觉得否认超频保修有什么奇怪的。当然，这在硬件上是可以避免的。然而，案例 2 完全是三星的错。 *Adam Outler* 已经一次又一次地表明，这些设备完全可以被做成*不易碎*——所以任何引导程序块都是 IMHO 三星的错。如果*亚当·奥特勒*能用烙铁阻止这种情况，那么原来的设计就被打破了。
> 
> 不管怎样，硬件应该在保修期内——不管我的设备有没有 root。泄露的服务中心文件显示，应检查设备的根，如果存在，拒绝保修。(这不只是三星，各大主机厂都这么做。)
> 
> 这是完全不能接受的。任何遵循该政策的 OEM 都是不良的 OEM——在一些国家，这甚至可能是非法行为(尽管祝你在法庭上胜诉)。由于 HSPL 在场，HTC 曾拒绝更换我的 HTC Diamond 上有缺陷的数字化仪(这是该设备常见的硬件问题)。他们声称 HSPL 已经不可逆转地损坏了主板，设备的整个内部都必须更换。Riiiiight。
> 
> Root 本身并不是犯罪，也不是一个指针，表明设备以任何方式损坏都不属于保修范围。但在原始设备制造商的眼中，我们似乎是罪犯。
> 
> 如果追踪的目的与公司安全等相关，我可以理解为什么三星想要进一步封锁。我当然能理解，尽管我不一定同意。

如果这个[让你想起了九十年代中期的](http://www.urbandictionary.com/define.php?term=skateboarding%20is%20not%20a%20crime)，你被原谅了。正如 Chainfire 所写的那样，能够以我们认为合适的方式使用我们自己的设备本身并没有什么恶意或犯罪。然而，各种原始设备制造商采用各种策略，旨在阻止我们真正定制我们的设备，以满足我们的心，因为害怕无效的保修。

如果(用 Chainfire 的个人例子)损坏的数字化仪硬件与闪存固件完全没有关系，为什么这是拒绝保修服务的理由。对于那些修补汽车的人来说，这就像是因为你增加了一个售后收音机而取消了动力系统保修。根本没有正当理由——无论从道德上来说。对美国人来说幸运的是，马格努森-莫斯保证法案提供了一点保护，但是想把它告上法庭还是祝你好运。而在其他国家，你可能完全不走运。

这就引出了这样一个问题:从实践和伦理角度来看，什么是最好的。Chainfire 对情况进行了评估，指出:

> 因此，我们兜了一圈——如果三星在保护他们的定制闪存数据方面更进一步，我会试图绕过它吗？我应该吗？我很大程度上不这么认为。

那些只是想为可能是最后一次的三角和闪光计数器开脱的人可以在 [Google Play](https://play.google.com/store/apps/details?id=eu.chainfire.triangleaway) 上购买该应用的捐赠版本，或者前往[原始发布线程](http://forum.xda-developers.com/showthread.php?t=1494114)获取免费版本。那些只是想在这个问题上了解更多的人应该前往 [Chainfire 的开发博客帖子](http://www.chainfire.eu/articles/118/Triangle_Away_vs_Samsung/)。