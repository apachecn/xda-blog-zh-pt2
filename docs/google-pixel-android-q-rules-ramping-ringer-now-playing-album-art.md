# Android Q 上的 Google Pixel 可能会获得规则，增加铃声，现在播放专辑封面

> 原文：<https://www.xda-developers.com/google-pixel-android-q-rules-ramping-ringer-now-playing-album-art/>

谷歌 Pixel 4 泄露季节已经开始了。从泄露的[非 XL](https://www.xda-developers.com/google-pixel-4-leaked-renders/) 和 [XL](https://www.xda-developers.com/google-pixel-4-xl-render-notch-less-dual-front-cameras-triple-rear/) 型号的 CAD 渲染图到[现场图片和官方媒体渲染图](https://www.xda-developers.com/google-pixel-4-teaser/)，关于谷歌 2019 年旗舰智能手机，我们已经知道了很多[。谷歌的下一代 Pixel 智能手机可能不会赢得任何设计奖项，但如果有一件事我们可以指望谷歌，那就是软件体验。根据应用程序的拆除，我们可以推测谷歌的下一代设备将会有哪些新功能。在深入研究](https://www.xda-developers.com/google-pixel-4-leaks-rumors/) [Android Q beta 5](https://www.xda-developers.com/android-q-beta-5-rolling-out/) 时，我们启用了一些可能会在 2019 Pixel 4 中出现的功能。这些功能包括在每个网络或每个位置配置声音行为的“规则”，在来电时逐渐增加铃声的音量，最后，在正在播放的历史页面中显示专辑封面。

[**谷歌像素 4 论坛**](https://forum.xda-developers.com/pixel-4) **[谷歌像素 4 XL 论坛](https://forum.xda-developers.com/pixel-4-xl)**

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

* * *

## Android Q 中的规则

在 Android Q beta 3 发布后不久，我们[在 SettingsIntelligence APK 中发现了](https://www.xda-developers.com/google-pixel-android-q-settings-routines/)个新字符串，概述了一个叫做“规则”的新功能该功能有助于“自动执行您定期在设置中进行的更改”，并且它是专门设计来让您在连接到您选择的 Wi-Fi 网络或您在地图上选择的位置附近时，将声音模式更改为响铃、振动、静音或免打扰。例如，你可以在上班时将手机设置为静音，或者在电影院时将手机设置为勿扰模式。

我在运行 Android Q beta 5 的谷歌 Pixel 2 XL 上激活了这项功能，你可以在下面的截图中看到。“规则”的当前实现驻留在设置>系统中。您可以在这里添加规则或启用自动规则建议，自动规则建议使用位置和日历信息来建议规则。

该功能似乎已经完全可用。我启用了一个规则，当我的 Google Pixel 2 XL 连接到我家的 Wi-Fi 网络时，它会使我的 Google Pixel 2 XL 静音，我还制定了另一个规则(上面没有显示)，当我在当地超市 H-E-B 附近时，它会使我的手机静音。

“规则”功能是谷歌像素专属设置智能 APK 的一部分，但尚不清楚一旦推出，是否所有谷歌像素智能手机都可以使用该功能。我高度怀疑谷歌会在稳定的 Android Q 版本或后续的每月更新中悄悄添加这项功能，所以我打赌我们会在谷歌 Pixel 4 发布软件上看到它的首次亮相。

* * *

## 渐变振铃音量

在我们关于“规则”的第一篇文章中，我们还发现了一个名为“渐变振铃”的新设置在来电时，该功能会使手机振动几秒钟，然后逐渐提高铃声音量。我设法让“ramping ringer”出现在我的谷歌 Pixel 2 XL 上的 Android Q beta 5 的设置中。该设置将出现在“设置”>“声音”>“来电振动”中，以前是一个开/关开关，现在是一个子菜单。

这项功能目前的设计方式是让手机振动 5 秒钟，然后在 10 秒钟内提高音量。如果你在任何时候点击来电提醒，音量就会迅速上升到用户定义的铃声音量。似乎没有任何东西将这项功能锁定在 Pixel 手机上，但我们无法确认它是否会在非 Pixel 智能手机上可用。

* * *

## Google Pixel 现在播放历史中的专辑封面

随着谷歌 Pixel 2 系列的推出，谷歌推出了一项名为“ [Now Playing](https://www.xda-developers.com/how-google-pixel-2-now-playing-works/) ”的新功能。每 60 秒一次，现在播放使用麦克风在背景中采样音频。如果它检测到一首歌曲正在播放，那么它会将这首歌曲的音频指纹与手机离线歌曲识别数据库中存储的指纹进行比较。该数据库包含数万首歌曲的列表，每周通过 Wi-Fi 进行更新，并基于您所在地区 Google Play 音乐目录中最受欢迎的歌曲。

自从最初发布以来，Now Playing [收到了一个更新](https://www.xda-developers.com/google-pixel-3-google-pixel-3-xl-specs-features-pricing-availability/)来显示已识别歌曲的历史。今年早些时候，我们发现了[的证据](https://www.xda-developers.com/google-pixel-now-playing-location-activity-tracking/)，Now Playing 将增加位置和活动跟踪支持，这样当你听到一首特定的歌曲时，你会更好地知道你在哪里，你在做什么。现在，我们发现谷歌正准备显示当前播放历史中每首歌曲的专辑封面。

虽然你可以通过点击列表中的任何歌曲，然后查询谷歌来查找专辑封面，但一旦“现在播放”更新为在左侧以图标形式显示专辑封面，你就可以跳过这一步。当在当前状态下激活该功能时，专辑封面只是一个占位符，我们在最新的 AmbientSensePrebuilt 中检查的代码确认了当前没有实际提取专辑封面的实现。即使所述专辑封面图像最终是微小的缩略图，在您的设备上存储数万张它们也会增加大小。因此，我认为这些图片只能从网上提供。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*