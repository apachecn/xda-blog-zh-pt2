# Android 应用捆绑包和 Google Play 动态交付将减少应用大小，有助于提高用户留存率

> 原文：<https://www.xda-developers.com/android-app-bundle-google-play-dynamic-delivery-apk-size/>

作为一个开发者，你要尽你所能来提高用户留存率。保持尽可能低的安装卸载率对于你的应用程序获得高排名是非常重要的。随着谷歌继续向印度和多个非洲国家等市场扩张，每年都有数百万新用户加入 Android 生态系统。这些新兴市场的用户往往比大多数人更注重数据，所以你可能甚至没有意识到，你的 APK 尺寸已经变得太大，无法吸引这些用户。这就是为什么谷歌推出了一种新的 Android 应用模型，称为 Android 应用捆绑包。再加上新的 Google Play 动态交付，应用程序大小可以大幅减少，以帮助提高关键市场的用户保留率。

* * *

## 通过 Android 应用捆绑包和 Google Play 动态交付减少 APK 大小

如果您正在构建一个旨在提供与 Android 设备最大兼容性的应用程序，这意味着您需要构建所有外形规格，包括 Android 智能手机、平板电脑和 Chromebooks，以及所有硬件架构，包括 ARM、ARM64 和 x86。您还需要创建多种布局来适应屏幕分辨率、宽高比和密度的多样性。为了给不同地区的用户提供最佳体验，你还需要[将你的应用翻译成多种语言](https://www.xda-developers.com/reviewing-app-translation-services-how-to-make-your-app-truly-global/)。将所有这些放在一起会导致一个庞大、臃肿的 APK，其中包含大量与大多数用户无关的资源。当然，您可以为每种架构、外形、布局等提供不同的 apk。让 Google Play 来处理为用户提供哪个版本的服务，但最终用户还是会安装包含不必要资源的应用。

借助名为 Android App Bundle 的新应用模型，您可以为每台设备捆绑应用所需的一切。只需将你的应用上传到 [Google Play 开发者控制台](https://www.xda-developers.com/google-play-store-developers-internal-test-channel/)并点击“创建捆绑包”就这么简单！然后，由于 Google Play 动态交付，*只有*与用户特定设备相关的资源和代码才会被提供。例如，如果主要语言是法语的用户下载了您指定了法语语言字符串的应用程序，那么动态交付将提供法语翻译，而不是包含所有语言的 APK。这可能会极大地减少总的下载和安装大小。我们被告知 [LinkedIn](https://play.google.com/store/apps/details?id=com.linkedin.android) 的应用程序大小减少了 23%,而 [Twitter](https://play.google.com/store/apps/details?id=com.twitter.android) 减少了 35%。

Android 应用捆绑包也是模块化的，因此您可以按需提供功能，而不是在安装过程中提供。这要求你加入 [Google Play 动态交付](http://g.co/play/dynamicdeliverybeta)的测试版，并下载最新的 [Android Studio](https://www.xda-developers.com/tag/android-studio/) 3.2 Canary 版本，在[谷歌 Play 商店](https://www.xda-developers.com/tag/google-play-store/)上发布你的应用。你将通过应用捆绑和动态交付节省的数据量将取决于你提供的应用变体的数量和你与应用捆绑的资源的种类，但鉴于谷歌让开发者能够轻松减少 APK 规模，如果你想吸引更多来自新兴市场的用户，你应该尽快利用新工具。