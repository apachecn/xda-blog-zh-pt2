# 一键曝光模块让您从各种应用程序下载视频

> 原文：<https://www.xda-developers.com/one-tap-video-download-xposed-module-lets-you-download-videos-from-various-websites/>

当你在移动时，互联网往往会成为一种特权，而不是无处不在的功能。因此，我们的媒体消费程序需要调整，以适应网络质量和速度的变化。毕竟，与通常无限制的家庭 WiFi 的舒适性相比，在不稳定的 3G 网络上观看视频是一种两极分化的体验。

如果您发现自己经常处于这种情况，并且仍然希望在旅途中使用媒体，请查看 [One Tap 视频下载曝光模块](http://forum.xda-developers.com/xposed/modules/mod-one-tap-video-download-t3309452)。

顾名思义，One Tap 视频下载模块可以让您从各种网站下载视频，而无需经历太多麻烦。这款应用是 XDA 资深会员 [mr.phantom](http://forum.xda-developers.com/member.php?u=4900001) 的努力成果，他提到该模块与涉及 android.media.MediaPlayer 的方法挂钩，从各种应用程序中提取视频链接，并在 Android 4.0+上工作。

基本应用程序与您选择的浏览器应用程序配合使用效果最佳，适用于在自己的服务器上存储视频而不是选择 YouTube 等社区视频服务的网站。当您访问包含此类视频的网页时，app/Xposed 模块会为您提供下载视频或使用外部视频播放应用程序播放视频的选项。第一种情况在您希望离线播放这些视频时很有用，而第二种情况在您不希望从浏览器播放视频但更喜欢外部应用程序时起作用。

主要的 One Tap 视频下载模块应用程序不支持脸书和 YouTube。然而，如果你真的想从这些来源下载视频，**你可以从同一个 dev 安装附加模块**，使你能够从这些网站下载。

更重要的是，YouTube 的主模块和附加模块都是开源的，所以你可以自己看看是怎么做的。【来源:[一键视频下载](https://github.com/Ashish-Bansal/OneTapVideoDownload) | [一键 YouTube 模块](https://github.com/Ashish-Bansal/OneTapYoutubeModule)。我找不到脸书模块的源代码链接，所以请自行决定是否继续。

您可以从 [Play Store](https://play.google.com/store/apps/details?id=com.phantom.onetapvideodownload) 下载 [One Tap 视频模块](http://forum.xda-developers.com/xposed/modules/mod-one-tap-video-download-t3309452)。附加模块可以从各自的 Xposed Repo 页面下载: [One Tap YouTube 模块](http://repo.xposed.info/module/com.phantom.onetapyoutubemodule)、 [One Tap 脸书模块](http://repo.xposed.info/module/com.phantom.onetapfacebookmodule)。对所有这些的支持都在我们的论坛的[单线程中提供。](http://forum.xda-developers.com/xposed/modules/mod-one-tap-video-download-t3309452)

请在下面的评论中告诉我们您对本模块的想法！

请继续阅读相关内容: