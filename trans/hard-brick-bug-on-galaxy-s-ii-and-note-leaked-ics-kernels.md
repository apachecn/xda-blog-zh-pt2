# Galaxy S II 和 Note 泄露 ICS 内核上的硬砖错误

> 原文：<https://www.xda-developers.com/hard-brick-bug-on-galaxy-s-ii-and-note-leaked-ics-kernels/>

自从三星 Galaxy S2 系列的最新泄漏消息不断冲击我们，人们一直在 rom 之间跳跃——主要是在有缺陷的预发布 ICS 版本和非常稳定的 GB 之间跳跃。毕竟，这是我们在 XDA 做的一个习惯:我们看到漏洞，我们闪现它，我们使用它，我们调整它。如果它飞不起来，我们就简单地回滚。当然，闪存本来就不应该在你的设备上的东西总是有内在的风险，但是在今天这个时代完全阻塞设备的风险相当小。特别是，因为有工具可以让你的设备起死回生，如 XDA 精英公认的开发者[阿达穆特勒](http://forum.xda-developers.com/member.php?u=3682533)的 [UnBrickable Mod](http://www.xda-developers.com/android/explaining-and-advancing-the-unbrickable-mod/ "Explaining and Advancing the UnBrickable Mod") 。

话虽如此，在泄密的世界里，似乎并不是一切都很好。感谢 XDA 精英公认的开发商 [Entropy512](http://forum.xda-developers.com/member.php?u=591147) ，我们已经了解到，大多数接收泄漏的设备在一次闪光后永远不会醒来的风险非常高。原来，泄露的 ICS 内核中有一个重大错误，影响了 eMMC 芯片中的*/数据*分区，这显然是在某些操作(如擦除和闪存)中损坏的。最初认为这只会影响在 CWM 等自定义恢复中执行的操作。然而，有报道称，[库存恢复](http://forum.xda-developers.com/showpost.php?p=26046849&postcount=140)的废料也能生产出坚硬的砖块。受影响的设备有:

Entropy 和其他开发者在网站上发布了一些警告，详细解释了正在发生的事情。我们的建议是，在内核中的错误被完全修复之前，用户应该远离闪存 IC 的泄漏——当然，除非你正在寻找硬砖你的设备。请记住，这不是可以通过 Unbrickable Mod 甚至通过 JTAG 复活的东西，因为这是 eMMC 的固件错误。这是直接来自熵的，如果你们对细节感兴趣的话:

> *危险:许多三星 ICS 泄漏内核可能会损坏您的设备！*
> 
> 那些关注各种三星设备的人可能已经注意到，当使用 ICS 泄漏内核时，一些设备会遇到大量的硬砖。这些硬盘尤其令人讨厌，因为 JTAG 服务的供应商无法复活这些设备，不像简单的引导加载程序损坏硬盘。这是因为这些内核实际上正在设法对 eMMC 存储设备造成似乎是永久性的损坏。
> 
> *确认受影响的内核有:*
> 
> *[*]所有 Epic 4G Touch (SPH-D710) ICS 泄漏[*]所有 Galaxy Note (GT-N7000) ICS 泄漏[*]AT&T Galaxy S II(SGH-I777)ucld 3 泄漏-可能还有所有其他[*]韩国 SHW-M250S/K/L 官方版本和任何从其来源构建的内核*
> 
> *应该安全的内核有:*
> 
> *[*]GT-I9100 ICS 泄漏[*]GT-I9100 官方版本[*]基于 GT-I9100 Update4 源代码库构建的内核*
> 
> *运行受影响内核时可能造成损害的操作:*
> 
> *在 CWM 中擦拭(以及可能的任何其他自定义恢复)(已确认)*
> 
> *在 CWM 中恢复 Nandroid 备份(先擦除)*
> 
> *在 CWM 中刷新另一个固件(大多数刷新先擦除)*
> 
> *擦拭库存 3e 恢复(疑似，也擦拭一个分区)*
> 
> *运行受影响内核时删除大文件(疑似但未确认)*
> 
> *如果你有一个受影响的内核:*
> 
> 立即使用 Odin/Heimdall 刷新一个已知良好的内核。不要使用移动 Odin、CWM 或任何设备上的方法来刷新。已知的好内核包括:
> 
> *[*]几乎所有的姜饼内核[*]ICS 内核都是从 GT-I9100 Update4 源代码构建的*
> 
> *此问题的根本原因尚未确定，但是，XDA 众多知名开发人员怀疑这是由于三星在受影响的内核中启用了一项功能 MMC _ CAP _ ERASE——这是一项性能功能，可以极大地提高闪存写入性能，但似乎带来了闪存芯片组中的一个缺陷。GT-I9100 ICS 内核没有启用此功能，看起来很安全。然而，还没有足够的信息来宣布所有没有这个功能的内核是安全的——唯一能够确认这个问题的根本原因并宣布修复它而不冒很大风险(破坏多个设备而没有办法修复它们)的实体是三星自己。*
> 
> *一般来说，除非另行通知，否则如果您正在为 GT-I9100 以外的任何基于 Exynos 的设备运行三星 ICS 泄漏，强烈建议您刷新其他设备。*

这也是今天早上在我们的论坛上出现的，由 XDA 成员 [garwynn](http://forum.xda-developers.com/member.php?u=4194834) 提供。显然，已经联系了谷歌，他们意识到了这个问题，一名工程师希望能够解决这个问题。

> *Well, it's been some time but thankfully Mr. Sumrall from Android did get back to us on our questions. I think the community will find that this was worth the wait.****Issue: fwrev not set properly.****As we suspected the bugfix is not in our build. (The patch applies this unconditionally.)*
> 
> *报价:*
> 
> | *最初由**肯·苏姆拉尔**发布**该补丁在 mmc.c 中包含一行将 fwrev 设置为 cid 寄存器的权限位。在此修补程序之前，文件/sys/class/block/mmcblk 0/device/fw rev 未从 emmc devices rev 4 和更高版本的 CID 初始化，因此显示为零。* *(第二次查询)* *fwrev 为零，直到应用补丁。* |
> 
> ***Question: Revision didn't match the fix****(Emphasis mine in red as it discusses the superbrick issue.)*
> 
> *报价:*
> 
> | *最初由**肯·苏姆拉尔**发布**你可能有这个错误， **但版本 0x19 是我们原型设备中的固件的早期版本，但我们发现它有另一个错误，如果你发出 mmc 擦除命令，它可能会破坏芯片中的数据结构，并导致设备锁定，直到它重新通电。当我们开发 ICS 时，我们的许多开发人员在进行快速启动擦除用户数据时，我们发现了这一点。** **于是三星修复了问题，转移到固件版本 0x25。**是的，0x19 是十进制的 25 是非常令人讨厌的，这在试图诊断 emmc 固件问题时导致了许多混乱。我终于学会了总是用十六进制来指代 emmc 版本，并在编号前加上 0x，这样才不会混淆。* *不过，即使 0x19 可能存在可以将 32k 字节的 0 插入 flash 的 bug，也不能在固件版本为 0x19 的设备上使用这个补丁。该补丁对修订版 0x25 固件中的两个字节的代码进行了非常具体的黑客攻击，该补丁很可能不会在 0x19 上工作，并且很可能会导致芯片在最好的情况下出现故障，在最坏的情况下会丢失数据。将此补丁应用到 emmc 固件的选择标准如此严格是有原因的。* *几天后，我将我们的结果告诉了大家，并提到文件系统在擦除之前没有损坏。这是对后续行动回应。* *正如我在之前的帖子中提到的，固件版本 0x19 有一个错误，在发出擦除命令后，emmc 芯片可能会锁定。不是每次，但足够经常了。通常，设备可以在此之后重新启动，但在启动过程中会锁定。很少情况下，它甚至可以在加载快速启动之前锁定。你的测试者不走运。由于你甚至不能启动快速启动，该设备可能是砖。:-(如果他可以运行快速启动，那么该设备可能可以用我拥有的固件更新代码恢复，假设我可以共享它。我去问问。* |
> 
> ***Question: Why the /data partition?***
> 
> *报价:*
> 
> | *原帖由**肯·苏姆拉尔(安卓 SE)****因为/data 是芯片经历最多写入活动的地方。从不写入/system(除非在系统更新期间),并且很少使用/cache(主要用于接收 OTA)。* |
> 
> ***Question: Why JTAG won't work?***
> 
> *报价:*
> 
> | *最初由**肯·苏姆拉尔**发布**正如我上面提到的，修订版 0x19 固件有一个缺陷，在 emmc 擦除命令后，它可能会使 emmc 芯片的内部数据结构处于不良状态，导致芯片在访问特定扇区时被锁定。唯一的解决办法是擦除芯片，并更新固件。我有这样做的代码，但我不知道是否可以共享。我去问问。* |
> 
> ***Question: Can a corrupted file system be repaired (on the eMMC)?***
> 
> *报价:*
> 
> | *最初由**肯·苏姆拉尔**发布*e2fsck 可以修复文件系统，但通常在块组的开头插入 32 千字节，这会擦除许多信息节点，因此运行 e2fsck 通常会导致许多文件丢失。 |
> 
> *So, while the fix doesn't apply to us at the moment, we've been given a great insight into the superbrick issue as well as information that a fix **is** already developed (hopefully we'll see it released!). The bug likely applies to us and assuming the fix for the 0x19 firmware is given then it would apply to our devices.**On a lighter note, I wanted to include his close:*
> 
> *报价:*
> 
> | *最初由**肯·苏姆拉尔**发布*你将一瞥 Android 内核开发人员激动人心的生活。:-)事实证明，这项工作主要是与有缺陷的硬件进行斗争。至少，有时候看起来是这样。 |
> 
> 在问题解决之前，请不要在您的设备上闪烁任何 IC。

想在门户网站上发表什么吗？联系任何新闻记者。

感谢您的辛勤工作！！！！]