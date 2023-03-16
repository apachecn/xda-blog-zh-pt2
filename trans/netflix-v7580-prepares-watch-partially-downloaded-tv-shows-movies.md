# 网飞 7.58.0 准备让你观看部分下载的节目

> 原文：<https://www.xda-developers.com/netflix-v7580-prepares-watch-partially-downloaded-tv-shows-movies/>

# 网飞 7.58.0 版准备让你观看部分下载的电视节目或电影

我们在网飞应用 7.58.0 版本中发现了新的字符串，这表明你很快就可以在 Android 上观看部分下载的节目和电影。

网飞可能很快会让你在安卓上观看部分下载的节目和电影。自 2016 年以来，网飞在移动和桌面应用程序上都支持[离线下载](https://www.xda-developers.com/netflix-android-auto-download-episodes-offline/)，但它不会让你播放任何未完全下载的视频。但这可能很快会改变。我们在[网飞应用](https://play.google.com/store/apps/details?id=com.netflix.mediaclient)7 . 58 . 0 版本中发现字符串，表明该公司正计划添加对播放部分下载内容的支持。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

这些是网飞应用 7.5.80 版中的新字符串

```
 <string name="label_partial_download_use_cellular_message">"You've reached the end of what you've downloaded so far. Would you like to download over cellular to continue watching?"</string>
<string name="label_partial_download_use_cellular_no">No Thanks</string>
<string name="label_partial_download_use_cellular_title">Download over cellular to continue watching?</string>
<string name="label_partial_download_use_cellular_yes">Download Now</string>
<string name="label_partial_download_download_more_message">You need to download a bit more to continue watching, or you can watch what you already have downloaded from the beginning.</string>
<string name="label_partial_download_download_more_no">Watch from Beginning</string>
<string name="label_partial_download_download_more_yes">Wait for Download</string>
<string name="label_partial_download_end_of_downloaded">"You've reached the end of what's been downloaded so far. Please connect to the internet to continue watching."</string>
<string name="label_partial_download_not_ready">You need to download a bit more to start watching.</string> 
```

当你的网络连接不稳定或移动数据有限时，能够观看部分下载的视频将非常有用。这里的想法是，如果你在下载过程中用完了数据或失去了连接，你至少可以观看部分下载的位。正如我们自己的 [Zachary Wander](https://www.xda-developers.com/author/zacharywander/) 所指出的，该功能的另一个可能的应用是，当您处于慢速连接时，您可以使用该功能来解决缓冲问题。例如，你可以提前 30 分钟开始下载你最喜欢的节目，然后开始不间断地观看。如果做得巧妙，可以在看最新一集的时候有一个无缓冲的体验。

二月份的时候，一位用户联系网飞，建议增加对部分下载的支持。网飞答复说，他们已经考虑了这个建议。然而，也完全有可能网飞在收到这个建议之前就已经在研究这个特性了。

该功能尚未向用户推出，但根据我们发现的一些新布局文件，它可能会在最新更新中作为 A/B 测试运行。