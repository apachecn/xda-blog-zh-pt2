# Treble 项目对未来定制 ROM 的发展意味着什么

> 原文：<https://www.xda-developers.com/project-treble-custom-rom-development/>

在 XDA 这里，我们之前已经谈论过 [Project Treble](https://www.xda-developers.com/googles-project-treble-modularize-android-so-oems-can-update-devices-faster/) ，这是自近 10 年前第一个 Android 测试版发布以来，Android 基础上引入的最大的底层变化，以及[你如何判断你的设备是否有](https://www.xda-developers.com/project-treble-android-oreo/)。对于那些仍然不知道 Project Treble 是什么的人来说，它通过将供应商实现(专有 blobs 和软件、CPU 和 GPU 驱动程序等)与主要的 Android 框架和系统分离，将 Android 的下层模块化。这通过模块化硬件抽象层(HALs)并将其与 Android 操作系统的其余部分分离，以及通过消除 OEM 对芯片制造商缓慢的驱动程序更新的依赖，从而加快了系统更新。最终目标是希望延长目前大多数设备制造商承诺的 24 个月主要软件更新支持期。

这应该有助于让 Android 手机能够接收类似苹果的更新，至少在旗舰手机上是如此。虽然 Android 旗舰产品平均在 24 个月内获得 2 次重大更新，但 iPhone 设备至少获得 4 年的 iOS 更新，包括次要更新。在支持 Treble 的 Android 手机上，这最终会成为现实，前提是手机制造商准备更新他们的手机。那些想要在相似的时间框架内保持他们的设备更新的人没有其他选择，只能求助于定制的 rom。

幸运的是，项目高音也应该让自定义 ROM 用户的草更绿。事实上，它有彻底改变定制 ROM 开发场景的潜力——而且是永久性的。

* * *

### 自定义 rom 如何利用高音？

为什么非官方的 Android Oreo 端口正在被慢慢开发，而不仅仅是开发人员可以编译、启动和运行的东西，原因很简单。为了在现有设备上运行新的 Android 版本，需要对内核和设备树进行大量修改，以使现有的 Android 手机能够与新的 Android 版本一起工作。这是因为当前的供应商实现，包括所有专有的二进制 blobs，都是为了与单个 Android 版本一起工作，因此需要重新制作并移植到新的 Android 版本，以便设备正常工作。

几乎手机内部的所有组件都使用一个独立的专有 blob，并且需要独立地进行修补和工作，以便新的软件可以使用它，同时确保其他组件在此过程中不会中断。这确实是一项耗时的任务，也是大多数*稳定的*定制 rom(如 LineageOS weeklies 或其他官方支持的 rom)直到最终的 Android 版本在 AOSP 发布后 2-3 个月才出现的主要原因。所有这些努力也意味着最终的 ROM 只能在一种设备上工作，或者在最好的情况下，只能在少数相同或相似规格的设备上工作。

据来自 *ArsTechnica* 的 [Ron Amadeo 称，这似乎正在随着 Project Treble 而改变，并得到了定制 ROM 开发商 SultanXDA 的独立证实。](https://arstechnica.com/gadgets/2017/09/android-8-0-oreo-thoroughly-reviewed/2/#h4)

> #### 马尔切夫说，Treble 将 Android 硬件支持标准化到如此程度，以至于从 AOSP 编译的通用 Android 版本可以在每台 Treble 设备上启动和运行。事实上，这些“原始 AOSP”版本将被用于一些 CTS 测试，谷歌要求所有 Android OEMs 厂商通过这些测试以获得谷歌应用的许可——这不仅仅是因为*应该*工作，而是因为*需要*工作。

为了说明这一点，这意味着由于 Android 下层的模块化方式，市场上所有的 Treble 设备都将能够启动一个通用股票，AOSP Android build 。这消除了将定制 rom 移植到旧设备的大部分麻烦，因为一个单一的通用 Android 版本可以在许多设备上运行。这使得 Android 设备更接近个人电脑，你可以在 10-12 岁的电脑上启动最新、最先进的 Windows 10 版本或任何 Linux 发行版。

你还不能在你的 Treble 设备上完美地启动普通的 Android 9.0 版本，尽管设备树和内核仍然需要改进。这仍然是一个很好的开始:由于模块化的 HALs，带来下一个 Android 版本的工作量应该会大大减少，我们可以在几天/几周而不是几个月内看到稳定的 9.0 版本。我们应该记住，Project Treble 虽然现在已经推出，但仍是一项正在进行的工作，因为它仍在 AOSP 接受更改，供应商层最终可能会标准化，安装新的 Android 版本将与在计算机上安装 Windows 相同。

这是一个巨大的技术进步，它有可能极大地改善我们论坛上基于 AOSP 的定制 ROM 开发。不过，这只适用于带有 Project Treble 的设备，目前市面上仅有的高音手机有谷歌 Pixel、谷歌 Pixel XL、索尼 Xperia XZ1 和 XZ1 紧凑型。现有的奥利奥之前的手机会发生什么变化？

* * *

### 定制 ROM 能给现有手机带来高音吗？

我们已经有了现有手机的 Android Oreo ROMs 目录，包括 Nexus、一加、小米和摩托罗拉手机。然而，这些 rom 中的一个能给你的手机带来 Project Treble 吗？答案:**不太可能**。

对 Android 底层平台所做的改变非常复杂，不是你能在普通的定制 ROM 上就能完成的。它不是类似饼图控件或设备手势的东西，而是对供应商实现的全面重新设计。这需要高通和其他硅制造商的努力。谷歌目前正在与不同的原始设备制造商合作，为一些现有的旗舰手机带来三重功能，但即使如此，我们也不确定 T2 的原始设备制造商正在做什么，因为名单还没有公布。然而，我们已经看到一些高音相关的提交在 LineageOS Gerrit 中浮动，所以可以肯定地说它确实正在被尝试。

最后，现在说还为时过早。我们之前已经在我们的论坛上看到了一些令人惊叹的开发壮举，包括像[通用无系统接口](https://forum.xda-developers.com/apps/magisk)或 [eMMC 存储升级](https://www.xda-developers.com/nexus-5-hardware-modded-to-64gb-internal-storage-by-replacing-emmc/)这样令人敬畏的东西，所以谁知道呢？有人可能会以某种方式让 Project Treble 在传统手机上工作。

但是我们只有大约两周的时间去挖掘安卓奥利奥来源，所以正如我们所说的，现在下结论还为时过早。不过，我们仍然对可能性感到兴奋，我们将在 XDA 门户网站上让您了解未来与高音相关的发展，最好通过 XDA 实验室应用程序访问！

**感谢偏执的 Android 团队成员 [/u/evan1123](https://www.reddit.com/user/evan1123) 澄清了文章中的一个错误！**