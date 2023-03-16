# 微软开源的 Windows 10 计算器被移植到安卓系统

> 原文：<https://www.xda-developers.com/microsoft-open-source-windows-10-calculator-android/>

# 微软开源的 Windows 10 计算器被移植到 Android 和 iOS 上

微软开源了 Windows 10 计算器，开发者获取了该应用的可用源代码，并将其移植到 Android 和 iOS 上。

这可能会令人惊讶，但是微软是开源社区中最大的玩家之一。你可以看看他们的 [GitHub 账户](https://github.com/Microsoft)，了解一下他们贡献了多少。就在几周前，[他们开源了](https://github.com/microsoft/calculator)他们的另一个应用:Windows 10 计算器。Uno 平台的开发者决定利用该应用的可用源代码，并将其移植到其他平台。然而，这并不像有些人想象的那么容易。

Uno Platform 决定将应用程序移植到 web、Android 和 iOS 上。问题是，尽管 Windows 10 的计算器带有流畅的设计语言和相当新的实践，但它的代码仍然是传统的。引擎是从 90 年代开始的[，所以你可以想象将旧的 C++代码移植到 C#或任何现代语言有多困难。这就是为什么 Uno Platform 的开发团队在前进的道路上发现了很多挑战。不过，将代码转换成 XAML 代码，然后为移动平台做好准备是相当容易的。Uno Platform】创建了自己的 GitHub 页面](https://github.com/microsoft/calculator/blob/master/src/CalcManager/Ratpack/conv.cpp#L7)来帮助开发者构建一个多平台计算器。

移植的应用程序的网页版本是使用 WebAssembly 编译的，可以在这个网站找到[。不幸的是，Chrome 对 WebAssembly 的支持很差，所以我建议使用 Microsoft Edge 或任何其他浏览器来打开应用程序。至于 Android 和 iOS，你可以从各自的应用程序市场下载应用程序。iOS 上移植的 Windows 10 计算器](https://calculator.platform.uno/)[可以在这里找到](https://testflight.apple.com/join/A1mUXddc)。下面是 Android 的 Play Store 列表。

* * *

**来源: [Uno 平台](https://platform.uno/a-piece-of-windows-10-is-now-running-on-webassembly-natively-on-ios-and-android/) | Via: [MSPoweruser](https://mspoweruser.com/windows-10s-calculator-app-gets-ported-to-android-ios-and-the-web/)**