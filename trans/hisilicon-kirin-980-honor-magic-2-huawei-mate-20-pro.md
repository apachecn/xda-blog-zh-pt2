# 麒麟 980 将为 Honor Magic 2、华为 Mate 20 和 Mate 20 Pro 提供动力

> 原文：<https://www.xda-developers.com/hisilicon-kirin-980-honor-magic-2-huawei-mate-20-pro/>

尽管中国科技巨头华为出席了今年的柏林 IFA，但它并没有发布新的旗舰智能手机。相反，他们宣布了海思麒麟 980 片上系统——他们的最新芯片组将为未来的华为和 Honor Magic 2、华为 Mate 20 和华为 Mate 20 Pro 等旗舰智能手机提供动力。华为的麒麟 980 在很多方面都是第一:它是第一个基于 TSMC 7 纳米工艺制造的商用芯片组，第一个嵌入 ARM 的 Cortex-A76 CPU 内核，第一个采用双 npu，第一个支持 Cat。21 LTE。让我们来分解这款新芯片组的各个方面，以便更好地理解海思的最新产品。

* * *

## 海思麒麟 980 制造工艺

海思麒麟 980 据说是首款商用 7nm SoC。这意味着它将是第一款基于 TSMC 7 纳米制造工艺的商用芯片组。据华为称，麒麟 980 在 1 平方英寸的空间内集成了 69 亿个晶体管。厘米芯片尺寸—与麒麟 970 上使用的 10 纳米制造工艺相比，增加了 1.6 倍。华为表示，新的 7 纳米工艺使 SoC 性能提高了 20%，能效提高了 40%。

据报道，TSMC[也在使用 7 纳米制造工艺制造](https://www.xda-developers.com/report-tsmc-qualcomms-chip-orders-2018/)下一代旗舰[高通骁龙芯片组](https://www.xda-developers.com/qualcomm-snapdragon-855-sdx50-5g-modem/)。虽然高通[已经证实](https://www.xda-developers.com/qualcomm-samples-flagship-chipset/)他们正在对即将推出的 7 纳米骁龙芯片组进行采样，但该公司尚未确认该芯片组将被称为[骁龙 855 还是骁龙 8150](https://www.xda-developers.com/qualcomm-snapdragon-855-dedicated-npu/) 。无论如何，看看下一代高通骁龙芯片组与海思麒麟 980 的比较会很有趣。麒麟 980 将首先出现在 Honor Magic 2 或华为 Mate 20/Mate 20 Pro 上，而我们没有任何信息表明哪款设备将率先采用高通的下一代芯片组。(在一篇现已被删除的帖子中，[联想副总裁承诺](https://www.xda-developers.com/lenovo-vp-promises-worlds-first-5g-smartphone/)将推出全球首款搭载“骁龙 855”的 5G 智能手机，尽管鉴于[联想 Z5](https://www.xda-developers.com/lenovo-z5-official-display-notch/) 的遭遇，我们不得不半信半疑地看待该公司的玩笑。)

* * *

## hisilin Kirin 980 CPU/GPU/ISP

### 中央处理器

麒麟 980 将采用以下配置的总共 8 个 CPU 核心:2 个 ARM Cortex-A76 高性能核心(2.6GHz)，2 个 ARM Cortex-A76 高效核心(1.92GHz)，4 个 Cortex-A55 超高效核心(1.8GHz)。华为表示，与 Cortex-A75 内核相比，Cortex-A76 内核的性能提高了 75%，能效提高了 58%。华为还推出了一种具有“弹性调度”技术的 CPU 子系统，以分配“正确的核心到正确的任务”。

麒麟 980 是首款采用 ARM Cortex-A76 内核的 SoC。我们在 5 月份探索了 ARM 的新 CPU 内核，但总的来说，Cortex-A76 为移动设备带来了“笔记本电脑级的性能”。像 Cortex-A75 内核一样，Cortex-A76 使用 ARM 的 [DynamIQ 技术](https://www.xda-developers.com/arms-dynamiq-focuses-on-performance-efficiency-redundancy-scalability-and-latency/)。Cortex-A76 的每时钟整数指令数增加了 25%，带宽提高了 90%，浮点性能提高了 35%，机器学习应用的计算性能提高了 4 倍。

### 国家政治保卫局。参见 OGPU

在性能方面，较早的麒麟 SOC 中包含的 Mali GPUs 一直落后于高通的 Adreno GPUs，但随着 ARM 的 Bifrost GPU 架构的推出，这种情况近年来有所改变。Mali-G71，华为 Mate 9 的海思麒麟 960，[中的](https://www.xda-developers.com/huawei-mate-9kirin-960-early-testing-comparison-with-pixel-xlsnapdragon-821/) [GPU 在我们的早期测试](https://www.xda-developers.com/analyzing-soc-market-relative-standing-chipset-processor/)中表现充分。然而，Mali-G71 表现出较差的能效，而其继任者 [Mali-G72](https://www.xda-developers.com/arm-unveils-cortex-a75-a55-processors-and-mali-g72-gpu/) 仍然无法与高端 Adreno 的持续性能和能效进行正面竞争。然而， [Mali-G76](https://www.xda-developers.com/arm-cortex-a76-cpu-mali-g76-gpu-mali-v76-vpu-announcement/) 承诺比上一代产品的功效高 30%,性能密度高 30%,机器学习应用性能提高 2.7 倍。

华为声称，集成到麒麟 980 中的 Mali-G76MP10 (10 核，720MHz)提供了 46%的图形处理能力和 178%的功率效率。该公司还声称，游戏性能总体上比竞争对手高出 22%，我们假设这是指高通骁龙 845 SoC 中的 [Adreno 630](https://www.xda-developers.com/qualcomm-snapdragon-845-adreno-630-gpu/) 。然而，尚不清楚华为的 GPU Turbo 技术将如何影响这些数字。华为显然一直在推动游戏性能成为最近的一个主要卖点，所以我们必须看看第一批麒麟 980 设备在我们的测试中表现如何。我们当然希望 Honor Magic 2 和华为 Mate 20/Mate 20 Pro 在我们的[堡垒之夜移动测试](https://www.xda-developers.com/fortnite-mobile-android-testing-performance/)中比 Honor 10 做得更好。

### 网络服务提供商

关于麒麟 980 中的新图像信号处理器(ISP ),我们得到的信息很少。我们被告知与上一代产品相比有望实现以下改进:与竞争对手相比，相机处理速度提高 46%，录制能效提高 23%，延迟提高 33%，对比度和白平衡更好。

* * *

## 希西林 980 双 NPU

海思麒麟 970 是第一款配备专用神经处理单元(NPU)的芯片组。尽管由于(在我们看来)激进的市场营销，人工智能已经成为一个时髦的词汇，但当涉及到摄影时，还是有一些实际的好处。如今，许多智能手机的相机中都有某种形式的智能场景检测——这只是 npu 应用的一个例子。谷歌在 Firebase 中的 [ML Kit API 为机器学习增强的功能开辟了更多可能性，由于麒麟 970 中的专用 NPU，如果应用程序使用 ML Kit 的设备上 API，它们可以提供更好的性能。](https://www.xda-developers.com/google-ml-kit-machine-learning/)

海思麒麟 980 凭借双 NPU 更进一步。麒麟 980 可以识别“每分钟多达 4，500 张图像”，与麒麟 970 中的 NPU 性能相比，提高了 120%。麒麟 980 支持常见的 ML 框架，如 Caffe、TensorFlow 和 [TensorFlow Lite](https://www.xda-developers.com/tensorflow-lite-mobile-machine-learning/) 。我们不确定哪些 EMUI 功能将利用麒麟 980 的双 NPU，但一旦 Honor Magic 2 或华为 Mate 20/Mate 20 Pro 智能手机公布，我们将了解更多信息。我们被告知，物体识别现在支持视频，实时[物体分割](https://www.xda-developers.com/honor-10-multi-scene-detection-filters-camera/)更加精确。公司喜欢吹嘘他们的人工智能功能，但除了人脸过滤器或[微软的离线翻译](https://www.xda-developers.com/microsoft-translator-ai-powered-offline-language-packs/)等小众应用之外，双 NPU 提供的改进对普通消费者来说几乎没有什么影响。

* * *

## 海思麒麟 980 调制解调器

麒麟 980 是第一款带有支持 Cat 的调制解调器的芯片组。21 LTE。这意味着它支持 1.4Gbps 的峰值理论下载速度。这在理论上听起来不错，但在现实中，[你不会接近那些峰值速度](https://www.xda-developers.com/opensignal-february-state-lte-report-2018/)。例如，OnePlus 6 支持[猫。16 LTE 支持千兆下载速度](https://www.xda-developers.com/oneplus-6-cat-16-lte-gigabit-speed/)，但你很难找到一个可以实现这种速度的区域。然而，这并不意味着麒麟 980 调制解调器的改进没有好处，因为其他网络改进，如 4x4 MIMO、256-QAM 和 3CC 载波聚合仍将改善网络连接。我们距离世界上大多数运营商升级其基础设施以支持[新 5G 标准](https://www.xda-developers.com/5g-specification-standard-3gpp/)还有数年时间，因此我们今天看到的改进是我们未来将看到的垫脚石。

我们了解的其他细节包括 Hi1103 调制解调器允许 1，732 Mbps 的 Wi-Fi 速度，芯片组具有双频 GPS (L1 和 L5 波段)用于精确定位。

* * *

## 麒麟 980 -在华为 Mate 20 上可用

Honor 前几天在舞台上宣布 Honor Magic 2 将采用海思麒麟 980，抢了华为的风头。我们不知道 Honor Magic 2 将于何时推出，但麒麟 980 将在 10 月份推出的华为 Mate 20 中出现。我们之前已经[泄露了华为 Mate 20 的规格](https://www.xda-developers.com/huawei-mate-20-specifications-features-rumor/)以及[的第一张渲染图](https://www.xda-developers.com/huawei-mate-20-notch-render-specifications/)，所以我们对即将发布的华为旗舰将采用最新的海思芯片组一点也不惊讶。有趣的是，华为 Mate 20 和 Mate 20 Pro 很可能是第一批采用麒麟 980 的智能手机，这意味着我们可以预计 Honor Magic 2 将在 Mate 20 系列之后的某个时候推出。

*华为 Mate 20 水滴槽口渲染图。要了解更多，请查看我们独家的 Mate 20 设计的[泄露。](https://www.xda-developers.com/huawei-mate-20-notch-render-specifications/)*