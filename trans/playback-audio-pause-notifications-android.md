# 在为 Android 8.0 构建的应用中，播放音频不会因通知而暂停

> 原文：<https://www.xda-developers.com/playback-audio-pause-notifications-android/>

# 在为 Android 8.0 构建的应用中，播放音频不会因通知而暂停

播放音频可以通过 Android 上的通知来停止，在听音乐或看视频时可能会很烦人。奥利奥想要改变这种状况。

Android 上的音频闪避指的是当另一个音频源(通常是通知)开始播放时，音频的音量降低。当通知避开已经播放的音频源的音频时，它将音频焦点从应用程序上移开，就像 Pokemon Go 在音乐已经播放时启动它一样。顺便说一下，这里的详细介绍了一种解决方法。应用程序可以选择回避音频，甚至完全停止播放；例如，如果你在 Spotify 上播放一首歌曲，然后打开 YouTube 视频，Spotify 会完全停止音乐播放。然而，对于任何以 Android Oreo(SDK 26 级)为目标的应用程序，这将发生变化，因为**播放音频将不再因收到通知而暂停**。

* * *

## Android Oreo 改变了播放音频响应通知的方式

现在有了 [Android Oreo](https://android.googlesource.com/platform/frameworks/base/+/461922fcfc8572415aa39c43c06afce685bd998d) ，每当另一个应用程序或通知获得音频焦点时，针对最新版本的应用程序将不再停止播放。相反，这些应用程序会简单地默认避开音频。例如，Podcast Addict 应用程序会在收到新通知时短暂停止媒体播放，然后恢复播放。如果 Podcast Addict 改为更新到目标 SDK 级别 26(又名 Android 8.0 Oreo)，那么它的音量将会降低(音频闪避)，而不是在收到通知时完全暂停。

这与其他变化如[救援队](https://www.xda-developers.com/android-oreo-rescue-party-bootloop/)和[项目三冠王](https://www.xda-developers.com/project-treble-android-o-exist-flagship/)一样，表明 Android Oreo 更多的是优化和幕后改进，而不是大规模的变化。很高兴看到谷歌在较小的领域做出改进，并关注操作系统的小部分。多年来，Android 的小漏洞一直是批评的对象。

我们将继续寻找其他已经发生的变化。请使用我们的 XDA 实验室应用程序继续关注 XDA 门户网站，了解所有最新的 Android 8.0 和其他 Android 相关新闻。