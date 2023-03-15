# 谷歌 Android 版 Chrome 浏览器很快将获得 YouTube 的双击快进或快退功能

> 原文：<https://www.xda-developers.com/google-chrome-android-double-tap-fast-forward-rewind-youtube/>

今年早些时候，谷歌为 YouTube 应用程序添加了一个漂亮的新功能:双击视频侧边，快进或快退 10 秒。这个特性[在一月份开始向一些用户](https://www.xda-developers.com/psa-double-tap-to-fast-forward-rolling-out-to-youtube-app-on-android/)推出，然后在二月份的版本中正式启用。现在，随着 Chrome Canary 和 Chromium 的最新夜间版本推出，同样的功能也将出现在谷歌 Android 版 Chrome 上。

前几天晚上，我在开源 Chromium gerrit 中发现了一个[少数](https://chromium-review.googlesource.com/c/chromium/src/+/839420) [新](https://chromium-review.googlesource.com/c/chromium/src/+/757138)提交，它将双击手势识别添加到媒体控制覆盖中。查看文件，它提到如果用户双击视频的边，视频将向前或向后跳转 10 秒。这与 YouTube 应用程序中的播放控制行为相同。

进一步观察，我发现如果你使用的是谷歌 Chrome for Android 的最新版本，这个功能现在就可以启用。你需要使用最新的 Chrome Canary 版本(v65.0.3301.0)或者类似的 Chrome 版本。

为了启用这个功能(以及 Chrome 的所有新媒体播放控件)，你需要在 chrome://flags 中启用一个特殊的标志。只需将下面一行粘贴到浏览器的地址栏中，启用该功能，然后重启浏览器。然后，你可以双击任何通过 Chrome 内置媒体播放器播放的视频来快进或快退。

```
 chrome: 
```

享受新功能！除此之外，还有几个其他即将推出的功能令人兴奋。谷歌宣布，原生广告拦截(针对违规广告)将于 2 月 15 日到来。我们还发现 Chrome 将很快支持[并行下载以加速下载](https://www.xda-developers.com/google-chrome-parallel-download-accelerate-download-speeds/)和 [HDR 视频播放](https://www.xda-developers.com/hdr-video-playback-support-chrome-for-android/)以在支持的设备上获得更高的视频质量。一旦我们发现更多有趣的谷歌 Chrome 相关新闻与大家分享，你将是第一个在 XDA 门户网站上发现的人。敬请期待！

* * *

**P.S** 如果你想知道在我的视频中引起超级用户吐司消息的应用程序是什么，那就是[环境锁定屏幕音乐](https://www.xda-developers.com/ambient-lock-screen-music-pixel-2/)——一个根应用程序，它在环境显示锁定屏幕上显示当前正在播放的任何媒体的标题和艺术家。这是谷歌 Pixel 2 和 Pixel 2 XL 独有的，但如果你[在 Nexus 6P、Pixel 或 Pixel XL](https://www.xda-developers.com/enable-google-pixel-2-always-on-display-on-nexus-6p-pixel-xl/) 上启用永远显示，也可以工作。