# 谷歌发布 Flutter 1.20 稳定版，增加了新功能和开发者工具

> 原文：<https://www.xda-developers.com/google-flutter-1-20-stable/>

Google 的跨平台 UI 工具包 Flutter 已经到了 1.20 版本稳定。在[之前的稳定版本](https://www.xda-developers.com/google-flutter-117-dart-2-8-stable-sdk-app-development/)中，谷歌引入了实质性的性能改进，改善了 iOS 对 Metal 的支持，以及新的材料小部件。今天的 Flutter 1.20 稳定版包括更多的性能改进、几个 UI 增强、Visual Studio 代码扩展的更新、移动文本字段的自动填充等等。

Flutter 1.20 包括来自全球 359 个贡献者的 3029 个合并的 PRs 和 5485 个关闭的问题，是迄今为止任何 Flutter 版本贡献者数量最多的。谷歌还夸口说，现在 Google Play 上有超过 90，000 个用 Flutter 开发的应用程序，比 4 月份的 50，000 个有所增加。这种增长很大一部分来自印度，谷歌称印度现在是 Flutter 开发者的首选地区。

**性能提升**

以下是谷歌提高颤振 1.20 性能的一些方法:

*   谷歌包含了对[树摇图标](https://github.com/flutter/flutter/pull/55417)的性能修复，该图标现在是构建非网络应用时[的默认图标](https://github.com/flutter/flutter/pull/56633)。此功能通过移除任何不使用的图标来减小应用程序的大小。图标字体树抖动目前仅限于 TrueType 字体，但谷歌表示，这一限制将在未来取消。
*   如果一个应用程序在第一次运行时有 janky 动画，后来在随后的启动中变得平滑，这可能是由于着色器编译 jank。通过 [Skia 着色语言着色器预热](https://github.com/flutter/flutter/wiki/Reduce-shader-compilation-jank-using-SkSL-warm-up)，着色器编译 jank 最多可减少 2 倍。
*   Google 重构了鼠标点击测试，将基于 web 的微基准测试的性能提高了 15 倍。因此，Google 已经能够添加对鼠标光标的支持，鼠标光标将显示在几个常用的小部件中。
*   谷歌在 Dart 2.9 中提高了 Dart 的 UTF-8 解码器的解码速度。在 UTF-8 解码基准测试中，该公司测量了低端 ARM 设备上英文文本近 200%的改善和中文文本 400%的改善。

**自动填充移动文本字段**

开发人员强烈要求的一个功能是支持 Flutter 应用程序中的文本自动填充。在 Flutter 1.20 中，已经添加了基本的自动填充功能，尽管不支持一些特定于平台的配置(如 iOS 上的 passwordRules)。谷歌也为网络应用程序的文本字段支持带来了自动填充功能。

**互动查看器小工具**

这个新的小部件是为在你的应用中构建交互元素而设计的，比如平移、缩放、拖放等等。API 文档可在[这里](https://api.flutter.dev/flutter/widgets/InteractiveViewer-class.html)获得，而上传的演示文稿[在](https://www.youtube.com/watch?v=ChFa0A72Uto)这里深入研究这个新部件的开发过程。

**嵌入 Visual Studio 代码的 Dart dev tools**

Google 增加了新的 Visual Studio 代码扩展，将 Dart DevTools 直接引入 Visual Studio 代码编码工作区。这可以通过 dart.previewEmbeddedDevTools 设置来启用。

**其他变化**

在 Flutter 1.20 中有很多其他的新特性和开发者工具。仅举几个例子:更新的 Slider、RangeSlider、TimePicker 和 DatePicker 小部件；“关于”对话框中提供了一个新的“响应许可证”页面；发布新的或更新的 Flutter 插件的新的 pubspec.yaml 格式要求；Dart DevTools 中更新的网页，支持 web socket 配置文件；支持在 Visual Studio 代码中移动或重命名文件时自动更新导入语句；还有更多。

谷歌表示，Flutter 1.20 是该框架迄今为止最大的版本，但还有很多尚未推出。该公司表示，他们仍在努力实现[声音零安全支持](https://www.xda-developers.com/google-flutter-117-dart-2-8-stable-sdk-app-development/)，新版本的广告、地图和 WebView 插件，更多的工具支持，等等。他们还致力于更好的网络和桌面支持，特别是在 Linux 上，他们刚刚[宣布与 Canonical](https://www.xda-developers.com/google-partners-canonical-bring-flutter-apps-linux-ubuntu-snap-store/) 合作。