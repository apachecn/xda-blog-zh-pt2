# Galaxy S III、Galaxy Camera 的革命性 SD 卡引导程序工作正在进行中

> 原文：<https://www.xda-developers.com/revolutionary-sd-card-bootloader-released-for-galaxy-s-iii-galaxy-camera/>

我们很少提到“游戏规则改变者”这个词。这些年来，XDA 取得了许多令人印象深刻的发展。然而，改变游戏规则的人确实很少。最近在三星 Galaxy S III(T1)、三星 Galaxy 相机(T3)和其他基于三星 Exynos 的设备上有了一些突破。

XDA 精英公认的开发商[阿达穆特勒](http://forum.xda-developers.com/member.php?u=3682533)和[雷贝洛斯](http://forum.xda-developers.com/member.php?u=1767826)已经想出如何从 SD 卡启动。我们也不是在谈论 chroot 风格的双引导。我们说的是用开源引导装载程序进行完全引导。此外，他们还让 Fastboot 在 Galaxy 相机上工作。正如 adamoutler 解释的那样:

> 这是什么意思？我们现在可以在三星 TrustZone 内的生产设备上工作了！这意味着一些严重的引导加载程序调试是可能的。这到底意味着什么？这意味着我们不仅有办法摆脱三星闭源引导加载程序，而且我们现在可以完全从 Galaxy 相机和 Galaxy S3 上的 SDCard 启动....那是什么意思？我们可以修复被砖头窃听的银河 S3 设备！

尽管如此，仍有许多工作要做，如下所述:

> 1.EMMC 禁用硬件模式(稍后可以撤消)
> 
> 2.用于调试和在快速启动模式下工作的 UART 连接。
> 
> 3.尝试为 SDCard 启动重新制作 GS3 内存磁盘。
> 
> 4.在 16gb 上重新创建正确的分区结构。

这是个大新闻。除了从通常的 EMMC 引导之外，使用 Exynos 处理器的设备用户现在有了第二个选择。mod 还远未完成，但有了这个 mod，至少 Galaxy S III 和 Galaxy Camera 是不可能永久砖块化的。毫无疑问，更多的设备将会及时跟上。我们必须执行简单的硬件模式，直接从 SD 卡启动，而不是恢复 EMMC 芯片并再次从该芯片启动。如果你碰巧又砖头了，换个 SD 卡就行了。

此外，能够使用开源引导程序意味着用户不再需要担心刷新锁定的引导程序来保存他们的设备。为了让事情变得更好，亚当说其他事情也是可能的。这些包括引导备用操作系统，但实际上，可能性是无限的。Adam 在他的最新视频[2012 年最佳黑客](http://www.xda-developers.com/android/best-hacks-of-2012-xda-developer-tv/)中也简单提到了这种模式。随着事态的发展，很可能会有更多关于这方面的进展，所以请保持警惕。

为了保持对这一进展的关注，请查看[原始线程](http://forum.xda-developers.com/showthread.php?t=2061437)。