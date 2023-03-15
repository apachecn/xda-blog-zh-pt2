# 亚马逊 Prime 视频准备随机集按钮和选择下载的音频语言

> 原文：<https://www.xda-developers.com/amazon-prime-video-preps-random-episode-button-shuffled-playlist-choosing-audio-language-downloads/>

Amazon Prime Video 是世界上最受欢迎的流媒体服务之一，这部分归功于它与 Amazon Prime 的捆绑，部分归功于它提供的内容。在过去的几个月里，该服务增加了新的功能，以保留其用户群并获得更多的用户。例如，[观看聚会功能可以让你和你的朋友一起观看内容](https://www.xda-developers.com/amazon-prime-video-watch-party/)，而[个人资料可以让多个用户使用同一个账户](https://www.xda-developers.com/amazon-prime-video-netflix-profiles/)，并且仍然有独立的内容提要。现在，[亚马逊 Prime Video](https://play.google.com/store/apps/details?id=com.amazon.avod.thirdpartyclient) 正准备让用户随机播放一集，还可以选择一种音频语言进行下载。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

我们在适用于 Android 的亚马逊 Prime Video 3 . 0 . 227 . 35447 应用中发现了以下字符串:

```
 <string name="AV_MOBILE_ANDROID_ACTION_BAR_SHUFFLE_EPISODES">Shuffle episodes</string>
<string name="AV_MOBILE_ANDROID_ACTION_BAR_SHUFFLE_EPISODES_TOOLTIP">Love every episode? Shuffle the entire series for a playlist of random episodes.</string> 
```

随机剧集功能类似于为网飞准备的随机剧集选项(但还没有推出)。我们认为这一功能背后的动机是模仿有线电视的怀旧情绪，用户可以经常看到他们可以观看或重温的随机剧集。这对于不遵循严格时间表的轻松节目来说效果最好，因此用户可以简单地观看一些内容，而不必花力气选择内容。根据字符串描述，随机播放剧集按钮会创建一个随机播放列表，其功能类似于仅仅选择一串随机的剧集。

此外，该应用还允许用户选择下载内容的音频语言:

```
 <string name="AV_MOBILE_ANDROID_DOWNLOAD_BOTTOM_SHEET_DIALOG_ALWAYS_ASK_CHECKBOX">Always Ask</string>
<string name="AV_MOBILE_ANDROID_DOWNLOAD_BOTTOM_SHEET_DIALOG_AUDIO_LANGUAGE_TITLE">Audio Language</string>
<string name="AV_MOBILE_ANDROID_DOWNLOAD_BOTTOM_SHEET_DIALOG_CHOOSE_AUDIO_LANGUAGE_TO_DOWNLOAD">Choose an audio language to download</string>
<string name="AV_MOBILE_ANDROID_DOWNLOAD_BOTTOM_SHEET_DIALOG_PREFERRED_LANGUAGE_UNAVAILABLE">Your preferred audio language is unavailable for this video. Choose audio language to download</string> 
```

这项即将推出的功能将主要针对具有多种语言选项的电视节目和电影，这对于在多语言地区发布的内容来说非常常见。从描述来看，这款应用似乎会显示一个底部的表格，询问你想要下载哪种音频语言。

我们不知道这些功能何时会向所有用户推出，但我们希望能很快看到它们上线。

* * *

*感谢 PNF 软件为我们提供了使用* *[JEB 反编译](https://www.pnfsoftware.com/?aid=xdadev)* *的许可，这是一款针对 Android 应用的专业级逆向工程工具。*