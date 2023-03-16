# 联发科发布集成 5G 的 7 纳米 SoC Dimensity 1000

> 原文：<https://www.xda-developers.com/mediatek-dimensity-1000-7nm-soc-integrated-5g/>

5 月，ARM 宣布了下一代 [ARM Cortex-A77 CPU](https://www.xda-developers.com/arm-cortex-a77-cpu-announcement/) 架构和采用 Valhall 架构的 [ARM Mali-G77 GPU](https://www.xda-developers.com/arm-mali-g77-valhall-gpu-announcement/) 。仅仅几天后，联发科[宣布其首款 5G SoC](https://www.xda-developers.com/mediatek-7nm-5g-soc-helio-m70/) 震惊了芯片行业。SoC 集成了 Cortex-A77 CPU 和 Mali-G77 GPU。联发科透露，该芯片将采用 7 纳米工艺制造，但关于 SoC 的进一步细节仍不得而知。现在，在早期宣布近六个月后，联发科准备填补空白，包括 SoC 的名称。联发科天玑 1000 是 [5G Dimensity 系列](https://i.mediatek.com/mediatek-5g)中的第一款 SoC，它旨在将联发科带回旗舰 SoC 市场。

Dimensity 的名称旨在将联发科的 5G 芯片家族与 Helio 系列的 4G SoCs 区分开来。联发科表示，“Dimensity 代表着迈向移动新时代的一步——第五维度——以刺激行业创新，让消费者释放 5G 连接的可能性”。Dimensity 1000 SoC 代表着联发科重返高端 SoC 市场，它是该公司自 Helio X30 以来的第一款旗舰 SoC，Helio X30 在 2017 年未能在大多数旗舰手机中找到出路。

根据联发科的说法，第一款 Dimensity 驱动的设备将于 2020 年在 Q1 上市。

联发科天玑 1000 有一个八核(4+4) CPU。它有四个主频为 2.6GHz 的 ARM Cortex-A77“大”核心，四个主频为 2.0GHz 的 ARM Cortex-A55“小”核心。该 SoC 的核心配置很有趣，因为它是 4+4 配置，而三星和华为的海思分别在 [Exynos 990](https://www.xda-developers.com/samsung-exynos-990-5g-modem-5123-7nm/) 和[麒麟 990](https://www.xda-developers.com/huawei-hisilicon-kirin-990-5g-integrated-modem/) 中都有 2+2+4 配置。另一方面，高通骁龙 855 具有 1+3+4 CPU 核心配置。因此，联发科选择不使用任何中等核心，因为所有四个 A77 核心的主频都将达到 2.6 GHz。2.6 GHz 的主频正好符合 TSMC 7 纳米(N7)工艺的目标，再加上 A77 架构 20-35%的 IPC 改进，Dimensity 1000 的 CPU 性能应该与旗舰竞争对手相当，甚至更好。

联发科是第一家使用 ARM 的 Mali-G77 GPU 的供应商，该 GPU 也已经进入了即将发布的 Exynos 990。麒麟 990 有更老的 Mali-G76。联发科使用的是 9 核版本的 Mali-G77 (Mali-G77MC9)，而 Exynos 990 则有 11 核版本。GPU 的时钟速度目前未知。

该公司还在推广其第三代人工智能处理单元(APU/NPU)，用于设备上的人工智能操作，其性能是联发科之前的 APU 的两倍以上。它有两个大内核、三个小内核和一个“小”内核。联发科完全支持 NNAPI 功能，而其竞争对手却不完全支持，这有助于其在 AI 基准测试中的地位。

内存规格方面，联发科 SoC 支持 4 通道 LPDDR4X 内存，最大 16GB RAM。

Dimensity 1000 集成了 5G 调制解调器，这使其比骁龙 855 和 Exynos 990 更胜一筹。这使它与麒麟 990 5G 持平。联发科表示，集成 5G 调制解调器“与竞争解决方案相比，显著节省了电力”。

该芯片组支持 6GHz 以下的 5G，而不支持毫米波(mmWave) 5G。这并不像看起来那么重要，因为毫米波 5G 目前仅在美国成为现实。(日本和韩国也将在 2020 年拥有 mmWave 5G 网络。)Dimensity 1000 不适合这样的市场。世界上大多数市场都选择了中频段和低频段形式的 6GHz 以下 5G。联发科技特别指出，Dimensity 1000 是为在亚洲、北美和欧洲推出的全球 6GHz 以下网络而设计的。

它还支持 5G 双载波聚合(2CC CA)，据说具有“全球最快的吞吐量 SoC，在 6GHz 以下的网络上具有 4.7Gbps 的下行链路和 2.5Gbps 的上行链路速度”。(这种说法是不正确的，因为 Exynos 5G 调制解调器 5123 -与 Exynos 990 配对-在低于 6GHz 的网络上的下行链路速率高达 5.1Gbps。)据说它的速度是配有高通 X50 调制解调器的骁龙 855 的两倍。

该芯片支持独立(SA)和非独立(NSA)6 GHz 以下网络，并且包括对从 2G 到 5G 的每一代蜂窝连接的多模式支持。

Dimensity 1000 集成了最新的 Wi-Fi 6 (2x2 802.11ax)和蓝牙 5.1+标准，这使其能够在下行链路和上行链路速度方面提供超过 1Gbps 的吞吐量。该芯片还具有双频 GPS (L1+L5 波段)。关于这个特性为什么重要的更多信息，[阅读这篇文章](https://www.xda-developers.com/dual-frequency-gnss-important-location-feature-your-phone-probably-missing/)。

最后，这款 SoC 据说还拥有世界上第一个双 5G SIM 技术，此外还支持新无线电语音(VoNR)等服务。联发科表示，该芯片的集成 5G 调制解调器提供了“极高的能效”，“是一种比竞争解决方案更节能的设计”。这将让品牌将额外的空间用于更大的电池或更大的相机传感器等功能，这听起来不错。5G 载波聚合也让芯片发布更高的平均速度。它在用于高速连接的两个连接区域(高速层和覆盖层)之间执行无缝切换。

Dimensity 1000 拥有全球首款结合联发科 Imagiq+技术的五核图像信号处理器(ISP)。它支持 24fps 的 80MP 摄像头传感器，以及一系列多摄像头选项，如 32MP + 16MP 双摄像头。据称，该芯片的 APU 支持先进的人工智能相机增强功能，包括自动对焦、自动曝光、自动白平衡、降噪、HDR 和面部检测，以及另一项世界首创的多帧 HDR 视频功能。

至于显示器，它支持高达 120Hz 的全高清+ 1080p 面板和高达 90Hz 的 2K+ 1440p 面板。除了支持 H264、HEVC 和 VP9 之外，它还是第一款支持谷歌 AV1 格式高达 60 fps 4K 的移动 SoC。

上一次联发科在旗舰 SoC 领域的竞争，没有好下场。与高通的芯片相比，该公司的旗舰产品 Helio X10 和 Helio X20 SoCs 的性能和效率都较差。Helio X30 是为 2017 年的旗舰产品制造的，但它只找到了两款手机。随着[联发科在 2018 年](https://www.xda-developers.com/mediatek-helio-x-return-2018/)腾出高端空间，SoC 行业竞争减少。

现在，凭借 Dimensity 1000，联发科重新投入战斗。理论上，该芯片似乎拥有与现有竞争对手竞争的一切，如即将推出的高通骁龙 865、海思麒麟 990 5G 和 Exynos 990。设备采用是关键，但如果 Dimensity 系列起飞，竞争将恢复正常。根据联发科总裁陈乔恩的说法，联发科的 5G 技术与业内任何人都不相上下。我们很想知道这些说法在未来几个月是否会付诸实践。