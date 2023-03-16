# Google Play Movies 准备增加数百部广告支持的免费电影

> 原文：<https://www.xda-developers.com/google-play-movies-ad-supported-free-movies/>

有数百种视频流媒体服务可以让你在家观看你最喜欢的电视剧和电影，如[网飞](https://www.xda-developers.com/netflix-hdr-samsung-galaxy-s20-more-phones/)，亚马逊 Prime Video，Hulu，以及最近的 Disney+。这是谷歌没有真正竞争的一个领域。虽然上述其他服务允许你每月付费访问他们的所有视频内容，但 Google Play Movies & TV 是一个市场，你可以单独租赁和购买数字电影和电视节目。然而，谷歌似乎正在计划一些改变来促进采用，特别是电影的免费广告计划。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

正如我们之前提到的，该应用程序目前只允许你租赁和购买电影和电视剧，只有极少数例外的电影和节目是免费的。然而，在 4.18.37 版本的 Android 应用程序中，我们发现了一些字符串，暗示谷歌将推出一个新的带广告的免费电影选择。特别是一个字符串，暗示了“数百部电影，只有几个广告”的存在，这表明该应用程序的大部分库可能会以这种新格式提供。然而，目前还不清楚谷歌的所有图书馆是将免费提供广告，还是只提供少数电影。然而，它将彻底改变这项服务目前的工作方式，并使其成为其他流媒体服务的有力竞争者。

```
 <string name="athome_add_birthdate_to_watch">Add birthdate to watch</string>
<string name="athome_free_with_ads">Free with ads</string>
<string name="athome_free_with_ads_description">Hundreds of movies, just a few ads</string>
<string name="athome_introduce_free_movies">Introducing</string>
<string name="athome_watch_free_with_ads">Watch free with ads</string> 
```

这项功能目前还不可用，但鉴于谷歌的正常工作方式，我们可以在发布后的任何时候看到这项功能作为服务器端更新推出到 Google Play Movies。