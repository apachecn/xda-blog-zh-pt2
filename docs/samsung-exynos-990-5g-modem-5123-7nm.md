# 三星宣布推出 7 纳米 Exynos 990 SoC 和 5G Exynos 调制解调器 5123

> 原文：<https://www.xda-developers.com/samsung-exynos-990-5g-modem-5123-7nm/>

在 2019 年三星技术日上，三星宣布了片上系统，几乎肯定会为明年 Galaxy S11 手机的国际版本提供动力:Exynos 990。该公司还宣布了一款新的尖端分立 5G Exynos 调制解调器 5123，旨在与 Exynos 990 配对。

### Exynos 990

Exynos 990 是三星第一款采用该公司新 SoC 命名系统的旗舰 SoC。它接替了 [Exynos 9820](https://www.xda-developers.com/samsung-galaxy-s10e-review-exynos/) 和 [Exynos 9825](https://www.xda-developers.com/samsung-exynos-9825-announced-galaxy-note-10-launch/) ，旨在定位于上个月宣布的中端 [Exynos 980](https://www.xda-developers.com/samsung-exynos-980-5g-modem/) SoC 之上。这确实有点令人困惑——尤其是考虑到三星的主要竞争对手华为也有一款名为[海思麒麟 990](https://www.xda-developers.com/huawei-hisilicon-kirin-990-5g-integrated-modem/) 的旗舰 SoC。

Exynos 990 和 5G Exynos 调制解调器 5123 都是采用三星新的 7 纳米 LPP EUV(极紫外)工艺制造的。Exynos 990 具有三集群 CPU 核心设置，类似于 Exynos 9820 和 Exynos 9825。这两个大内核是三星定制内核的下一代产品——exy nos M5，它接替了 9820 和 9830 中的 Exynos M4。三星声称 Exynos M5 比其前代产品性能提高了 20%。这似乎是一个保守的目标，尤其是考虑到高通的下一代旗舰 SoC 几乎肯定会使用性能提升 20-35%的 [ARM Cortex-A77](https://www.xda-developers.com/arm-cortex-a77-cpu-announcement/) 架构。就真实世界的性能而言， [Exynos M3](https://www.xda-developers.com/samsung-unveils-exynos-9810-3rd-generation-custom-cpu-cores-mali-g72mp18-gpu/) 令人大失所望，而 M4 则是一大进步，尽管它并不是在所有方面都与 Cortex-A76 相匹配。

另一方面，中间的两个内核是 [ARM Cortex-A76](https://www.xda-developers.com/arm-cortex-a76-cpu-mali-g76-gpu-mali-v76-vpu-announcement/) 内核。它们继承了 Exynos 9820/9825 中的 Cortex-A75 中间核心集群。这应该会在使用中间核心集群的现实世界任务中提供可观的性能提升，这应该有助于三星缩小 Exynos 9820/9825 与高通骁龙 855 以及麒麟 980 之间的性能差距。最后，小内核集群依赖于四个 ARM Cortex-A55 内核。三集群 CPU 设置的整体改善据说是 13%，但三星尚未提供任何集群的时钟速度。

在 GPU 方面，三星在 Exynos 990 中融入了 Mali-G77MP11。 [Mali-G77](https://www.xda-developers.com/arm-mali-g77-valhall-gpu-announcement/) 是第一款使用新的 Valhall GPU 架构的 ARM GPU，据说其性能比其前身提高了 1.4 倍。尽管采用了新的架构，**三星只是承诺将图形性能*或*功效提高 20%** 。理论上，这很令人失望，因为这意味着三星不会在苹果 A12 和 A13 中赶上苹果的 GPU，而且该公司也不太可能在高通 2020 年的旗舰 SoC 中与下一个 Adreno GPU 竞争。

在设备上的 AI 方面，Exynos 990 具有双核 NPU(神经处理单元)和改进的 DSP(数字信号处理器)。**它们的组合每秒可以执行超过 10 万亿次运算(TOPs)**，与 Exynos 9820 每秒 1.86 次 TOPs 相比，这是一个很大的进步。NPU 支持智能手机中的本地化人工智能，允许数据在设备上处理，而不是发送到云。三星提到了面部识别和场景检测的典型用例，它们将受益于这一改进。

Exynos 990 还支持新的 **LPDDR5 标准**，带宽速率高达 5500 Mbps。该 SoC 具有一个 **120Hz 刷新率显示驱动器**，旨在减少屏幕撕裂，甚至在具有多个显示器的设备上实现更流畅的动画，如可折叠手机。最后，ISP 支持多达六个单独的图像传感器，同时处理三个。支持的最大分辨率为 108MP，值得注意的是，三星开发了 [ISOCELL Bright HMX 108MP 传感器](https://www.xda-developers.com/samsung-isocell-bright-hmx-108mp-camera-sensor-xiaomi/)，目前只在 Mi Mix Alpha 中看到。

### 5G Exynos 调制解调器 5123

值得注意的是，Exynos 990 没有集成 5G 调制解调器。相反，三星正在营销 5G Exynos 调制解调器 5123 分立调制解调器，它将与 Exynos 990 一起使用。这是基于 7 纳米 EUV 工艺生产的首批 5G 调制解调器之一。

它带来的进步是显而易见的:**它支持两种类型的 5G** ，即 sub-6GHz(将在全球范围内更广泛使用)和 mmWave 频谱(目前仅限于美国和日本)。除了 5G，它还支持传统的 2G/3G/4G LTE 技术，具有同类最佳的理论速度。在 4G LTE 中，在 422 Mbps 上传的情况下，可以达到的最大理论下行速度是 3Gbps(不会被任何消费者看到)。在 5G sub-6GHz 中，它可以达到最大 5.1Gbps 的下行链路，而 mmWave 允许它达到 7.35Gbps。它具有 1024 QAM，它最大支持 8 载波聚合(8CA)。这使得它成为第一个拥有如此先进功能集的调制解调器。

* * *

据三星称，Exynos 990 和 5G Exynos 调制解调器 5123 预计将于今年年底开始大规模生产。三星 Galaxy S11 的国际版本将使用这种芯片。随着海思芯片[已经宣布了他们的旗舰 SoC](https://www.xda-developers.com/huawei-hisilicon-kirin-990-5g-integrated-modem/) ，所有的目光都将集中在高通的下一代骁龙旗舰 SoC 上。

**来源 1:三星 [(1)](https://shop-links.co/link/?exclusive=1&publisher_slug=xda&article_name=Samsung+announces+the+7nm+Exynos+990+SoC+and+the+5G+Exynos+Modem+5123&article_url=https%3A%2F%2Fwww.xda-developers.com%2Fsamsung-exynos-990-5g-modem-5123-7nm%2F&u1=UUxdaUeUpU26313&url=https%3A%2F%2Fwww.samsung.com%2Fsemiconductor%2Fminisite%2Fexynos%2Fproducts%2Fmobileprocessor%2Fexynos-990%2F) ，** **[(2)](https://news.samsung.com/global/new-premium-mobile-processor-and-5g-modem-unveiled-at-samsung-tech-day)**

**故事 Via:[Anand tech](https://www.anandtech.com/show/15021/samsung-announces-exynos-990-7nm-euv-m5-g77-lpddr5-and-5g-modem-flagship-soc)**