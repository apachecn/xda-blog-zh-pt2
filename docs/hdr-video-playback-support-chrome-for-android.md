# Android 版 Chrome 将支持 HDR 视频播放

> 原文：<https://www.xda-developers.com/hdr-video-playback-support-chrome-for-android/>

# Android 版 Chrome 将支持 HDR 视频播放

根据最近的提交，HDR 视频播放支持将在谷歌 Android Chrome 上实现。这将导致更好的对比度和颜色准确性。

高动态范围(HDR)视频的普及是提高全民视频质量的下一步。HDR 显著提高了亮度范围，拓宽了色彩空间，从而提高了对比度和色彩准确度。Android [从 Android 7.0 牛轧糖开始正式支持](https://source.android.com/devices/tech/display/hdr) HDR 播放支持，尽管支持高色深格式取决于个人设备，支持从视频中提取 HDR 元数据取决于个人应用程序。当然，它还需要能够产生更宽色彩空间的兼容显示器。

许多当前的旗舰设备能够回放 HDR 的内容，尽管目前缺少可供观看的 HDR 视频内容。Google Play Movies & TV 、[网飞](https://www.xda-developers.com/netflix-hdr-dolby-vision-lg-g6/)以及最近的 [YouTube](https://www.xda-developers.com/youtube-hdr-playback-support-android/) 支持在少数设备上播放 HDR，尽管它们的库有限。然而，看起来谷歌 Android 版 Chrome 将很快加入能够播放 HDR 视频的应用行列。

根据 Chromium gerrit 上的[两个](https://chromium-review.googlesource.com/c/chromium/src/+/755952)最近的[提交](https://chromium-review.googlesource.com/c/chromium/src/+/756443)，Google Chrome for Android 将能够从视频容器中提取 HDR 元数据，并将其传递给 MediaCodec 类。然后，可以在支持的设备上播放以 VP9 Profile 2 (10 位)视频编解码器编码的 HDR 视频。

谷歌 Chrome 的这一改进将在未来带来更高质量的视频观看体验。不幸的是，由于可用的 HDR 内容数量如此有限，大多数用户至少在几年内无法欣赏 HDR 带来的改进。此外，由于编码的数据量更大，流式 HDR 内容自然比非 HDR 内容需要更多的带宽，因此在世界许多地区，数据速度可能仍然是一个限制因素。

如果你有一台能够播放 HDR 内容的设备以及与之匹配的互联网速度，请查看 YouTube 上的这段视频，体验一下 HDR 能给你的视频观看体验带来什么。