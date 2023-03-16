# 一加 8 Pro 的 Kirisakura 定制内核支持控制流完整性(CFI)以获得更好的安全性

> 原文：<https://www.xda-developers.com/kirisakura-custom-kernel-for-the-oneplus-8-pro-enables-control-flow-integrity-cfi-for-better-security/>

一加手机在修补者中很受欢迎，主要是因为该公司对开发者友好的态度，当然还有其无痛引导加载解锁政策。公司本身并不害怕尝试，改装者也完全接受同样的想法。例如，一加手机是首批支持[节能调度](https://www.xda-developers.com/google-pixel-fastest-android-phone-eas/) (EAS)的非像素设备，这要归功于 XDA 丰富的售后市场开发社区。这就是为什么第三方内核在 XDA 总是受欢迎的一个重要原因，因为它们可以被定制以引入新的性能特性和安全措施。

XDA 公认的开发者 freak 07 T1，更为人所知的是 Kirisakura 内核的维护者，现在已经通过他的定制内核为一加 8 Pro 引入了一个漂亮的安全功能。这种机制被称为**控制流完整性** (CFI)，它被设计成一种运行时强化特性，但也可以被归类为一种 bug 查找工具——使其非常独特。

**[一加八大职业 XDA 论坛](https://forum.xda-developers.com/oneplus-8-pro)**

通过修复可利用的代码来提高安全性是内核开发的一个非常重要的方面。除其他外，这是由每月的 Android 安全更新定期完成的。

然而，众所周知，并非所有 OEM 厂商都像我们希望的那样定期推出这些更新。此外，Android 内核由成千上万行代码组成，这些代码都不在树中。由于 Android 内核的复杂性和规模，以及 Android 生态系统的多样性，很难修复每一个漏洞。与其修复每一行可被利用的代码，不如通过使现有的安全缺陷不可被利用来使系统更能抵御攻击。这种技术被称为硬化。

这就是控制流完整性(CFI)发挥作用的地方。CFI 是一种安全机制，它不允许对编译后的二进制文件的原始控制流图进行更改。由于[现有的内存保护](https://android-developers.googleblog.com/2016/07/protecting-android-with-more-linux.html)使得代码注入更加困难，一种常见的攻击手段是覆盖内存中存储的函数指针。

下面是 Freak07 的一个技术解释，它对控制流完整性做了更多的解释:

### 关于控制流完整性的技术细节

“内核中大量函数指针的可用性助长了这种攻击模式的流行。即使攻击者不能注入他们自己的可执行代码，也可以执行现有内核代码的任意部分来完成他们的攻击。

LLVM 的 CFI 试图通过限制有效调用目标并在检测到 CFI 违规时强制内核崩溃来缓解这些攻击。在每个间接分支之前添加检查，以确认目标地址指向具有正确签名的有效函数。这防止了间接分支跳转到任意代码位置，甚至限制了可以调用的函数。如果漏洞允许访问，攻击者仍然可以更改函数指针。但是 LLVM 的 CFI 将 55%的间接呼叫限制为最多 5 个可能的目标，将 80%的间接呼叫限制为最多 20 个目标。为了确定每个间接分支的所有有效调用目标，编译器需要一次看到所有内核代码。

LTO ( [链路时间优化](https://llvm.org/docs/LinkTimeOptimization.html))的使用使这成为可能。LLVM 的 CFI 需要使用 LTO，其中编译器为所有 C 编译单元生成特定于 LLVM 的位代码，支持 LTO 的链接器使用 LLVM 后端将位代码合并并编译成本机代码。

作为允许使用 CFI 的补充，LTO 通过整体程序分析和跨模块优化实现了更好的运行时性能。

[ThinLTO](http://blog.llvm.org/2016/06/thinlto-scalable-and-incremental-lto.html) 几乎赶上了 LTOs 的性能提升。在 ThinLTO 模式下，与常规 LTO 一样， [Clang](https://clang.llvm.org/) 在编译阶段后发出 LLVM 位代码。ThinLTO 位代码增加了模块的压缩摘要。在链接步骤期间，仅读取摘要并将其合并到组合摘要索引中，该索引包括用于以后跨模块函数导入的函数位置索引。然后，对组合的摘要索引进行快速有效的整体程序分析。ThinLTO 允许多线程链接过程，从而减少编译时间。

由于 CFI 在遇到某些 bug 类时会中断程序的执行，所以如前所述，当在许可模式下使用时，它也被归类为 bug 查找工具。许可 CFI 将在内核日志中显示 CFI 违规，而不会导致内核崩溃。core 4.9 (Pixel 3 代设备)和 4.14 (Pixel 4 代设备)内核有几个函数类型不匹配，导致 CFI 违规，Google 在内核/公共回购上可用的补丁集中解决了这些问题。

然而，由于 Android 生态系统的性质，这些不匹配很可能会在 SoC 制造商(在这种情况下，高通)或 OEM(一加)的特定代码中发现。一加 8 Pro 的 Kirisakura 内核修复了高通代码中几个与 4.19 内核不同的 CFI 违规问题(例如: [1](https://github.com/freak07/Kirisakura_OP8PRO_InstantNoodle/commit/9982e3c2793de95f12ff2c8bcf6adc924359e254) 、 [2](https://github.com/freak07/Kirisakura_OP8PRO_InstantNoodle/commit/090419042846c119dc8d8f2133493d53e9ce9301) 、 [3](https://github.com/freak07/Kirisakura_OP8PRO_InstantNoodle/commit/f3be2647ad6ef562d5d91ac95ee41ebcf0d38f01) )。

在许可的 CFI 中运行内核揭示了与一加驱动程序相关的代码中的 CFI 违规(相关的提交可以在这里的[和这里](https://github.com/freak07/Kirisakura_OP8PRO_InstantNoodle/commit/202da10e9b256443d10e9aff4f10b34d251613f0)的[中找到)。一加 8 Pro 的 Kirisakura 内核在 CFI 强制下运行，保护其用户免受这种代码重用攻击。"](https://github.com/freak07/Kirisakura_OP8PRO_InstantNoodle/commit/9f320aa5cb1a7d1581ef7b3fc513e452b2931451)

据我们所知，唯一正式支持 CFI 的 Android 智能手机型号是谷歌 [Pixel 3](https://forum.xda-developers.com/pixel-3) 和 [Pixel 4](https://forum.xda-developers.com/pixel-4) 系列。开发者告诉我们，他的内核是少数几个拥有完全工作的[内核——CFI](https://security.googleblog.com/2018/10/posted-by-sami-tolvanen-staff-software.html)的定制内核之一。一加 7 Pro 论坛上还有另一个内核[，它支持 Kernel-CFI 以及](https://forum.xda-developers.com/oneplus-7/oneplus-7-7-pro-7t-7t-pro-cross-device-kernel-development/kernel-glassrom-kernel-t4009237) [Freak07](https://forum.xda-developers.com/member.php?u=3428502) 自己为华硕 ROG 手机 II 开发的 [Kirisakura 内核，但他为一加 8 Pro 发布的内核是第一个为使用 Linux 内核版本 4.19 的设备定制的、强制执行 CFI 的内核。](https://forum.xda-developers.com/rog-phone-2/development/kernel-kirisakura-1-0-0-asus-rog-phone-t4028237)

**[Kirisakura kernel for the 一加 8 Pro — XDA 下载与讨论线程](https://forum.xda-developers.com/oneplus-8-pro/development/kernel-kirisakura-1-0-0-oneplus-8-pro-t4119585)**

如果设备运行的是 Android 9 Pie 或更高版本，谷歌强烈建议使用 Kernel-CFI。随着原始设备制造商有时会落后于最近的安全更新几个月，以及我们的手机越来越多地与我们的生活联系在一起，保存着宝贵的私人数据，专注于强化系统的安全功能确实是我们个人智能手机的一个受欢迎的补充。但是，还有其他的内核安全特性，即使不比 Kernel-CFI 更重要，也是同样重要的，所以不要把 CFI 当作防止所有缺陷的灵丹妙药。