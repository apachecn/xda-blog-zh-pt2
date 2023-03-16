# T-Mobile 一加 7T 专业迈凯轮与解锁引导加载程序不会获得 OxygenOS 更新

> 原文：<https://www.xda-developers.com/dont-unlock-t-mobile-oneplus-7t-pro-mclaren-bootloader-oxygenos-updates/>

一加 7T Pro 迈凯轮版是一加智能手机 2019 年的[高潮。超平滑的 90Hz 显示屏和骁龙 855 Plus 的胆量只是一加最新高端设备中的一些功能，包括迈凯轮的品牌，设计和支持。它从里到外看起来都令人惊叹。一加设备在我们的论坛中非常受欢迎，7/7T 系列也是如此。除了一个事实，如果你通过 T-Mobile 获得了一加 7T Pro 迈凯轮版设备，并且你打算解锁其引导加载程序并对其进行 root，你可能不想这样做，除非你不介意完全错过 OxygenOS 更新。](https://www.xda-developers.com/oneplus-7t-pro-mclaren-edition-5g-t-mobile/)

如果你以前修改过一加设备，你会知道当你解锁引导程序时，只能使用完整的系统 OTA zips 来更新它们，而当它被锁定时，你可以选择使用更小的增量 zip。对于为什么会发生这种情况的快速入门，基本上是因为增量 OTA ZIPs 要求所有只读分区，如/system、/vendor、/boot 和/product，完全不被修改——这在 bootloader 解锁时无法保证，因为 bootloader 解锁允许 boot(即修改引导映像)。

**[一加 7T Pro XDA 论坛](https://forum.xda-developers.com/7t-pro)**

在/data 分区中有一个名为 reserve.img 的 img 文件。它包含一些 OxygenOS 应用程序，这些应用程序不是设备启动所必需的，但它会在启动时安装在/system/reserve 中。因为解锁引导加载程序会彻底清除/data 分区，所以存储在该分区中的 reserve.img 文件也会随之清除。因为这个文件已经不存在了，所以手机不能在/system 分区中挂载它，所以从技术上来说它被篡改了。如果它被篡改，那么手机就不能进行增量更新。通常，OxygenOS updater 应用程序可以自己解决这个问题:它可以检测你的手机是否解锁/根，并下载完整的固件压缩文件，无论它是否解锁/根，它都可以刷新，因为它会覆盖所有只读分区。

那么这里的问题是什么呢？T-Mobile 一加 7T Pro 迈凯轮版与大多数其他一加设备不同，没有一加网站上提供的完整固件。因此，如果解锁的引导加载程序阻止你进行增量更新，并且没有完整的 zip 文件，那么如果你决定提前解锁引导加载程序，你将被卡在你的手机正在运行的任何 OxygenOS 版本上。普通的一加 7T Pro 确实有完整的拉链可供下载，但你不能在这款设备上下载，因为它是运营商品牌的，并且是 T-Mobile -而不是一加-负责该设备的 OxygenOS 固件。

现在，如果你不关心 OxygenOS，只打算闪存 GSIs 或其他基于 AOSP 的定制 rom，那么这个问题不会以任何方式阻止你。然而，如果你曾经需要完全恢复你的设备到股票，你现在运气不好。因此，我们真的希望 T-Mobile 和一加能够很快为这款设备提供全拉链或其他形式的恢复。

* * *

*更新:这篇文章被更新以纠正关于 reserve.img 的信息，以及这个问题不影响刷新定制 rom 的能力的事实。*