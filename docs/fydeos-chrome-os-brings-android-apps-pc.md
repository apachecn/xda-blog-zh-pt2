# FydeOS 是中国的 Chrome OS 分支，它带来了 Android 应用程序支持

> 原文：<https://www.xda-developers.com/fydeos-chrome-os-brings-android-apps-pc/>

即使这不是一个经常性的话题，我们现在对 Chrome OS forks 并不陌生。就像谷歌 Chrome 浏览器一样，Chrome OS 基于一个开源项目——特别是 Chrome OS 项目，因此，它可以被分叉。这些分叉——无论是没有谷歌附件的纯 Chrome 操作系统，还是内置了额外功能——都可以让你选择在非 Chromebook 设备上运行 Chrome 操作系统。无论是您的笔记本电脑、笔记本电脑，甚至是台式电脑，它们实际上都是无法正常运行 Windows 10、Windows 8.1 甚至 Windows 7 的旧电脑的可靠替代品。但是 Chrome OS 与 Chromebooks 中官方认证的 Chrome OS 版本之间存在明显的差异。其中之一是缺乏 Android 应用程序支持。

Android 应用程序支持实际上是 Chrome OS 的一个相当新的东西，但自从该功能首次推出以来，受支持的 Chromebooks 列表已经变得相当大。即使这样，一些旧的 Chromebooks 也不支持 Android 应用程序，大多数 Chrome OS forks 也因为这样或那样的原因缺乏对它的支持。有一个 Chrome OS 分支叫做 FydeOS，服务于中国的教育领域，它支持 Android 应用程序。

* * *

## FydeOS 将 Android 应用程序引入个人电脑

FydeOS 以前被称为 FlintOS，看起来与其他分支没有太大区别，比如 Neverware 的 CloudReady。GalliumOS 是一个流行的 GNU/Linux 发行版，旨在取代 Chromebooks 上的操作系统，但它也不提供 Android 应用支持。但与其他选项不同，FydeOS 默认启用 arc++(Chrome 的 Android 运行时),并包括允许您在 x86 PCs 上运行 Android 应用程序所需的库。据开发者称，FydeOS 主要是为中国市场开发的——那里的普通人根本不熟悉谷歌 Play 商店或 Google Play 服务。但由于 Android 在中国仍然非常受欢迎，中国用户非常习惯于侧装应用程序，因此缺乏单一的中央应用程序商店在那里不是什么问题。

由于第三方仿真器，如 [BlueStacks](https://www.xda-developers.com/bluestacks-android-emulator-performance-upgrade/) 或针对 x86 优化的 Android 版本，如 [Android-x86](https://www.xda-developers.com/android-x86-android-8-1-oreo/) 或 RemixOS，用户已经能够在 PC 上运行 Android 应用程序一段时间了，但每个解决方案都有自己的局限性。有了 BlueStacks 这样的东西，Android 系统运行在一个孤立的实例(虚拟机)中，因此需要一台相当强大的计算机来运行基本的游戏。然而，Android forks 需要你要么在虚拟机上运行一个实例，要么在单独的分区上引导它。虽然我们习惯了 Android 作为一个移动操作系统，但它作为一个成熟的桌面操作系统并不太好，尽管有人试图用 RemixOS 这样的叉子来“桌面化”它，所以你可能不会喜欢这种体验。

*在 Dell Vostro 成就 3546 上运行的 FydeOS 的根实例。*

由于 FydeOS 基于 Chromium OS，即使它比 Windows，Linux 或 macOS 更受限制，但它绝对是一个轻量级操作系统，具有网页浏览功能和(现在)完整的 Android 应用程序支持。FydeOS 只是从 Chromebooks 中获取 Android 应用支持，并将其带到 x86 PCs 上。Android 应用程序在这里本地运行，因此，你不应该遇到任何重大问题。

### 进行中的工作

虽然您可以在备用计算机上安装和测试它，但我们不建议您在主计算机上这样做。这是因为 FydeOS 目前仍处于非常早期的开发阶段，很可能你迟早会遇到问题。它旨在供中国市场使用，这个市场不熟悉谷歌 Play 商店或谷歌的服务，每个 OEM 厂商都在自己的设备上安装自己的应用商店。该操作系统的主要目的是将 Chrome 操作系统带到中国用户手中。因此，由于许可问题以及 Play 服务或谷歌服务在 mainland China 无法使用的事实，FydeOS 在默认情况下不会附带谷歌 Play 商店或谷歌 Play 服务。

 <picture>![](img/ca8af52ac225ea9a64b8bc8e5bf5e3ce.png)</picture> 

The Google Play Store running on FydeOS.

然而，国际用户可以选择在他们的会话中安装谷歌应用程序，如果这是他们想要的。显然，它们甚至会在连接到互联网后自动下载。然而，鉴于 fork 以中国为先的重点，你可能会在使用 Play Store 时遇到问题。

### 在哪里可以下载？

FydeOS 的版本可以从他们的网站[这里](https://fydeos.com/download/)获得。你可以下载并安装在任何电脑上，但你需要至少 2 GB 的内存，16 GB 的存储空间，以及相对较新的硬件来获得良好的体验。然而，如果你打算玩游戏或使用较重的 Android 应用程序，你将需要一台相对强大的机器。

FydeOS 的大部分源代码也可以在 GitHub 上获得[。不过，请记住，FydeOS 的一些附加功能，尤其是那些针对中国网络情况的功能，是开源的。](https://github.com/fydeos/)

* * *

## 底线

FydeOS 似乎是一个非常有趣的项目——它添加了 Android 应用程序，并允许它们在旧的、更慢的计算机上运行，而不仅仅是 Chromebooks、平板电脑和手机。然而，这是一项正在进行的工作，我们不建议将它安装在您的主要台式机或笔记本电脑上，因为您可能会发现自己有意想不到的错误和问题。如果你有一个备用设备，尽管去吧。你可以在这里查看他们的网站。

我们很兴奋地看到这个项目将如何结束。大多数 Chromium 操作系统很少获得关注，但 FydeOS 专注于中国第一(同时提供 Android 应用支持)，这使它与众不同，甚至可能帮助它获得一个不错的用户群。我们会让你知道任何值得注意的未来发展。

你对费德奥斯有什么看法？请在评论区告诉我们。

* * *

*本文已更新，更正了关于 Chrome OS 开源特性的事实，并更正了 GalliumOS 是一个独立的 GNU/Linux 发行版。*