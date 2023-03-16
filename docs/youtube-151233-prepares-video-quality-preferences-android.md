# [更新:截图] YouTube 15.12.33 准备在 Android 上添加视频质量偏好

> 原文：<https://www.xda-developers.com/youtube-151233-prepares-video-quality-preferences-android/>

**更新(美国东部时间 3/25/20 @下午 2:20):**一张截图揭示了 YouTube 即将推出的默认视频质量偏好将会是什么样子。

YouTube 是迄今为止全球最受欢迎的视频流媒体服务。由于正在进行的新冠肺炎疫情，人们一般被建议尽可能呆在家里。自然，这导致了视频和相关媒体内容的消费激增，以此来打发随之而来的无聊。这一点，再加上随着世界越来越多地转向数字解决方案，互联网使用的增加，导致许多地区的互联网基础设施出现了前所未有的负荷。虽然互联网基础设施到目前为止基本上保持完好，但这种休闲类消费可以被取消优先级，以确保基础设施在这些情况下不会崩溃。YouTube [刚刚宣布，为了缓解互联网流量，它将在未来一个月内将全球默认视频质量](https://www.bloomberg.com/news/articles/2020-03-24/youtube-to-limit-video-quality-around-the-world-for-a-month)限制在 480p。现在，我们还发现了证据，表明 YouTube 正在努力允许用户在 Android 应用程序上设置他们喜欢的默认视频质量。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

目前，在 YouTube for Android 上，你只能在观看视频时逐个视频地更改视频质量。您也可以选择在使用 Wi-Fi 时限制高质量流。最近的 480p 限制适用于播放的默认设置，但 YouTube 也提到，如果用户想看，它将允许用户以高清方式观看，但他们必须有意识地做出这一选择。人们很自然地认为，这种选择是基于每个视频的，因为这对于消费的每一个视频来说都是足够的，这将有效地阻止用户转向更高的质量。

然而，YouTube for Android v15.12.33 增加了一个关于视频质量偏好的新设置页面的新活动，这表明用户也可以改变默认的视频质量。

```
 <string name="persistent_settings_video_quality_title">Video quality preferences</string>
<string name="persistent_video_quality_auto_description">Adjusts to give you the best experience for your conditions</string>
<string name="persistent_video_quality_auto_label">Auto (recommended)</string>
<string name="persistent_video_quality_high_description">Uses more data</string>
<string name="persistent_video_quality_high_label">Higher picture quality</string>
<string name="persistent_video_quality_intro_description">Select your default streaming quality for all videos. You can change streaming quality in player options for single videos.</string>
<string name="persistent_video_quality_intro_heading">Video quality preferences <b>(BETA)</b></string>
<string name="persistent_video_quality_low_description">Lower picture quality</string>
<string name="persistent_video_quality_low_label">Data saver</string>
<string name="persistent_video_quality_mobile_network_heading">VIDEO QUALITY ON MOBILE NETWORKS</string>
<string name="persistent_video_quality_wifi_heading">VIDEO QUALITY ON WI-FI</string>
<string name="pref_settings_video_quality">Video quality preferences <b>(BETA)</b></string> 
```

虽然这种可能的变化在选择方面是有意义的，但在我们特殊的环境下却令人困惑。用户有权选择更好的质量，通常，我们会支持这个选择。但是此时这种可能的改变会破坏 480p 质量限制的真正目的。我们没有关于将呈现给用户选择的质量的信息，所以我们希望质量被限制在上限，因为考虑到我们的特殊情况，这将仅仅是一个小的不便。

* * *

## 更新:截图

杰出的逆向工程师简·满春·王分享了 YouTube 即将推出的默认视频质量偏好的截图。“视频质量首选项”部分清楚地标记为“测试版”，描述如下:*“为所有视频选择默认的流媒体质量。您可以在单个视频的播放器选项中更改流质量。*用户可以选择移动网络和 Wi-Fi 的默认质量。选项包括自动，“更高的图像质量，”和数据保护。