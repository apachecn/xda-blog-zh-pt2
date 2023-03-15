# 谷歌与 Canonical 合作，将 Flutter 应用程序引入 Linux

> 原文：<https://www.xda-developers.com/google-partners-canonical-bring-flutter-apps-linux-ubuntu-snap-store/>

过去几年，谷歌一直在努力创造和扩大 Flutter。当我们上次谈到 [Flutter](https://www.xda-developers.com/tag/flutter/) ，[谷歌在 Flutter](https://www.xda-developers.com/google-rebuilds-flutter-dart-devtools/) 中完全从零开始重建了 DevTools，以获得更好的性能、更大的通用性，并展示他们对这一应用开发框架的信心。谷歌设想 Flutter 是一个编程框架，开发者可以用它来构建针对多个系统的应用，因此该团队正在不断努力改善 Flutter 对平台的支持。今天，谷歌宣布它正在与 Canonical 的 Ubuntu 桌面团队合作，将 Flutter 应用程序引入 Linux。

概括地说，Flutter 是一个跨平台的编程框架，本质上让开发人员可以在 Android、iOS、web 和桌面上创建具有漂亮 ui 的应用程序。作为一个编程框架，Flutter 利用编程语言 Dart 来创建 Flutter 应用程序。 [Flutter 1.0](https://www.xda-developers.com/flutter-1-0-is-now-available-stable-native-cross-platform-development/) 经过 10 个月的测试期，于 2018 年 12 月到来。而且现在这个阶段，框架对构建 iOS 和 Android 应用的支持已经相当成熟了。但对于构建 web、macOS、Linux 或 Windows 应用程序来说，情况并非如此。谷歌一直在更新其在非移动平台上的努力，今天的公告是一系列非移动平台发布的最新公告。[版本 1.9](https://www.xda-developers.com/flutter-19-web-repo-ios-13-macos-catalina-support-ml-code-completion-dart-25/) 带来了为 macOS 构建应用的早期支持，而[版本 1.12](https://www.xda-developers.com/google-flutter-112-support-web-macos-more/) 改进了 macOS 和 Web 支持，并将其提升到 beta 分支。在那个阶段，开发人员在技术上也可以为 Windows 和 Linux 创建 Flutter 应用程序，但这些库处于 alpha 测试之前的状态，API 可能会在没有通知的情况下发生变化。

上个月，谷歌展示了为 Windows 和 Linux 构建 Flutter 应用程序的重大进展。在 Flutter 的产品经理 Tim Sneath 的一篇中期文章中，他总结了该团队在框架支持构建桌面界面应用方面的进展。该团队增加了显示密度支持、更好的鼠标和键盘支持、平台查询和桌面导航小部件。此外，他们还在开发一个适用于所有平台的插件模型。结合 Dart 的外部函数接口(FFI)和“Win32”插件，Flutter 应用程序可以像作为 EXE 文件提供的原生 Windows 应用程序一样运行，并且还可以向后兼容 Windows 7。与此同时，通用 Windows 平台(UWP)支持实现了对 Xbox 和 Windows 10X 等平台的支持。

今天发布的 Linux alpha for Flutter 得到了 Ubuntu 发行商 Canonical 的支持，Ubuntu 是世界上最流行的桌面 GNU/Linux 发行版。由于这种合作关系，开发者将能够将他们的 Flutter 应用程序部署到 Snap Store 或其他现代 Linux 部署中。Snap Store 附带 Ubuntu 20.04 Focal Fossa 版本，因此直接访问 Snap 包管理系统对于在 Linux 上部署应用程序是一大优势。

> 通过使 Linux 成为一流的颤振平台，Canonical 邀请应用程序开发人员向数百万 Linux 用户发布他们的应用程序，并扩大他们可用的高质量应用程序的可用性。

Canonical 也对框架进行了重大投资，它派出了一个开发团队与 Google 的开发人员一起工作，为大多数 Linux 发行版带来最佳的 Flutter 体验。该公告进一步承诺 Canonical 和 Google 将继续合作，进一步改进 Linux 支持，并保持与其他支持平台的功能对等。