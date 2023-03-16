# 华为发布面向 Android 设备的 EROFS 文件系统

> 原文：<https://www.xda-developers.com/huawei-erofs-linux-file-system-android/>

# 华为发布面向 Android 设备的 EROFS Linux 文件系统

华为的一名工程师宣布，该公司正在开发一种名为 EROFS 的只读文件系统，该系统有望在不牺牲压缩的情况下提高性能。

文件系统是一种概述如何存储和检索数据的技术。有许多不同种类的文件系统，每一种都有自己的优点可供选择。你可能听说过像 exFAT、F2FS、ext4 这样的文件系统。[选择一个文件系统而不是另一个](https://www.xda-developers.com/f2fs-why-file-systems-matter-interview-stan-dmitriev-tuxera/)会对存储性能和稳定性产生深远的影响，因此设备制造商不会轻易做出这个决定。大多数设备制造商满足于像 ext4 这样广受欢迎、经过良好测试的文件系统，但这并不意味着公司不愿意尝试替代方案。这正是华为正在做的一个名为 EROFS 的开源 Linux 文件系统，该系统旨在在某个时候用于 Android 设备。

华为工程师高翔宣布了这一消息。EROFS 是“可扩展只读文件系统”的缩写 EROFS 仍处于非常早期的开发阶段，它采用了改进的压缩模式，追求与其他文件系统不同的设计方法，主要关注性能和速度。华为工程师承诺，与其他只读文件系统相比，EROFS 将提供更高的磁盘性能和速度，同时还能节省磁盘空间。发布会上公布的服务器硬件和麒麟 970 处理器的压缩数字听起来很有希望。可悲的是，由于其发展状况，没有披露太多信息。

EROFS 仍然是一个相当大的进展中的工作。最终目标是将其包含在 Android 设备中，但这可能需要几个月，甚至更长时间，直到华为甚至考虑将文件系统包含到主流 Linux 内核中。如果我们谈论在实际的消费者 Android 设备中包含它，我们很可能会看到这个数字增加到年。我们已经看到原始设备制造商在他们的设备上试验并随后放弃了 F2FS，所以如果 EROFS 的采用从未真正发生也不要惊讶。如果你想看看当前的代码，你可以在查看一下[内核邮件列表。](http://lkml.iu.edu/hypermail/linux/kernel/1805.3/07858.html)

* * *

[**Via: Phoronix**](https://www.phoronix.com/scan.php?page=news_item&px=EROFS-File-System)