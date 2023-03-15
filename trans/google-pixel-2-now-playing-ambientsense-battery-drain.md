# [更新]谷歌 Pixel 2 的“正在播放”功能使用 AmbientSense 来最小化电池消耗

> 原文：<https://www.xda-developers.com/google-pixel-2-now-playing-ambientsense-battery-drain/>

**2017 年 10 月 16 日更新:**谷歌已经联系我们，通知我们“正在播放”**不是基于 AmbientSense** 。我们已经回复了关于此功能的更多信息，并将根据他们的回复更新本文。

**2017 年 10 月 19 日更新:**我们已经了解了更多关于 Now Playing 如何工作的细节。请[阅读这篇后续文章](https://www.xda-developers.com/how-google-pixel-2-now-playing-works/)了解更多详情。

* * *

经过数月的泄露，谷歌 Pixel 2 和 Pixel 2 XL T1 正式发布。其中一个更有趣(也更有争议)的功能是“正在播放”，它可以检测背景中正在播放的音乐，并向您显示锁定屏幕上正在播放的内容。在推出的几周前，我们第一次听说了这个功能[，但是我们没有太多关于这个功能的信息，除了谷歌告诉我们它可以离线工作，不需要向云发送任何数据(鉴于](https://www.xda-developers.com/pixel-2-xl-stereo-speaker-music-recognition-portrait-mode/)[最近披露的关于谷歌 Home Mini](https://www.xda-developers.com/google-home-mini-top-touch-bug/) 的消息，后者尤其重要)。在深入研究了 Now Playing 功能后，我们发现该功能基于一项名为 **AmbientSense** 的古老技术，该技术承诺**最小的电池消耗**。

*谷歌 Pixel 2 的现在播放功能*

当我们分析谷歌 Play 商店上提供的 Pixel Ambient Services 应用程序时，我们第一次得到了这方面的提示。

但让我们意识到 AmbientSense 联系的并不是这个应用本身。相反，它是谷歌 Pixel 2 上预装在/system/priv-app 中的 APK 的名称。APK 被称为 AmbientSense，它与研究人员 M. Rossi、S. Feese、O. Amft、N. Braune、S. Martis 和 G. Trö ster 在 2013 年 IEEE 普适计算和通信研讨会国际会议上提交的研究论文中描述的技术名称相匹配。

## 什么是 AmbientSense，它与“正在播放”有什么关系

我们发现一个网页显示了这篇论文的第一页[这里](https://www.deepdyve.com/lp/institute-of-electrical-and-electronics-engineers/ambientsense-a-real-time-ambient-sound-recognition-system-for-9vWQ7kDSlD)。根据论文摘要，AmbientSense 是智能手机上的一个**实时环境声音识别系统 AmbientSense 最有趣的是，它可以作为 Android 应用程序来实现，只需要访问设备的麦克风来分析环境声音。**

文中描述了两种处理模式:**自治**和**服务器模式**。只有通过将音频样本与本地存储的数据库进行比较，智能手机才会进行自主处理。相比之下，服务器模式向服务器发送音频特征，然后服务器发回分类结果。显然，谷歌的“正在播放”功能正在“自主”模式下运行 AmbientSense，因为它可以离线工作，无需向谷歌发送任何信息。

该论文继续描述了研究小组如何在一组 23 种环境声音类别中测试自主和服务器模式识别下的识别性能、运行时间、CPU 负载和识别延迟。他们发现 AmbientSense 应用程序在三星 Galaxy SII 上运行了 13.75 小时，在谷歌 Nexus One 上运行了 12.87 小时。记住这些设备有多旧；谷歌 Nexus One 于 2010 年发布，配有 1400 毫安时电池，与 Pixel 2 相比是一只恐龙。我们只能想象通过谷歌的测试，AmbientSense 被提炼了多少。

## 有没有可能在非谷歌 Pixel 2 手机上移植 Now Playing 功能？

我还不能做出任何承诺，但我认为这是可能的。我们正与 XDA 公认的贡献者[昆尼 899](https://forum.xda-developers.com/member.php?u=3563640) 一起努力让它发生。为了让 Now Playing 功能在第一代谷歌 Pixel/Nexus 智能手机上运行，我们认为需要做几件事:

*   像素环境服务(AmbientSense.apk)
*   音频匹配数据库
*   一些缺失的库
*   对环境显示的系统用户界面修改
*   Root 访问(将上述文件推送到/system)

*截图鸣谢:基隆·奎因(Quinny899)*

我们目前已经拥有一个名为“matcher.leveldb”的音频匹配数据库，这是一个基于谷歌 [LevelDB](https://github.com/google/leveldb) 的 53MB 存储库。这是 AmbientSense 在自主模式下进行音频匹配所依赖的数据库。

至于库，我们知道它们的名称以及在哪里可以找到它们，但是在我们能够得到 Pixel 2 来提取它之前，还需要一些时间。

最后，SystemUI 需要修改，因为“Now Playing”功能将文本写入环境显示——这在第一代 Pixel 上的环境显示功能上目前是不可能的。

至于让它在非谷歌手机上工作，我们将在谷歌 Pixel 和 Nexus 手机上工作后进行测试。如果或当我们在使这一功能工作上取得突破性进展时，您将首先在 XDA 门户网站上了解到这一点——请继续关注更多内容！