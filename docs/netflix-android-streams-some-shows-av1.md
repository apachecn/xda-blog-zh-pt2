# Android 版网飞现在可以在 AV1 中播放一些节目以保存数据

> 原文：<https://www.xda-developers.com/netflix-android-streams-some-shows-av1/>

# Android 版网飞现在可以在 AV1 中播放一些节目以保存数据

Android 版网飞现在支持精选节目的免版税 AOMedia Video 1 (AV1)编解码器，这将帮助用户节省移动数据。

开放媒体联盟早在 2017 年就推出了免版税的 AOMedia Video 1 (AV1)编解码器，以取代 H.264 作为在线流媒体和媒体消费的主要编解码器。新的编解码器比谷歌以前的 VP9 标准提供了大约 30%的更好的压缩，而不影响图像质量。编解码器[在 2018 年 10 月的 Chrome 70 更新中转向了谷歌 Chrome](https://www.xda-developers.com/chrome-70-google-sign-in-pwa-support-av1-decoder/) ，当时谷歌在浏览器中添加了 AV1 解码器，MP4 被用作支持的容器(ISO-BMFF)。去年早些时候，随着 Android 10 beta 1 的首次推出，我们得知谷歌已经在平台上[增加了对 AV1 编解码器](https://www.xda-developers.com/android-q-new-features/)的支持。此后不久，流行的视频流媒体平台 [Vimeo 增加了对免版税的 AV1 编解码器](https://www.xda-developers.com/vimeo-supports-av1-video-codec/)的支持，现在网飞似乎正在跟随它的脚步。

根据网飞最近的一篇博客文章，该公司宣布在其 Android 应用程序上支持 AV1 编解码器。根据帖子，流媒体服务的选定标题现已在 AV1 中提供给“希望通过启用‘保存数据’功能来减少蜂窝数据使用量的客户”该编解码器将网飞的 VP9 编码的压缩效率提高 20%，这将大大减少移动数据的使用，而流。此外，网飞还透露其在 Android 上的 AV1 支持使用了开源的 dav1d 解码器。不知道的是，dav1d 解码器是由 VideoLAN、VLC 和 FFmpeg 社区构建的，并由开放媒体设备(网飞是其创始成员)赞助。流媒体服务已经优化了解码器，以播放 10 位颜色的网飞内容。为了让 AV1 广泛可用，网飞还赞助了一项开源工作，以进一步优化 10 位性能。

截至目前，AV1 编解码器仅限于 Android 上的网飞。但是随着编解码器性能的提高，该公司计划扩展对更多用例的支持。值得注意的是，[最近推出的联发科天玑 1000](https://www.xda-developers.com/mediatek-dimensity-1000-7nm-soc-integrated-5g/) 是唯一支持 AV1 上硬件加速解码的 SoC，因此具有其他 SoC 的设备将不得不进行软件解码，这是资源密集型的，并可能导致更高的电池消耗。然而，网飞透露，它正在与设备和芯片组合作伙伴合作，将 AV1 支持扩展到更多的硬件。

* * *

**来源:[网飞理工大学博客](https://netflixtechblog.com/netflix-now-streaming-av1-on-android-d5264a515202)**

**Via: [安卓警察](https://www.androidpolice.com/2020/02/05/netflix-for-android-adopts-av1-video-codec-currently-limited-to-save-data-mode/)**