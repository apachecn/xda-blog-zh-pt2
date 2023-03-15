# 高通 Kryo 385:半定制 A75 和 A55，性能提升 30%

> 原文：<https://www.xda-developers.com/qualcomm-snapdragon-835-kryo-385-cpu-cores/>

昨天，高通发布了用于旗舰设备的下一代旗舰处理器:骁龙 845。据证实，三星代工厂将采用 10 纳米工艺制造芯片，周三，高通透露了新的片上系统的更多细节，包括[第二代 Spectra ISP](https://www.xda-developers.com/qualcomm-second-gen-spectra-isp-massive-improvements-smartphone-photography/) 和 [Hexagon 685 DSP](https://www.xda-developers.com/qualcomm-snapdragon-845-spectra-uhd-premium-video/) 的规格。它还详细介绍了其全新的 Kyro 385 架构，该架构拥有比去年的 Snapdragon 835 显著的性能提升。

背景:骁龙系列的芯片架构使用基于 ARM 设计的定制 CPU 内核，在过去十年中有了长足的进步。高通的蝎子 CPU 核心其次是其定制的 Krait CPU 核心，从 2012 年的骁龙 S4 开始。2015 年，高通在 Snapdragon 810 和 808 中采用了 64 位库存 ARM Cortex-A57 和 Cortex-A53 内核的组合，并在此过程中淘汰了 Krait。但仅仅一年后，高通就带着 Snapdragon 820 重返定制 CPU 核心游戏。它标志着 Kryo 的首次亮相，Kryo 在单线程性能方面非常重视浮点 IPC(每时钟指令数)。

Kryo 的 CPU 性能和能效在高通在骁龙 808 和 810 中实施的 ARM Cortex-A57 上有所改善，但根据基准测试的[，它在整数 IPC 方面无法与 ARM 的 2016 内核 Cortex-A72 相匹配。不过，Kryo 在浮点 IPC 方面走在了前面。](https://www.xda-developers.com/geekbench-4-how-the-processor-ranking-changed-under-the-new-more-accurate-benchmark/)

然后，在 Snapdragon 835 上，高通用“半定制”CPU 内核再次改变了事情。Snapdragon 835 采用 Kryo 280“性能”内核，在每时钟整数指令数(IPC)方面比完全定制的前辈更快，但在浮点数学(FPM)方面有所退步。但是 Snapdragon 835 仍然是 Android 市场上最快的片上系统之一。

但是一种新的芯片即将取代它。**高通透露，其下一代旗舰片上系统骁龙 845 具有八个 Kryo 385 CPU 内核，四个 A75“性能”内核与四个 A55“效率”内核配对。**Kryo 385 内核基于 ARM Cortex license 高通设计，首次用于 Snapdragon 835 的 Kryo 280 内核，并采用第二代 10LPP(低功耗增强型)FinFET 工艺制造。

这些内核拥有一个专用的单内核 L2 高速缓存和一个共享的 2MB 三级高速缓存。他们使用 ARM 的 DynamIQ 技术，这是 ARM 在 5 月宣布的 big 的继任者。很少，它们有 3 个独立的时钟和电压域。

**另一方面，Kryo 385“高性能”内核的主频高达 2.8GHz，高于 Snapdragon 835 中 Kryo 280 的主频 2.4GHz。高通承诺“高性能”内核的性能提升 25-30%，整体能效提高 25-30%。**

另一方面,“高效”内核的主频为 1.8GHz。据高通称，它们比上一代产品快 15%。半定制内核基于 ARM Cortex-A55，高通承诺其异构计算平台利用骁龙 845’adre no GPU、Hexagon DSP 和 Spectra ISP 的组合处理能力，大幅提高性能和能效。

骁龙 845 还配备了高通快速充电 4.0，可以在 15 分钟内将智能手机电池充电 0 至 50%。快速充电 4.0 是 USB PD 的兼容超集，这意味着快速充电 4 充电器也将为 USB PD 兼容设备充电。

高通将骁龙 845 定位为不仅仅是一个处理器和一个强大的 GPU。它将其重新命名为“移动平台”，不难看出为什么——鉴于 ISP、DSP 等方面的[改进，高通的新芯片几乎无所不能。](https://www.xda-developers.com/qualcomm-second-gen-spectra-isp-massive-improvements-smartphone-photography/)

但是可以说 CPU 仍然是片上系统最重要的元素。乍看之下，看到高通承诺在 Kryo 385“性能”内核中实现高达 25-30%的性能提升令人兴奋。考虑到 Kryo 280 内核已经有多好，我们没有理由怀疑 Kryo 385 正如芯片制造商所说的那样令人印象深刻，但我们必须进行我们自己的测试，然后才能肯定地说。

编者按:这些是我们对高通骁龙 845 平台的初步印象——我们还没有时间来检验它。请放心，我们将继续我们的“热门话题”报道，更全面、详细地了解新的片上系统及其所有特性。