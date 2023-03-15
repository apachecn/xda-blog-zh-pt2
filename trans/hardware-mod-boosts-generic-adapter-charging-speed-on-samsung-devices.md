# 硬件模块提高三星设备上通用适配器的充电速度

> 原文：<https://www.xda-developers.com/hardware-mod-boosts-generic-adapter-charging-speed-on-samsung-devices/>

硬件模块可能是棘手的事情。修改软件是一回事，因为如果它出了问题，你可以随时恢复备份，我们所有的老读者现在都应该有了。然后就恢复正常，改天再尝试不同的东西。不过，对于硬件模块来说，风险要大得多，因为如果你搞砸了，那么无论你在做什么硬件模块，这都是你的末日。所以，记住这一点，在做硬件改装的时候要小心，因为如果搞砸了，那就是穷途末路。

除了令人沮丧的后果，XDA 公认的开发商 [TRusselo](http://forum.xda-developers.com/member.php?u=3531712) 发布了一种修改廉价售后快速交流充电器的方法，以像 OEM 三星交流充电器一样运行。这将为用户提供三星品牌交流充电器的全部充电容量，价格更便宜。

这种修改非常简单明了，只需弯曲并连接充电器本身的几个引脚，就可以欺骗三星 Android 手机，让它相信自己使用的是真正的三星充电器。正如 TRusselo 解释的那样:

> 其背后的理论与三星 galaxy 手机和“官方充电器”有关:
> 
> 如果 usb 上的中间 2 个数据引脚，而外部 2 个引脚获得 5v 电压，它会告诉手机这是一个*官方三星*充电器，并支持全速充电。
> 
> 如果没有连接中间的 2 个引脚(有或没有数据流),将不会全速充电。即使你提供 800 毫安的电流，也只能充 350 毫安左右的电流。

这个模块修复了 350 毫安问题，并以其支持的最大容量给手机充电。如果这是你唯一的充电器，强烈建议你不要尝试，因为弄坏它会让你通过 USB 充电，没有人喜欢通过 USB 充电。

对于任何有兴趣将他们的充电器变成三星充电器的人来说，请查看[修改线程](http://forum.xda-developers.com/showthread.php?t=1384253)，查看它如何工作的照片以及关于它如何工作和为什么工作的完整解释。此外，对于那些携带[三星 Galaxy Nexus](http://forum.xda-developers.com/forumdisplay.php?f=1336) 的用户，请查看您本地的内核开发人员，看看他们是否已经实现了 [force AC charge 内核模块](http://www.xda-developers.com/android/kernel-patch-allows-force-ac-charge-for-faster-charging/)，理论上类似，但没有硬件修改。