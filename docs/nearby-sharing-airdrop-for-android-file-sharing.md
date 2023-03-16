# 首先看看附近的共享——谷歌的安卓隔空投送克隆版

> 原文：<https://www.xda-developers.com/nearby-sharing-airdrop-for-android-file-sharing/>

苹果的隔空投送功能已经成为生态系统协同的代名词，因为它使在苹果设备之间传输文件的任务变得微不足道，消除了依赖任何第三方解决方案的需要。在这一领域，即使是最好的 Android 手机也已经落后了，因为开源操作系统不得不依赖第三方解决方案来完成本地文件传输的任务。我们确实有 Android Beam 几年了，但这个功能没有得到充分利用和营销，最终，[弃用了](https://www.xda-developers.com/google-deprecate-android-beam-api-nfc-share-files/)。直到现在，一些主要的参与者才意识到要建立相互竞争的解决方案——[小米、OPPO 和 Vivo 已经联手开发了一个跨设备的文件传输解决方案](https://www.xda-developers.com/xiaomi-oppo-vivo-cross-device-file-transfers-protocol/)；三星也在以[快速分享](https://www.xda-developers.com/quick-share-samsung-alternative-airdrop-galaxy-phones/)的形式开发自己的解决方案；谷歌也在以[快速分享](https://www.xda-developers.com/fast-share-android-beam-airdrop-android/)的形式开发自己的解决方案，在即将发布之前，它最近被更名为[附近分享](https://www.xda-developers.com/fast-share-google-upcoming-airdrop-service-renamed-nearby-sharing/)。XDA 知名开发者 Quinny899 通知我们，他成功地在他的设备上激活了附近共享，允许我们自己激活它，并在谷歌正式发布之前一睹该功能的运行。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

在下面的视频中，我们测试了谷歌 Pixel 2 XL 和谷歌 Pixel 4 之间的无线文件传输，两者都运行 Android 10 但 Quinny899 展示了它在他的谷歌 Pixel 2 XL 和一加 7T Pro 之间的工作情况。因此，我们认为这项功能应该可以在预装 Google Play 服务的 Android 设备上普遍使用，尽管我们不能绝对肯定，直到谷歌翻转开关，为所有用户启用这项功能。

我在 Pixel 2 XL 上将联系人可见性设置为“隐藏”，所以每次我想接受 Pixel 4 的文件传输请求时，我都必须下拉 Pixel 2 XL 上的快速设置面板，并选择附近的共享快速设置磁贴。我首先将一张图片从我的 Pixel 4 传输到我的 Pixel 2 XL，然后在图片浏览器中打开它。然后，我将三个图像文件从我的 Pixel 4 传输到我的 Pixel 2 XL——在这种情况下，我无法在图像查看器中打开它们，但这些文件都存储在*/DCIM/nearly Sharing*中，这使它们易于访问。最后，我将一个视频文件从 Pixel 4 传输到 Pixel 2 XL。所有的传输都非常快，因为附近的共享使用 WiFi 进行文件传输。

在为所有支持 GMS 的设备发布附近共享服务之前，谷歌仍有一些粗糙的地方需要磨平。但是正如我们上面演示的，这个特性看起来已经准备好发布了。下个月，Android 可能会从没有第一方隔空投送竞争者变成至少有三个隔空投送竞争者。与三星和 OPPO-Vivo-小米的解决方案相比，谷歌的附近共享可能会更有优势，因为它在安卓设备上的普遍性，但其他公司也可以通过在 UX 和自己的应用程序之间进行更紧密和更突出的集成，为自己的服务提供优势。我们很快就会知道了。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*