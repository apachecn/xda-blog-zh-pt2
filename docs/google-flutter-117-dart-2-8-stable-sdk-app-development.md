# 谷歌发布用于应用开发的 Flutter 1.17 和 Dart 2.8 SDKs

> 原文：<https://www.xda-developers.com/google-flutter-117-dart-2-8-stable-sdk-app-development/>

Flutter 是一个[跨平台编程框架](https://www.xda-developers.com/flutter-1-0-is-now-available-stable-native-cross-platform-development/)，旨在解决开发跨平台应用而没有非本机代码混乱的困境。有了 Dart 编程语言的知识，开发人员可以为 Android、iOS、web 和桌面构建具有统一 UI 外观的应用程序。 [Flutter 1.9](https://www.xda-developers.com/flutter-19-web-repo-ios-13-macos-catalina-support-ml-code-completion-dart-25/) 让 macOS 和 Catalina 的支持处于 alpha 状态，而 [v1.12 版本使他们的支持超过了前 alpha 状态](https://www.xda-developers.com/google-flutter-112-support-web-macos-more/)。现在，谷歌推出了新的 1.17 版 Flutter 和 2.8 版 Dart，标志着它们将成为 2020 年 Flutter 和 Dart 的第一个稳定版本。

## 颤振 1.17

上个月，谷歌[宣布改变其发布流程](https://medium.com/flutter/flutter-spring-2020-update-f723d898d7af#d6e5)。该公司早期的流程缺乏对何时发布、发布中包含哪些代码等问题的明确性。现在，谷歌计划大约每季度发布一次稳定版本。这本身就提出了一些挑战，因为发布基础设施必须为新的发布过程进行重组。现在，Flutter 1.17 正在面向开发者发布到稳定通道。自从上一次 Flutter 1.12 发布以来，谷歌已经关闭了 6339 个问题，他们关闭的错误比今年开放的更多，导致净减少约 800 个问题。

除了错误修复，Flutter 1.17 还带来了实质性的性能提升，改善了 iOS 对 Metal 的支持，并包括了新的材质小部件。

### 性能改进

与旧版本相比，使用 Flutter 1.17 构建的应用程序在默认导航情况下会有 20-37%的加速，其中有不透明的路线。使用 Flutter 1.17 构建的应用程序大小也有相当大的改进。例如，颤振画廊样本现在在 2020 年为 8.1MB，而在 2019 年底为 9.6MB。对于内存使用，1.17 版本在快速滚动大图像时减少了 70%的内存。

[Metal](https://developer.apple.com/metal/) 是苹果的底层图形 API，提供对 iOS 设备底层 GPU 的近乎直接的访问。现在，Flutter 在为支持的 iOS 设备构建时默认使用金属，使 Flutter 应用程序运行更快。改进的金属支持将 iOS 应用程序的渲染速度平均提高了约 50%。在不完全支持 Metal 的 iOS 设备上，即 iOS 版本低于 10 且在 A7 处理器之前发布的设备上，Flutter 回落到 OpenGL。

Flutter 1.17 增加了对新材质小部件的支持。现有的小部件也有更新。例如，NavigationRail 帮助开发人员向应用程序添加响应性应用程序导航模型，对于可以在移动和桌面外形之间切换的应用程序来说非常棒。DatePicker 和 TextSelection 溢出小部件也已更新:DatePicker 的新视觉效果与更新的材料指南相匹配，并添加了新的文本输入模式，而 TextSelection 现在提高了 iOS 和 Android 在按钮长度超过可以显示而不溢出时的保真度。最后，谷歌还发布了新的动画包，提供了实现新的[材质运动](https://material.io/components/pickers/#mobile-pickers)规范的预建动画。

### 颤振 1.17 的其他变化

*   谷歌已经改进了 Flutter 应用程序的可访问性，修复了滚动、文本字段和其他输入部件。
*   谷歌还准备用新的 Flutter 版本替换当前版本的 Dart DevTools。开发者可以通过启动 DevTools，然后点击 DevTools 右上角的“breaker”图标来测试这个新版本。Dart DevTools 的新 Flutter 版本的最大改进是新的网络选项卡，当你点击“记录”按钮时，它会显示你的 Flutter 应用程序的网络流量。
*   另一个改进是一个实验性的“快速启动”选项，允许你在为 Android 构建应用程序时，启动 Flutter 应用程序调试的速度加快 70%。

谷歌还为 Superformula 团队在 Flutter 中重新制作了整个米高梅度假村 Android 应用程序而欢呼。

* * *

## Dart 2.8

Dart 是用于在 Flutter 中构建应用程序的编程语言。随着 Dart 2.8 SDK 的发布，Google 引入了一些变化:

*   对 *pub* 客户端工具的改进，该工具用于管理从 [pub.dev 包存储库](https://pub.dev/)下载的包。
    *   谷歌通过增加对并行获取包的支持和推迟*发布运行*预编译，提高了*发布获取*的性能。
    *   谷歌还增加了一个新工具(*pub outsided*)来确保软件包依赖关系保持最新。
*   为健全的空安全做好准备，因为当代码试图读取具有空值的变量时，空引用是应用程序崩溃的常见原因。
    *   Google 正准备在 Dart 中添加对声音 null 安全的支持，这将确保所有表示的变量都持有非 null 值。
    *   实现声音空安全是一项巨大的任务，最初会导致 Dart 语言和库的中断。谷歌希望开发者能够意识到这些突破性的变化，并在他们的 T2 问题追踪器上记录任何问题。

* * *

你可以在 Flutter 1.17 和 Dart 2.8 的公告文章中读到更多关于这些和其他变化的细节。