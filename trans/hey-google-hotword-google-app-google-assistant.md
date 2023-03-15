# 谷歌应用程序暗示“嘿谷歌”热门词汇将出现在手机上的谷歌助手中

> 原文：<https://www.xda-developers.com/hey-google-hotword-google-app-google-assistant/>

**2017 年 10 月 20 日**更新:一些用户报告称该功能即将推出。这些用户报告说，他们看到一个通知，告诉他们用“嘿谷歌”重新训练他们的热门词汇检查您的通知，看看该功能是否适合您！

谷歌 Pixel 2 和谷歌 Pixel 2 XL T1 仅在 10 天前正式宣布，虽然它们还没有到达消费者手中，但它们已经在美国各地的威瑞森无线商店展示。我们一直在挖掘 Pixel 2 的系统应用程序，为您带来最新的 [Pixel Launcher](https://www.xda-developers.com/get-google-pixel-2-pixel-launcher-bottom-search-bar/) 和 [Google Camera](https://www.xda-developers.com/download-google-camera-motion-photo/) 应用程序，但我们也一直在寻找更多隐藏的方面，如[黑暗快速设置主题](https://www.xda-developers.com/hidden-dark-theme-google-pixel-2/)和[蓝牙电池电量报告的证据](https://www.xda-developers.com/google-pixel-2-adds-bluetooth-battery-level-reporting/)。Pixel 2 上预装的大多数谷歌应用程序都不是新的，只有一个明显的例外——谷歌应用程序。谷歌应用程序的 7.3.28.21 版本只能在 Pixel 2/Pixel 2 XL 上找到，它暗示**“嘿谷歌”热词检测将在手机上的谷歌助手中出现。**

虽然 APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都有可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

* * *

## “嘿谷歌”热门词汇检测即将来到谷歌助理

目前智能手机上能触发谷歌助手的热词只有一个。你必须说“Ok Google”才能让助手开始听。你们中的许多人可能已经习惯了这个热门词汇，但对于我们中的许多拥有 Google Home 设备的人来说，还有另一种方式来激活 Assistant。另一个只在谷歌家庭设备上可用的热门词汇是“嘿谷歌”就我个人而言，我认为这个热门词汇更自然地脱口而出，所以我只说“嘿谷歌”来唤醒我的谷歌主页。

这就是为什么我很兴奋地在 Pixel 2 上的最新谷歌应用程序版本中找到以下字符串:

```
 <string name="hotword_enrollment_summary_text_screen_assistant_device">Your Assistant can now recognize your voice when you say \"%1$s\" or \"%2$s\".</string>
<string name="hotword_enrollment_summary_usage_example_first">"Ok Google, what's my name?"</string>
<string name="hotword_enrollment_summary_usage_example_second">"Hey Google, what's the traffic to work?"</string>
<string name="hotword_enrollment_summary_usage_example_third">Ok Google, tell me about my day.</string> 
```

正如你所看到的，该应用程序宣传说，当你说出两个热门词汇中的一个时，Assistant 可以识别你的声音。这两个热门词汇将在接下来的几行中详细阐述:“Ok Google”或“嘿 Google”

将此与 Play Store 上现有的 Google app 版本中的相同系列进行比较:

```
 <string name="hotword_enrollment_summary_text_screen_assistant_device">Your Assistant can now recognize your voice.</string>
<string name="hotword_enrollment_summary_usage_example_first">"%1$s, what's my name?"</string>
<string name="hotword_enrollment_summary_usage_example_second">"%1$s, what's the traffic to work?"</string>
<string name="hotword_enrollment_summary_usage_example_third">%1$s, tell me about my day.</string> 
```

之前，该应用程序只告诉你一个热门词汇就可以唤醒助手(我们知道这是“Ok Google”)。

我还无法确认“嘿，谷歌”热词检测是否真的可以在最新版本的谷歌应用程序上启用。这是因为，不幸的是，我从 Pixel 2 中提取的谷歌应用程序版本不完整——我还需要获取 odex 文件。此外，威瑞森的演示单元显然不允许我添加谷歌账户，所以我无法在商店里训练谷歌助手来查看“嘿谷歌”是否是一个可接受的短语。

一旦我得到了谷歌 Pixel 2 XL，我一定会让你们知道，如果你真的可以使用“嘿谷歌”来与你的手机交谈。