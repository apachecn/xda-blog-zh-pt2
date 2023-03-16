# 谷歌相机 7.1 暗示保存深度照片，揭示社交分享应用

> 原文：<https://www.xda-developers.com/google-camera-7-1-depth-photos-social-media-social-share-supported-apps/>

谷歌今天早些时候开始推出谷歌相机应用的 7.1 版本，它带来了新的用户界面、取景提示和社交分享功能。我们开始挖掘 APK，看看还有什么可能在工作中，我们发现了更多关于支持动态深度格式(DDF)的线索。我们还发现了新的社交分享功能支持哪些应用程序。这是我们的发现。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

**社交媒体深度特征**

Android 10 增加了对动态深度格式(DDF)的支持。DDF 文件包含您拍摄的照片的深度数据，因此应用程序可以在后期处理中更改模糊效果，而无需修改原始图像。在我们对[泄露的谷歌相机 7.0 狗粮版本](https://www.xda-developers.com/google-pixel-4-camera-features-google-camera-leak/)的拆解中，我们发现了 Pixel 4 将支持将深度数据保存为 DDF 文件，用于保存从前置和后置摄像头拍摄的照片。7.1 版的字符串显示了选择是否要在 DDF 文件中保存深度数据的首选项。这个名为“社交媒体深度功能”的偏好有一个描述，称该功能可以“被社交媒体应用程序使用”，尽管我们还不知道任何支持 DDF 的社交媒体应用程序。

```
 <string name="pref_depth_every_photo_summary">Depth data will be saved. This data may be used by social media apps. Motion photos will be turned off and photos may take longer to process.</string>
<string name="pref_depth_every_photo_title">Social media depth features</string> 
```

将深度数据保存在 DDF 文件中可能会在 Pixel 4 和 Pixel 4 XL 上首次亮相，但我们不知道它是否会在旧的 Pixel 智能手机上启用。在谷歌制造活动期间，我们应该在一周内了解更多信息。

**社交分享**

社交分享是一项新功能，我们最初是从新的 [Pixel Tips 应用](https://www.xda-developers.com/google-pixel-4-tips-pro-sessions-google-one-social-share-google-camera/)中了解到的。此功能可让您轻松分享最近拍摄的照片，只需在照片预览上向上滑动，并从三个选项中选择一个。

在设置中，我们注意到你可以选择你希望在社交分享快捷方式中显示的应用，但不清楚具体支持哪些应用。根据字符串，谷歌相机 7.1 目前支持 Discord、Facebook Messenger、Facebook Messenger Lite、Chat、Messages、GroupMe、Hangouts、Helo、Imo Messenger、Instagram Stories、KakaoTalk、Kik、LINE、ShareChat、Signal、Skype、Snapchat、Telegram、Textra、Twitter、威瑞森 Message+、Viber、微信和 WhatsApp。

```
 <string name="social_app_discord">Discord</string>
<string name="social_app_fb_add_story">Add to Your Story</string>
<string name="social_app_fb_messenger">Messenger</string>
<string name="social_app_fb_messenger_lift">Messenger Lite</string>
<string name="social_app_fb_your_story">Your Story</string>
<string name="social_app_google_chat">Chat</string>
<string name="social_app_google_messages">Messages</string>
<string name="social_app_groupme">GroupMe</string>
<string name="social_app_hangouts">Hangouts</string>
<string name="social_app_helo">Helo</string>
<string name="social_app_imo_messenger">Imo Messenger</string>
<string name="social_app_instagram_stories">Stories</string>
<string name="social_app_kakaotalk">KakaoTalk</string>
<string name="social_app_kik">Kik</string>
<string name="social_app_line">LINE</string>
<string name="social_app_sharechat">ShareChat</string>
<string name="social_app_signal">Signal</string>
<string name="social_app_skype">Skype</string>
<string name="social_app_snapchat">Snapchat</string>
<string name="social_app_telegram">Telegram</string>
<string name="social_app_textra">Textra</string>
<string name="social_app_tweet">Tweet</string>
<string name="social_app_verizon_messages">Message+</string>
<string name="social_app_viber">Viber</string>
<string name="social_app_wechat">WeChat</string>
<string name="social_app_whatsapp">WhatsApp</string> 
```

谷歌可能会在谷歌相机应用程序的未来更新中更新更多应用程序。到时候我们会通知你的。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*