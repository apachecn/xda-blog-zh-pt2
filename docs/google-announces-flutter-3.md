# 谷歌宣布推出 Flutter 3，现在支持 macOS 和 Linux 桌面系统

> 原文：<https://www.xda-developers.com/google-announces-flutter-3/>

谷歌几年前创建了 Flutter，目的是开发一个跨平台的软件框架。Flutter 最大的优势在于，它可以用于为 Android、iOS、Linux、Windows、macOS 甚至 web 构建应用程序，并且都来自同一个共享代码库。虽然为 Windows 开发应用程序在二月份得到了稳定的支持，但 macOS 和 Linux 都还处于测试阶段。现在这种情况正在改变，因为谷歌在今年的谷歌 I/O 上宣布了 Flutter 3，为 macOS 和 Linux 构建应用程序提供了稳定的支持。

当然，对这两个新平台的跨平台支持需要的不仅仅是程序能够运行。他们需要适应体验的其余部分，他们还需要支持可能是独特的特定功能。这就是谷歌强调两点的原因:第一点是 Linux 支持得到了 Canonical(Ubuntu 的发行商)和谷歌合作的帮助，以便“为开发提供一个高度集成的最佳选择”

正如谷歌所说，Canonical 已经在开发“包括安装和固件更新在内的关键 shell 体验”此外，他们的 Linux 专用包*“为核心操作系统服务提供了一个惯用的 API，包括 dbus、gsettings、networkmanager、蓝牙和桌面通知，以及为 Yaru(Ubuntu 外观和感觉)提供了一个全面的主题和小部件集。”*

至于 macOS，谷歌投资支持英特尔和苹果硅设备，通过通用二进制支持，允许应用程序打包可执行文件，在这两种架构上本地运行。

## 燃烧和颤动

Google 的 Firebase 是一套非常全面的开发工具。它的目标是通过详细的崩溃报告、用户分析、身份验证和存储等功能，使应用程序的开发和维护变得更容易。根据谷歌的数据，63%的 Flutter 开发者在他们的应用中使用 Firebase，因此该团队一直在试图整合 Firebase 和 Flutter。这种集成现在比以往任何时候都更好，有了改进的文档和工具以及新的小部件，如 [FlutterFire UI](https://pub.dev/packages/flutterfire_ui) ，它为开发人员提供了可重用的用户界面，用于授权和个人资料屏幕。

此外，Flutter 的 Crashlytics 插件已经更新，开发者可以实时跟踪用户的致命错误，其他 iOS 和 Android 开发者也可以获得相同的功能。设置和配置也容易得多。

## 颤振 3 的基本改进

当然，Flutter 3 不仅仅是扩展框架的平台支持。它还引入了其他东西，包括对材质设计 3 的支持。 [Android 12](https://xda-developers.com/android-12) 见证了材质设计 3 的推出，包括你给材质上色主题引擎。

材料设计 3 并不是颤振 3 带来的唯一根本性改进。它现在原生支持 Apple Silicon 用于开发和编译输出。Dart 去年年底增加了对苹果芯片的支持，Flutter 可以利用它在 M1 驱动的设备上进行更快的编译。

至于 Dart 特有的变化，Google 说它已经引入了三个新的语言特性来帮助开发者。这三个特性是[增强枚举](https://github.com/dart-lang/language/blob/master/accepted/future-releases/enhanced-enums/feature-specification.md)、[随处命名参数](https://github.com/dart-lang/language/blob/master/accepted/future-releases/named-arguments-anywhere/feature-specification.md)和[超级构造函数](https://github.com/dart-lang/language/blob/master/working/1855%20-%20super%20parameters/proposal.md)。他们还增加了可执行签名、实验性 RISC-V 支持、升级的 linter 和新文档。谷歌有一个专门的博客，你可以查看更多关于 [Dart 2.17](https://medium.com/dartlang) 的信息。