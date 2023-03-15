# 对 Android 的完整 NTFS 读/写支持

> 原文：<https://www.xda-developers.com/full-ntfs-readwrite-support-for-android/>

NTFS 是微软专有的首选文件系统，取代了更广为人知的 FAT 文件系统。与后者相比，它有许多优点，例如改进了对元数据的支持，以及使用高级数据结构来进一步提高性能、可靠性和磁盘空间利用率。

目前，只有少数 Android 设备有完全的支持，因为在大多数内核中默认情况下是不支持的。现在，随着一些高端设备对 USB-OTG 的支持，对 NTFS 的完全读/写支持变得非常有用。感谢 XDA 资深会员 [shardul_seth](http://forum.xda-developers.com/member.php?u=4196928) 的辛勤研究和发布他的发现，我们现在可以完全支持 NTFS 的读/写了！

根据 OP 的说法，他为 Android 编写了一个通用的 NTFS-3G 驱动程序，应该可以在所有带有 *fuse.ko* 模块的 ARM 设备上运行。由于大多数设备都有内核源代码，所以驱动程序可以被*嵌入到普通内核中，以提供所需的 Fuse 支持。这是 NTFS-3G 的最新稳定版本，已经在 Linux PCs 上进行了时间测试。如果用正确的交叉编译器编译，这甚至可以在非 ARM 架构的设备上工作。*

随着 USB OTG 越来越流行，在某个时候安装 NTFS 驱动器将变得很有必要。如果这激发了你内心的极客，那就去试试[原始线程](http://forum.xda-developers.com/showthread.php?t=1724078)吧。