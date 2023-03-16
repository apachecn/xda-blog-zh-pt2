# 谷歌手机应用程序准备添加通话录音支持

> 原文：<https://www.xda-developers.com/google-phone-app-call-recording/>

谷歌手机应用程序是谷歌 Pixel 智能手机(这是你能得到的一些最好的 Android 手机)、Android One 计划中的设备以及最近在欧洲销售的[小米智能手机](https://www.xda-developers.com/xiaomi-pre-install-google-phone-messages-global-european-phones/)上预装的拨号应用程序。当小米宣布他们在欧洲销售的所有手机都将预装谷歌手机应用程序时，一些用户感到失望，因为这意味着失去记录电话的功能，这是股票 MIUI dialer 应用程序中的一项功能。小米承诺这项功能将在 2020 年“可获得”，现在谷歌手机应用程序中支持通话记录的第一个暗示已经出现。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

今天早些时候，谷歌手机应用程序的 43.0.289191107 版本为我的 Pixel 4 推出，在解码资源后，我发现谷歌在 dialer 应用程序中添加了新的布局、图标和其他与通话记录有关的资产。新的字符串还显示，将有一个通话按钮来启动新的记录。

```
 <string name=<span >"</span>incall_label_record<span >"</span>>Record</string>
<string name=<span >"</span>incall_content_description_record_unchecked<span >"</span>>Record</string>
<string name=<span >"</span>incall_content_description_record_checked<span >"</span>>Recording</string> 
```

在 Android 9 Pie 之前的 Android 版本[中，可以记录电话通话的音频。在 Android 9 Pie 中，谷歌关闭了开发者用来记录电话通话音频的变通办法。由于自 Android 6 Marshmallow 以来，谷歌一直没有提供官方的通话记录 API，用户不得不依赖 OEM 厂商在其预装的拨号器应用程序中启用通话记录支持。到目前为止，谷歌还没有提供一种在谷歌手机应用程序中记录电话的官方方法，迫使 Pixel 和 Android One 用户在他们想要这样做的时候扎根他们的手机。虽然我们知道谷歌正在努力](https://www.xda-developers.com/android-pie-blocks-non-root-call-recording-apps/)[在未来版本的 Android 中恢复通话记录 API](https://www.xda-developers.com/future-android-version-call-recording/)，但这意味着迫切需要记录电话的用户(出于个人或商业原因)将不得不寻找其他方式来这样做。

即使添加了这段代码，我们也不知道谷歌是否会为谷歌手机应用的所有用户启用通话记录。与该功能相关的代码的添加与小米最近的公告不谋而合，这让我们相信该功能是针对小米智能手机的。然而，这个功能并不需要小米手机，所以谷歌应该很容易为 Pixel 和 Android One 用户启用它。

尽管谷歌手机应用程序增加了这些新资源，但最新版本的应用程序中尚未出现用于通话记录的通话按钮。我们将尝试启用这个功能，如果成功的话，我们会用截图更新这篇文章。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*