# 三星发布 Exynos 9810:第三代内核，Mali-G72MP18 GPU

> 原文：<https://www.xda-developers.com/samsung-unveils-exynos-9810-3rd-generation-custom-cpu-cores-mali-g72mp18-gpu/>

11 月，三星开玩笑宣布 Exynos 9810，[入选 CES 2018 创新奖](https://www.xda-developers.com/samsung-announces-exynos-9810-soc-isocell-sensor/)。当时，关于新的片上系统的细节还很少。几天前，三星通过 Twitter 确认将于 1 月 4 日正式推出下一代 Exynos SoC，现在，它公布了其最新芯片的细节。

* * *

**背景**:自从 [Galaxy S](http://xda-developers.com/tag/galaxy-s) 之后，三星就在其旗舰手机中使用 Exynos SoCs。值得注意的是，Galaxy S 采用了单核 Exynos 3110 SoC，其次是双核 Exynos 4210 和四核 Exynos 4412，分别用于 [Galaxy S II](http://xda-developers.com/tag/galaxy-s-ii) 和 [Galaxy S III](http://xda-developers.com/tag/galaxy-s-iii) 。不过，2013 年，三星采用了不同的策略。它采用了手臂的大。Exynos 5410 的技术很少，它有四个 ARM Cortex-A15 性能内核和四个 ARM Cortex-A7 效率内核。

Exynos 5410 被降级为 3G 版的[银河 S4](http://xda-developers.com/tag/galaxy-s4) ，这意味着它在西方被高通的骁龙 600 芯片取代。因为那时是大人物的早期。很少，Exynos 5410 遇到了一些问题，包括高速缓存一致性互连(CCI)无法正常工作，以及由于使用集群迁移(而不是异构多处理)而无法同时使用所有八个内核。它很快被 Exynos 5420 取代，但多亏了 HMP，Exynos 5422 在 [Galaxy S5](http://xda-developers.com/tag/galaxy-s5) 中的发布才能够同时使用所有八个内核。

此后，Exynos 芯片组稳步成熟。2015 年是值得注意的一年，三星跳过了 Snapdragon 810，转而在包括美国在内的所有市场使用八核 exy nos 7420(4 个 Cortex-A57 内核和 4 个 Cortex-A53 内核)。Exynos 7420 也是第一款采用 14 纳米 FinFET 工艺制造的移动 SoC，使其在 Android 世界中拥有竞争优势。

2016 年，三星凭借 Exynos 8890 转向定制核心。该 SoC 有四个高性能 Exynos M1 定制内核，结合四个 Cortex-A53 效率内核，与 Mali-T880MP12 GPU 配对。Exynos M1 定制内核的性能与 ARM 的 Cortex-A72 大致相当。

三星在去年的 [Exynos 8895](https://www.xda-developers.com/samsung-launches-the-exynos-9-series-8895-octa-core-processor-on-10nm-finfet-process-technology/) 中继续使用定制核心。Exynos 8895 拥有第二代 Exynos M2 内核和 Cortex-A53 内核，以及更宽的 Mali-G71MP20 GPU。Exynos M2 的单核性能与 ARM Cortex-A73 和高通的半定制 Kryo 280(基于 A73)大致处于同一水平。

* * *

**Exynos 9810:** 周四，三星发布了 Exynos 9810，这是其 Exynos 9 系列的第二款芯片。Exynos 9810 基于三星第二代 10 纳米 FinFET 工艺(10 纳米低功耗 Plus)构建，拥有第三代定制 CPU 内核。

准确地说，Exynos 9810 有四个主频高达 2.9GHz 的高性能定制核心，四个主频为 1.9GHz 的 ARM Cortex-A55 核心。它还使用了 [ARM 的 DynamIQ tech](https://www.xda-developers.com/arms-dynamiq-focuses-on-performance-efficiency-redundancy-scalability-and-latency/) ，这是去年宣布的对 big.LITTLE 的改进。

简单来说，这里的 CPU 升级是一个重大的。三星表示，该芯片的架构具有更宽的流水线和改进的高速缓存，这使其单核性能**比前代产品**提高了两倍。据该公司称，**多核性能比其前身提高了约 40%**。据说 SoC 还可以实现“无缝多任务处理”，加快应用程序之间的加载和转换时间。

单核性能提升两倍的说法很有趣，因为这是三星 SoC 各代产品中最大的性能飞跃之一。如果它在实践中发挥作用，Exynos 9810 可能会领先于竞争对手([并进一步缩小苹果和安卓设备之间的性能差距](https://www.xda-developers.com/a-widening-gap-the-a10-fusion-puts-a-chokehold-on-qualcomms-prospects/))，但在没有基准数据的情况下，现阶段很难确定任何事情。

转到 GPU，Exynos 9810 拥有 Mali-G72MP18 GPU，但其时钟速度没有透露。值得注意的是，与 Exynos 8895 的 Mali-G71MP20 相比，GPU 核心数量有所减少，但总体性能应该仍然更快。ARM 的 Heimdall Mali-G72 也在麒麟 970 SoC 上使用，尽管该芯片组选择了 12 核配置。虽然我们不知道三星实施的时钟速度，但我们通常会看到该公司的 Mali GPU 结果一直优于麒麟芯片组，麒麟芯片组传统上具有更低的内核数量(尽管每内核频率更高)。

三星最新的 SoC 也有新的调制解调器。Exynos 8895 采用了世界上第一个千兆位 LTE 调制解调器，Exynos 9810 具有业界首款 1.2Gbps 千兆位 LTE 调制解调器，具有 LTE Cat 18 1.2Gbps 下行链路和 LTE Cat 18 200Mbps 上行链路。它支持高达 6 倍的载波聚合(6CA)，据说可以以更快的速度实现更稳定的数据传输。它支持 4x4 MIMO(多输入多输出)和 256-QAM 方案，还使用增强型许可辅助接入(eLAA)。据三星称，新技术使广播或流媒体视频更容易达到 UHD 分辨率，甚至 360 度视频。

Exynos 9810 具有专用的图像处理和升级的多格式编解码器(MFC)。据说它具有更快、更节能的图像和视觉处理能力，能够以高达 UHD 的分辨率实现照片和视频的高级稳定。它还允许以更高的分辨率进行实时失焦摄影，并在低光下拍摄更亮的照片，减少噪音和运动模糊。它支持高达 24MP 的后置和 24MP 的前置摄像头，以及双 16MP+16MP 摄像头。

升级后的 MFC 可以录制和播放高达 120FPS 的 UHD 分辨率的视频(尽管我们不太可能在即将发布的 Galaxy S9 中看到这一功能，因为与骁龙 845 的能力存在差距)。它还支持 HEVC 和 VP9 编解码器，这使得 MFC 能够为每种原色(红色、绿色和蓝色)渲染 1024 种不同的色调。这意味着可以渲染 10.7 亿种颜色，是之前 8 位颜色格式的 1670 万种颜色的 64 倍。

最后，Exynos 9810 据说可以增强基于神经网络的深度学习。据三星称，它引入了复杂的功能，使处理器能够“准确识别照片中的人或物品，以进行快速图像搜索或分类，或者通过深度传感，以 3D 方式扫描用户的面部，以进行混合面部检测”。当使用面部解锁时，混合面部检测使用硬件和软件来实现逼真的面部跟踪过滤器和更强的安全性。SoC 还有一个独立的安全处理单元来保护重要的个人数据，如面部、虹膜和指纹信息。

三星电子系统大规模集成电路营销副总裁 Ben Hur 表示:“Exynos 9 系列 9810 是我们迄今为止最具创新性的移动处理器，具有第三代定制 CPU、超高速千兆位 LTE 调制解调器和深度学习增强的图像处理功能。“对于即将到来的人工智能时代，Exynos 9810 将成为智能平台创新的关键催化剂，如智能手机、个人计算和汽车。”

三星表示，Exynos 9 系列 9810 目前正在量产。它将在 1 月 9 日至 12 日在拉斯维加斯举行的 2018 年消费电子展上展出，预计它的 SoC 将在下个月宣布的 [Galaxy S9](http://xda-developers.com/tag/galaxy-s9) 和 Galaxy S9+的国际版本中推出。

* * *

[**来源 1:三星(新闻稿)**](https://news.samsung.com/global/samsung-optimizes-premium-exynos-9-series-9810-for-ai-applications-and-richer-multimedia-content) [**来源 2:三星**](https://shop-links.co/link/?exclusive=1&publisher_slug=xda&article_name=Samsung+Unveils+the+Exynos+9810%3A+3rd+Generation+Custom+CPU+Cores+and+Mali-G72MP18+GPU&article_url=https%3A%2F%2Fwww.xda-developers.com%2Fsamsung-unveils-exynos-9810-3rd-generation-custom-cpu-cores-mali-g72mp18-gpu%2F&u1=UUxdaUeUpU19782&url=http%3A%2F%2Fwww.samsung.com%2Fsemiconductor%2Fminisite%2Fexynos%2Fproducts%2Fmobileprocessor%2Fexynos-9-series-9810%2F)