# ARM 宣布推出 Mali-G77 GPU，采用全新的“val hall”GPU 架构，性能提升 1.4 倍

> 原文：<https://www.xda-developers.com/arm-mali-g77-valhall-gpu-announcement/>

ARM 在其年度 TechDay 上发布了 Mali-G77 GPU 以及 Cortex-A77 CPU。虽然 Cortex-A77 相对于其前身 Cortex-A76 来说是一个重大的时代进步，但 Mali-G77 GPU 则完全不同。这是自 2016 年带来 Bifrost 架构的 Mali-G71 以来，ARM Mali 阵容中第一个带来新 GPU 架构的 GPU。Mali-G77 带来了全新的“Valhall”架构。

尽管 ARM 的 CPU IP 在更广泛的智能手机领域一直颇具竞争力，但该公司的 Mali 系列多年来一直难以与一流的解决方案竞争。一次又一次，Mali 系列 GPU 在性能和能效方面被证明不如他们的 Adreno 和 Imagination Technologies 的 PowerVR GPUs。Bifrost 架构继承了 Midgard 架构，从向量类型切换到标量类型。不幸的是，它并没有克服性能和能效之间的差距，而这一差距似乎越来越大。Mali-G71 和 Mali-G72 遭受了过高的功耗和节流，这使得它们不如高通的 Adreno GPUs 和苹果的定制 GPU(从苹果 A11 开始)。

糟糕的 GPU 性能成为一个如此重要的问题，以至于供应商们正在展望一代人之后实现的较小 GPU 增益的前景。例如， [Exynos 9810](https://www.xda-developers.com/samsung-unveils-exynos-9810-3rd-generation-custom-cpu-cores-mali-g72mp18-gpu/) 的 Mali-G72MP18 GPU 是对其前身的温和改进。华为的海思集团与 Mali GPUs 的斗争要大得多。海思[麒麟 960](https://www.xda-developers.com/huawei-mate-9kirin-960-early-testing-comparison-with-pixel-xlsnapdragon-821/) 和[麒麟 970](https://www.xda-developers.com/huawei-p20-pro-review/) 被 GPU 消耗异常高的功率，同时提供相对较少的性能，以至于华为被迫引入一种非常规的节流机制，导致去年几款华为手机被发现[基准测试作弊](https://www.xda-developers.com/huawei-p20-huawei-nova-3-honor-play-cheating-benchmarks/)。

令人欣慰的是，去年的 Mali-G76 确实在性能和功效方面取得了实质性的进步。使用 10 核版本的 Mali-G76，海思能够承诺 46%的性能提升，即使该公司达到了性能数字，[它仍然无法获得 GPU 性能(峰值和持续性能)](https://www.xda-developers.com/huawei-mate-20-pro-review/)以及能效冠军。三星系统 LSI 在 Exynos 9820 中实现了 12 核版本的 GPU，[最终缩小了与](https://www.xda-developers.com/samsung-galaxy-s10e-review-exynos/)[高通骁龙 855 的 Adreno 640 GPU](https://www.xda-developers.com/qualcomm-snapdragon-855-snapdragon-845-kirin-980-cpu-gpu-ai-benchmarks/) 的差距。高通的 Adreno GPUs 仍然是安卓市场的领头羊，但苹果去年凭借苹果 A12 的定制 GPU 走得更远。苹果能够在峰值和持续性能方面击败高通，该公司也展示了具有竞争力的能效。目前，A12 的 GPU 仍然是领导者，而骁龙 855 的 Adreno 640 GPU 在大多数基准测试中排名第二。

面对这种竞争环境，ARM 需要站出来迎接挑战。

其结果是 Mali-G77 和新的 Valhall 架构。ARM 表示，它的性能密度提高了 30%，能效提高了 30%，机器学习(ML)提高了 60%。ARM 预计基于 Mali-G77 的移动设备的峰值图形性能将提高 40%。

该公司预计 Mali-G77 将为手机带来更多高端游戏，并指出 2018 年是移动游戏收入首次超过主机和 PC 游戏收入的一年。

关于 ML，ARM 表示，Mali-G77 为设备提供了在设备上更快地执行“日益复杂”的 ML 任务的能力，性能密度提高了 60%。这比将它们发送到云中进行处理要好，后者会导致更多的安全问题和性能下降，以及更高的延迟。

新的 Valhall 架构是 Mali-G77 和未来 Mali GPUs 的基础。ARM 表示，Valhall 的以下特性使其成为一种“新颖的架构”:

*   “全新的超标量引擎，在能效和性能密度方面实现了又一次飞跃
*   一个简化的标量 ISA，具有新的指令集，对编译器更加友好
*   新的指令动态调度
*   返工的数据结构更好地符合现代 API，如 Vulkan。
*   虽然有许多不同的进步和新功能，但两个关键的是 Mali-G77 中的执行引擎和纹理映射器。"

根据 ARM 的说法，Mali-G77 的宽执行引擎通过共享对大量通道的控制来提高性能密度。Mali-G76 有 8 个宽度的扭曲，每个着色器核心共有 24 个 FMA 通道，而 Mali-G77 有 16 个宽度的扭曲，32 个通道(每个执行引擎有两个 16 FMA 的集群)，每个着色器核心有一个引擎。据该公司称，与 G76 相比，这导致相同区域的计算量增加了 33%。

ARM 还表示，Mali-G77 游戏性能的提高与四纹理映射器有关，该映射器每周期提供四个纹理元素，吞吐量比 Mali-G76 高 2 倍，比 G72 高 4 倍。据说它可以全面改善高保真和休闲游戏，但它对纹理密集型游戏的影响尤其大。根据 ARM 的说法，G77 的计算能力已经增加，因此纹理能力也需要增加，以保持机器的平衡。最终目标是什么？每平方毫米的性能比以前更高。

Mali-G77 已经过优化，以匹配新的 16 宽执行引擎和四纹理映射器。这种优化包括 LSC 和属性管道的重新设计，重点是性能密度和能效。

ARM 表示，它“非常重视”提高能源效率，并宣传 Mali-G77 可以用两年前 Mali-G72 的 50%的能源完成同样的工作。据该公司称，Valhall 架构和 Mali-G77 提高了所有工作负载的能效，使“各种内容”的能效提高了 1.3 倍，这意味着用户将在高端设备上获得更长的电池寿命。

ARM 表示，现在在硬件中处理动态指令调度，以实现更好的性能。据说动态调度器决定从哪个 warps 执行哪个指令，然后工作以超标量方式被发送到独立的并行 alu。

最后，ARM 指出，Valhall 架构通过 AFBC 1.3 延续了 ARM 帧缓冲压缩的发展。它带来了一些新功能，可以在 ARM 的博客文章中读到。

ARM 对 Mali-G77 有一些重大承诺，宣称它将在复杂的 AR 和 ML 中带来显著的性能改善，并提供“毫不妥协的图形性能和更高的效率”。如果这种说法成立，我们最终可能会看到 ARM Mali GPU 与特定一代的 Adreno GPU 并驾齐驱，甚至更胜一筹，移动 GPU 市场的竞争将变得更加激烈。

**来源** : [手臂](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/introducing-arm-mali-g77-with-new-valhall-architecture?_ga=2.263563279.2020090613.1558938898-871757968.1558938898)

**经** : [安耐特](https://www.anandtech.com/show/14385/arm-announces-malig77-gpu)