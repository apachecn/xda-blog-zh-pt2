# ML 工具包中的 Google 数字墨水识别 API 支持手写和绘图识别

> 原文：<https://www.xda-developers.com/googles-digital-ink-recognition-api-ml-kit-enables-handwriting-drawing-recognition/>

大约一个月前，谷歌对其 ML Kit SDK (软件开发工具包)进行了一些重大的[改变，以使开发者更容易利用机器学习进行移动开发。该公司将 ML Kit 的设备上 API 从 Firebase 中分离出来，并在一个单独的 SDK 下提供它们，为所有 API 添加了](https://www.xda-developers.com/google-decouples-ml-kits-on-device-apis-from-firebase-and-introduces-early-access-apis/) [Android Jetpack 生命周期](https://developer.android.com/reference/androidx/lifecycle/Lifecycle)支持，并宣布了[早期访问计划](https://developers.google.com/ml-kit/early-access)，让开发者可以访问即将推出的 API 和功能。现在，该公司已经在 Android 和 iOS 上推出了数字墨水识别 API，允许开发人员创建使用手写笔和触摸作为输入的应用程序。

根据谷歌关于此事的博客文章，数字墨水识别 API 能够识别屏幕上的手写笔/触摸输入，并识别正在写的内容。该 API 使用了与 Gboard 应用上的手写识别相同的技术，以及谷歌的 [Quick，Draw！](https://quickdraw.withgoogle.com/)和[自动绘制](https://experiments.withgoogle.com/autodraw)实验。

随着数字墨水识别 API 的加入，开发人员现在将能够在他们的应用程序中实现这项技术，*“从让用户用手指或手写笔输入文本和数字到转录手写笔记以使其可搜索；这一切几乎都是实时的，而且完全在设备上完成。”*目前，数字墨水识别 API 支持超过 300 种语言和超过 25 种书写系统，包括所有主要的拉丁语言、中文、日文、韩文、阿拉伯文、西里尔文等。

除了手写，API 还将能够识别形状，它目前支持自动绘制草图识别器、表情识别器和基本形状识别器。谷歌声称，该 API 将能够在没有活跃的互联网连接的情况下完成所有这些工作。但是，用户需要下载一个或多个模型才能使用识别器。

如果你有兴趣使用新的数字墨水识别 API 为你的 Android 应用程序添加手写或形状识别功能，你可以点击[此链接](https://developers.google.com/ml-kit/vision/digital-ink-recognition)查看所有相关文档。如果你想看看 API 的运行情况，你可以看看这些用于 [Android](https://github.com/googlesamples/mlkit/tree/master/android/digitalink) 和 [iOS](https://github.com/googlesamples/mlkit/tree/master/ios/quickstarts/digitalinkrecognition) 的示例应用。

* * *

**来源:[谷歌开发者博客](https://developers.googleblog.com/2020/08/digital-ink-recognition-in-ml-kit.html)**