# 谷歌推出了 Play Billing Library 第 3 版，并计划在 2021 年将应用捆绑包作为一项要求

> 原文：<https://www.xda-developers.com/google-play-billing-v3-app-bundle-requirement-2021/>

应用内购买。尽管有些人可能讨厌它们，但它们肯定会继续存在。不过，它们也不是没有优势。应用内购买允许开发者提供其应用的免费和付费版本，而实际上不必维护两个独立的应用。如果你在 Play Store 上发布你的应用，谷歌通常要求你的应用内购买通过他们(因为他们得到 30%的提成)。

值得庆幸的是，谷歌确实让设置应用内购买变得非常容易，它提供了所有有趣的东西，比如许可证验证。开发者可以简单地实现 Google Play 计费库，而且他们已经做好了准备。为了让应用内购买变得更加容易， [Google 发布了](https://android-developers.googleblog.com/2020/06/meet-google-play-billing-library.html)Play 计费库的第 3 版，增加了一些新功能和改进，同时也有一项重要的政策变化。

## Google Play 计费库 v3 -有什么变化

**现金支付**

谷歌 Play 计费库的第三版允许用户用现金支付。这听起来可能很奇怪，但可能不是你想的那样。世界上仍有许多地方信用卡和银行账户并不普遍。此功能旨在解决此问题。

你可以选择用现金支付，而不是点击应用程序中的“购买”按钮并用信用卡支付。一旦你确认购买，谷歌会向你显示一个代码。将该代码带到最近的参与便利店，给他们适量的现金，然后您的购买将被解锁。

目前，该功能仅在印度尼西亚和马来西亚推出，但计划在更大范围内推广。开发者也将很快能够将这种支付方式添加到他们的应用程序中。

**更轻松的促销代码兑换**

开发者可以选择为他们的应用提供推广代码。如果是付费应用，推广码可以让用户免费获得应用。如果应用程序有应用内购买或订阅，促销代码可以提供免费项目或免费订阅试用。虽然可以直接在 Play Store 中兑换应用推广代码，但要兑换订阅试用版，您之前必须下载应用。

不过现在，Google Play 计费库版本 3 增加了直接从 Play Store 兑换应用内促销的功能；用户甚至不需要下载他们申请的应用程序。

**购买归属**

如果一个应用程序或游戏有一堆你可以在里面购买的不同东西，开发者需要一些方法来跟踪谁购买了什么。在此之前，开发人员必须使用现已废弃的 AIDL 框架来构建自定义解决方案。然而，在 Google Play 计费库第 3 版中，现在有了对购买属性的原生支持，允许开发者轻松跟踪购买了什么。

**库版本需求**

如果你正在阅读这篇文章，你可能知道 Google Play 在商店发布的最低 SDK 版本要求。目前，[应用必须至少以 API 28](https://www.xda-developers.com/all-apps-require-target-android-pie-play-store/) (Android Pie)为目标才能在 Google Play 上发布，并且这一要求每年都在增加。

现在对实现 Google Play 计费库的开发人员也有类似的要求。要在 Play Store 上发布使用此库的应用程序，它需要使用相对较新的版本。目前，所有版本的 Play Billing Library 都是允许的，但从 2021 年 8 月 2 日开始，所有新发布的应用程序都必须至少使用版本 3。现有的应用程序将在 2021 年 11 月 1 日之前升级。

**迁移指南**

由于现在要求使用新版的 Play Billing 库，Google 发布了一个迁移指南来帮助开发者更新。本指南展示了如何实现该库的最新版本，以及开发人员需要做哪些更改才能使用它。

你可以点击查看迁移指南[。如果对你有帮助的话，还有一个](https://developer.android.com/google/play/billing/migrate)[视频指南](https://www.youtube.com/watch?v=Cj5vq1AOJeQ)。

这就是目前关于新的 Google Play 计费库的内容。如果你实现了应用内购买，并且你的应用在谷歌 Play 商店上，你可能应该考虑更新你的账单库实现，如果你还没有的话。

## 2021 年新发布应用的强制安卓应用捆绑包

*米沙·拉赫曼的章节*

在 Google I/O 2018 上， [Google 推出了](https://www.xda-developers.com/android-app-bundle-google-play-dynamic-delivery-apk-size/)一种替代的应用分发格式，称为 Android 应用捆绑包，文件扩展名为. aab，Android 应用捆绑包的目标是减少最终 Android 应用包的文件大小(。apk)交付给用户，减少了用户的安装大小和下载时间。的。aab 文件包含基本应用程序和所有支持的架构(ARM、ARM64 和 x86)、语言和布局变体的 APK 文件。这种格式要求向 Google 提供一份应用程序签名密钥的副本，以便 Google Play 开发者控制台可以生成一个捆绑包，其中包含每个 APK 的签名版本；特定设备的架构、语言和布局的正确 APK 通过 Google Play 动态交付交付。

开发者可以在 [Android Studio、Unity](https://www.xda-developers.com/google-announces-improvements-app-bundles-instant-apps-tools/) 或 [Flutter](https://www.xda-developers.com/flutter-1-7-androidx-android-app-bundles/) 中部署 Android 应用捆绑包，虽然支持安装 APK 大小高达 500MB 的大型应用捆绑包，但不支持 OBB 文件。作为替代方案，谷歌最近扩展了 Android 应用捆绑包，推出了[游戏资产交付](https://www.xda-developers.com/google-for-games-new-developer-tools-play-firebase-android-studio/)，供游戏开发者动态交付大型游戏资产。在所有这些改进的背景下，谷歌现在计划将 Android 应用捆绑包作为谷歌 Play 商店新发布应用的一项要求。

在 Android 开发者 YouTube 频道上周发布的“[Google Play 新功能](https://www.youtube.com/watch?time_continue=320&v=cMr-b660Esw&feature=emb_logo)”视频中(via[*AndroidPolice*](https://www.androidpolice.com/2020/06/12/google-play-store-will-make-app-bundles-a-requirement-in-2021/))，谷歌人米莲娜·尼科利茨宣布，Google Play 上的新应用将需要应用捆绑支持。这项新要求没有给出具体的日期，尽管我们知道它将在 2021 年的某个时候发生。

大多数开发人员和最终用户不会注意到这个新需求带来的任何变化，但这并不意味着没有人会注意到。开发人员将不得不把他们的签名密钥副本交给谷歌，让他们签署应用程序，这可能会让一些开发人员感到不安。aab 的进一步扩散将使在不同平台上的再分发更加困难，减少下载量，从而减少潜在的广告收入。(对于开发者来说，他们可以使用谷歌的开源 [bundletool](https://github.com/google/bundletool) 来构建自己的 aab，提取出来，然后上传到其他平台。)用户也很难手动侧装 aab，因为 Android 的软件包安装程序本身不支持 aab，必须将其解压缩。

随着 2021 年的临近，我们有望了解更多关于这一新要求的信息。