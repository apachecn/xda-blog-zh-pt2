# 随着 Galaxy A50s、A90 和 Tab S6 获得支持，ROG Phone II、Redmi K20 Pro、Xperia 5 等将很快正式支持谷歌的 AR 服务

> 原文：<https://www.xda-developers.com/google-play-services-for-ar-rog-phone-ii-redmi-k20-pro-xperia-5-realme-5-galaxy-a50s-a90-tab-s6/>

Google Play Services for AR，以前称为 ARCore，是一款为开发者提供 SDK 的应用程序，用于将增强现实体验构建到他们的应用程序中。我们已经在 Google Play 上看到了许多使用该 SDK 构建的应用，从 [AR 购物应用](https://www.xda-developers.com/google-pixel-ar-google-shopping-hands-on/)到 AR 测量应用到 [AR 导航应用](https://www.xda-developers.com/google-maps-ar-navigation-timeline-sharing-features/)。使用这个 SDK 构建的功能越多，设备支持它就越重要。谷歌与原始设备制造商合作，校准每台设备上的摄像头和传感器，以确保用户获得最佳的增强现实体验。当一个设备支持谷歌的 AR 服务时，它会被添加到谷歌的“ [ARCore 支持的设备](https://developers.google.com/ar/discover/supported-devices)”列表中。上周，3 款新的三星设备被添加到该列表中，但我们也知道其他一些设备也将获得对 ARCore 的官方支持。

谷歌网页上列出的设备可以从谷歌 Play 商店下载用于 AR 的 Google Play 服务，如果它还没有自动安装的话。受谷歌 AR 服务支持的设备(如，它们已经完成了必要的校准，并被应用程序识别)但没有列在谷歌的网页上，不能从 Play Store 下载应用程序，但仍然可以为 AR 下载 Play 服务，然后玩使用该服务的应用程序。如果用户试图运行任何使用 AR 播放服务的应用程序，既没有在线列出也没有正确校准的设备将面临错误。

谷歌官方将[三星 Galaxy A50s](https://www.xda-developers.com/samsung-galaxy-a50s-a30s-announced/) 、[三星 Galaxy A90 5G](https://www.xda-developers.com/samsung-galaxy-a90-5g-snapdragon-855-dex-launched/) 、[三星 Galaxy Tab S6](https://forum.xda-developers.com/galaxy-tab-s6) 列为支持 AR 的 Play 服务，因此您可以下载并安装任何依赖于 AR 服务的应用程序，没有任何问题。然而，AR APK 的最新 Play 服务版本 1.12 现已在 APKMirror 上提供，它现在包含以下智能手机的正确校准:

我在我自己的 ROG 手机 II 上证实，为 AR 和使用该服务的应用程序(如 [Just a Line](https://www.apkmirror.com/apk/google-creative-lab/just-a-line-draw-anywhere-with-ar/just-a-line-draw-anywhere-with-ar-2-1-4-release/just-a-line-draw-anywhere-with-ar-2-1-4-android-apk-download/) )侧装 Google Play 服务现在可以工作，而在以前的 APK 上则不能工作。我还问了两位 Redmi K20 Pro 用户，以确认他们的设备上也可以使用相同的功能。

 <picture>![Google Play Services for AR working on Redmi K20 Pro](img/a7fcec888f283db87af46b9f9273d537.png)</picture> 

"Just a Line" app powered by Google Play Services for AR running on the Redmi K20 Pro. Screenshot courtesy of @GodsAmongU on Telegram.

因此，尽管这些设备还没有被正式添加到谷歌的 ARCore 支持设备列表中，但一旦谷歌将它们列入 Play Store 的白名单，它们应该很快就会获得官方支持。当谷歌更新列表以包括这些设备时，我们会通知您。