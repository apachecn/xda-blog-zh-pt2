# ARM 宣布推出采用 Valhall 架构的中端 Mali-G57 GPU

> 原文：<https://www.xda-developers.com/arm-mali-g57-gpu-launch-valhall-architecture/>

5 月，ARM 公布了 ARM [Cortex-A77 CPU](https://www.xda-developers.com/arm-cortex-a77-cpu-announcement/) 架构和 ARM [Mali-G77 GPU](https://www.xda-developers.com/arm-mali-g77-valhall-gpu-announcement/) 。Mali-G77 GPU 是首款采用新“Valhall”架构的 GPU，该架构继承了自 2016 年以来一直为 ARM 的 GPU 提供支持的 Bifrost 架构。高级 Mali-G77 将作为三星全新 Exynos 990 旗舰 SoC 的一部分出现，但 ARM 也开发了面向平价设备的中档主流 GPU。最后一个这样的中端 ARM GPU 是 ARM [Mali-G52](https://www.xda-developers.com/arm-mali-g52-g31-gpus-mali-d51-display-mali-v52-video-processors/) ，它找到了通往[海思麒麟 810](https://www.xda-developers.com/hisilicon-kirin-810-honor-9x-benchmark-snapdragon-730/) 的道路。现在，ARM 宣布了它的继任者 Mali-G57 GPU，这是第一款采用 Valhall 架构的主流 ARM GPU。

根据 ARM 的说法，Mali-G57 支持高级功能，如高保真内容、手机上类似控制台的图形以及更复杂的 ML、AR 和 VR 工作负载。它通过带来我们期望从高端 GPU 获得的性能改进来实现这一点。与 Mali-G52 相比，Mali-G57 在从游戏到高分辨率 2D 内容的一系列内容中提供了 30%的更高性能密度，并且其纹理性能也提高了一倍。ARM 表示，这“大大提高了 4K 和 8K 数字电视、AR 和 VR 以及游戏的高分辨率用户界面的性能”。据说它也是处理更复杂的 3D 工作负载的绝佳选择，如基于物理的渲染(PBR)、HDR 渲染和体积效果。

更重要的是，ARM 声称已经“显著提高了能效”。该公司过去的高级 GPU，如 Mali-G71 和 Mali-G72，一直以来能效都很低。Mali-G57 声称与 Mali-G52 相比能效提高了 30%,这应该会延长电池寿命。

ARM 优先考虑的是成本效益。该公司表示，Mali-G77 至少有 7 个内核，而 Mali-G57 根据配置有 1 到 6 个内核。这应该使它适合主流手机——例如，麒麟 810 使用六核版本的 Mali-G52。

ARM 也在谈论机器学习(ML)性能。Mali-G77 将 ML 性能提高了 60%，Mali-G57 据说也有“类似”的改进。与 Mali-G52 相比，fma 增加了 2 倍，实现了 60%的片上 ML 性能提升，同时实现了架构优化。根据 ARM 的说法，这为语音识别、人脸检测和图像质量增强等 ML 用例提供了更快的响应速度，并具有执行不同 ML 工作负载的灵活性。

该公司然后继续谈论 AR 和 VR。虽然 AR 在智能手机上仍然是一个新兴的主题，但随着谷歌 Daydream 的死亡和消费者对智能手机 VR 的普遍缺乏兴趣，虚拟现实通常被业界认为已经被埋葬了。然而，根据 ARM 的说法，Mali-G57 性能的提高和新技术的引入有助于提供更好的 AR 和 VR 体验。

最后，ARM 说说 Valhall GPU 架构。自然，该公司表示，这对开发人员至关重要，因为它的设计符合 Vulkan 等现代 API。ARM 承诺，由于 Mali-G57 的性能和能效改进，游戏在设备上的运行将更流畅、更持久。Valhall 架构是 ARM 最新一代 GPU 的当前基础，有关它的更多细节可以在 [Mali-G77 发布文章](https://www.xda-developers.com/arm-mali-g77-valhall-gpu-announcement/)中阅读。该架构的主要特性包括一个新的超标量引擎、一个简化的标量 ISA 和指令的动态调度——这些因素是 ARM 宣布在 Mali-G57 中实现性能和能效改进的关键。

高通在智能手机中使用自己的 Adreno GPUs，而三星系统 LSI、海思和联发科都依赖于 ARM 的 Mali GPUs。比如红米 Note 8 Pro 的[联发科 Helio G90T](https://www.xda-developers.com/mediatek-helio-g90-series-hyperengine-game-technology-launched/) SoC 采用 Mali-G76MC4 GPU。我们预计 Mali-G57 将出现在上述三家厂商生产的新型中端 GPU 中。如果它兑现承诺，从竞争角度来看，这对中端智能手机 GPU 市场只会是一件好事。

除了 Mali-G57 GPU，ARM 还发布了 Ethos-N57 和 Ethos-N37 NPUs(神经处理单元)以及 Mali-D37 DPU(显示处理单元)。后者据说可以在“最小的面积”内提供丰富的功能集，实现全高清和 2K 分辨率，而 npu 则是智能手机的专用神经处理硬件。N37 和 N57 NPUs 针对 1 和 2 TOP/S ML 性能范围进行了优化。

* * *

**来源:** [手臂](https://community.arm.com/developer/tools-software/graphics/b/blog/posts/arm-mali-g57-gpu)