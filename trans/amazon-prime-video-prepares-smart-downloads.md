# 亚马逊 Prime Video 可能很快会推出类似网飞的智能下载功能

> 原文：<https://www.xda-developers.com/amazon-prime-video-prepares-smart-downloads/>

有几个原因使网飞成为最好的视频流媒体服务之一。该平台不仅提供了一些很棒的内容，还包括一些非常方便的功能，可以显著改善您的体验。像 Skip Intro 按钮和 [smart downloads](https://www.xda-developers.com/netflix-android-auto-download-episodes-offline/) 这样的功能起初看起来并不怎么样，但当你切换到另一个没有这些功能的流媒体服务时，你就会意识到它们的重要性。例如，亚马逊 Prime Video 还没有智能下载功能。就我而言，当我在它的移动应用程序上观看节目时，我非常想念它。令人欣慰的是，用不了多久，这个功能最终会出现在亚马逊 Prime Video 上。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

亚马逊 Prime Video APK (v 3.0.259.65541)最近被拆除，暴露了暗示即将到来的自动下载功能的代码串。该功能的工作原理与网飞的智能下载非常相似，可以自动下载你正在观看的任何电视剧的下一集，以提供不间断的观看体验。

```
 <string name="AV_MOBILE_ANDROID_AUTO_DOWNLOADS_HELP_MESSAGE">"As you watch TV shows on your mobile device, we'll automatically download the next episode for you."</string>
<string name="AV_MOBILE_ANDROID_AUTO_DOWNLOADS_STATUS_BAR_SETTINGS_LINK">Manage</string> 
```

正如下面的截图所示，自动下载功能将默认在 WiFi 网络上工作，除非您启用移动数据下载。为了节省空间，该应用程序将在下载下一集时自动删除已观看的剧集，您可以选择自动下载多少集。

此外，我们还发现了暗示另一个很酷的功能进入应用程序的字符串。这项功能将允许你在 Amazon Prime Video 上关注顶级演员，并在他们的视频上线时收到通知。如果你不确定要关注哪些演员，该平台还将包括一个发现部分，提供顶级演员推荐(如上面的截图所示)。

```
 <string name="AV_MOBILE_ANDROID_FOLLOWING_DIALOG_EXPERIMENT_BODY">We are currently experimenting with this feature. We may disable it without notice.</string>
<string name="AV_MOBILE_ANDROID_FOLLOWING_DIALOG_EXPERIMENT_TITLE">Experiment details</string>
<string name="AV_MOBILE_ANDROID_FOLLOWING_EMPTY_BODY">Follow your favorite actors to get notifications when their videos are added to Prime Video.</string>
<string name="AV_MOBILE_ANDROID_FOLLOWING_EMPTY_BODY_NOTIFICATIONS_DISABLED">Keep track of all your favorite actors in one place.</string>
<string name="AV_MOBILE_ANDROID_FOLLOWING_EMPTY_TITLE">"You're not following anyone yet..."</string>
<string name="AV_MOBILE_ANDROID_FOLLOWING_SEE_TOP_ACTORS">Discover top actors to follow</string>
<string name="AV_MOBILE_ANDROID_FOLLOWING_TITLE">Following</string>
<string name="AV_MOBILE_ANDROID_FOLLOWING_TOP_ACTORS">Top actors</string> 
```

我们的主编[米沙·拉赫曼](https://forum.xda-developers.com/member.php?u=7050182)手动启动了应用程序中的新活动来抓取上面的截图。然而，这些功能似乎还没有上线。截至目前，我们还没有从亚马逊获得关于这些新功能发布时间表的信息。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*