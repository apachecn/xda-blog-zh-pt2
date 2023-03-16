# ARM 大的 Linux 内核 5.0 RC1 可用。几乎没有 EAS 支持，F2FS 修复，等等

> 原文：<https://www.xda-developers.com/linux-kernel-5-0-rc1-arm-big-little-eas-support-f2fs-fixes/>

虽然我们通常不会涵盖主流 Linux 内核领域发生的事情，但对我们来说，跟踪每个新内核版本发生的事情很重要，因为 Google 对每个新版本的 Android 都强制要求最低的 Linux 内核版本。最近[将 LTS 发布从 2 年延长到 6 年的决定](https://www.xda-developers.com/linux-kernel-long-term-support-google/)将在减少安全补丁碎片方面发挥重要作用，因为设备制造商将不得不减少安全补丁的回溯工作。另外，主线内核确实经常集成与移动设备相关的新特性。

例如，最近发布了下一个 LTS 版本内核的第一个候选版本——Linux 内核 5.0 RC1。距离稳定版发布还有一两个月的时间，但是我们已经可以一窥即将到来的发布会有什么了。我将重点介绍一些与移动设备相关的更新，但是如果您对开源开发和 Linux 内核感兴趣，我建议您查看完整的 changelog。

## 手臂大。几乎没有 EAS 支持

自从最初的 Pixel 发布以来，节能调度就一直是 Android 设备上的事情。EAS 是谷歌 Pixel 设备普遍比竞争对手更快的原因之一。高通发布的骁龙 845 内核已经支持 EAS，因此任何具有该 SoC(或更新版本)的设备都将支持 EAS。尽管如此，直到现在，Linux 还没有能量感知调度的上游支持。理论上，上游支持应该会使硅和设备制造商更容易将该技术应用到他们的设备中。然而，对于最终用户来说，上游支持并不意味着什么。

## 绝热支架

Speck 是 NSA(国家安全管理局)开发的加密算法，在低端硬件上运行良好。谷歌[打算](https://android-review.googlesource.com/q/%2522speck%2522)增加对 speck 的支持，因为它为缺乏硬件加速加密扩展的 SOC 的廉价设备提供数据加密支持。斯派克的采用因其与美国国家安全局的联系而受到广泛批评。Linux 内核 4.20 中删除了对 speck 的支持，它的替代产品 Adiantum 在使用 EXT4/F2FS 文件系统的低端硬件上的性能一样好，甚至更好。

## F2FS 和 EXT4 修复

Flash 友好文件系统，或 F2FS，在 Android 设备中广泛使用。例如，谷歌 Pixel 3 和 Pixel 3 XL 正式支持 F2FS。显然，F2FS 的最初开发者 Jaegeuk Kim 向 Linux 库提交了一个合并请求，要求对文件系统进行大量的修复。这些变化处理了加密问题和空闲时间管理，以及垃圾收集修复。您可以在[这个拉动式请求](https://lkml.org/lkml/2018/12/28/387)中看到所有细节。总的来说，修复 F2FS 提高了支持它或将支持它的 Android 智能手机的稳定性和可靠性。

同样，流行的 EXT4 文件系统也收到了十几个补丁。EXT4 被用于许多 Android 设备，如最新的一加设备(包括 [OnePlus 5T](https://www.xda-developers.com/oneplus-5t-xda-review-part-1/) ，OnePlus 6 和一加 6T)。

## 新的 ARM 硬件支持

GNU/Linux 发行版可以说是在基于 ARM 的硬件上运行的最好的操作系统。它们基于开源模型提供可靠的多任务处理。ARM 处理器是专为同时执行大量任务而设计的。这就是操作系统与硬件保持同步的重要性。正如你们中的一些人所知，大多数 Android 智能手机和平板电脑都使用 ARM 架构的芯片组。基于 RISC 的芯片非常适合运行日常任务(你在智能手机上做的事情)。Linux 内核 5.0 增加了对许多新的 ARM 硬件的支持。以下是其中的一些:

*   整数 X2
*   泰格拉·泽维尔
*   Allwinner F1C100
*   高通 QCS404
*   全赢 T3
*   恩智浦层景 LX2160

除了对特定 ARM 硬件的通用兼容性支持，Linux kernel 5.0 还改进了电源管理。

## BinderFS 支持

Android 使用 Binder 来交换系统中不同进程之间的参数。应用程序、活动和流程使用 Binder 来启动和管理流程。Android 上的安全性高度基于 UID 权限。Binder 使用双向 IPC 调用检查应用程序提供的 uid，以确认它可以访问它想要使用的功能。BinderFS 是 Binder 的更新版本，但是它更加专门化，并且与系统兼容。对 BinderFS 的支持对最终用户来说不会有太大的改变，但从长远来看，它将为开发人员解决一些实现问题。这里是[相关提交](https://git.kernel.org/pub/scm/linux/kernel/git/gregkh/char-misc.git/commit/?h=char-misc-next&id=3ad20fe393b31025bebfc2d76964561f65df48aa)。

## 能源模型管理框架

另一个新增功能是支持能源模型管理框架。这个变化主要是针对 ARM 和内核开发者的。它从不同来源(如设备树或驱动程序)提供了一个新的标准化能源使用信息层。能耗和报告由类似的硬件和软件以不同的方式处理。能源模型管理框架将提供一个标准 API，内核中的另一个驱动程序可以使用该 API 来访问有关能源消耗的信息。理论上，这将使软件工程师和开发人员更容易从硬件中获得相关信息。你可以在这个提交中读到更多关于这个框架[的内容。](https://git.kernel.org/pub/scm/linux/kernel/git/tip/tip.git/commit/?h=sched/core&id=27871f7a8a341ef5c636a337856369acf8013e4e)

## ARM64 指针认证支持

每一个相关的硬件和软件解决方案，尤其是在移动设备上，都需要强大的安全协议。这就是 Linux 内核 5.0 在 ARM64 指针认证支持下提供的功能。由于大多数智能手机都有基于 ARM64 的芯片组，因此攻击者无法利用指针至关重要，指针在 Linux 内核中用于访问内存地址。新的认证协议将指针与密钥进行比较。指针认证将试图避免面向返回的编程(ROP)和其他类型的攻击。

* * *

对于 Linux 5.0 内核，还有很多我们没有提到的更新。它们中的大多数对于 Android 设备来说并没有太大的意义，所以这就是为什么我们不得不挑选变更日志。如果你想看到完整的“变更日志”，请查看 Phoronix 的报道。

*感谢 XDA 知名开发者 [flar2](https://forum.xda-developers.com/member.php?u=4684315) 协助撰写本文。*