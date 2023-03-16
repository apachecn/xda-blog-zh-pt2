# 通过将谷歌 Pixel 3 对接在 Pixel 支架上，谷歌助手的新用户界面

> 原文：<https://www.xda-developers.com/google-assistant-google-pixel-3-pixel-stand/>

谷歌将在一年一度的硬件盛会上发布 Pixel 3 和 Pixel 3 XL(尽管时间和地点与前些年不同)。)关于即将发布的谷歌 Pixel 3 XL，我们几乎没有什么不知道的[，这要感谢正在前往乌克兰和俄国的预生产单位。即使是 Pixel 3 XL 的小兄弟 Pixel 3，](https://www.xda-developers.com/google-pixel-3-xl-specs-features-pics-rumors/)[最近也出现在相机](https://www.xda-developers.com/google-pixel-3-leaked-photos/)上。我们几乎知道所有的[规格](https://www.xda-developers.com/google-pixel-3-xl-specs-features-pics-rumors/)、[设计](https://www.xda-developers.com/google-pixel-3-pixel-3-xl-renders-leak/)，甚至一些[新软件特性](https://www.xda-developers.com/google-pixel-3-xl-dual-front-camera-super-selfies/)。我们[早就怀疑](https://www.xda-developers.com/android-p-wireless-charging-dock-google-pixel-3/)谷歌 Pixel 3 系列将配备无线充电功能，而最新的泄露[证实了这一功能](https://www.xda-developers.com/google-pixel-3-xl-sample-photos-wireless-charging/)。我们还听说了一种可能的无线充电底座，称为“ [Pixel Stand](https://www.xda-developers.com/google-pixel-3-pixel-stand-wireless-charging-dock/) ”现在，我们已经成功激活了谷歌助手中的特殊用户界面，当你将谷歌 Pixel 3 或谷歌 Pixel 3 XL 插入 Pixel 支架时，它可能会启动。

## Pixel 支架中 Google Pixel 3 的 Google Assistant 停靠用户界面

这个新的用户界面，由 XDA 公认的开发者 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) ( [威武奎因应用](https://kieronquinn.co.uk/)的基隆·奎因)启用，当一个特殊的意图被发送到谷歌应用，并且“launched _ by _ dock”标志被设置为“真”时，这个用户界面就会被激活这与我们在 Android P beta 2 中发现的[“梦想飞机”无线充电底座支持](https://www.xda-developers.com/android-p-wireless-charging-dock-google-pixel-3/)以及我们在谷歌应用程序中发现的[像素支架字符串](https://www.xda-developers.com/google-pixel-3-pixel-stand-wireless-charging-dock/)非常吻合。提醒一下，以下是我们在谷歌应用 8.14 版本中发现的字符串:

```
 <string name="trusted_dock_action_text">I Agree</string>
<string name="trusted_dock_cancel_text">No thanks</string>
<string name="trusted_dock_message">Your Assistant can use your personal info to make suggestions, answer questions, and take actions for you when your phone is locked and on your Pixel Stand</string>
<string name="trusted_dock_title">Get personalized help when your phone is on your Pixel Stand</string> 
```

根据字符串，当谷歌 Pixel 设备对接时，谷歌助手可以提出个性化建议，回答问题，并做其他动作，即使手机被锁定。这意味着 dock 可以设置为受信任的设备，这样您就可以使用助理命令，否则当手机锁定且不在 dock 上时，您将无法使用这些命令。根据新界面的截图，当你将 Pixel 3 插入 Pixel 支架时，你可以看到以下内容:

*   天气信息
*   设置提醒
*   设置计时器
*   玩游戏
*   打电话
*   阅读我的信息
*   播放音乐
*   设置闹钟
*   设置计时器
*   播放新闻
*   探索新内容

下面是新界面的截图，由 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) 提供:

*注意:“confidental”水印是因为需要另一个标志来完成这项工作。启用该标志会将用户的谷歌账户贴满屏幕。这样做是为了防止谷歌应用程序 dogfooders 的泄露，Kieron 不是该应用程序的成员。*

请记住，我们使用谷歌应用程序的最新测试版激活了这个新的用户界面。谷歌可能会在推出 Pixel 3 和 Pixel Stand 之前添加更多功能或调整用户界面。如果我们发现 Google Assistant 的未来版本有任何变化，我们会通知大家。如果你有兴趣下载最新版本的谷歌应用，你可以从下面的 Play Store 链接下载。