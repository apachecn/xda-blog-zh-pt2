# 谷歌 Pixel Now Playing 功能可能会获得位置和活动跟踪

> 原文：<https://www.xda-developers.com/google-pixel-now-playing-location-activity-tracking/>

当谷歌[在 2017 年末宣布](https://www.xda-developers.com/google-pixel-2-xl-announced-price/)Pixel 2 和 Pixel 2 XL 时，他们为谷歌 Pixel 系列引入了一个名为“ [Now Playing](https://www.xda-developers.com/how-google-pixel-2-now-playing-works/) 的功能。该功能使用软件、硬件和机器学习的组合来分析背景音乐播放，通过将音频指纹与包含数万首歌曲的离线歌曲识别数据库进行比较，向您显示正在播放的歌曲。随着 Pixel 3 和 Pixel 3 XL 的推出，谷歌[更新了](https://www.xda-developers.com/now-playing-history-google-pixel-2/) Now Playing 以显示已识别歌曲的历史。现在，我们发现谷歌正准备再一次增强 Now Playing，增加位置和活动跟踪功能。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

## 谷歌 Pixel 2 和更高版本现在播放的位置和活动跟踪？

目前，谷歌 Pixel 上负责[正在播放功能](https://support.google.com/pixelphone/answer/7535326?hl=en)的系统应用 Pixel Ambient Services 会记录下你的手机识别了哪些歌曲以及它们是何时被识别的。3 月份发布的 Pixel Ambient Services 1 . 0 . 229715350 测试版中添加的字符串显示，Now Playing 准备同时显示歌曲被识别的位置以及当时你正在进行的活动。

```
 <string name="history_context_activation_dialog">" Your Now Playing history can include location and activities, like driving. To include this information, allow "<b>Pixel Ambient Services</b> to access your location on the next screen.</string>
<string name="history_context_activation_dialog_button_negative">Cancel</string>
<string name="history_context_activation_dialog_button_positive">Continue</string>
<string name="history_context_switch">history_context_switch</string>
<string name="history_context_switch_subtitle">Now Playing history will show location and activities, like driving</string>
<string name="history_context_switch_title">Include location and activities</string> 
```

该功能尚未在最新版本的 Pixel Ambient Services 中上线。我们第一次[看到暗示](https://www.xda-developers.com/googles-now-playing-prepares-to-finally-add-support-for-showing-history/)谷歌将在 2018 年 4 月下旬保存已识别歌曲的历史——在该功能在 Pixel 3 系列上首次亮相之前 5 个多月。由于该功能没有在 [Pixel 3a 或 Pixel 3a XL](https://www.xda-developers.com/google-pixel-3a-3a-xl-specs-features-price/) 发布时宣布，谷歌可能会在[谷歌 Pixel 4 和 Pixel 4 XL](https://www.xda-developers.com/google-pixel-4-xl-mysterious-third-device-codename/) 发布时宣布该功能。或者，该公司可能会在下一次谷歌制造活动之前宣布像素环境服务的更新。如果该功能面向用户推出，我们会通知大家。

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*