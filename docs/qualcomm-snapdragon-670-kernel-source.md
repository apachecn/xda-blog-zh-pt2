# 高通骁龙 670 内核源码显示 2+6 CPU 核心，Adreno 615 GPU

> 原文：<https://www.xda-developers.com/qualcomm-snapdragon-670-kernel-source/>

我们第一次听说高通骁龙 670 是在八月份。这是该公司的下一代中端片上系统，是骁龙 660 的继任者。

随后的报道显示，它将采用 10 纳米工艺制造，并采用 Adreno 6xx 家族的 [GPU。现在， *WinFuture* 公布了关于骁龙 670 的更多细节，也被称为 SDM670。该芯片的许多规格在 12 月泄露，但内核来源证实它将是一个更便宜、降级的](https://www.xda-developers.com/arms-dynamiq-focuses-on-performance-efficiency-redundancy-scalability-and-latency/)[骁龙 845 的表亲。](https://www.xda-developers.com/qualcomm-2018-snapdragon-tech-summit-roundup/)

与骁龙 660 不同，骁龙 670 不会有四个高端和四个低端核心。配置小。相反，高通已经转向双核高端 CPU 集群和六核低端 CPU 集群。低端内核是高通的 ARM Cortex-A55 的改编版本，“Kryo 300 Silver”。另一方面，性能核心是 ARM Cortex-A75 的定制版本，“Kryo 300 Gold”。

CPU 内核有一个 32KB 的 L1 缓存。每个集群有一个 128KB 的 L2 缓存，外加一个 1024KB 的三级缓存用于整个 SoC。

骁龙 670 的低端效率核心的时钟频率最高为 1.7GHz (1708MHz)，而高端性能核心的时钟频率将能够达到 2.6 GHz(2611 MHz)——对于中端 SoC 来说，这是一个相对较高的时钟速度。(相比之下，骁龙 845 的 [Kryo 385](https://www.xda-developers.com/qualcomm-snapdragon-835-kryo-385-cpu-cores/) 性能内核的主频为 2.8GHz。)

骁龙 670 的 GPU 据说是高通 Adreno 615，它的标准时钟速度为 430MHz - 650MHz，动态斜坡高达 700MHz。

骁龙 670 将支持 UFS 2.1 和 eMMC 5.1 闪存。该芯片与高通的骁龙 X2x 调制解调器配对，理论上能够提供 1Gbps 的下行速度。

得益于专业的图像处理器，骁龙 670 的 Adreno GPU 支持双摄像头配置中的高分辨率摄像头。高通尚未透露支持的最大分辨率，但 *WinFuture* 指出，该公司的参考设计硬件有 13MP + 23MP 传感器。说到显示器，该芯片支持高达 WQHD (2560x1440)的分辨率，尽管具体数字尚未透露。

新 SoC 的发布时间表目前还不清楚，但高通可能会选择在 2 月底的世界移动通信大会上发布骁龙 670。无论如何，我们可以预计在未来几个月内，至少会有几款配备新 SoC 的智能手机上市。

* * *

[**来源:WinFuture(德语)**](http://winfuture.de/news,101858.html)