# 联发科天玑 800 是一款面向中端智能手机的新型 5G 芯片

> 原文：<https://www.xda-developers.com/mediatek-dimensity-800-5g-chip-mid-range-phones/>

联发科是一家台湾芯片供应商，主要以生产中低端智能手机 SOC(片上系统)而闻名。过去，该公司也生产用于旗舰智能手机的高端 SOC。这在 2018 年发生了变化，由于高通在市场上的主导地位，[联发科腾出了高端 SoC 空间](https://www.xda-developers.com/mediatek-helio-x-return-2018/)。对于 2018 年和 2019 年，联发科选择专注于中端 Helio P 和 [Helio G](https://www.xda-developers.com/mediatek-helio-g90-series-hyperengine-game-technology-launched/) 系列。随着 2020 年的到来，[联发科](https://www.mediatek.com/)再次选择涉足 5G Dimensity 系列旗舰产品领域。该公司于 2019 年 11 月公布了高端手机的旗舰产品 [Dimensity 1000](https://www.xda-developers.com/mediatek-dimensity-1000-7nm-soc-integrated-5g/) SoC。12 月，OPPO 公布了尺寸为 1000L SoC 的 [OPPO Reno3](https://www.xda-developers.com/oppo-reno3-pro-5g-quad-rear-camera-china-launch/) ，虽然截至目前，尺寸 1000 和尺寸 1000L 的区别不得而知。现在，联发科通过宣布中端 Dimensity 800 5G SoC 扩展了 dimension ty 系列。该公司旨在为 2020 年的高端中端 5G 手机带来旗舰功能、功率和性能。

**连通性**

Dimensity 5G 系列的主要特点是它在单个芯片上提供集成的 5G 调制解调器，使其类似于[高通骁龙 765/765G](https://www.xda-developers.com/qualcomm-snapdragon-765-processor-specifications-features/) 和[海思麒麟 990 5G](https://www.xda-developers.com/huawei-hisilicon-kirin-990-5g-integrated-modem/) 。相比之下，[高通骁龙 865](https://www.xda-developers.com/qualcomm-snapdragon-865-benchmarks-cpu-gpu-performance-vs-kirin-990-snapdragon-855-snapdragon-845/) 和三星 [Exynos 990](https://www.xda-developers.com/samsung-exynos-990-5g-modem-5123-7nm/) 等 SoC 都有独立的 5G 调制解调器(这意味着有两个芯片——即 SoC +调制解调器)。拥有一个集成的 5G 调制解调器理论上应该可以提高能效。Dimensity 800 采用 TSMC 的 7 纳米工艺(N7)制造，首批采用该 SoC 的设备预计将于 2020 年上半年推出。

Dimensity 800 5G SoC 支持双载波聚合(2CC CA)5G，与使用单载波(1CC，无 CA)的其他解决方案相比，可实现 30%的更宽高速层覆盖、更无缝的 5G 切换和更高的平均吞吐量性能。它支持独立(SA)和非独立(NSA)的 6GHz 以下网络(目前所有 5G 网络都是 NSA，而首批 5G SA 网络预计将于今年晚些时候到达)。包括 2G/3G/4G 多模支持，还支持动态频谱共享(DSS)。Dimensity 800 系列支持新无线语音(VoNR)等服务。据联发科称，该芯片的集成 5G 调制解调器提供了“极高的能效”，据称是比市场上其他解决方案更节能的设计。调制解调器下行和上行速度的细节尚未披露。

**CPU**

联发科天玑 800 有四个主频高达 2GHz 的大 [ARM Cortex-A76](https://www.xda-developers.com/arm-cortex-a76-cpu-mali-g76-gpu-mali-v76-vpu-announcement/) 内核，与四个主频高达 2GHz 的小 ARM Cortex-A55 内核配对。与高通骁龙 765/765G 等 SOC 相比，联发科特别推广该芯片包含更多性能核心，因为拥有更多性能核心可以缩短应用和游戏启动时间，并提高多线程性能。Dimensity 800 是第一款将四款旗舰级高性能内核架构引入主流市场的 SoC。它没有使用更新的旗舰 [ARM Cortex-A77](https://www.xda-developers.com/arm-cortex-a77-cpu-announcement/) 内核，这有点令人失望。联发科可能决定使用旧的 Cortex-A76 来区分不同的产品，高通的骁龙 765 系列也没有跳到 Cortex-A77。

Dimensity 800 拥有 2133MHz 的双通道(2x16b) LPDDR4X RAM，这意味着它的内存带宽只有其兄弟 Dimensity 1000 的一半。

**GPU**

在 GPU 性能方面，Dimensity 800 使用的是 Mali-G57MC4，这是 10 月份发布的 [Mali-G57](https://www.xda-developers.com/arm-mali-g57-gpu-launch-valhall-architecture/) 的四核变体。它的时钟速度尚未透露。这与联发科的超引擎游戏技术相结合，提供了“不折不扣”的游戏体验，理论上，这种特殊的 GPU 实现应该可以与骁龙 765G 的 Adreno 620 GPU 相竞争。

**艾**

联发科的 APU 3.0(人工智能处理单元)在其设计中有四个核心，由三种不同的核心类型组成，这使得 Dimensity 800 能够提供高达 2.4 倍的人工智能性能。APU 硬件设计据说对 FP16 来说更有效和更强大，以实现最精确的人工智能相机结果。

**ISP**

ISP 也有很多话要说。该公司宣称它是一款“旗舰级”图像信号处理器，因为它支持多达四个并行摄像头。Dimensity 800 支持高达 64MP 的摄像头，这意味着其 ISP 可以处理 64MP 图像，或大型多摄像头选项，如 32MP + 16MP 双摄像头，由硬件深度引擎支持。人工智能相机的增强据说也是旗舰级的。Dimensity 800 系列包括人工智能自动对焦、自动曝光、自动白平衡、降噪、高动态范围(人工智能 HDR)和专用面部检测硬件。据说它拥有世界上第一个多帧 4K 视频 HDR 功能(HDR 视频)。

**显示**

最后，Dimensity 800 系列支持刷新率高达 90Hz 的全高清+显示器。虽然这为中端市场带来了旗舰级的功能，但骁龙 765 在这方面甚至更好，因为它支持 120Hz 的刷新率显示器。

**可用性**

联发科指出，Dimensity 800 系列是为全球 6GHz 以下的 5G 网络设计的，这些网络将在亚洲、北美和欧洲部署到 2020 年。理论上，SoC 似乎是高通骁龙 765/765G 的强大竞争对手，因为它可能有更好的 CPU 性能和有竞争力的 GPU 实现。为了竞争，我们希望在 2020 年看到中端手机采用 Dimensity 800 系列作为高通 SOC 的替代产品。