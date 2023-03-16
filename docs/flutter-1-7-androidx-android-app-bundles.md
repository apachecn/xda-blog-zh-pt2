# Flutter 1.7 为新的 Android 应用程序、Android 应用程序捆绑包等带来了 AndroidX 支持

> 原文：<https://www.xda-developers.com/flutter-1-7-androidx-android-app-bundles/>

Flutter 是发展最快的移动应用开发框架之一。它的 GitHub 知识库中有将近 70，000 颗星星，并被该领域的软件工程师广泛采用。开发团队正在努力解决任何问题，事实证明，自从[发布 Flutter 1.5](https://www.xda-developers.com/flutter-1-5-support-web-embedded-desktop/) 以来，他们在过去的两个月中关闭了超过 1250 个报告。现在，被 Flutter 的产品经理 Tim Sneath 称为优化更新的 1.7 版本已经正式发布。

## android 对新应用的支持

从 1.7 开始，Flutter 现在支持 AndroidX 支持库，这是去年[引入](https://www.xda-developers.com/android-jetpack-components-kotlin-android-studio-3-2/)Android 开发平台的。AndroidX 旨在允许开发人员使用最新的组件，同时保持向后兼容性。谷歌还[开源了它](https://www.xda-developers.com/googles-androidx-aosp/)，这样开发者就能保持最新版本。由于很多 Flutter 的包现在已经被更新以支持 Android，开发团队决定允许用 Android 创建新的 Flutter 项目。您所要做的就是将`--androidx`标志添加到您的项目中，以指向支持库。关于迁移现有项目的文档可以在[这里](https://flutter.dev/docs/development/packages-and-plugins/androidx-compatibility#for-plugin-maintainers-migrating-a-flutter-plugin-to-androidx)找到。

## Android 应用捆绑包(AAB)支持

距离谷歌完全停止在 Play Store 上提供 32 位原生应用还有两年多一点的时间，但其他一些限制很快就会发生。从今年 8 月 1 日开始，所有使用原生库和针对 Android 9 Pie 或更高版本[的应用将被要求提供](https://www.xda-developers.com/google-play-stop-serving-native-apps-without-64-bit-cpu-support/) 64 位支持。Flutter 已经支持生成 64 位 Android 应用程序，但该框架的 1.7 版本现在允许开发人员使用 32 位和 64 位版本的应用程序创建 [Android 应用程序捆绑包](https://www.xda-developers.com/android-app-bundle-google-play-dynamic-delivery-apk-size/)。这将使使用 Flutter 的原生应用程序开发者更容易同时支持 32 位和 64 位，以满足 8 月 1 日的最后期限，然后最终在 2021 年放弃 32 位支持。在这里你可以找到发布安卓应用捆绑包的[指令](https://flutter.dev/docs/deployment/android#how-do-i-build-a-release-from-within-android-studio)，以及为 32 位和 64 位设备生成不同 APK 文件的指令。

虽然 Flutter 的目标是成为一个一体化的跨平台开发框架，但它主要专注于支持移动操作系统。这就是为什么该团队不断添加新的小部件和组件，以满足移动应用程序开发人员和 UI 设计人员的幻想。颤振 1.7 在这方面没有什么不同。有一个新的 [RangeSlider](https://github.com/flutter/flutter/pull/31681) 材质值组件，用于设置最小值和最大值之间的范围。Android 用户也将在 Flutter 应用程序中获得更新的 [SnackBar](https://github.com/flutter/flutter/pull/31275) 小工具。iOS 的小工具 Cupertino 也更新了改进的 [CupertinoPicker 和 CupertinoDateTimePicker](https://github.com/flutter/flutter/pull/31464) 小工具。

Flutter 第一次获得了对游戏控制器的支持。尽管目前在 Flutter 上编写一个完整的游戏并不容易，但它仍然有潜力。这个[平台设计样本](https://github.com/flutter/samples/tree/master/platform_design)告诉开发者如何为同时适应 iOS 和 Android 设计语言的组件编写代码。还有一个新的 fontFeatures 属性，它允许开发人员为特定的字体定义特定的样式。你可以在 [Flutter API 目录](https://api.flutter.dev/flutter/dart-ui/FontFeature-class.html)中看到该属性的所有用例。

这基本上是这个版本。正如你所看到的，自 Google I/O 以来，该团队没有添加太多新功能。他们主要专注于完善和添加对关键 API 和基本应用程序库的支持。

要更新到 1.7 版本，请使用 cd 进入 Flutter 目录的根目录，并执行`flutter upgrade`命令。如果你想手动升级或重新安装框架，Flutter 1.7 也可用于新安装的。

* * *

**来源:** [**蒂姆·斯奈思/中**](https://medium.com/flutter/announcing-flutter-1-7-9cab4f34eacf)