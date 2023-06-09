# ARM 宣布推出 Cortex-A78 CPU、Mali-G78 GPU、Ethos N78 NPU

> 原文：<https://www.xda-developers.com/arm-announces-cortex-a78-cpu-mali-g78-gpu-ethos-n78-npu/>

作为 TechDay 2020 的一部分，ARM 发布了三项重大声明。头条新闻是 Cortex-X 定制程序(CXC)，包含新的 [Cortex-X1 CPU 内核](https://www.xda-developers.com/arm-announces-cortex-x-custom-cpu-program/)。Cortex-X1 带来了比任何 Cortex-A 系列 CPU 更高的峰值性能，同时打破了 Cortex-A 系列的 PPA 极限。ARM 发布的另外两个公告要常规得多。Cortex-A78 CPU 和 Mali-G78 CPU 现已正式发布，分别作为 [Cortex-A77](https://www.xda-developers.com/arm-cortex-a77-cpu-announcement/) CPU 和 [Mali-G77](https://www.xda-developers.com/arm-mali-g77-valhall-gpu-announcement/) CPU 的继任者。让我们逐一介绍这些公告:

## 手臂皮层-A78

对于 Cortex-A78，ARM 的主要关注点是效率需求，例如更长的电池续航时间、新的移动外形和不断缩小的 SoC 面积。持续的性能是 Cortex-A78 的关键词，而 Cortex-X1 的目标是实现最大的短期峰值性能。

ARM 表示，Cortex-78 代表了其以同类最佳效率实现高端性能的“最佳”驱动力。这些也不仅仅是空话。在过去几年中，Cortex-A76 和 Cortex-A77 表现出了同类最佳的能效和 PPA(性能、功耗和面积)。他们没有与苹果 A 系列芯片竞争所需的设计，但由于产生的功率较低，他们的能效在最坏的情况下与苹果相同，在最好的情况下甚至高于苹果。

A78 的性能改进涵盖了生产力、通信、安全性和基于相机的任务、高级游戏、XR 和基于 ML 的体验等使用案例。

在持续性能方面，Cortex-A78 带来了两位数的提升。与前代产品 Cortex-A77 相比，在相同的移动散热功率范围内，它的持续性能提高了 20%。 *AnandTech* 仔细查看了这些数字，并解释说，20%的数字是比 A77 高 7%的 IPC 的组合，而其余 13%的性能提升归功于 5 纳米工艺，下一代 SOC 都将在此基础上制造。ARM 指出了持续性能的重要性，称移动设备的功耗有限，持续性能可以避免对需要大量功率的应用进行功率调节。这反过来又通过避免延迟或丢帧来提高 UX。

提高能效意味着更高的能效，因为两者是相关的，但却是不同的概念。根据 ARM 的说法，在高性能点，如当前移动设备的峰值，Cortex-A78 在与 Cortex-A77 相同的性能下，比 2019 年的设备*节能 50%。这令人印象深刻，它使 A78 成为 CPU ARM 设计的最节能的 Cortex-A。*

ARM 对持续性能的关注将有利于下一波移动创新，如新的外形(可折叠手机)以及通过 5G 改善的“数字沉浸感”。现实的检验是，对于现在这一代人来说并非如此，即使在下一代也不会有太大影响。

Cortex-A78 将改进的一个用例是 AAA 移动游戏，与 ARM 自己的新 Mali-G78 GPU 结合使用。两者的结合旨在为手机带来高保真的游戏体验。它们更高的性能，加上 5G 的快速速度和高带宽，将使移动设备上的优质游戏成为可能。A78 的效率在这里有一个好处，因为它将为长时间的游戏提供更长的电池寿命。ARM 表示，它也在与生态系统合作，以进一步提高性能和构建更丰富的游戏体验，并给出了一个与 Unity 合作将 Burst 编译器引入 Android 的例子。

机器学习(ML)性能是 ARM 的另一个重点。CPU 是移动设备上 ML 计算的首选处理器，尽管现在高端 SOC 都带有独立的神经处理单元(npu)。ARM 的 CPU 支持智能手机上最受欢迎的真实世界 ML 应用和用例，如社交媒体过滤器、听写、安全和安全性。与 A77 相比，Cortex-A78 在处理基于 ML 的任务时平均耗电少 8%,官方效率提高了 10%。

### ARM Cortex-A78 -架构

ARM Cortex-A78 的架构与上一代相同(仍然是 ARM v8.2 内核)。然而，ARM 确实增加了微架构特性，旨在以更高的面积和能效推动性能。ARM 节省面积和功耗，同时保持所需的性能水平。同样，ARM 对 Cortex-A 系列的关注仍然是面积和能效，而不是峰值性能，后者现在由 Cortex-X 计划接管。

Cortex-A78 的性能提升是通过优化宽度和深度的额外微架构特性实现的。指令解码宽度保持为 4 宽度，与 A77 和 A76 相同。(另一方面，Cortex-X1 的解码宽度为 5，而 A13 的解码宽度为 7。)ARM 针对带宽和准确性以及指令融合情况增加了更好的分支预测。这些架构改进使单线程性能比 A77 提高了 7%。

通过减少低性能和低面积的结构，例如 L1-I 和 L1-D 高速缓存，效率得到了最大化。ARM 优化了现有结构以降低功耗，例如品牌预测结构。ARM 表示，与 A77 相比，这导致每兆瓦性能功耗降低 4%，每平方毫米性能面积降低 5%。

A78 始终专注于在集群级别实现一流效率的持续性能。由 4 个 Cortex-A77 和 4 个 Cortex-A55 CPU 组成的 DynamIQ 集群可以升级到 4 个 A78 内核和 4 个 A55 内核。这在减少 15%的面积中提供了 20%的持续性能提升。需要并行处理多个高性能线程的应用(如高保真游戏)将受益于持续的性能提升。

ARM 指出，A78 DynamIQ 集群的增强区域效率使其成为可折叠手机和多个更大显示器的理想选择。另一个重点是通过性能和能源的改善让智能手机为 5G 做好准备。5G 理应提供“更快的速度”、“更低的延迟”和“更快、更普遍的高带宽应用移动设备连接”。这可能是几年后的情况，但目前，这些好处对最终消费者来说并不明显。

总的来说，Cortex-A78 是一款可靠的产品。下一代旗舰 SOC 将集成多个 A78 内核，以补充具有更高功率和面积要求的单个 Cortex-X1 内核，一些价值导向型 SOC 甚至会选择完全跳过 Cortex-X1。对于中端 SoC 市场，A78 将成为 2021 年 SoC 的首选 CPU 内核，其对持续性能的关注值得欢迎。

* * *

## 马里武装部队-78 国集团

委婉地说，ARM 的 Mali 系列 GPU 远不如 Cortex 系列 CPU 成功。年复一年，Mali GPUs 在性能和能效方面一直优于苹果的定制 GPU 和高通的定制 Adreno GPUs。可悲的是，去年推出的新 Valhall 架构和 Mali-G77 GPU 并没有改变这一点。以 Mali-G77 为特色的 SOC 分别包括 [Exynos 990](https://www.xda-developers.com/samsung-exynos-990-5g-modem-5123-7nm/) 和[联发科天玑 1000L](https://www.xda-developers.com/mediatek-dimensity-1000-7nm-soc-integrated-5g/) 。不幸的是，这两款产品的实现都很弱，这意味着它们的 GPU 性能无法与高通的 Adreno 650 GPU 竞争，更不用说苹果 A12 和 A13 中的一流 GPU 了。Mali 已经落后多年，它的改进不足以改变移动 GPU 领域的现状。

然而，如果不乐观的话，ARM 什么都不是。它指出，其合作伙伴每年已售出超过 10 亿个 Mali GPUs，使 Mali 成为全球第一大 GPU 出货量。据推测，这个数字只会增加，因为更多不同类型的设备支持图形密集型用例，如高级移动游戏和 XR (VR 和 AR)。根据 ARM 的说法，这使得 Mali 成为整个生态系统中最广泛用于移动开发的 GPU。

ARM 指出，2019 年，它宣布了第一款基于 Valhall 架构的 GPU——Mali-G77。2020 年，Mali-G78 将接替 G77，后者也基于 Valhall 架构。虽然 ARM 说它是迄今为止高端移动设备中性能最高的 GPU，但数字并不支持它，尽管 ARM 讽刺地说这是有数字支持的事实。G78 在性能上比 G77 提高了 25%,这至少可以说是微不足道的。G77 和苹果 A13 的 GPU 之间的峰值 GPU 性能差距很大，这意味着 G78 将无法赶上 A13，更不用说即将推出的苹果 A14 的 GPU 了。高通也将继续保持领先一步，因为它自己的增量性能的改善。

改变游戏规则的图形和移动设备上的全天游戏已经可以在其他 GPU 上实现，所以 ARM 在这里的营销听起来有点空洞。

据 ARM 称，Mali-G78 是为开发者和最终用户设计的。它支持高质量的移动游戏体验，现在可以在移动设备上使用主机游戏。G78 为高端移动设备带来更长的电池寿命。它还为移动设备上更复杂的游戏、视频、相机和安全 ML 功能带来了进一步的 ML 性能提升。

ARM 看好手机游戏的前景。2019 年，移动游戏占全球游戏市场的 46%以上，收入达到 682 亿美元。它还将在未来几年继续增长，因为它将超过 PC 和主机游戏。越来越多的高端游戏将登陆移动设备，用户希望在移动设备上获得与游戏机类似的体验。

为了让这些体验成为可能，Mali-G78 配备了必要的性能提升。与 G77 相比，它的游戏内容性能密度提高了 15%。对于与上一代相同的面积，G78 将提供更高的性能。这一提升得益于四个关键特性:

*   支持多达 24 个内核
*   异步顶层
*   瓷砖改进
*   改进的片段依赖跟踪

虽然 G77 的最大内核数是 16 个，但 ARM 已经将 G78 的最大内核数增加到了 24 个。当然，仅仅因为有一个最大值并不意味着移动芯片供应商将实际纳入 24 核。到目前为止，我们看到的 G77 最广泛的核心变体是 Exynos 990 上的 Mali-G77MP11，而 Dimensity 1000 有一个 Mali-G77MC9。

ARM 认为异步顶级是 GPU 性能的一个改变游戏规则的特性。据说这是为了尽可能多地挤出手机游戏的性能，确保最大性能。

另一方面，Tiler 的改进为手机游戏增加了一层额外的质量。从 PC 和主机上带来的游戏，往往有着极其复杂的资产和精良的场景，造成了性能的症结和瓶颈。Tiler 的改进减少了这些复杂场景和资源在 GPU 上的顶点负载。这提高了复杂的类似控制台的游戏内容的性能。

ARM 还增强了 G78 上的片段依赖跟踪。这尤其会影响到包含烟雾、树木和草地等复杂游戏场景的手机游戏。结果是，与 G77 相比，ARM 在顶级移动游戏上的性能提高了 17%。

Mali-G78 的能效比上一代产品高 10%。同样，这也不足以赶上高通或苹果。ARM 在这里的目标似乎特别保守。异步顶级功能在能效方面发挥着重要作用，因为它可以降低功耗，从而以可持续的方式生成内容。因此，当设备以所需的帧速率输出内容时，它可以降低时钟频率以节省能源。增加该任务的顶级使用更多的能量，但是通过降低着色器核心的频率节省的能量要高得多。这是因为着色器核心使用了 GPU 90-95%的能量预算。

得益于融合乘加(FMA)，78 国集团也实现了更高的能效。它已经完全重新设计，导致该单位的能源减少 30%。FMA 单元负责 GPU 内部发生的大部分计算，这就是 ARM 将其作为节能目标的原因。

GPU 的并行数据处理能力使其适合运行 ML 工作负载，尽管 ARM 承认 CPU 和 GPU 仍然是 ML 的主要处理器。随着用例变得越来越复杂，一些工作负载将被卸载到 GPU。GPU 的主要 ML 用例与设备上的安全功能、不同的摄像头和视频模式以及具有 AR 功能的应用程序相关联。

ML 在 GPU 上的作用是实现照片或视频帧中的面部跟踪、使用 AR 功能的游戏等体验。对于这些基于 ML 的任务，与 G77 相比，Mali-G78 对各种 ML 工作负载的平均性能提高了 15%。与前几代产品相比，G77 的 ML 性能提高了 60%,因此今年的同比改善要小得多。异步顶级在提升 ML 性能方面至关重要，因为为着色器核心计时有助于 GPU 上的各种 ML 用例。

此外，还有 Mali-G68 的发布。这只不过是 Mali-G78 的缩小版，正如 Mali-G57 是 Mali-G77 的缩小版一样。ARM 表示，这是第一款用于 2021 设备的次高级 Mali GPU。它拥有 G78 的所有功能，如 tiler 改进和执行引擎中的新 FMA 单元，但支持多达 6 个内核，而不是 24 个。这款 GPU 的目标是以更低的成本获得近乎完美的性能。

ARM 在听取了合作伙伴的反馈后开发了这一次高级 GPU 层，这些合作伙伴希望他们的设备组合具有高级功能。正如预期的那样，G68 具有更低的芯片面积，并为更广泛的开发者和消费者带来高性能游戏。

最后，ARM 提到了它的开发者合作伙伴关系。它使得开发者可以很容易地优化他们的内容，以便在 Mali GPUs 上更好地运行(理论上)。性能顾问就是一个例子。其次是 ARM 与 Unity 合作，带来了 Burst 编译器。这方面的详细信息可以在源文章中阅读。

### 马里-78 国集团-展望

马里-78 国集团的前景黯淡。看起来，ARM 似乎对在苹果和高通过去制造的同一模具中实现逐年大幅性能提升不感兴趣。虽然高通的改善速度也有所放缓，但其基线水平高于 ARM。当评论者用数字证据表明 A13 的 GPU 持续性能高于骁龙 865 的峰值性能时，这对 Android 生态系统来说看起来很糟糕。苹果和安卓 GPU 之间的性能差距正在扩大，而且只会越来越大。

因此，G78 并不是解决 ARM 的 Mali GPU 困境并将其带到性能图表顶端的神奇解决方案。它的排名仍将低于苹果和高通的 GPU。它将成为一些 SOC 的默认选择，因为它是 ARM 的股票 GPU IP，定制解决方案有进入壁垒，成本也更高。

明年，三星系统 LSI 是否真的会使用 Mali-G78 还是个疑问。三星一直是 Mali GPUs 的重要客户，但去年，[它与 AMD 签署了合作伙伴关系，将在 2021 年将 RDNA GPU 架构](https://www.xda-developers.com/samsung-amd-partnership-hatch-game-streaming-galaxy-s10-5g/)引入其移动 SOC。如果这个路线图保持在正轨上——在这一点上，我们没有理由怀疑它不在正轨上——那么 Exynos 990 的继任者将采用 AMD RDNA GPU，而不是 Mali GPU。事实上，这将是 ARM 在设计上的一大损失。即使是其他厂商，如联发科，这些天也有更多的选择。Imagination Technologies 的新 [A 系列 GPU 架构](https://www.xda-developers.com/imagination-technologies-a-series-gpu-architecture-launch/)的设计目标是比 G78 更高的性能，联发科有可能在未来放弃 Mali。当然，高通没有理由放弃其 Adreno GPU 的努力，当专门谈论 Android 智能手机市场时，它在性能和效率方面仍然是同类最佳的。

因此，很明显，ARM 需要提高 Mali GPUs 的年改进率，才能在移动 GPU 市场上发挥真正的作用。如果做不到这一点，它将面临在高端旗舰移动 GPU 领域被边缘化的风险。

* * *

## ARM Ethos N78

最后，ARM 还宣布了 Ethos N78 神经处理单元(NPU)。它是 N77 NPU 的继任者。它提供了更强大的设备上 ML 功能，性能效率提高了 25%。可配置性也是一个优势，因为可用的配置范围从 1 TOP/s 到 10 TOP/s。有关更多详细信息，请查看 [ARM 的博客文章](https://community.arm.com/developer/ip-products/processors/b/processors-ip-blog/posts/arm-ethos-n78-npu?_ga=2.207546451.1140308209.1590544784-339760549.1590544784)。由于高通、三星、海思和联发科都有自己的神经处理单元/人工智能引擎，这种 NPU 可能只会获得有限的设计胜利。

* * *

**来源:ARM ( [1](https://community.arm.com/developer/ip-products/processors/b/processors-ip-blog/posts/arm-cortex-a78-cpu) 、 [2](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/arm-mali-g78-gpu) )、AnandTech ( [1](https://www.anandtech.com/show/15813/arm-cortex-a78-cortex-x1-cpu-ip-diverging) 、 [2](https://www.anandtech.com/show/15816/arm-announces-the-malig78-evolution-to-24-cores) )**