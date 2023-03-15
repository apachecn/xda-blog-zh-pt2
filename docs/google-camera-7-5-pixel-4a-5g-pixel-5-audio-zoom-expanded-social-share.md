# 谷歌摄像头 7.5 证实了 Pixel 4a 5G 和 Pixel 5，并暗示了音频缩放、扩展的社交分享等功能

> 原文：<https://www.xda-developers.com/google-camera-7-5-pixel-4a-5g-pixel-5-audio-zoom-expanded-social-share/>

用于谷歌 Pixel 智能手机的谷歌相机应用程序的最新版本 7.5 版昨晚开始推出。我们反编译了 APK，看看我们是否能找到任何关于即将到来的像素相机功能的线索，我们发现了一些值得注意的功能。我们还发现了更多证据，表明今年不会有 Pixel 5 *XL* 型号，但除了已经广泛泄露的标准 [Pixel 4a](https://www.xda-developers.com/tag/pixel4a/) 之外，还会有 Pixel 4a *5G* 。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

**谷歌 Pixel 4a 5G = bramble，谷歌 Pixel 5 = redfin**

本月早些时候，谷歌应用程序中的[代码表明，这两款 2020 年末的 Pixel 设备将被命名为 Pixel 4a 5G(代号为“bramble”)和 Pixel 5(“redfin”)。当](https://www.xda-developers.com/pixel-4a-5g-pixel-5-leak/) [AOSP 的一家存储库透露](https://www.xda-developers.com/google-pixel-2020-code-names-snapdragon-765-snapdragon-730/)这些设备将由 sm7250 移动平台驱动时，我们之前已经看到过代号为“bramble”和“redfin”的设备，sm 7250 移动平台可以是高通骁龙 765、骁龙 765G 或骁龙 768。我们还看到“redfin”出现在用于反向无线充电的 [Android 11 代码](https://www.xda-developers.com/android-11-battery-share-reverse-wireless-charging-pixel-5/)中，这表明这项高级功能不会在“bramble”上提供我们再次看到代码表明今年不会有 Pixel 5 XL。谷歌相机 7.5 中的一个类(请注意，与谷歌应用中看到的谷歌镜头相关的类相同)同样引用“bramble”是像素 4a 5G，“redfin”是像素 5。

一个库中的一行建议 Pixel 4a 5G，Pixel 5，或者两个设备都有双摄像头。这一行引用了一个名为 P20 _ dual _ camera _ rig _ proto . binary Pb 的二进制文件，但我们无法访问它。我们还不太有信心从这一条线得出任何结论，但我们会密切关注今年像素旗舰相机能力的更多证据。

**音频缩放**

在 Pixel 4 发布之前，我们首先发现[谷歌正在开发](https://www.xda-developers.com/google-pixel-4-camera-features-audio-zoom-live-hdr-better-wide-angle-photos/)一项名为音频缩放的新功能。这项功能在 HTC、LG、三星和其他设备制造商的几款智能手机上都可以看到，当你放大或缩小时，它使用手机的麦克风来调整音频焦点。当 Pixel 4 推出时，该功能并不存在。然而，它仍然在工作中，正如谷歌相机 7.5 中添加的新字符串所证明的那样:

```
 <string name="pref_audio_zoom_summary">Boost the sound where the user is zooming in on.</string>
<string name="pref_audio_zoom_title">Audio zoom</string> 
```

在 XDA 资深会员的帮助下，我们在谷歌相机的设置中提出了音频缩放的开关。然而，它在我的 Pixel 4 上不起作用。也许我的设备缺少必要的硬件(摄像头旁边还有一个麦克风？)或库来实现这个特性。

**帮助改进谷歌摄像头**

谷歌相机应用程序的另一个新切换是随着时间的推移改进相机的偏好。根据字符串，相机应用程序将在您使用它时“随着时间的推移而学习”。相机应用程序存储的所有数据都将“留在你的设备上”，尽管谷歌将使用“隐私保护技术”“[结合]来自你和许多其他参与者的信息，让相机对每个人来说都更智能。”我们不确定谷歌会收集什么样的数据，以及基于这些数据可以做出什么样的改进。

```
 <string name="pref_camera_improve_camera_summary">Allow Camera to learn over time as you use it. Your data stays on your device while privacy-preserving technology combines information from you and many other participants to make Camera smarter for everyone.</string> 
```

**扩大社交份额**

随着 Pixel 4 的发布，谷歌相机应用程序中引入了一个很棒的功能，那就是“社交分享”。此功能可让您快速轻松地分享刚刚拍摄的照片。拍照后，只需从缩略图向上滑动，即可将照片分享到社交媒体。在谷歌相机的设置中，你可以选择哪 3 个社交媒体应用出现在社交分享的转盘中。支持的社交媒体应用程序包括 Discord、Facebook Messenger、Facebook Messenger Lite、Chat、Messages、GroupMe、Hangouts、Helo、Imo Messenger、Instagram Stories、KakaoTalk、Kik、LINE、ShareChat、Signal、Skype、Snapchat、Telegram、Textra、Twitter、威瑞森 Message+、Viber、微信和 WhatsApp。

隐藏在谷歌相机 7.5 代码深处的是一个由 25 个应用程序组成的允许列表，用户可以快速分享视频。本质上，谷歌正在扩大社交分享，以支持快速分享视频到社交媒体和/或消息应用程序。目前支持的应用包括脸书、Facebook Messenger、谷歌消息、Instagram、KakaoTalk、Line、Snapchat、Telegram、Viber、微信、WhatsApp、GroupMe、Kik、Skype、Discord、Signal、imo、ShareChat、Helo、威瑞森消息、Textra、Twitter、Hangouts、Slack 和 VSCO。

**新的相机模式**

我们一直在跟踪谷歌相机添加新的相机功能，7.5 版本添加了更多的相机模式模糊背后的代码名称。这些包括千层面，火影忍者，鲶鱼，和猫鲨。一旦我们确信我们确切地知道这些是什么，我们将让你知道。

* * *

*感谢 XDA 资深会员 [cstark27](https://forum.xda-developers.com/member.php?u=2712580) 对这些发现的协助，感谢 PNF 软件为我们提供使用许可**[JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev)**，这是一款针对 Android 应用的专业级逆向工程工具。*