# 谷歌推出了 Flutter 1.2 和 Dart DevTools，这是一套基于网络的编程工具

> 原文：<https://www.xda-developers.com/google-launches-flutter-1-2-dart-devtools/>

Flutter 是应用开发者的最新武器之一。这是一个 UI 框架，使用 Dart 语言在 iOS 和 Android 上构建漂亮、流畅和交互式的跨平台原生应用。第一个稳定的跨平台开发工具包发布于[三个月前](https://www.xda-developers.com/flutter-1-0-is-now-available-stable-native-cross-platform-development/)。今天，谷歌在世界移动通信大会上宣布了第一个为 Flutter 更新的功能，Flutter 1.2，以及一个新的基于网络的编程工具套件，名为 Dart DevTools。

与它的替代品相比，Flutter 最大的优势之一就是开发社区。Flutter 是开源的，因此您可以看到它是如何构建的，并为其开发提出建议。Google 一直致力于提高框架的稳定性和性能，同时也增加了一些有趣的开发工具。

颤振团队努力工作，以像素完美的设计组件。他们更新了 Material 和 Cupertino 小部件集。在 iOS 端，他们在编辑文本的同时加入了[浮动光标支持](https://github.com/flutter/flutter/pull/25384)。该团队解释说，他们确保考虑到动画和绘画组件应该如何在系统上呈现的所有次要细节。一套受[罗伯特·彭纳启发的](http://robertpenner.com/easing/)动作和动画功能也出现在了 Flutter 1.2 中。显然，该团队还在为即将到来的键盘事件和鼠标悬停支持的桌面支持做准备。

## 更多插件

Flutter 团队也一直在努力添加新的插件，以使框架更加完整。最大的增加是支持应用内购买。从 Flutter 1.2 开始，所有开发人员都可以将 IAP 购买集成到他们的应用程序中。还修正了[视频播放器](https://pub.dartlang.org/packages/video_player)、[网络视图](https://pub.dartlang.org/packages/webview_flutter)和[地图](https://pub.dartlang.org/packages/google_maps_flutter)的错误。得益于 Intuit 开发者的拉取请求，Android 应用捆绑包也已经推出。所有这些额外的特性将帮助你构建完美的 Flutter 应用，而不依赖于其他框架和 SDK。

## Dart 2.2 SDK

在 Flutter 1.2 中也引入了 Dart 2.2。最新版本的编程语言带来了大量的性能改进和新的语言支持。Dart 更新版本的细节还不清楚。当有更多可用的细节时，我们将确保让您知道。Dart 2.2 SDK 现已正式发布。它包括改进的 AOT 编译器性能和一些新特性。

根据[发布的博客文章](https://medium.com/dartlang/announcing-dart-2-2-faster-native-code-support-for-set-literals-7e2ab19cc86d)，虽然 Dart 2.1 引入了针对 JIT(实时)和 AOT(提前)编译代码的性能优化，但 Dart 2.2 主要关注 AOT。他们承诺以代码长度增加 1%为代价，性能提高 11-16%。减少静态调用的开销也有助于使 Flutter 应用程序更加直观。Dart 2.2 还包括对地图、列表和集合的更新的文字语言支持。这一增加应该有助于您编写更有吸引力的代码。 [Dart 语言规范](https://www.dartlang.org/guides/language/spec)也随着 Dart 2.2 版本进行了更新。

还有更多的更新。你可以在[中的博文](https://medium.com/dartlang/announcing-dart-2-2-faster-native-code-support-for-set-literals-7e2ab19cc86d)中看到所有相关细节。Dart 2.2 作为 Dart 2.1.2 包含在 Flutter 1.2 中，所以如果您偶然发现一个稍微不同的版本号，请不要混淆。

Flutter 的写法有很多种。你可以使用官方支持的 Android Studio 和 Visual Studio 代码，或者任何其他 IDE，如果你愿意到处安装一些插件的话。谷歌的开发团队一直致力于为 Flutter 带来另一个官方解决方案。Dart DevTools 是一个基于 web 的编程套件。它旨在减轻调试和分析应用程序代码的痛苦。你可能已经知道了，Flutter apps 是用 Dart 编程语言编写的，所以 Dart DevTools 支持两个平台。该套件还将与 Android Studio 和 Visual Studio 代码高度集成，以满足您的所有写作需求。

Dart DevTools 有几个有趣的新特性。它们都没有突破性或创新性，但它们能帮助你更轻松地完成工作。首先，该套件使您能够检查小部件，探索应用程序中所有元素的层次结构。想想类似于 IDE 的“检查元素”浏览器工具。这个特性在 [DartConf 2018](https://www.youtube.com/watch?v=JIcmJNT9DNI) 中首次显露。下面是 Android Studio 中运行的 widget inspector 的参考 GIF。该功能的网页版看起来会略有不同。

基于 web 的编程套件的下一个特性是时间轴视图。它将帮助开发人员逐帧分析和诊断他们的应用程序。这将有利于他们识别讨厌的错误和图形故障。然后是源代码级调试器。它拥有所有必需的特性，比如断点和时间戳，可以帮助你及时有效地跟踪代码中的问题。还有一个日志视图，它记录应用程序的每一个活动，无论是网络/框架级的活动还是垃圾收集事件。

这些只是 Dart DevTools 目前的功能。Flutter 的开发团队承诺，他们将定期更新该套件，增加更多功能，使其成为“Flutter 开发者的一流统一工具”该团队在 wiki 中清晰地记录了他们的 [2019 年路线图，这让我们所有人都可以一窥未来。他们还透露，他们将更加关注“蜂鸟”，这是一个承诺在网络上运行 Flutter 的项目。该平台的第一个技术预览版将在未来几个月内发布。](https://github.com/flutter/flutter/wiki/Roadmap)

谷歌还宣布了一项名为 [Flutter Create](https://flutter.dev/create) 的在线竞赛，开发者有机会赢得一台顶级的 14 核 iMac Pro，内存为 128 GB。你要做的就是做一个代码大小小于 5KB 的 Flutter app，去 Flutter Create 网站，提交你的 app。我认为比 iMac Pro 更酷的是，谷歌将在 5 月的[谷歌 I/O 活动上宣布获胜者。我祝你们每个人好运。](https://www.xda-developers.com/google-io-2019-may-7-9/)