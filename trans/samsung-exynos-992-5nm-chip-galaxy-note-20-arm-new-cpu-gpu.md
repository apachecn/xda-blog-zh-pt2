# 三星的 Exynos 992 可能是 Galaxy Note 20 的 5 纳米芯片，采用 ARM 的新 CPU 和 GPU 设计

> 原文：<https://www.xda-developers.com/samsung-exynos-992-5nm-chip-galaxy-note-20-arm-new-cpu-gpu/>

本周，ARM 宣布了新的 [ARM Cortex-A78 CPU 以及 ARM Mali-G78 GPU](https://www.xda-developers.com/arm-announces-cortex-a78-cpu-mali-g78-gpu-ethos-n78-npu/) ，作为其 TechDay 2020 的一部分。两者分别继承了去年的 [Cortex-A77](https://www.xda-developers.com/arm-cortex-a77-cpu-announcement/) CPU 和 [Mali-G77](https://www.xda-developers.com/arm-mali-g77-valhall-gpu-announcement/) GPU。通配符公告是 Cortex-X 定制程序(CXC)，其中 ARM 宣布在 CXC 下制造的第一个 CPU 将是 Cortex-X1，这是 ARM 迄今为止最强大的 CPU。Cortex-X1 将专门以峰值性能为目标，而不是能效和 PPA(性能、功率和面积)，这将使其与苹果领先的 A 系列芯片正面竞争。在宣布的时候，我写道三星是采用 ARM 新的移动 CPU IP 的有力候选人。Exynos 990 中的 Exynos M5 定制核心是三星在可预见的未来的最后一个完全定制的核心，因为该公司在 SARC 的定制 CPU 核心项目已经结束(要了解更多有关该项目失败的原因，[请阅读本文](https://www.xda-developers.com/samsung-galaxy-s20-plus-review/))。因此，三星别无选择，只能从其下一代旗舰 SoC 开始使用 ARM 的 CPU IP。现在，ZDNet Korea*的一份报告称，三星即将发布的 Exynos 992 将是 Galaxy Note 20 的 5 纳米芯片，采用 ARM Cortex-A78 和 Mali-G78，但*不是*Cortex-X1。*

一个月前，由于 ZDNet Korea 的另一篇报道，我们第一次听说了 Exynos 992。当时，该出版物曾表示，新的 SoC 旨在用于 Galaxy Note 20 系列，并将采用三星的 6 纳米工艺制造，比其尖端的 5 纳米工艺低一个档次。另一方面，Exynos 990 是由 EUV 三星代工的 7 纳米 LPP 工艺制造的。现在，该出版物声称，Exynos 992 毕竟将采用 5 纳米工艺制造。

报告指出，三星继续与 TSMC 争夺下一代尖端代工工艺的优势。在过去的几年里，三星代工工厂已经失去了两个 TSMC 的大客户。从 2016 年苹果公司完全迁移到 TSMC 开始，它失去了苹果公司的客户。然后在 2019 年，它错过了高通的骁龙 855 合同，因为 TSMC 的 7 纳米工艺优于自己的 8 纳米工艺。今年，三星的 7 纳米 EUV 工艺本应成为建造骁龙 865 的候选工艺，但出于目前尚不完全清楚的原因，高通选择将技术较差的 7 纳米 N7P (DUV)工艺的合同授予 TSMC。因此，三星一直在与 TSMC 打一场必败之战，正因为如此，它抓紧时间从 7 纳米 EUV 转移到下一代 5 纳米工艺，而 6 纳米工艺将低于它。

据 *ZDNet Korea* 报道，半导体行业消息人士 5 月 27 日称，三星电子最近完成了基于 5nm 工艺的下一代 Exynos SoC(暂定名为 Exynos 992)的量产。SoC 将于 8 月发布，这与 Galaxy Note 20 系列的发布时间一致。

报道援引一位未透露姓名的半导体行业官员的话说，8 月下半月推出基于 5 纳米工艺的新应用处理器(Exynos 992)的所有准备工作已经完成。现在，它应该只是决定它是否会被用于 Galaxy Note 20 的问题。

据称，与之前的 Exynos 990 相比，Exynos 992 的功效和 GPU 性能有了显著提高，因为它采用了 ARM 的最新 IP (Cortex-A78 和 Mali-G78)。没有提到 Cortex-X1，ARM 表示它将作为下一代旗舰 SOC 的一部分，采用 1+3+4 配置(1 个 Cortex-X1+3 个 Cortex-A78+4 个 Cortex-A55)。关于电源效率和 GPU 性能显著提高的说法是合理的，因为 Exynos 990 在效率方面非常差。与骁龙 865 的 Cortex-A77 内核相比，其 Exynos M5 定制内核的效率为 100%，因此迁移到更新的 Cortex-A78(与上一代 Cortex-A77 相比，其能效提高了 20%，性能提高了 20%)应该可以节省大量能源。Mali-G78 也比其前身快 25%，更节能，但鉴于这些数字，它仍无法在每瓦性能方面与高通的 Adreno 650 GPU 相媲美。ARM 注意到 Cortex-A78 将在 5 纳米上量产-5 纳米工艺使 A78 的性能比 A77 提高了 13%，而剩余的 7%是由于更好的整数单线程 CPU 性能而实现的。

*ZDNet Korea* 注意到三星在国内的韩国 Galaxy S20 变种中没有使用 Exynos 990，而是选择使用骁龙 865。当时，这是一个令人惊讶的决定，被许多人解读为表明三星本身对 Exynos 990 的性能和功率缺乏信心。不过现在，三星系统 LSI 希望通过在 Galaxy Note 20 系列的韩国国内版本中使用 Exynos 992 来扩大其市场份额。然而，骁龙 865 仍将在一些海外市场使用，可能指的是美国/中国/香港/拉丁美洲/日本版本的手机。因此，Exynos 992 将成为首款采用尖端 5 纳米工艺制造的主要移动 SoC，从而证明三星代工的竞争力。

2020 年，三星电子在 Q1 的系统半导体业务收入为 36.4 亿美元。尽管 Galaxy S20 的韩国型号排除了 Exynos 990，转而支持骁龙 865，但还是出现了这种情况。Exynos 覆盖范围的减少通过向小米提供高分辨率图像传感器( [108MP ISOCELL Bright HMX](https://www.xda-developers.com/samsung-isocell-bright-hmx-108mp-camera-sensor-xiaomi/) )来弥补，从而增加了销量。现在，证券行业预计，在 Galaxy Note 20 发布的今年第三季度，三星系统 LSI 将录得超过 37.7 亿美元的销售额。根据 Counterpoint Research 的数据，三星电子去年在全球应用处理器(AP)市场以 14.1%的份额排名第三，低于市场领导者高通

33.4%的份额和排名第二的联发科。

据我们所知，ZDNet 韩国的报道似乎是可靠的。因此，Galaxy Note 20 系列的 Exynos 变体预计将比 Exynos Galaxy S20 变体更快、更节能。希望三星最终能够克服对骁龙的性能赤字，并以积极的方式区分自己的 SoC。如果这一点最终得以实现，智能手机市场的竞争性质将最终回到正轨。

* * *

**来源:** [ZDNet Korea](https://www.zdnet.co.kr/view/?no=20200527134911)