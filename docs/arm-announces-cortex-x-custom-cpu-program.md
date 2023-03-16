# ARM 的 Cortex-X 定制 CPU 计划可能最终会使 Android 旗舰性能与苹果竞争

> 原文：<https://www.xda-developers.com/arm-announces-cortex-x-custom-cpu-program/>

每年 5 月，总部位于英国、隶属于日本软银(Softbank)的 ARM 都会宣布其用于移动设备的新移动 IP(知识产权)。该 IP 由新的 CPU 内核和新的 GPU 组成。ARM 的指令集用于世界上每一部智能手机——这是一家至关重要的公司。在 CPU 核心架构方面，从 2021 年开始，note 的每个主要移动芯片厂商都将使用 ARM 的库存 CPU IP(正如三星系统 LSI [在其 Exynos M 定制核心上已经放弃了](https://www.xda-developers.com/samsung-galaxy-s20-plus-review/))。这就是为什么，ARM 把事情做好是加倍重要的。今年，ARM 已经宣布了 ARM Cortex-A78 CPU 架构和 Mali-G78 GPU，分别是 [Cortex-A77](https://www.xda-developers.com/arm-cortex-a77-cpu-announcement/) CPU 和 [Mali-G77](https://www.xda-developers.com/arm-mali-g77-valhall-gpu-announcement/) GPU 的继任者。虽然这些发布是意料之中的，但没想到的是 ARM 以 Cortex-X 的形式发布了另一款 CPU 内核。多年来，技术评论者和用户一直哀叹苹果的 CPU 架构比 ARM 的 Cortex-A 系列领先多年。随着 Cortex-X CPU 计划和 Cortex-X1 的推出，这种情况可能会在 2021 年最终改变。

ARM 知道，客户在不同的产品领域，基于不同的需求，要求更多的解决方案和产品。例如， [Cortex-A76](https://www.xda-developers.com/arm-cortex-a76-cpu-mali-g76-gpu-mali-v76-vpu-announcement/) 用于旗舰 SOC 以及一些较低的中档 SOC。它的最高性能没有苹果的竞争对手高，因为 ARM 需要首先关注 PPA(性能、功率和面积)。对该公司来说，能效和电力效率比绝对性能更重要。

#### 有了 Cortex-X1，这一切都变了。

ARM 宣布了 Cortex-X 定制(CXC)计划。该计划需要与 ARM 工程团队和 ARM 的计划合作伙伴密切合作，他们可以塑造最终的 CPU 产品来满足特定的市场需求。ARM 指出，这允许项目合作伙伴在“通常的皮层——PPA 的信封”之外定义自己的绩效点。由 ARM 设计和制造的最终定制 CPU 将以 ARM Cortex-X 品牌交付。作为 CXC 计划一部分的第一个 CPU 是 ARM Cortex-X1 CPU。

ARM 对 Cortex-X1 非常自豪，称它是迄今为止最强大的 Cortex CPU。与当前的 Cortex-A77 相比，它带来了 30%的峰值性能提升。据说它将为下一代定制解决方案带来“终极性能”。CPU 是为了响应合作伙伴的需求，他们希望根据自己的使用情况最大限度地提高性能。

正如预期的那样，Cortex-X1 也比新发布的 Cortex-A78 更快，后者位于它的下方。这里措辞很重要。ARM 表示，与 Cortex-A78 相比，它提供了高达 22%的单线程整数性能提升。ARM 表示,“提升”是指这种改善与高性能的短期爆发有关，这对于反应性和响应性来说是最好的。据称，这将为智能手机和大屏幕设备带来有史以来最高的性能，但鉴于这些数字，Cortex-X1 仍无法与即将推出的苹果 A14 相匹敌。不过，它可能会与 2019 年的苹果 A13 不相上下。

Cortex-X1 的机器学习(ML)性能是 A77 的两倍。这是一个显著的改进，它是 ARM 更广泛推动本地计算性能的一部分。

与 4x Cortex-A77 和 4x Cortex-A55 集群相比，具有 4x Cortex-A78 和 4x Cortex-A55 内核的 DynamIQ 集群提供了 20%的持续性能提升。有关 20%索赔的更多信息，请查看我们的文章。(是的，ARM 没有宣布 Cortex-A55 的继任者，很遗憾。明年可能会来。)另一方面，Cortex-X1 在提升峰值性能的同时实现了更高的可扩展性。合作伙伴将 1 个 Cortex-X1 作为 DynamIQ 集群的一部分，同时添加 3 个 Cortex-A8 和 4 个 Cortex-A55，其峰值性能将比上一代产品提高 30%，这是一个值得注意的壮举。A78 专为效率而生，因此当与 Cortex-X1 结合使用时，该组合将提供最佳的持续和峰值性能。旗舰 Android 手机将会变得更快。

ARM 表示，Cortex-X1 解决方案的主要市场是智能手机和新的外形(可折叠手机和大的多屏设备)。X1 提供了更快的 UX、更快的应用程序加载时间和改进的网页滚动响应能力。AI 和基于 ML 的体验会随着 ML 性能的提升而变得更好。可以预见，X1 还将改善工作效率、通信、安全性、多重数字沉浸、基于相机、高级游戏和 XR 体验等用例。

## ARM Cortex-X1 - CPU 架构

Cortex-X1 的架构是有趣的地方。它有许多微体系结构升级，提供了峰值性能提升。2018 年发布的 Cortex-A76 将 Cortex-A75 的指令解码宽度从 3 宽度升级到 4 宽度，而 Cortex-A75 的指令解码宽度又从 Cortex-A73 的 2 宽度增加了。然而，Cortex-A77 选择将解码宽度保持在 4-wide。苹果的 A 系列芯片又大又宽，因为自 A11 以来所有 A 系列芯片的解码宽度都是 7-wide，甚至比桌面 CPU 架构还要宽。ARM 通过 Cortex-X1 向苹果迈进了一步，解码带宽增加了 25%，每周期解码 5 条指令。

此外，ARM 表示，MOP 缓存吞吐量增加了 33%，达到每周期 8 个 MOP。Cortex-X1 的 Neon 引擎增加了两个管道，其计算能力是 A78 的两倍。在缓存大小方面，X1 支持 64kB L1 和高达 1MB 的 L2 缓存，而 DynamIQ 集群已经升级到现在支持 8MB 的三级缓存，以实现终极性能。与 Cortex-X1 结合使用时，A78 也可以使用较大的 L3。

Cortex-X1 是 CXC 项目下生产的第一个 Cortex-CPU。CXC 计划最需要的是将性能提升到 PPA 皮层之外的极限。这是因为所有提高的性能都是有代价的。Cortex-X1 的尺寸是 Cortex-A78 的 1.5 倍。这意味着它的 PPA 更差，能效也更低。因此，它不太可能出现在任何中档或经济型手机中，因为它可能仅限于高端旗舰手机。允许合作伙伴拥有符合其市场需求的 CPU 将使 Cortex-A CPU 的发展蓝图与众不同。这里需要注意的是，在 CXC 计划下，计划合作伙伴不能直接定制任何 CPU。相反，CXC 计划本质上是“为 Cortex 打造”许可证的继承者，ARM 根据合作伙伴的请求进行修改，并设计出售给合作伙伴的 CPU IP。ARM 表示，通过这种方式，它将满足不断扩大的生态系统的需求。

Cortex-X1 的目标时钟速度是 3GHz。自 A76 以来，ARM 一直以 3GHz 为目标，时钟速度明显未能实现。然而，随着 5 纳米 SOC 的即将到来，ARM 希望供应商最终能够以 3GHz 的速度发布 ARM 的大核心设计。ARM 指出，所有性能评估都基于 SPECint2006，这是一个行业标准基准。

## 观点

Cortex-X1 的发布对于渴望在 2021 年购买旗舰 Android 手机的人来说是令人兴奋的。自 2013 年和苹果 A7 以来，ARM 将首次能够在峰值性能方面接近苹果的 A 系列芯片。即使 Cortex-X1 与 A14 不匹配，它也会比过去七年更接近。

即将推出的高通骁龙 875 可能会将 Cortex-X1 和 Cortex-A78 作为其“主要核心”和“性能核心”的一部分。海思[不可能采用 ARM 的最新 IP，因为 TSMC 被禁止向其提供芯片，所以华为手机今年不会采用新的 CPU 核心，甚至可能不会在明年年初。值得注意的是，三星在采用 Cortex-X1 + Cortex-A78 作为下一代旗舰 Exynos SoC 的一部分方面处于有利地位，该 SoC 将接替](https://www.xda-developers.com/huawei-honor-high-end-mediatek-chipsets-new-phones-new-u-s-trade-restrictions/) [Exynos 990](https://www.xda-developers.com/samsung-exynos-990-5g-modem-5123-7nm/) 。三星发布了一份声明，称看到 ARM 在 Cortex-X 定制程序方面的新方向，它感到“非常兴奋”。Cortex-X1 基本上否定了三星失败的定制核心业务。希望明年，Exynos 驱动的 Galaxy S21/S30 手机在与骁龙驱动的竞争中最终不会出现或大或小的 CPU 性能缺陷。最后，联发科是否会采用 Cortex-X1 还不确定。[dimension 1000](https://www.xda-developers.com/mediatek-dimensity-1000-plus-new-5g-chip-144hz-display/)的继任者可能只会采用 A78，或者它可能会采用 X1 加 A78 组合，以便与高通正面竞争。我们必须等着看明年事情如何发展。

尽管一家主要的 CPU 芯片生产商[站在关闭的边缘](https://www.xda-developers.com/huawei-honor-high-end-mediatek-chipsets-new-phones-new-u-s-trade-restrictions/)，Android 的 CPU 性能的未来看起来还是一片光明。

* * *

**来源:ARM ( [1](https://community.arm.com/developer/ip-products/processors/b/processors-ip-blog/posts/arm-cortex-x-custom-program) 、 [2](https://www.arm.com/company/news/2020/05/new-arm-ip-delivers-true-digital-immersion-for-the-5g-era) )、 [AnandTech](https://www.anandtech.com/show/15813/arm-cortex-a78-cortex-x1-cpu-ip-diverging)**