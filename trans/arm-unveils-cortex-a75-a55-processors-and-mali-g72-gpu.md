# ARM 推出 Cortex-A75、A55 处理器和 Mali-G72 GPU

> 原文：<https://www.xda-developers.com/arm-unveils-cortex-a75-a55-processors-and-mali-g72-gpu/>

ARM 正式宣布了三款新产品，它们肯定会进入下一代移动设备。该公司在将于 5 月 30 日至 6 月 3 日在台北举行的 COMPUTEX 活动之前展示了其新产品。

ARM 的产品组合现已扩展为高性能的 **Cortex-A75** 微架构和高能效的 **Cortex-A55** 。除了这两款产品，ARM 还展示了其高端 **Mali-G72** GPU。Cortex-A75 和 A55 是 ARM 的首款 DynamiQ CPUs。

ARM 新推出的最强大的 CPU Cortex-A75 是今年我们开始在手机中看到的 Cortex-A73 的继任者。后者正好在一年前发布，也是在 COMPUTEX 展会期间。ARM 的这款最新产品支持 ARMv8-A 架构，旨在在各种设备上实施，包括智能手机和平板电脑。像往常一样，生产商专注于带来更高的性能和最大限度地降低能耗。ARM 认为 Cortex-A75 在大多数指标上都优于 Cortex-A73，包括高达 20%的整数核心性能。CPU 还为高级和专门的工作负载提供额外的性能，如**机器学习**。

ARM 也推出了新的内存子系统。在新功能中，ARM 提到了对共享集群 L3 缓存的访问，对异步频率的支持，以及每个 CPU 或内核组的潜在独立电压和电源轨。Cortex-A75 CPU 还在每个内核上使用了一个专用的 L2 缓存，延迟是 A73 的一半。这些变化直接转化为更好的性能，尽管这些具体的好处不会在所有地方都出现，但在高级用例中，A75 芯片比其前身快 48%。

 <picture>![](img/cc4c2ab16e74dc0fae8c2b639398a057.png)</picture> 

Note that the scale of ARM's graphs is misleading, pay attention to the multipliers and not the length.

ARM 最新的高端 CPU 也可以用在大屏幕的设备上。这家英国公司一年半前开设了一个专门的大屏幕计算部门，并希望在英特尔称王的细分市场上解决问题。ARM 在 A75 上做了一个重大的架构改变，为使用该内核的芯片打开了一个更大的功耗信封，现在功耗已扩展到 2W。结果，根据 ARM 的说法，笔记本电脑将获得 30%的额外性能。

下面你可以看到最新的 ARM 的领跑者的完整技术规格。

| **通用** | 体系结构 | ARMv8-A(哈佛) |
| 扩展ˌ扩张 | ARMv8.1 扩展 ARMv8.2 扩展加密扩展 RAS 扩展 ARMv8.3(仅适用于 LDAPR 指令) |
| ISA 支持 | A64、A32 和 T32 指令集 |
| **微架构** | 管道 | 无序的 |
| 超标量 | 是 |
| 氖/浮点单元 | 包括 |
| 密码单元 | 可选择的 |
| 集群中的最大 CPU 数量 | 四(4) |
| 物理寻址 | 44 位 |
|  |  |  |
| **存储系统和外部接口** | L1 指令缓存/指令缓存 | 64KB |
| L2 高速缓存 | 256KB 至 512KB |
| L3 缓存 | 可选，512KB 至 4MB |
| ECC 支持 | 是 |
| LPAE | 是 |
| 总线接口 | ACE 还是 CHI |
| 酰基-载体蛋白质(Acyl Carrier Protein) | 可选择的 |
| 外围端口 | 可选择的 |
|  |  |  |
| **其他** | 功能安全支持 | ASIL·D |
| 安全性 | 信任地带 |
| 中断 | GIC 接口，GIVv4 |
| 通用定时器 | ARMv8-A |
| 电源管理单元 | PMUv3 |
| 调试 | ARMv8-A(加上 ARMv8.2-A 扩展) |
| CoreSight | CoreSightv3 |
| 嵌入式跟踪宏单元 | ETMv4.2(指令跟踪) |

Cortex-A75 和 A55 是第一个 [**DynamIQ big。小小的**来自 ARM 的](https://www.xda-developers.com/arms-dynamiq-focuses-on-performance-efficiency-redundancy-scalability-and-latency/)CPU。DynamIQ 还为供应商提供了新的灵活组合。标准的半+半多集群组合可以替换为 1+7 或 2+6 -本质上，SoC 供应商可以决定他们是否希望在单个集群中使用更多的大 CPU 或小 CPU。新处理器经过重新设计，配备了全新的基本 DynamIQ 共享单元(DSU ),负责电源管理、ACP 和外设端口接口。它们还首次为 ARM 的移动处理器配备了 L3 缓存。值得一提的是，A55 和 A75 都是基于该公司最新的 ARMv8.2-A 架构构建的。这使得它们与包括 A73 和 A53 在内的任何其他处理器都不兼容。

较小的 Cortex-A55 是 Cortex-A53 的长期替代品。后者在过去三年中已经在 17 亿台设备上销售，你可能已经遇到过它，因为它已经出现在廉价设备和旗舰产品中。在可预见的未来，新的 A55 将被放置在大多数智能手机中。Cortex-A55 是 ARM 设计的所有中端 CPU 中能效最高的。事实上，它比 Cortex-A53 节省 15%的能源。最后，ARM 声称最新的小内核是最强大的中端设备。它还具有最新的架构扩展，引入了用于机器学习的新 NEON 指令、高级安全功能以及对可靠性、可访问性和可维护性(RAS)的更多支持。

Cortex-A55 的完整规格如下。

| **通用** | 体系结构 | ARMv8-A(哈佛) |
| 扩展ˌ扩张 | ARMv8.1 扩展 ARMv8.2 扩展加密扩展 RAS 扩展 ARMv8.3(仅适用于 LDAPR 指令) |
| ISA 支持 | A64、A32 和 T32 指令集 |
| **微架构** | 管道 | 按顺序 |
| 超标量 | 是 |
| 氖/浮点单元 | 可选择的 |
| 密码单元 | 可选择的 |
| 集群中的最大 CPU 数量 | 八(8) |
| 物理寻址 | 40 位 |
|  |  |  |
| **存储系统和外部接口** | L1 指令缓存/指令缓存 | 16KB 至 64KB |
| L2 高速缓存 | 可选，64KB 至 256KB |
| L3 缓存 | 可选，512KB 至 4MB |
| ECC 支持 | 是 |
| LPAE | 是 |
| 总线接口 | ACE 还是 CHI |
| 酰基-载体蛋白质(Acyl Carrier Protein) | 可选择的 |
| 外围端口 | 可选择的 |
|  |  |  |
| **其他** | 功能安全支持 | 直到 ASIL D |
| 安全性 | 信任地带 |
| 中断 | GIC 接口，GIVv4 |
| 通用定时器 | ARMv8-A |
| 电源管理单元 | PMUv3 |
| 调试 | ARMv8-A(加上 ARMv8.2-A 扩展) |
| CoreSight | CoreSightv3 |
| 嵌入式跟踪宏单元 | ETMv4.2(指令跟踪) |

再来看 GPU，ARM 也准备了一款新产品。Mali-G72 是 G71 的继任者，由于其出色的可扩展性，它也以多种配置出现在 2017 年 SOC 中。然而，新的 GPU 提供了 20%的更高性能密度，这意味着制造商可以在相同的芯片面积上使用更多的 GPU 核心。据估计，智能手机最多将使用 32 个着色器核心。此外，新的 GPU 将使用 25%的能源，而且它在机器学习效率方面也有所提高- ARM 声称它在 ML 基准测试中比 G71 高出 17%。

SoC 供应商应该开始在其新一代产品中实施 ARM 的新产品组合。我们最迟应该在明年年初，可能在巴塞罗那世界移动通信大会期间，看到使用 ARM 硬件的设备。

* * *

[**来源:ARM【1】**](https://developer.arm.com/products/processors/cortex-a/cortex-a55)[**来源:ARM【2】**](https://developer.arm.com/products/processors/cortex-a/cortex-a75)