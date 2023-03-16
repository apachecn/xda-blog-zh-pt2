# 谷歌镜头可能很快会帮你做作业

> 原文：<https://www.xda-developers.com/google-lens-education-mode-homework-help-offline-translation/>

谷歌镜头是谷歌的图像识别服务，根据你的相机指向的任何东西，从谷歌搜索中传递信息。去年 5 月，谷歌[重新设计了该服务的 Android 版本](https://www.xda-developers.com/google-search-google-lens-augmented-reality-features/)，将用户界面分为 5 种不同的扫描模式:翻译、文本、搜索、购物和餐饮。在包含镜头服务的谷歌应用程序的 11.3.7.29 版本中，我们发现谷歌正在开发第六项服务:教育。我们还了解到，谷歌正准备允许你在离线时使用 Lens 的翻译模式。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

**离线翻译**

谷歌应用 11.3.7.29 的新字符串显示，你可以下载语言包，这样你就可以在没有互联网连接的情况下使用 Lens 翻译文本。这些字符串没有透露将支持哪些语言，但你可能可以下载谷歌镜头已经支持的大多数语言。值得注意的是，谷歌翻译应用在其“相机”模式下支持[离线翻译，这在功能上与 Lens 中的翻译模式非常相似。](https://www.xda-developers.com/google-translate-instant-translation-automatic-language-detection-camera-mode/)

```
 <string name="lens_translate_cancel_language_pack_download_dialog">Cancel download of the %1$s offline package?</string>
<string name="lens_translate_cancel_language_pack_no">No</string>
<string name="lens_translate_cancel_language_pack_yes">Yes</string>
<string name="lens_translate_download_language_pack_dialog">Translate even when you are offline by downloading the %1$s translation file (%2$s)</string>
<string name="lens_translate_download_language_pack_dialog_title">Translate %1$s offline</string>
<string name="lens_translate_download_language_pack_tooltip">Tap to download offline translations</string>
<string name="lens_translate_download_language_pack_yes">Download</string>
<string name="lens_translate_remove_language_pack_dialog">If you remove this offline translation file, this language will be unavailable for offline translation.</string>
<string name="lens_translate_remove_language_pack_yes">Remove</string>
<string name="lens_translate_space_remaining_dialog">%1$s storage available</string> 
```

**教育模式**

接下来是一个新的“教育”模式，我们设法简单地浮出水面。这种“教育”模式的描述告知用户“指向[一个]家庭作业问题以获得帮助。”遗憾的是，我们无法测试这项功能，但对谷歌应用程序代码的简要分析显示，你可以使用教育模式来扫描数学问题。不过，我们不知道教育模式是否能支持复杂的数学问题。

你可以通过抓取谷歌应用程序的最新测试版来下载最新版本的谷歌镜头服务。谷歌 Play 商店的 Lens 应用程序只是启动这项服务的快捷方式，而不是一个独立的应用程序。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*