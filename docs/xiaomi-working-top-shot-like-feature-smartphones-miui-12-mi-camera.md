# 小米可能正在开发类似谷歌相机的 Top Shot 功能

> 原文：<https://www.xda-developers.com/xiaomi-working-top-shot-like-feature-smartphones-miui-12-mi-camera/>

小米的 MIUI 用户体验“皮肤”给了其手机独特的体验，尽管它以 Android 为基础。该公司目前正在为其手机产品线推出 MIUI 12 稳定版，它肯定让其用户群兴奋不已，因为这标志着 MIUI 体验的[体面提升](https://www.xda-developers.com/miui-12-hands-on-new-features-added-xiaomi-android/)。小米相机应用是 MIUI 体验的亮点之一，最近增加了一些显著的功能，如[魔法克隆](https://www.xda-developers.com/xiaomi-miui-12-beta-magic-clone-miui-camera/)和[全屏手势支持](https://www.xda-developers.com/xiaomi-miui-camera-app-full-screen-gesture-support-miui-12-beta-builds/)。小米正在开发更多功能，其中一项叫做 AI Shutter，似乎模仿了与 Top Shot 类似的功能。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

在 MIUI 相机应用程序中发现的来自最近 [MIUI 12 中国测试版](https://www.xda-developers.com/download-miui-12-closed-beta-xiaomi-redmi-devices/)的字符串表明小米正在开发自己的 Top Shot 实现。 [Top Shot](https://www.xda-developers.com/sideload-pixel-3-google-photos-top-shot-pixel-2/) ，在谷歌 Pixel 设备上看到的，快速拍摄一组图像，然后利用机器学习指出系列中的最佳镜头。这种最佳拍摄通常是对象微笑、眨眼和/或看着相机的情况。这减轻了拍摄时机的压力，让最终用户更有信心拍摄出有用的图像。

```
 <string name="pref_camera_ai_shutter_description">Select best moment automatically when pressing the shutter button</string>
<string name="pref_camera_ai_shutter_title">AI shutter</string> 
```

小米的实现暂定名为“人工智能快门”，它的目标是做同样的事情。当你按住快门按钮时，手机会自动从一系列照片中选择一张好照片。字符串中的语法是不正确的，因为它们是从中文翻译过来的，但函数背后的一般思想似乎与 Top Shot 相同。该功能可能会作为一个选项来实现，因此如果您希望保留对拍摄内容的完全控制，您仍然可以这样做。

像 MIUI 图库中的[天空替换这样的功能已经得到了社区的好评，所以我们很好奇小米对 AI 快门的实现有多好。如果做得好，它可以降低点击适时照片的门槛，让普通消费者更容易获得。该功能尚未在 MIUI 12 测试版中上线，但我们会密切关注它何时出现。](https://www.xda-developers.com/xiaomi-testing-sky-replacement-feature-miui-gallery/)

* * *

*感谢@Deiki on Telegram 的提示！*