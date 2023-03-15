# Android Oreo 为支持 IPP 的设备提供内置打印机服务

> 原文：<https://www.xda-developers.com/android-oreo-print-service-ipp/>

当打印机第一次开始用于消费 PC 时，要正确连接设备通常是一件令人难以置信的事情。驱动程序经常坏掉，用户界面不直观，当你需要从电脑上打印东西的时候只会带来麻烦。近年来，随着无线打印机的出现，甚至谷歌通过其谷歌云打印服务所做的工作，这种情况已经得到缓解。尽管如此，它总是可以更容易，这就是为什么 Android Oreo 的默认打印机服务使用的技术是由 Mopria 贡献给 AOSP 的。

对于那些不知道的人，打印服务是一个位于后台的应用程序，它试图发现连接到您所在网络的打印机。然后，它会将这些打印机呈现给设备的打印框架，以便平台可以尝试使用它。使用早期版本的 Android，用户经常需要在谷歌 Play 商店上搜索第三方打印服务，以便从智能手机或平板电脑上打印一些东西(除非它与谷歌云打印服务兼容)。

随着 Android Oreo 的更新，我们现在有了一个默认的打印服务，使人们能够在支持互联网打印协议(IPP)的现代打印机上打印，而无需使用任何额外的应用程序。但是，如果你有一台不支持 IPP 的旧打印机，那么你仍然需要安装由[printremmendationservice](https://android.googlesource.com/platform/frameworks/base/+/android-7.0.0_r1/packages/PrintRecommendationService/)推荐的应用程序。你可以从[谷歌 I/O 2016 展示中了解更多信息。](https://www.youtube.com/watch?v=M_JGeGLpOKs&feature=youtu.be&t=16m20s)

这一变化完全归功于 Mopria 和由佳能、惠普、三星和施乐成立的 Mopria 联盟。随着时间的推移，该联盟在全球范围内已经发展到 20 个成员，新成员包括 Adobe、柯尼卡美能达、高通、利盟、京瓷、东芝、兄弟、爱普生、富士施乐、NEC、Pantum、理光、YSoft、夏普、戴尔和 Primax。统计数据显示，Mopria 认证的打印机占全球销售的打印机的 97%，因此看到这项技术用于 Android 8.0 Oreo 的默认打印机服务是一件大事。

* * *

[**资料来源:Mopria【新闻稿】**](http://www.businesswire.com/news/home/20170822005181/en/)