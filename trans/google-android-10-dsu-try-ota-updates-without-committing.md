# Android 10 DSUs 可能会让你尝试 OTA 更新，而无需提交

> 原文：<https://www.xda-developers.com/google-android-10-dsu-try-ota-updates-without-committing/>

Android 操作系统和安全级别碎片化是一个巨大的问题，谷歌正在投入大量的工程努力来解决。在过去的两年中，谷歌宣布了两项旨在加速更新推出的重大举措:[项目三重](https://www.xda-developers.com/googles-project-treble-modularize-android-so-oems-can-update-devices-faster/)和[项目主线](https://www.xda-developers.com/android-q-project-mainline-security/)。后者仅在今年 5 月[谷歌 I/O 2019](https://www.xda-developers.com/tag/google-io-2019/) 期间宣布，并且仅在搭载 Android 10 的设备上支持。然而，前者自 [Google I/O 2017](https://www.xda-developers.com/tag/google-io-2017/) 以来就一直存在，所以我们已经看到它对 Android 9 Pie 和 [Android 10](https://www.xda-developers.com/android-q-beta-3-released/) 的 Android 更新[产生了多大的影响。](https://www.xda-developers.com/android-p-beta-program-is-now-available/)

除了减少碎片化，谷歌还希望 Project Treble 对应用开发者有用。这就是为什么他们在 Android 10 中推出了[动态系统更新](https://www.xda-developers.com/android-q-dynamic-system-updates-project-treble/) (DSU ),让开发者在不解锁引导加载程序或擦除数据的情况下尝试新操作系统更新的准系统版本。看到 DSU 的潜力，谷歌并没有止步于此——他们正在扩展其效用，使原始设备制造商的 OTA 更新可以像 GSI 一样安装。

这是一大堆行话，但想象一下未来会发生什么:一家 OEM 厂商发布了一款搭载 Android 10 的手机，并开始了 Android 11 的测试程序。你有兴趣尝试这个测试版，看看新的功能，但你不想冒险你目前的日常驱动程序的稳定性。与其更新测试版，然后希望它非常稳定，为什么不通过 DSU 流暂时安装它呢？如果你不喜欢它，只需重新启动，你的设置将恢复正常。如果你喜欢，你可以“提交”更新。

我不知道你怎么想，但这将是对 Android 的一个受欢迎的改变，这将使 beta 测试更加有趣。你将不再需要提交测试版更新来看看它对你来说是什么样的。我敢肯定，你们中的许多人都渴望看到 Android 10 测试版，但你可能不会马上安装它。随着 DSU 的改变，这将不再是一个问题。

## Android 10+ -中的动态系统更新有什么变化

Luca Stefani，XDA 门户网站的一个朋友，也是一个被认可的开发者，他告诉我们关于一个在 AOSP 合并的名为“当存在时挂载多个 DSU 分区”的 T2 新提交 commit 对文件系统表(fstab)和 init 进程进行更改，以便在引导过程中可以挂载除 system 以外的 DSU 分区，现在包括 product 和 vendor。

 <picture>![](img/eeb5f3abf1b5b2b60e25c6699a19d2b6.png)</picture> 

New code in fstab to add support for loading product_gsi and vendor_gsi images in place of the existing product and vendor partitions respectively. A comment notes that DSUs can be signed by the OEM, but otherwise support Google's official GSIs.

目前，DSU 被设计成只能让你启动一个通用的系统映像(GSI)，一个从 AOSP 编译的准系统映像，所以你可以在最新的 Android 更新中测试新的 API 和其他变化。然而，随着这一变化，DSU 也将接受产品和供应商的形象。前者包含特定于设备的应用程序、库和其他文件，而后者包含特定于设备的二进制文件。Project Treble 使你可以使用没有设备特定文件的系统映像来启动设备，所以现在允许加载产品和供应商似乎没有多大意义。

然而，一名谷歌工程师明确表示，这一变化是为了“允许 OEM 在/data 上安装 OTA 包，然后使用' DSU '流从/data 挂载 product.img，system.img，[和] vendor.img。”这意味着，OTA 可以通过 DSU 临时加载，而不是用新的 OTA 包覆盖当前安装。试用 OTA 更新后，“用户可以决定是否要将这些图像‘提交’给/super。”关于“提交”变更的最后一部分仍在进行中，正如一位谷歌工程师指出的那样，“目前我们还没有在 DSU 环境下使 DSU 分区永久化的计划。”然后他陈述了如何实现这一点，但是这一实现“超出了当前补丁的范围”。

这里我们需要解释一些术语和概念，因为谷歌喜欢在每个 Android 版本中改变分区方案。对于初学者，我建议阅读我以前关于[动态系统更新](https://www.xda-developers.com/android-q-dynamic-system-updates-project-treble/)的文章，以全面了解它是如何工作的，但总而言之，它利用了“动态分区”的概念，这是一个真正的存储分区(称为“超级”分区)，它被分成可调整大小的逻辑分区(包括系统、供应商、产品和 system_ext)，以临时安装 GSI。安装 GSI 时，DSU 通过调整现有用户数据分区的大小来为新系统和用户数据映像创建空间。DSU 支持的构建模块(动态分区、内存磁盘和数据备份检查点)是 [Android 10](https://www.xda-developers.com/tag/android10) 的发布要求，因此任何使用新 Android 操作系统版本发布的设备都应该支持 DSU。DSU 不是你们中的一些人正在寻找的定制 rom 的双启动解决方案，因为只有匹配 Android 验证启动(AVB)密钥的映像才能被安装。然而，有了这个新的变化，它在未来可能会更有用。

在动态分区之上，谷歌还在 Android 10 中引入了“虚拟 A/B”的概念。这基本上是以前的[双 A/B 分区](https://www.xda-developers.com/how-a-b-partitions-and-seamless-updates-affect-custom-development-on-xda/)的实现，但是用逻辑分区代替。A/B 分区包含重要分区的副本，以允许无缝和安全的更新。使用“虚拟 A/B”是一位 Google 工程师设想的将 DSU 分区“提交”到当前安装的分区上的方式；与当前的 A/B OTA 更新过程一样，也许来自新映像的更改会被应用到非活动分区。

这些变化仍在开发中，可能需要一段时间才能被谷歌或原始设备制造商使用。最早在明年 Android 11 R 发布之前，我们可能不会看到任何这方面的实现。即便如此，也不能保证原始设备制造商会在其 OTA 更新中采用这一功能。鉴于这似乎对 beta 测试非常有用，我猜想 Google 已经在与感兴趣的 OEM 厂商合作，在未来的更新中启用这一功能。我个人对先试后买新的 Android 更新的前景感到兴奋，但是你呢？