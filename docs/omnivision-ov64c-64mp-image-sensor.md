# OmniVision OV64C 是 OmniVision 的首款 6400 万像素图像传感器

> 原文：<https://www.xda-developers.com/omnivision-ov64c-64mp-image-sensor/>

正如我们之前解释的那样，智能手机摄像头百万像素大战[已经全面恢复](https://www.xda-developers.com/samsung-galaxy-s20-ultra-108mp-nona-binning-camera/)。2019 年，大多数主流的中低端、中高端和平价旗舰手机都选择使用某种形式的 [48MP 四拜耳传感器](https://www.xda-developers.com/sonys-imx586-48mp-smartphone-camera/)。2020 年，64MP 似乎将成为智能手机相机的新标准分辨率。三星和索尼分别以[三星 ISOCELL GW1](https://www.xda-developers.com/samsung-64mp-isocell-sensor-smartphones/) 和索尼 IMX686 的形式发布了他们的 6400 万像素传感器。三星甚至更进一步，发布了两个 108MP 传感器，分别是 [ISOCELL HMX](https://www.xda-developers.com/xiaomi-mi-note-10-first-impressions-108mp-of-greatness/) 和 ISOCELL HM1[，后者用于](https://www.xda-developers.com/samsung-galaxy-s20-ultra-108mp-nona-binning-camera/)三星 Galaxy S20 Ultra。当这两家公司为争夺优势而争斗时，第三家竞争者正悄悄地在市场上推出自己的产品。竞争者是 OmniVision，到目前为止，它还没有取得成功。不过，它的目标是继续尝试，现在它已经以 OV64C 的形式宣布了自己的 64MP 图像传感器。

近年来，OmniVision 的图像传感器已被用作双摄像头、三摄像头和四摄像头手机的辅助摄像头。然而，在主图像传感器方面，我们必须一直追溯到[小米 Mi A1](https://www.xda-developers.com/xiaomi-mi-a1-xda-android-review/) 和 OnePlus 2，才能找到使用 OmniVision 的图像传感器作为主摄像头的智能手机。OmniVision 在 CES 上推出了 [48MP OV48C 图像传感器](https://www.xda-developers.com/omnivision-ov48c-new-48mp-image-sensor/)，其规格理论上优于目前市场上的 64MP 传感器，因为它通过保持分辨率不变来实现更高的像素尺寸。随着 OV64C 的发布，OmniVision 回到了公平竞争的舞台上，因为该传感器的规格与其竞争对手相似。这意味着，与 OV48C 不同，它与 IMX686 等产品相比没有任何重大的根本优势。这是因为相机的一个主要限制是像素大小，OV48C 的 1.2 微米像素大小和 2.4 微米“有效像素大小”对于高百万像素智能手机相机来说是无与伦比的，而 OV64C 的 0.8 微米像素大小和 1.6 微米“有效像素大小”与其竞争对手不相上下。

OV48C 是一个 1/1.7 英寸的传感器，与 ISOCELL GW1 和 IMX686 一样大。它具有相应的 0.8 微米像素尺寸。它使用 OmniVision 的 PureCel Plus 堆叠芯片技术，为高端手机提供“领先的静态图像捕捉”和“卓越的 4K 视频性能”，以及电子图像稳定(EIS)。该传感器还提供多种功能，如用于全分辨率 Bayer 输出的 4 单元 remosaic 和数字作物缩放，以及使用更少引脚实现更大吞吐量的 CPHY 接口。这使得它适用于多摄像头配置中的主后置摄像头。

OmniVision 指出，根据 TSR(一家市场研究公司)的数据，2020 年将有 1.27 亿个 64MP 或更高分辨率的图像传感器运往智能手机制造商。这证实了市场现实，即由于华为在其旗舰手机中成功实施了 4000 万像素摄像头，高像素传感器被视为必不可少的。即使三星、谷歌和苹果等公司的旗舰手机仍然拥有 1200 万像素的主摄像头，效果也很好。它将 OV64C 作为一种定位良好的传感器进行推广，以满足“高端智能手机设计师的需求增长”

OV64C 集成片内 4 单元彩色滤波器阵列和硬件再镶嵌，可实时提供高质量 64MP Bayer 输出。(这使得它看起来好像是一个 Quad Bayer 传感器，因为所有 Quad Bayer 传感器都有一个 QCFA，但“64MP Bayer 输出”术语的含义不清楚。)在弱光下，该传感器可以使用“近像素宁滨”输出 1600 万像素的图像，灵敏度为 4 倍，因为它为预览和静态捕捉提供了 1.6 微米的等效性能。无论是哪种情况，OmniVision 都向我们保证，该传感器可以始终捕捉最佳质量的图像。它还具有 16MP 分辨率的 2 倍数字作物变焦和快速模式切换。

有趣的是，该传感器具有 type-2，2x2 微透镜相位检测自动对焦(微透镜-PDAF)功能，以提高自动对焦精度，特别是在弱光下。(这个解决方案类似于[索尼的 2x2 自动对焦镜头解决方案](https://www.sony-semicon.co.jp/e/products/IS/mobile/2_2_ocl.html)，这被证实是 [OPPO Find X2 相机](https://www.xda-developers.com/oppo-find-x2-sony-image-sensor-snapdragon-865/)的一个特点。)输出格式包括 64MP、15fps(表示缺少零快门延迟)、16MP、4 单元宁滨、30fps、4K 视频、30fps 的 4K 视频。(这清楚地表明，60fps 的 4K 视频不支持 EIS，不幸的是，这是整个 Android 智能手机行业的常见疏忽。)此外，OV64C 支持最高 16Mp 视频模式的 3 次曝光、交错 HDR 时序。

OmniVision 表示，OV64C 图像传感器的样品现已上市。在 2020 年的智能手机发布会上，主要智能手机供应商是否会选择这种传感器，而不是 IMX686 和 ISOCELL GW1，还有待观察。

* * *

**来源:[OmniVision](https://www.ovt.com/news-events/product-releases/omnivision-announces-its-first-64-megapixel-08-micron-image-sensor)**