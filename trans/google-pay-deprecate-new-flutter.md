# Google Pay 2.118 确认旧应用将被 Flutter 取代

> 原文：<https://www.xda-developers.com/google-pay-deprecate-new-flutter/>

上周，Google Pay 团队[宣布](https://www.xda-developers.com/google-pay-india-app-new-design-built-with-flutter/)Google Pay for India 应用程序(以前称为“Tez”)正在使用 Google 的开源 UI 开发套件 Flutter 进行重大设计重写。谷歌目前有两个版本的付费应用:一个面向全球用户，一个面向印度用户。在博客文章中，谷歌表示，他们“期待在 iOS 和 Android 上向世界各地的所有人推出 Google Pay on Flutter。”[一些](https://twitter.com/ArtemR/status/1307364493370908673)认为这意味着现有的面向全球用户的应用程序将通过 Flutter 重建，而[另一些](https://twitter.com/RonAmadeo/status/1307134808485703681)认为这意味着旧的应用程序将被淘汰。今晚，Google Pay 版本在 Play Store 上推出，它证实了后者将会发生。

用 Flutter 构建的新 Google Pay 应用。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

APK 中的字符串表示，将会有一个“弃用提示”，通知用户下载新版本的应用程序。

```
 <string name="deprecation_prompt_get_gp3">Get the new GPay</string>
<string name="deprecation_prompt_install_gp3">Download the new Google Pay</string>
<string name="deprecation_prompt_open_gp3">Open the new GPay</string>
<string name="deprecation_prompt_switch_to_gp3">Use the latest Google Pay</string> 
```

还有一项新活动，提供了更多关于应用迁移的详细信息。该屏幕告诉用户，他们将“仍然可以找到[他们]最喜欢的功能，加上跟踪消费，获得有用的见解，赚取独特的奖励，等等！”如果你点击底部的“获取新的 GPay”按钮，前 Google Pay for India 应用程序的 Play Store 列表将会启动。目前，新的应用程序仍然受到地区限制，所以我无法直接从 Play Store 下载到我自己的设备上。

旧:

新:

一旦谷歌开始提示用户迁移到用 Flutter 构建的新 Google Pay 应用，我们会让你们都知道。

*感谢 PNF 软件为我们提供了使用* *[JEB 反编译](https://www.pnfsoftware.com/?aid=xdadev)* *的许可，这是一款针对 Android 应用的专业级逆向工程工具。*