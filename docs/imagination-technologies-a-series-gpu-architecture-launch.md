# Imagination 的新 A 系列 GPU 架构是该公司 15 年来最大的一次发布

> 原文：<https://www.xda-developers.com/imagination-technologies-a-series-gpu-architecture-launch/>

如今，移动 GPU 市场由高通的定制 Adreno GPUs 和 ARM 的 Mali GPUs 主导。然而，在过去，情况有所不同。移动 GPU 市场上多了一些竞争对手，这有助于提高行业竞争力。尤其是 Imagination Technologies，它是该行业的主要参与者之一。这家总部位于英国的公司仍然是移动 GPU 领域的领导者之一，这要归功于供应商对其 GPU 技术的许可，但目前其自有 PowerVR 品牌的 GPU 很少出现在产品中。过去，其高端移动 GPU 被苹果用于该公司的 A 系列 SOC，直到 2016 年的苹果 A10。另一方面，其低端和中端 GPU 被联发科、瑞芯微等公司使用。现在，Imagination Technologies 以新 A 系列架构的形式推出了主要的 GPU 架构。该公司称之为 15 年来最重要的 GPU 公告，并宣传新的 GPU 拥有世界上最快的 GPU IP。

要了解这如何影响移动 GPU 市场，让我们深入研究该公司的背景，看看它如何适应移动 GPU 市场。

## 想象科技-背景

Imagination Technologies 自 20 世纪 90 年代以来一直是移动 GPU 市场的领导者之一。该公司拥有多项 GPU IP 专利，这意味着 SoC 厂商必须向其支付许可费。其基于图块的延迟渲染(TBDR)技术就是一个很好的例子。GPU 的 PowerVR 品牌与高通的 Adreno GPUs 和 ARM 的 Mali GPUs 竞争，但在德州仪器 2012 年倒闭后，该公司在高端的唯一授权厂商是苹果。

苹果和 Imagination 一直联系到 2017 年，因为 Imagination 甚至为 iPhones 和 iPads 构建了定制版本的 PowerVR GPUs。苹果证实，2016 年 3 月，它正在与 Imagination 讨论收购该公司，但没有达成交易。2017 年 4 月，Imagination 宣布，苹果已经告诉该公司，它将在 15-18 个月内过渡到定制 GPU，从 Imagination 的 PowerVR GPUs 转移。几个月后，Imagination 宣布了一个令人震惊的消息:它准备出售自己，由于最大的客户不再使用它的技术，它的市值在短时间内大幅减少。Imagination 于 2017 年 9 月被中国投资者投资的加州股权公司 Canyon Ridge 收购。至少可以说，事态的发展令人惊讶。

同月，苹果在推出 iPhone 8/iPhone X 的同时推出了 A11 SoC。A11 据说包含苹果的第一个定制 GPU。然而，苹果继续向 Imagination 支付许可费，因为 A11 的定制 GPU 仍然使用 Imagination 的 GPU 技术(包括 TBDR)。据 [*AnandTech*](https://www.anandtech.com/show/11867/imagination-technologies-to-be-acquired-by-canyon-bridge-for-550m) 报道，苹果的定制 GPU 设计通常被认为是 2015 年 Imagination 的 IP 的一个分叉，苹果凭借一个架构许可继续独立开发。苹果和 Imagination 之间的关系目前还不得而知，官方称，苹果的定制 GPU 架构仍然是一个黑盒。

被 Canyon Ridge 收购后，Imagination 发现自己的高端 GPU 没有客户。该公司的 PowerVR Rogue 架构已经在高端的 iPhone 和 iPad 上找到了出路，但在 A11 之后，就没有其他买家了。在低端和中端市场，Imagination 继续将 GPU 技术授权给联发科技、瑞芯微和优尼科等厂商。不过，它的 PowerVR 8XT 和 9XTP 架构没有进入任何出货产品。事实上，联发科从使用 PowerVR GPUs 迁移到使用 ARM 的 Mali GPUs。例如， [Helio P90](https://www.xda-developers.com/oppo-reno-z-review-great-despite-the-software/) 使用了 Imagination 的 PowerVR GM9446 GPU(那是基于更老的 Rogue 架构)，但联发科随后在 [Helio G90T](https://www.xda-developers.com/mediatek-helio-g90-series-hyperengine-game-technology-launched/) 中转移到了 ARM 的 Mali-G76MC4 GPU。

与此同时，事实证明 ARM 的 Mali GPUs 本身在移动 GPU 市场上缺乏竞争力，因为与高通定制的 Adreno GPUs 和最近的苹果定制 GPU 相比，它们的 PPA(单位面积性能)较差。ARM 的 Mali-G71 和 [Mali-G72](https://www.xda-developers.com/arm-unveils-cortex-a75-a55-processors-and-mali-g72-gpu/) 相比当时的 Adreno GPUs，性能和功耗效率都比较逊色。虽然 [Mali-G76](https://www.xda-developers.com/arm-cortex-a76-cpu-mali-g76-gpu-mali-v76-vpu-announcement/) 是一个坚实的改进，但它仍然不足以从高通手中夺走 Android 市场上移动 GPU 性能和效率的桂冠。

高通在 Android GPU 市场处于有利地位，因为它的 GPU 享有同类最佳的性能，但在更广泛的 SoC 市场，它发现自己被苹果的定制 GPU 打败了。Apple A11、A12 和 A13 SoCs 中的定制 GPU 分别比 Snapdragon 835、骁龙 845 和骁龙 855 中的 Adreno 540、Adreno 630 和 Adreno 640 快得多。突然间，苹果在移动 GPU 性能上大幅领先，高通退居第二。ARM 的 Mali GPUs 在 PPA 和能效方面有些落后。

今年 5 月，ARM 开始纠正性能和效率方面的不足，宣布了采用新 Valhall GPU 架构的 Mali-G77，性能提高了 40%。GPU 以三星 [Exynos 990](https://www.xda-developers.com/samsung-exynos-990-5g-modem-5123-7nm/) 和[联发科天玑 1000](https://www.xda-developers.com/mediatek-dimensity-1000-7nm-soc-integrated-5g/)SOC 的形式赢得了前两次设计胜利。

截至 2019 年年中，移动 GPU 市场反映了苹果和高通开发的定制 GPU 优于 ARM 和 Imagination 等公司的授权 GPU 的现实。就竞争而言，这对行业来说是一件坏事，因为如果许可的知识产权劣于不会许可给任何第三方 SoC 供应商的定制知识产权，它就会成为竞争的障碍。三星知道这一点，该公司已经承诺在未来的 Exynos SoCs(将在两年内推出)中授权 AMD 的 GPU IP。

在这种背景下，Imagination 公司 15 年来最重要的公告发布了。

## AXT、AXM 和 AXE 系列 GPU

Imagination 宣布了其新的 A 系列 GPU 架构，声称它拥有有史以来最快的 GPU IP。这是一个很大的索赔。该公司的目标是展示该架构优于苹果和高通定制的 GPU。本质上，Imagination 希望让授权 GPU 重新变得可行，并提供比 ARM 的 Mali GPUs 更好的替代方案。

A 系列架构是 Imagination 的第十代 GPU 架构。它由三类 GPU 组成:XE、XM 和 XT 产品线，分别代表低端、中端和高端市场。PowerVR 品牌不再用于描述该架构，因为该公司现在使用它来描述 TBDR 理工大学。最快的 GPU IP 声明适用于 XT 产品线，因为它旨在作为移动 GPU 的高级系列。

在 ISO 面积和流程节点比较中，A 系列 GPU 架构被 Imagination 声称比 Imagination 的上一代 9 系列 GPU 快 2.5 倍。Imagination 没有将一个系列与 8XT 或 9XT 系列进行比较，因为没有公开可用的产品使用这些 GPU 系列。AnandTech 指出，这些数据可能基于 Helio P90 的 GM9446 GPU，这是一种基于 Rogue 的 9XM 系列 GPU。

A 系列的 alu 比 9XM Rogue GPU 多 4 倍。据说它的人工智能性能提高了 8 倍。最后，Imagination 表示，A 系列架构在性能相似的情况下，功耗降低了 60%。

新的 A 系列体系结构适用于 XT 系列中的四种配置和一种 XM 配置。XE 系列实际上并不是基于新的架构，因为它是 Rogue 的延续。AXT-64-2048 是一款旗舰 GPU，具有 2.0 TFLOPS，64 千兆像素/秒的填充速率，以及 8 项顶级的人工智能性能。另一方面，AXT-32-1024 据说是一款高级移动 GPU，具有 1 TFLOPS，32 千兆像素/秒的填充速率，以及 4 项顶级的人工智能性能。其他两种配置是 AXT-48-1536 和 AXT-16-512，而 AXM 系列有 AXM-8-256，其额定为 256 GFLOPS，8 千兆像素/秒的填充速率，以及 1 顶级的人工智能性能。

在移动 GPU 方面，Imagination 的计划是将 AXT-32-1024 作为高端移动 GPU 的最佳选择。例如，较大的两种配置可用于 Chromebooks 或服务器等设备。AXT-48-1536 仍然被 Imagination 设想为一种更大的高级移动 GPU，而 AXT-64-2048 是一种更大的 GPU，如果用户对它感兴趣，Imagination 可以创建它。

新的 GPU IP 包含了很多变化:4 倍多的 alu，128 宽的架构，等等。AnandTech 已经详细报道了新的 A 系列技术，因此读者应该查看该出版物的报道。

## 系列建筑——展望

想象力 A 系列建筑的前景看起来很棒。从表面上看，AXT-32-1024 GPU 甚至比高通在骁龙 865 的 Adreno GPU 甚至苹果的定制 GPU 都要快得多，更不用说 Mali-G77 了。当谈到 PPA 时，想象力也覆盖了它，该公司指出了现有的问题，即 Mali GPUs 与高通的 Adreno GPUs 具有相同的性能，但占用了 184%的硅面积，导致 PPA 较低。电源效率也应该很高。

Imagination 的 GPU 路线图也很激进。2020 年，A 系列架构将被 B 系列架构取代，性能提升 30%，而 C 和 D 系列将在 2021 年和 2022 年被取代，性能每年提升 30%。移动 GPU 市场已经在很大程度上放弃了这种级别的世代进步。Imagination 还计划在下一代 GPU 架构中启用光线跟踪。

就设计获胜而言，这是一个大杂烩。高通不会授权这种架构，世界上绝大多数的 Android 手机都使用高通的 SOC。三星已经与 AMD 签署了合作伙伴关系，在未来的 Exynos SoCs 中使用其镭龙知识产权。剩下的两个主要厂商是华为的海思集团和联发科，它们目前都使用 ARM 的 Mali GPUs。由于联发科之前使用了 PowerVR GPUs，因此该公司在未来的 SOC 中有可能从 ARM 回到 Imagination。该公司已经宣布了一款面向 2020 年设备的旗舰 SoC，即 Dimensity 1000。

Imagination 宣布推出新的 A 系列架构，这是移动 GPU 市场急需的。如果一切顺利，移动 GPU 市场现在在可由多家供应商使用的许可 GPU 方面竞争更加激烈。

* * *

**Via:** [AnandTech](https://www.anandtech.com/show/15156/imagination-announces-a-series-gpu-architecture)