# Google 的 Flutter 现在可以让你为 Windows 开发应用程序

> 原文：<https://www.xda-developers.com/flutter-google-now-build-apps-windows-development/>

Flutter 是 Google 做的一个[开源 app 开发框架。它的主要目标之一是通过允许开发人员在多个目标上共享一个代码库，使多平台开发变得更加容易。到目前为止，您可以使用 Flutter 为 Android、iOS、macOS、Linux 和 web 构建一个统一的应用程序。如果你仔细观察，你会发现列表中缺少了一个非常重要的操作系统。这一疏忽现在正在被弥补，因为](https://www.xda-developers.com/google-rebuilds-flutter-dart-devtools/)[谷歌已经宣布【Windows 的 Flutter 现在可以在 alpha 版本中使用。因此，Flutter 可能已经成为开发人员可以使用的最跨平台的框架。](https://medium.com/flutter/announcing-flutter-windows-alpha-33982cd0f433)

Windows 支持意味着很多事情，但可以说最大的影响是，现在可以为 6 个不同的平台开发一个应用程序，而不需要 6 个不同的代码库。除了鼓励开发者开始使用 Flutter，这也意味着现有的基于 Flutter 的应用程序现在可以原生地进入 Windows。

这也是适当的支持。Google 已经更新了 Flutter 工具链，以正确支持 Windows CLI，并添加了包含实际 Flutter 应用程序的必要 Win32 shell 应用程序。就像其他平台一样，如果你需要用本地代码做一些事情，你也可以这样做，这要感谢 Flutter 的插件系统。

如果你想知道 Flutter 在 Windows 上是什么样子，谷歌也有。你不需要下载整个 SDK 并构建你自己的应用。相反，你可以看看几个兼容 Windows 的 Flutter 应用程序，比如 gskinner 的[Flokk](https://github.com/gskinnerTeam/Flokk/releases)和 [Flutter Gallery](https://github.com/flutter/gallery) 。

最后，如果你想为 Windows 环境设置你自己的 Flutter，这里有一些方法。首先，按照[谷歌的说明在 Windows](https://flutter.dev/docs/get-started/install/windows) 上安装 Flutter 工具。接下来，通过运行以下命令启用 Windows 支持。

```
 flutter channel dev
flutter upgrade
flutter config  
```

就是这样！您现在应该已经为 Windows 安装并运行了 Flutter。如果你需要更多的信息，请看谷歌的文档。祝所有平台开发愉快！