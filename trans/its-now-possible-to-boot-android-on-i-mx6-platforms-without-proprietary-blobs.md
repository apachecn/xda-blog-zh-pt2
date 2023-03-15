# 现在可以在没有专有 Blobs 的 i.MX6 平台上启动 Android 了

> 原文：<https://www.xda-developers.com/its-now-possible-to-boot-android-on-i-mx6-platforms-without-proprietary-blobs/>

为了让 Android 在大多数硬件平台上启动，开发人员通常不得不将开源代码与专有文件混合在一起。这些所谓的 blobs 由供应商分发，以支持某些特定于平台的功能。来自 *Collabora* [的 Robert Foss 报道](https://www.collabora.com/news-and-blog/blog/2017/06/05/android-nxp-imx6-buffer-modifier-support/)现在可以在 i.MX6 平台上完全不使用专有 blobs 来引导 Android。

Mesa 和 gbm_gralloc 中都增加了对缓冲区修饰符的支持。Mesa 为许多缓冲区分配函数和 GBM(GBM _ gralloc 使用的 Mesa 提供的 API)增加了支持。另一方面，gbm_gralloc 又增加了对使用新的 GBM API 调用 GBM_BO_IMPORT_FD_MODIFIER 的支持，它导入一个缓冲区对象以及附带的信息，如所讨论的缓冲区对象使用的修饰符。

恩智浦的 i.MX6 是众多嵌入式 SOC 之一，不再需要专有 blobs 来启动 Android。这使得 i.MX6 作为开发平台更有吸引力，也为将来支持 i.MX8 平台打下了基础。

当修改器就位时，它们用于表示缓冲区的不同属性。这些属性可以涵盖一系列关于缓冲区的不同信息，例如，压缩和[平铺](https://github.com/laanwj/etna_viv/blob/master/doc/hardware.md#texture-tiling)。

对于它配备的 iMX6 和 Vivante GPU 来说，修改器与平铺相关。原因是缓冲区可以以不同的方式平铺(平铺、超级平铺等。)或者根本没有(线性)。在将缓冲区发送到显示器之前，它们需要提供相关的平铺信息，以便实际发送的图像不会被平铺。

为了更好地理解这一切是如何工作的，请看看下面的视频，看看 ZII RDU2 板(i.MX 6QuadPlus)使用 Mesa 开源图形堆栈启动 Android。

虽然这对开源软件来说是一个巨大的胜利，但我们不应该期望许多原始设备制造商开始在他们的设备中使用这种 SoC。该平台的一个主要缺点是它的年龄。该平台于 2011 年首次亮相。

* * *

[**来源:Robert Foss at Planet Collabora**](https://www.collabora.com/news-and-blog/blog/2017/06/05/android-nxp-imx6-buffer-modifier-support/)[**Via:Softpedia**](http://news.softpedia.com/news/it-s-now-possible-to-boot-android-on-i-mx6-platforms-without-proprietary-blobs-516364.shtml)