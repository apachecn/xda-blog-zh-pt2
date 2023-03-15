# 原始内存快照的 LiME Forensics 内核模块

> 原文：<https://www.xda-developers.com/lime-forensics-kernel-module-for-raw-memory-snapshots/>

在执行数据取证或入侵设备时，对内存的原始访问非常有用。有时，您需要一个内存快照来分析锁定的引导加载程序发生了什么，获取一个内存位置的快照来跟踪一个 bug，或者只是计算出愤怒的小鸟分数的正确内存位置。这就是 Linux 内存提取器，又名[LiME Forensics](http://code.google.com/p/lime-forensics/)的用武之地。LiME 是一个可加载的内核模块，允许你访问所有的设备内存。一旦内核模块被加载到内存中，它基本上会拍摄一个快照，从而允许非常高效的调试。

我请 LiME Forensics 的作者 Joe Sylve 解释 LiME 相对于 viewmem 等传统工具的优势:

> 为了回答你的问题，这些工具被设计成有不同的用途。LiME 旨在获取 RAM 物理内存布局的完整转储，用于取证分析或安全研究。它在内核空间中完成所有这些工作，并且可以将图像转储到本地文件系统或 TCP 上。它的设计是为了给你一个尽可能接近物理内存的副本，同时最小化它与系统的交互。
> 
> viewmem 似乎是一个用户域程序，它从内存设备(如/dev/mem 或/dev/kmem)中读取一系列虚拟内存地址，并将内容打印到 stdout。我不确定它是否比在这些设备上简单地使用 dd 做得更多。
> 
> 由于几个原因，这在法医学中不太被接受。首先，/dev/mem 和/dev/kmem 正在被淘汰，越来越多的设备不再附带这些设备。其次，/dev/mem 和/dev/kmem 限制您只能从第一个 896MB 的 RAM 中进行读取。此外，对于每个内存读取块，该工具会导致 userland 和 kernelland 之间的几次上下文切换，并使用其缓冲区覆盖 RAM。
> 
> 我认为每种工具都有其用途。如果您只需要知道第一个 896 MB RAM 内的地址的内容，并且您的设备有/dev/mem 和/dev/kmem，并且您不关心捕获法医声音图像，那么 viewmem(或 dd)会很有用。然而，LiME 并不是专门为那个用例设计的。

对于内存黑客来说，最重要的是，viewmem 依赖于 */dev/mem* 和 */dev/kmem* 设备。由于 */dev/mem* 和 */dev/kmem* 设备允许直接访问设备内存，因此它们是一个漏洞。这些 Linux 设备正在被逐步淘汰，因为它们已经成为最近多次攻击的目标。LiME 不仅取代了 viewmem 实用程序，而且做得更好。

制造商注意到:通过锁定开发者想要的特性，你促进了更好工具的开发。

来源:[石灰取证](http://code.google.com/p/lime-forensics/) &采访作者乔·西尔维

[图片来源:[由乔·西尔维制作的莱姆演示文稿](http://digitalforensicssolutions.com/Android_Mind_Reading.pdf)