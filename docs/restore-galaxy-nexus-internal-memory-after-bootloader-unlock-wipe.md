# 启动加载程序解锁擦除后恢复 Galaxy Nexus 内部内存

> 原文：<https://www.xda-developers.com/restore-galaxy-nexus-internal-memory-after-bootloader-unlock-wipe/>

大多数人都知道，解锁 Nexus 设备上的引导加载程序通常会擦除 */data* 分区。你有时可以 [root 而不解锁引导程序](http://www.xda-developers.com/android/root-your-galaxy-nexus-without-unlocking-the-bootloader/)，通过支持 root 的应用程序备份数据，解锁你的引导程序，然后恢复你的数据。然而，大多数人不愿意经历这样的麻烦。现在，您可以像往常一样解锁，并取回被擦除的数据。

XDA 论坛成员 [Wartickler](http://forum.xda-developers.com/member.php?u=2129788) 为[三星 Galaxy Nexus](http://forum.xda-developers.com/forumdisplay.php?f=1336) 发布了一种在数据被擦除后恢复数据的方法。正如 Wartickler 解释的那样:

> 通常，操作系统会删除索引中的引用指针，该指针指出某个文件以某个名称存在，它位于硬盘/内存位置的这个位置...问题是，数据恢复工具需要一个实际安装的驱动器，以便深入挖掘和挖掘那些你不幸意外删除的有趣的猫图片。这些最新批次的手机没有外置 sd 卡，这种 sd 卡非常容易安装为驱动器。内部内存以 MTP/PTP 的形式装载，不被视为装载的驱动器，无法被这些数据恢复工具扫描。

因此，创建了一种方法来扫描这些驱动器并恢复数据。这种方法适用于 Galaxy Nexus，但实际上应该与任何内置 SD 卡的设备兼容。虽然它是在 Windows 7 上使用的，但应该很容易翻译到 Linux 上。这是一个相当长的过程，但在遵循它之后，用户将能够在他们的设备上使用他们最喜欢的数据恢复工具来恢复丢失的数据。

欲了解完整说明和更多信息，请查看[原始螺纹](http://forum.xda-developers.com/showthread.php?t=1994705)。