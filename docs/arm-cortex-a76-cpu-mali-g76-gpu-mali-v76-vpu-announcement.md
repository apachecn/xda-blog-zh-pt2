# Arm 宣布推出 Cortex-A76 CPU、Mali-G76 GPU 和 Mali-V76 VPU

> 原文：<https://www.xda-developers.com/arm-cortex-a76-cpu-mali-g76-gpu-mali-v76-vpu-announcement/>

Arm 是移动行业的重要参与者。该公司的 Cortex CPUs 被 Android SoC 领域的所有供应商使用，而其 Mali GPUs 被三星、海思和联发科技使用。

几年来，Arm 一直有在 TechDay 上发布新移动产品的传统。TechDay 2017 带来了 Arm Cortex-A75 和 Mali-G72，而 2016 年的 TechDay 带来了 Cortex-A73 和 Mali-G71。在 TechDay 2018 上，该公司公布了三款产品。首先是 Cortex-A76 CPU。然后我们有 Mali-G76 GPU，接着是 Mali-V76 VPU(视频处理单元)。

让我们一个一个地看看这些公告:

## Arm Cortex-A76 CPU

#### **背景**

在大多数情况下，Arm 的 Cortex CPUs 在性能和能效方面都有着良好的记录。在这一过程中出现了一些错误，例如 2015 年的高功耗 Cortex-A57，其效率有所下降(再加上 Snapdragon 810 等内核的糟糕实现，情况就更糟了)。然而，自那以后，Arm 的业绩已经说明了一切。

2016 年的 Cortex-A72 是一款出色的 CPU，整体速度更快，效率更高，超过了其主要竞争对手，Exynos 8890 中使用的三星 Exynos M1 和 Snapdragon 820 中最初的定制 Kryo 内核。[它无法与苹果的 A 系列芯片](https://www.xda-developers.com/a-widening-gap-the-a10-fusion-puts-a-chokehold-on-qualcomms-prospects/)正面竞争，但在 Android 世界，它比 Cortex-A57 前进了一大步。

2017 年的 Cortex-A73 带来了较低的个位数性能提升，但事实证明其能效明显高于 Cortex-A72。在效率方面，它击败了三星的 Exynos M2 CPU(用于 Exynos 8895)，同时获得了同等的性能。使用 Cortex-A73 的 SOC 包括高通骁龙 835 和海思麒麟 970。这两个 SOC 因提供了更高的效率而广受赞誉。该核心也已进入中端 SOC，包括[骁龙 660](https://www.xda-developers.com/qualcomm-unveils-snapdragon-660-and-snapdragon-630-two-upper-mid-tier-socs/) 、[骁龙 636](https://www.xda-developers.com/qualcomm-snapdragon-636-kryo-260-cpu/) 和联发科 [Helio P60](https://www.xda-developers.com/mediamediatek-helio-p6/) 。

今年，高通以其“半定制”Kryo 385 黄金核心的形式使用了 [Cortex A75](https://www.xda-developers.com/arm-unveils-cortex-a75-a55-processors-and-mali-g72-gpu/) 。海思尚未宣布 2018 年的新 SoC，而三星继续遵循定制核心路线，雄心勃勃，但实施不力 [Exynos 9810](https://www.xda-developers.com/samsung-unveils-exynos-9810-3rd-generation-custom-cpu-cores-mali-g72mp18-gpu/) 。审查和测试发现，骁龙 845 to [中基于 Cortex-A75 的 Kryo 385 Gold 比其前身](https://www.xda-developers.com/qualcomm-snapdragon-845-hands-on-benchmarks-first-impressions/)实现了可观的 25-30%的性能提升。A75 也用于新发布的[骁龙 710。](https://www.xda-developers.com/qualcomm-snapdragon-710-announcement/)

这让我们想到了 Cortex-A76——2018 年底/ 2019 年 SOC 可能选择的 CPU。

根据 Arm 的说法，Cortex-A76 使用新的微体系结构，性能提高了 35%。该公司正在宣传 Cortex-A76 是一款具有“笔记本电脑级性能”的 CPU。它面向智能手机等移动设备以及 ARM 笔记本电脑上的 Windows。

Cortex-A76 使用 Arm 的 DynamIQ 技术，该技术是去年与 Cortex-A75 一起发布的。据该公司称，它提供了笔记本电脑级的性能，同时保持了智能手机的能效。**就数字而言，Arm 承诺比 Cortex-A75 性能提升 35 %,这是一个很大的同比提升。与此同时，其效率比上一代产品提高了 40%。**

Arm 还提到，在 [Geekbench](https://www.xda-developers.com/geekbench-4-1-is-available-changes-the-way-scores-are-calculated/) 中，性能将提升 28%。这应该意味着 A76 将能够在这方面与 Exynos M3 相媲美，同时具有明显更好的能效。JavaScript 性能提高了 35%。性能的提升得益于 A76 的整数 IPC(每时钟指令数)比 Cortex-A75 多 25%。它的带宽也增加了 90%。浮点(FP)性能提高了 35%。

根据 Arm 的说法，Cortex-A76 还为人工智能/机器学习提供了 4 倍的计算性能提升。Arm 计划在 TSMC 7 纳米产品上以 3GHz 配置发布 CPU。关于新 CPU 的技术细节可以在这里阅读[。CPU 很可能会在 2018 年底之前推出商业产品。](https://community.arm.com/processors/b/blog/posts/cortex-a76-laptop-class-performance-with-mobile-efficiency)

## Arm Mali-G76 GPU

Mali-G76 GPU 是 Mali-G72 的继任者，而 Mali-G72 又是 Mali-G71 的继任者。

G71 是首款基于新 Bifrost 架构的 Mali GPU，继承了 Midgard 架构。Mali GPUs 被三星、海思和联发科等公司使用，而高通在其 Adreno GPUs 中使用自己的 GPU 架构。

到目前为止，Mali GPUs 还无法在持续性能和能效方面与竞争对手展开直接竞争。特别是 Mali-G71 的能效表现不佳。Mali-G72 确实在性能和能效方面取得了稳固的进步，但就性能功耗比而言，这是高通继续大幅领先竞争对手的一个领域。

Mali-G76 将改善 Arm 的竞争状况。该公司承诺提高 30%的效率和 30%的性能密度。最高性能提高了 25%。机器学习(ML)的改进是 2.7 倍。关于新 GPU 的更多技术细节可以在这里阅读。

## 马里武装部队-VPU v 76

Mali-V76 继承了 2016 年发布的 Mali-V61。VPU(视频处理器)是一个编码器/解码器，这意味着它可以编码和解码视频。Mali-V76 支持高达 60FPS 的 8K 解码或 60FPS 的四个 4K 流。Arm 表示，这让消费者有机会在视频会议期间录制视频，或者在 4K 观看四场比赛。在全高清分辨率下，视频处理器支持多达 16 个内容流，创建一个 4x4 视频墙。

VPU 的解码性能提高了两倍，尺寸比前代产品小 40%，编码质量提高了 25%。

关于 Mali-V76 的技术细节可以在这里阅读[。](https://community.arm.com/graphics/b/blog/posts/mali-v76-enabling-efficient-8k60-content)