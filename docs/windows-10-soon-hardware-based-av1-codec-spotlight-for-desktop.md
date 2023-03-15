# Windows 10 将很快获得基于硬件的 AV1 编解码器，Spotlight for Desktop

> 原文：<https://www.xda-developers.com/windows-10-soon-hardware-based-av1-codec-spotlight-for-desktop/>

微软官方[宣布](https://techcommunity.microsoft.com/t5/media-at-microsoft/av1-hardware-accelerated-video-on-windows-10/ba-p/1765451)它终于在今年晚些时候将硬件加速的 AV1 视频编解码器引入 Windows 10。与现有的 H.265 编解码器相比， [AV1 编解码器](https://www.xda-developers.com/av1-future-video-codecs-google-hevc/)提供了更好的压缩，同时，它旨在减少在线视频流的数据使用量。该编解码器由开放媒体联盟(AOM)宣布，该联盟由微软、谷歌、Mozilla、思科、英特尔、网飞和亚马逊成立。AV1 或 AOMedia 视频编解码器 1.0 是一个免版税的规范，可以跨平台交付。与其他编解码器相比，它有可能以平均高出 30%的压缩率传送 4K·UHD 视频。

微软去年在微软商店发布了 AV1 视频扩展。这有助于用户在 Windows 10 上播放使用 AV1 视频编码标准编码的视频。通过启用 AV1 的硬件支持，所有解码工作负载将从软件转移到硬件，这将降低功耗并延长移动设备的电池寿命。

硬件加速的 AV1 视频支持将于今年秋季在配备最新 GPU 的新 Windows 10 系统上提供。以下是在 Windows 10 上体验硬件加速 AV1 视频所需的组件:

*   这些新的 GPU 或 CPU 之一:
*   Windows 10 内部版本 1909 或更高版本
*   AV1 视频扩展
*   支持 AV1 硬件加速的网络浏览器或其他应用，包括基于 Media Foundation 构建的应用
*   最新的图形驱动程序

## 聚光灯来到桌面

另一份独立报告也暗示，微软正致力于在 Windows 10 上扩展 Spotlight 功能。目前，用户可以启用这一功能，在锁屏上显示新的壁纸。当用户启用 Spotlight 时，他们还可以获得某些建议、事实和提示。据报道，最新的 Windows 10 预览版提供了将这一功能扩展到桌面壁纸的能力。该功能默认不启用，但推特用户 *[长鳍](https://twitter.com/thebookisclosed/status/1314174656258158592)* 有个小窍门。通过 *Albacore* 下载 [ViveTool app](https://github.com/thebookisclosed/ViVe/releases) ，在 PowerShell 中使用以下命令:

```
 .\ViveTool.exe addconfig 26008405 2 
```

微软还没有谈到这个特性，所以没有确认它是否会出现在最终版本中。话虽如此，将 Spotlight 添加到桌面上可能会对喜欢个性化个人电脑的用户非常有用。

* * *

**来源:[微软社区](https://techcommunity.microsoft.com/t5/media-at-microsoft/av1-hardware-accelerated-video-on-windows-10/ba-p/1765451)**

**故事 Via:[bleeding computer](https://www.bleepingcomputer.com/news/microsoft/windows-10-is-getting-hardware-accelerated-av1-video-this-fall/)， [Softpedia News](https://news.softpedia.com/news/the-windows-10-feature-that-everybody-loves-is-coming-to-the-desktop-531306.shtml) ，**