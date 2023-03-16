# 三星 Galaxy S10/S10e/S10+ (Exynos)现在可以通过 Magisk Canary 版本进行根

> 原文：<https://www.xda-developers.com/samsung-galaxy-s10-plus-s10e-s10-exynos-rooted-magisk-canary/>

三星 Galaxy S10 系列产品代表了[三星能够提供给消费者的所有技术中最好的](https://www.xda-developers.com/samsung-galaxy-s10-display-review/)。如果你现在想买一部高端智能手机，Galaxy S10 和它的兄弟姐妹将会出现在你的购买清单上。现在你会很高兴地知道，XDA 公认的开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 已经[成功地在基于 Exynos 的三星 Galaxy S10、S10+和 S10e 上实现了 root](https://www.xda-developers.com/exynos-samsung-galaxy-s10-rooted-magisk/) ，并且发布了利用 Magisk 的 Canary 版本的安装指南。

在我们开始之前，重要的是要知道，尽管 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 已经尽了最大努力使程序尽可能地方便用户，但仍然有一个很大的学习曲线。因此，如果你以前从来没有根过一个设备，或者如果你很难按照上面提到的顺序操作，那么我**不建议**在你全新的 S10 上尝试这个。在这个过程中有许多更小的复杂性，如果你搞砸了，就会损坏你的设备。开发者为这些新推出的 Android Pie 三星设备(即 Galaxy S10/S10+/S10e 和 Galaxy A50)创建了一个[单独的安装指南](https://topjohnwu.github.io/Magisk/samsung)。Galaxy A 系列的其他设备也推出了 Android Pie -我们还不知道它们的指令集是否不同。

为 S10 安装 Magisk 将导致 Knox 出错，这是意料之中的。您还需要一个解锁的引导加载程序(它反过来会启动数据擦除)，第一次安装 magisk 也需要一次完整的数据擦除。解锁这些新三星设备上的引导加载程序也是一个不同的过程，因为三星推出了一项“VaultKeeper”服务，该服务试图在数据被擦除后“*重新锁定*”引导加载程序。在您“解锁引导程序”之后，您必须引导设备，通过初始设置(您可以跳过几个步骤，因为您将再次擦除)，并再次检查引导程序解锁选项是否存在。

安装 Magisk 包括下载您设备的固件，提取其 AP tar 文件并在您的手机上用 Magisk 对其进行修补，然后在您的计算机上将修补后的 tar 文件作为 AP 闪存在 Odin 中。还有更多的细节需要记住和遵循，所以完整的指令集被有意地从本文的范围中省略了。请[完整阅读开发商的安装说明](https://topjohnwu.github.io/Magisk/samsung)以了解更多信息。

安装 Magisk 后，还会涉及一些技术问题。要引导至安装了 Magisk 的系统，每次都必须引导至恢复模式。由于恢复也和 Magisk 存在于同一个分区中，手机会根据你按下音量键的时间来决定启动方式。Topjohnwu 对后 Magisk 时代的情况总结如下:

*   **(正常上电)→(没有 Magisk 的系统)**
*   **(电源+ Bixby +音量增大)→(引导加载程序警告)→(释放所有按钮)→(带有 Magisk 的系统)**
*   **(Power+Bixby+Volume Up)→(boot loader 警告)→(保持音量上升)→(实际恢复)**

关于升级 Magisk，您可以在 Magisk 管理器中直接升级 Magisk。但是为了升级你的设备，你不能刷新你的 AP tar 文件，你需要在刷新 Odin 之前预先修补固件。

如果你正在寻找更多关于这个过程的技术细节，开发者已经创建了一个单独的线程。

这个新的 Magisk Canary 版本还增加了对 Android Q Beta 2 的支持。

[**根三星 Galaxy S10 配 Magisk**](https://forum.xda-developers.com/galaxy-s10/development/magisk-root-galaxy-s10-series-t3918699/)