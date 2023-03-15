# 独家:Pixel 软件更新、分区更改、双引导和无缝定制 ROM 更新

> 原文：<https://www.xda-developers.com/exclusive-dual-boot-may-be-possible-on-pixel-phones/>

在今年的谷歌 I/O 期间，谷歌[正式推出了 Android 牛轧糖](http://www.xda-developers.com/google-io-2016-roundup-part-1-google-assistant-google-home-allo-duo-android-n/)，它为我们这些有幸拥有一台现代 Nexus 设备的人带来了几项急需的可用性增强。谷歌在谷歌 I/O 期间概述的一些功能没有进入当前 Nexus 设备的最终牛轧糖生产版本，最著名的是[无缝更新](http://www.xda-developers.com/current-android-devices-are-unlikely-to-receive-android-ns-seamless-update-feature/)。

许多用户对无缝更新只能出现在装有 Android 牛轧糖的设备上感到失望，但对于我们这些计划升级到 T2 下一代 Nexus T4 Pixel 设备的人来说，我们有一个令人敬畏的新功能可以期待。然而，自从 Google I/O 以来，我们还没有真正看到关于这项新功能的任何其他细节。

然而，这并没有阻止我们中一些更好奇的人去弄清楚谷歌计划如何实现无缝更新。伊桑·杨克，网名为[迪斯·特洛伊](http://forum.xda-developers.com/member.php?u=912474)，因其作为[团队胜利恢复项目](http://twrp.me/)的首席开发人员的工作而闻名，为了理解当 Pixel 设备不可避免地发布时他将面对什么，他直接进入了谷歌发布的牛轧糖源代码。谷歌对即将推出的 Pixel 设备的分区布局做了一些有趣的改变——通过开发人员在我们论坛上的一些巧妙工作，Dees_Troy 推测**双引导可能是可行的。**

* * *

## 谷歌的 Pixel 手机及其分区

 <picture>![Partitions](img/6d03d47a4b68af1c9f9593b54efef5f1.png)</picture> 

Nexus 6P Partition Table

如果你不知道的话，你手机的存储被分成几个标准的内存分区。您可能最熟悉的分区是/boot、/system、/data、/recovery 和/cache，不过如果您感兴趣，可以在您的设备上查找[实际分区表。您(用户)可用的存储空间量由分配给/data 分区的大小决定。另一方面，/system 是大多数 Android 操作系统文件所在的位置。调整这两个分区的大小，为更多的用户应用程序或者新版本的 Android 提供合适的空间](http://www.xda-developers.com/current-android-devices-are-unlikely-to-receive-android-ns-seamless-update-feature/)[绝对是可能的](http://forum.xda-developers.com/galaxy-s2/development-derivatives/mod-increase-partition-size-t3011162)，但是这个过程可能会有风险，一般来说，你不应该期望你的设备会有这样的结果。

通常，当您更新时，仅修改/system 中的文件，更新在数据块级别应用，因此 dm-verity 保持不变。每当你更新你的设备时，你通常根本不能主动使用它。相反，您必须等待恢复来修改每个分区中所有必需的文件。这是为了防止 Android 操作系统试图访问当前正在更新的文件的任何潜在问题，但另一方面，这意味着用户必须耐心等待几分钟，观看 Android recovery 徽标应用更新。

在 Android Nougat 出现之前，每台设备都只能安装一个分区副本。这对于大多数 Android 智能手机来说是有意义的——存储空间非常珍贵(或者说我们被引导去相信),那么为什么要为多个备份分区的冗余而烦恼呢？答案是无缝更新。谷歌进军操作系统的另一个尝试——Chrome OS——被证明非常成功。Android 实际上借用了 Chrome OS 无缝更新的概念。Chrome OS 通过在后台更新一组冗余的非活动分区来实现无缝更新，然后在启动前立即将这些分区与当前活动的分区进行交换。

 <picture>![Chrome OS Update Workflow](img/52b4fba0484798700c76da81b2df4b46.png)</picture> 

Chrome OS Update Workflow - Presumably Android will follow something similar

最初，我们认为预装牛轧糖的手机只会附带一个二级/系统分区。根据 Dees_Troy 的说法，Pixel 手机将带有设备上大多数(如果不是所有)分区的两个副本。

> 新的 Pixel 手机将有 **2 个系统分区，2 个引导分区，2 个供应商分区，2 个调制解调器分区**等。一组分区将是活动的——当前用于引导设备的那组分区。发布更新时，该更新将应用于后台的第二个集合。应用更新后，会出现一个提示，要求重新启动。重新启动将不包括引导至恢复。取而代之的是，设备会将使用哪一组分区切换到第二组分区，这样你就可以快速地，也许几乎是立即地，引导一个更新的设备。-迪斯特洛伊

* * *

## 双启动 Pixel 手机和无缝定制 ROM 更新？

有了每个分区的两个副本，Dees_Troy 预测我们也许能够**劫持第二组分区来双引导**。如果你是支持 [MultiROM 项目](https://play.google.com/store/apps/details?id=com.tassadar.multirommgr&hl=en)的极少数设备之一，你可能对双引导 ROM 的前景很熟悉。如果你以前用过 MultiROM，那么你肯定知道他们使用的方法基本上是一个庞大的黑客集，让它在 Android 上工作。在每一个在设备上提供 MultiROM 的 XDA 线程中，顶部附近都有一个很大的免责声明，警告用户“这些系统都没有考虑到多引导”，即“有可能出现问题，你将不得不再次刷新工厂映像。”但是谷歌慷慨地为我们提供了第二组分区，Dees_Troy 预计，通过 ROM 社区各成员之间的一些合作，我们可能能够在 Pixel 手机上实现双启动运行。

如果我们可以劫持第二个分区设置为双引导，那么我们也可以潜在地使用这些第二分区来实现定制 rom 的**无缝更新。因此，如果你是许多专门的 Cyanogenmod 夜间用户之一，那么你可能可以在夜间更新到最新版本，而不必每天晚上重启手机进行恢复。尽管 TWRP 的开放恢复脚本和各种增量更新工具大大减少了执行夜间更新所需的时间和精力，但在后台无缝更新您的 ROM 肯定胜过所有其他选择。**

请注意，在我们实际拥有工作设备之前，我们不能确定这些功能是否会工作，但鉴于 Dees_Troy 对 TWRP 的广泛研究以及他对 Nougat 源代码的研究，我们相信这一推测是非常可信的。

虽然所有这些即将到来的和可能的功能听起来都很积极，但我们也发现了许多变化，这些变化使即将到来的 Pixel 设备的开发变得复杂。我们将在明天的另一篇文章中详细介绍这些，但同时请保持你的炒作在检查中！