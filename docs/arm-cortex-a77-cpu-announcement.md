# ARM 宣布推出性能提升 20-35%的 Cortex-A77 CPU 内核

> 原文：<https://www.xda-developers.com/arm-cortex-a77-cpu-announcement/>

在 ARM 的年度 TechDay 活动上，ARM 发布了 Cortex-A77 CPU 内核。Cortex-A77 的发布与 [ARM Mali-G77 GPU](https://www.xda-developers.com/arm-mali-g77-valhall-gpu-announcement/) 的发布同时进行，这是第一款拥有全新“val hall”GPU 架构的 GPU。这两款产品一起分别接替去年的 [Cortex-A76 CPU 和 Mali-G76 GPU](https://www.xda-developers.com/arm-cortex-a76-cpu-mali-g76-gpu-mali-v76-vpu-announcement/)。

总部位于英国的 ARM 于 2016 年被总部位于日本的软银收购，是科技行业最重要的公司之一。世界上的每一部智能手机都是由 ARM 的指令集驱动的。高通使用半定制的“为 Cortex 制造”许可证，允许该公司在其产品中集成 ARM 的 CPU IP 的定制变体(例如，Kryo 485 Gold 是 Cortex-A76 的半定制变体)。[华为的海思集团*是*另一个 ARM 的 CPU 知识产权](https://www.xda-developers.com/arm-suspend-business-huawei/)的高调授权者，使用 ARM 的 CPU 核心的库存版本，而三星系统 LSI 和苹果使用完全定制的核心基于 ARM 的指令集。三星和海思也授权 ARM 的 Mali GPUs 用于他们的内部 SOC，而高通和苹果选择使用他们的定制 GPU 解决方案(例如，高通使用自己的 Adreno GPUs)。

这就是为什么当 ARM 发布新的公告时，它会对智能手机行业产生重大影响。好消息是，ARM 在制造新的 CPU 微体系结构方面已经有一段时间了。Cortex-A72、Cortex-A73 和 [Cortex-A75](https://www.xda-developers.com/arm-unveils-cortex-a75-a55-processors-and-mali-g72-gpu/) 都是值得尊敬的设计，弥补了 Cortex-A57 的错误。然而，去年的 Cortex-A76 在性能方面更上一层楼，因为它承诺“笔记本电脑级的性能”，比已经具备功能的 Cortex-A75 性能提高 35%。因此，[高通承诺将骁龙 855](https://www.xda-developers.com/qualcomm-snapdragon-855-performance-gaming-ai-improvements-explained/) 的性能提升 45%--这是骁龙 SoC 有史以来最大的性能提升。

Cortex-A76 在 IPC、PPA 和效率领域表现出色。它拥有业界最好的 PPA，芯片面积小。它确实受益于 TSMC 出色的 7 纳米 FinFET 工艺，但它带来的 IPC 改进也留下了印记。它设法在 [Exynos 9810](https://www.xda-developers.com/samsung-unveils-exynos-9810-3rd-generation-custom-cpu-cores-mali-g72mp18-gpu/) 中胜过三星的 Exynos M3 定制核心，尽管解码宽度更窄(4 宽对 6 宽)。即使今年在 [Exynos 9820](https://www.xda-developers.com/samsung-exynos-9820-samsung-galaxy-s10/) 中发布的 Exynos M4 内核也不足以抢走 ARM 的性能优势(尽管它确实缩小了差距)，因为 Cortex-A76 [仍然比 Exynos M4 享有性能和效率优势](https://www.xda-developers.com/samsung-galaxy-s10e-review-exynos/)。(Exynos 也因低劣的制造工艺而令人失望:8 纳米 LPP 对 7 纳米 FinFET)。尤其是 Cortex-A76 的能效令人难以置信。使用 Cortex-A76 的 SOC 包括旗舰 SOC，如[海思麒麟 980](https://www.xda-developers.com/hisilicon-kirin-980-honor-magic-2-huawei-mate-20-pro/) 和[高通骁龙 855](https://www.xda-developers.com/qualcomm-snapdragon-855-snapdragon-845-kirin-980-cpu-gpu-ai-benchmarks/) ，但我们也开始在中端 SOC 中看到它，如[高通骁龙 675](https://www.xda-developers.com/qualcomm-snapdragon-675-chipset/) 和[骁龙 730/730G](https://www.xda-developers.com/qualcomm-snapdragon-665-snapdragon-730g/) 。对性能的影响是有效的。

在移动领域，就每时钟指令数(IPC)而言，Cortex-A76 仍不如苹果 A11 和苹果 A12 上的定制内核。然而，ARM 没有表现出放缓其改进速度的迹象。今年 8 月，该公司公布了其 CPU 核心路线图，其中包括 2019 年的“戴莫斯”核心和 2020 年的“大力神”核心，这两个核心都基于 Cortex-A76。令人印象深刻的是，该公司承诺 Austin core 系列中的每个新芯片组每年都会带来 20-25%的 CAGR 性能提升。手臂向前加速。

Cortex-A77 是“戴莫斯”CPU 核心，它将在 2019 年底和 2020 年初成为旗舰 SOC。它是 Cortex-A76 的演变，是奥斯汀核心系列的第二次迭代。CPU 是 A76 的直接微体系结构继任者，其大多数核心功能是相同的。供应商将能够轻松升级 SoC IP。在架构方面，它仍然是一个 ARM v8.2 CPU 内核，旨在与 Cortex-A55“小”内核配对，而不是一个 DynamIQ 共享单元(DSU)集群。

Cortex-A77 的缓存大小为:64KB L1 指令和数据缓存、256 和 512KB L2 缓存以及高达 4MB 的共享 L3 缓存。性能的提高必须来自微架构的改进，因为内核的频率预计不会改变(ARM 仍然像 A76 一样以 3GHz 为目标，但与 A76 一样，我们很可能会看到供应商推出更低时钟内核的设计)。下一代 SOC 的工艺改进预计不会像 2018 年那样大。(TSMC 今年已经转向 7 纳米 EUV 工艺，这很可能是下一代麒麟和骁龙芯片组的基础。)

因此，Cortex-A77 具有改进的微体系结构，性能提高了 20%-35%。A76 在架构方面不同于其前辈，它旨在为奥斯汀核心家族的下两个设计提供基线:2019 年的 Cortex-A77 和 2020 年的“大力神”。

ARM 的主要目标是提高架构的 IPC，并继续专注于提供业界最佳的 PPA(功率、性能和面积)。A76 的面积和能效优势仍将是 A77 的优势。

在微架构方面，ARM 有了很大的改变。在前端，内核具有更高的提取带宽，品牌预测器功能增加了一倍，新的宏运算高速缓存结构充当 L0 指令高速缓存，新的整数 ALU 流水线，以及改进的加载/存储队列和发布功能。此外还有动态代码优化，在 ARM 的博客中有详细的解释。解码宽度保持为 4 宽度。

内核的后端也有所改进，我建议用户阅读 AnandTech 的报道以了解更多细节。ARM 增加了一个额外的整数 ALU。数据预取器也得到了改进，这是一个好消息，因为根据 *AnandTech* 的说法，A76 已经拥有了优秀的预取器。添加了新的额外预取引擎，以提高预取准确性。这一切都与核心的内存子系统有关，这是一个根本性的方面。CPU 的内存子系统由内存延迟和内存带宽组成。

## ARM 承诺 Cortex-A77 的性能提升 20-35%

根据 ARM 的说法，Cortex-A77 的 IPC 单线程性能比其在 Geekbench 4 中的前辈提高了 20%，在 SPECint2006 中提高了 23%，在 SPECfp2006 中提高了 35%，在 SPECint2017 中提高了 20%，在 SPECfp2017 中提高了 25%。所有这些都是在 7 纳米工艺和 3GHz 频率下设计的。如果这些改进得以实现，下一代 SOC 可能会在未来的智能手机上提供一些惊人的性能和电池寿命体验。尤其是 FP 的改进是一代人的重大改进。当然，A77 不会没有竞争，因为三星将在 2020 年带着 Exynos M5 回来，在此之前，苹果的 A13 肯定会成为新 iPhones 的一部分。

ARM 还表示，A77 的能效将与 A76 SoCs 保持一致。这意味着，在最高性能下，CPU 内核将使用相同的能量(以焦耳为单位)来完成一项任务。但是，动力和能量是两个不同的概念。A77 的功耗将随着性能的提高而线性增加。这可能导致电话中 TDP 限制的问题。为了应对这种情况，我们已经看到主要厂商采用大+中+小的非常规核心配置(海思采用 2+2+4，高通采用 1+3+4)。A77 也将比 A76 大 17%，这意味着它仍将拥有一流的 PPA。

我一直是 A76 实现的忠实粉丝，因为它甚至在骁龙 675 等中档 SOC 中也工作得非常好。骁龙 855 和麒麟 980 都是高性能的旗舰 SOC，我迫不及待地想看到 A77 的实施在下一代 SOC 中带来的改进水平。ARM 表示，其主要客户仍然非常关注拥有最佳 PPA，很容易看出该公司在这方面提供了最佳解决方案。

我们什么时候能在 SoC 中看到 A77？在最近与华为的动荡事件之前，我会说海思麒麟 985 肯定会在 2019 年为真正的下一代 SoC 配备 A77 和 Mali-G77 GPU。然而，随着 ARM 决定切断与华为的联系，我怀疑这是否还有可能，除非与华为的一触即发的局面在未来几周得到解决。高通的下一代旗舰产品骁龙 SoC 可能要到 2020 年第一季度才会向消费者发货，所以希望使用 ARM 最新 CPU 内核的消费者可能需要等待一段时间。

**来源** : [手臂](https://community.arm.com/developer/ip-products/processors/b/processors-ip-blog/posts/new-arm-cortex-a77-provides-compute-performance-leadership?_ga=2.263563279.2020090613.1558938898-871757968.1558938898)

**经** : [安耐特](https://www.anandtech.com/show/14384/arm-announces-cortexa77-cpu-ip)