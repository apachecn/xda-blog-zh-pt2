# APK 的 Google Play 下载器浣熊现在支持应用捆绑包

> 原文：<https://www.xda-developers.com/raccoon-apk-downloader-google-play-app-bundle-support/>

在 [Google I/O 2018](https://www.xda-developers.com/tag/io-2018/) 期间，Google 推出了一个[新的应用打包模型，名为 Android App Bundles](https://www.xda-developers.com/android-app-bundle-google-play-dynamic-delivery-apk-size/) 。一个 [Android 应用捆绑包](https://developer.android.com/guide/app-bundle/)包含了该应用的所有编译代码和资源，但将 APK 的生成和签署推迟到 Google Play。谷歌 Play 商店通过动态交付服务模型，使用该应用捆绑包根据用户的设备配置生成和提供优化的 APK，确保用户仅下载应用在其特定设备上运行所需的代码和资源。

这种打包模式是为了方便那些必须处理大型 apk 的用户和开发人员，因为它致力于大幅减少应用程序的大小，以帮助提高数据敏感型市场的用户保留率。开发者不需要构建、签署和管理几个不同的 apk 来支持不同的设备配置，并且用户从更小和更优化的下载中受益。应用捆绑包和动态交付也使开发人员能够从核心应用功能中排除额外功能，并在以后需要时下载额外功能。

虽然应用捆绑和动态交付将为大量 Android 用户带来好处，但它们确实给在谷歌 Play 商店以外分发应用带来了一定的困难，也就是侧装。 [*Android Police* 有一篇很好的文章](https://www.androidpolice.com/2018/05/30/android-app-bundles-dynamic-delivery-will-change-way-phone-gets-software/)详细描述了这些变化对侧装的影响，因为它影响了他们的姐妹网站 *APKMirror* 处理应用分发的方式。

[浣熊](https://raccoon.onyxbits.de/)，一个 APK 下载器，可以让你直接下载 Google Play 应用到你的桌面，现在已经被[更新到 4.40](https://raccoon.onyxbits.de/content/440) ，支持 Android 应用捆绑。浣熊具有围绕谷歌 Play 商店访问的广泛功能，例如下载免费和付费应用程序的能力，绕过设备和国家限制，以及直接将应用程序安装到您的设备的 ADB 集成。

4.4.0 版的变更日志如下:

*   增加了对谷歌新发布格式的支持:应用捆绑包
*   增加了下载助推器功能，以减少下载时间
*   如果无法从 APK 中提取应用程序图标(例如，因为它是捆绑的应用程序)，请使用 Play 中的应用程序图标。
*   再次改变默认设备配置文件以支持应用程序捆绑包。

请注意，只有通过 ADB 才能安装应用捆绑包，因为这是 Android 固有的限制。

* * *

[**来源:浣熊**](https://raccoon.onyxbits.de/content/440)