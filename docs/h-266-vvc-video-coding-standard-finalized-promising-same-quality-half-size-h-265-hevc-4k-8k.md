# H.266/VVC 视频编码标准已经最终确定，有望以 H.265/HEVC 一半的尺寸获得相同的质量

> 原文：<https://www.xda-developers.com/h-266-vvc-video-coding-standard-finalized-promising-same-quality-half-size-h-265-hevc-4k-8k/>

视频流占互联网总流量的很大一部分，有人估计占互联网总流量的 80%。随着越来越多的视频消费设备、大众化的视频制作以及显示器分辨率的不断提高，预计这一贡献在未来几年仍将占很大比例。视频编码标准因此成为一个重要的平衡工具，确保视频流不会阻塞我们的互联网基础设施，也不会对用户体验产生不利影响。现在，[弗劳恩霍夫 HHI 公司宣布了一种新的视频编码标准，称为 H.266/VVC(通用视频编码)](https://newsletter.fraunhofer.de/-viewonline2/17386/465/11/14SHcBTt/V44RELLZBp/1)，它接替了 H.265/HEVC(高效视频编码)。

弗劳恩霍夫电信研究所，也称为弗劳恩霍夫 HHI，是开发视频编码压缩标准的组织。他们的最新公告是关于一个新的视频编码标准。这种视频编码标准被称为 H.266/VVC(通用视频编码)，据称具有相同的感知质量，但视频大小是其前身 H.265/HEVC 的一半。这意味着视频下载和视频流可以以更低的带宽提供更高质量的视频，从而降低消费者的数据使用量，同时也有利于提供商。例如，以 H.265/HEVC 编码的 90 分钟 4K/UHD 视频可能需要 10 GB 的数据来传输，而以 H.266/VVC 编码的 90 分钟 UHD 视频可能需要大约 5 GB 的数据来传输。就带宽减少的百分比而言，这是一个很大的节省，而且当你考虑到视频流的巨大规模时，它还会放大。

但这种扩大规模的过程中会遇到一些挑战。如果设备制造商想要增加 H.266/VVC 编码器或解码器，他们将不得不支付许可费，因为新的编码标准使用了多项专利技术。弗劳恩霍夫 HHI 承诺“基于公平、合理和非歧视原则的统一和透明的许可模式”。然而，如何许可这项技术仍将取决于专利持有者。成本可能高达数亿美元。这种高成本带来了明显的问题，即最终产品/服务的成本膨胀，使公司更难实现收支平衡。对于像 Mozilla Firefox 这样的项目，由于意识形态、经济和实际的原因，这根本不在考虑范围之内。

专利和成本难题是视频编码社区中许多利益相关者更喜欢免版税编解码器的原因。XDA 撰稿人 Steven Zimmerman 早在 2017 年就写了一篇关于 AV1 的优秀文章，AV1 是谷歌对 HEVC 的免费回答，也是视频编解码器的未来，他的分析和预测今天仍然有效。我们继续看到 [AV1](https://www.xda-developers.com/tag/av1/) 在流媒体平台如 [YouTube](https://www.xda-developers.com/youtube-for-android-tv-adopts-av1-video-codec-in-certain-devices/) 、[网飞](https://www.xda-developers.com/netflix-android-streams-some-shows-av1/)、 [Vimeo](https://www.xda-developers.com/vimeo-supports-av1-video-codec/) 、[脸书](https://www.xda-developers.com/facebook-aomedia-royalty-free-av1-video/)以及[联发科](https://www.xda-developers.com/mediatek-dimensity-1000-is-the-first-smartphone-soc-to-support-av1-hardware-decoding/)等 SoC 制造商中的采用率上升。H.266/VVC 与 AV1 等免版税编解码器相比表现如何还有待观察。

至少在 2021 年之前，我们不太可能在移动设备上看到 H/266/VVC 支持。目前没有移动 SoC 支持这种新视频编码格式的硬件加速解码或编码。一旦 SOC 开始支持 H.266/VVC 中的硬件加速视频编码，4K 和 8K 视频记录的文件大小将显著下降。同样，H.266/VVC 视频解码的硬件加速将减少数据使用，前提是视频流平台开始以这种新格式编码视频。弗劳恩霍夫·HHI 说“*使用 H.266/VVC 所需的新芯片，如移动设备中的芯片，目前正在设计中*”，因此我们最早可以在明年看到 SOC 支持它。

* * *

**来源:[弗劳恩霍夫电子报](https://newsletter.fraunhofer.de/-viewonline2/17386/465/11/14SHcBTt/V44RELLZBp/1)**

**参考 X.266/VVC 编码器:[弗劳恩霍夫 VC git](https://vcgit.hhi.fraunhofer.de/jvet/VVCSoftware_VTM/-/releases)**