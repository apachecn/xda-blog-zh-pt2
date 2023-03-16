# 用于 Android TV 的 YouTube 在某些设备中采用 AV1 视频编解码器

> 原文：<https://www.xda-developers.com/youtube-for-android-tv-adopts-av1-video-codec-in-certain-devices/>

# 用于 Android TV 的 YouTube 在某些设备中采用 AV1 视频编解码器

YouTube for Android TV 现在在某些硬件支持的设备中增加了对 AV1 视频编解码器的支持。看看吧！

对于大多数用户来说，关于视频编解码器的新闻可能不是特别令人兴奋，但它们可以在我们甚至没有意识到的情况下对我们的媒体消费产生巨大影响。尤其是因为我们都困在家里，用互联网上在线课程，看网飞的电视节目和电影，或者去 YouTube 的兔子洞。您最喜爱的在线视频服务背后的每家公司都仔细考虑了使用哪种视频编解码器来编码他们的视频，以优化大小，而不会严重牺牲最终用户的质量或功耗。最近有一个视频编解码器得到了很多爱好者的支持，那就是谷歌为一些 YouTube 视频和[谷歌双人视频通话](https://www.xda-developers.com/google-duo-av1-moment-screenshots-saving-messages/)实现的[免版税 AV1 编解码器](https://www.xda-developers.com/tag/av1/)。现在，谷歌在最新版本的 YouTube 应用程序中为 Android 电视设备添加了观看 AV1 编码视频的支持。

AV1 编解码器非常适合媒体流；与同类编解码器相比，它能够以更小的文件大小提供更高质量的视频，从而减少服务和用户的带宽使用。不过，这里的问题是，能够进行硬件加速 AV1 解码的 SOC 并不多。智能手机和 Android 电视盒子上使用的大多数 SOC 都依赖于 AV1 编码视频的软件解码，这可能会加重 CPU 的负担，并导致更高的功耗。在智能手机方面，只有[联发科天玑 1000 能够解码 AV1](https://www.xda-developers.com/mediatek-dimensity-1000-is-the-first-smartphone-soc-to-support-av1-hardware-decoding/) ，而只有少数最近用于 Android 电视设备的 SOC 支持硬件加速的 AV1 解码。其中包括博通的 bcm72190/72180 和 Realtek 的 RTD1311/RTD1319。

YouTube for Android TV 更新的变更日志确实提到该功能仅适用于“受支持的设备”，这表明可能有一个设备白名单在起作用。

如果你有一个支持芯片组的 Android 电视设备，那么你可以尝试下载 YouTube 更新，看看你是否能够播放 AV1 编码的视频。更新现在正在通过 Google Play 推出，但如果你没有看到，那么你也可以从 APKMirror 下载。