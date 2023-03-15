# WireGuard 宣布了一项重大的 Android 更新，支持 Android TV、更现代的代码和面向第三方应用的 API

> 原文：<https://www.xda-developers.com/wireguard-project-announces-big-android-update-android-tv-support-more-modern-code-api-third-party-apps/>

如果你重视隐私，你一定听说过由 XDA 知名开发商 [zx2c4](https://forum.xda-developers.com/member.php?u=5434776) 开发的 [WireGuard](https://www.xda-developers.com/wireguard-vpn-project-support-android-roms/) 。简而言之， [WireGuard 项目是一个运行在 Linux 内核中的 VPN 协议](https://www.xda-developers.com/us-senator-pushes-government-use-wireguard-vpn/)，旨在比许多其他替代方案更快更简单。今年早些时候，VPN 协议甚至[进入了正式的 Linux 内核](https://www.xda-developers.com/wireguard-vpn-linux-kernel-5-6/)。WireGuard 现在发布了一系列声明，通过他们的应用程序支持 Android TV，为流行的手机预建内核模块，Kotlin 重写的 UI，等等。

首先，预计到[即将到来的谷歌电视公告](https://www.xda-developers.com/google-nest-audio-chromecast-google-tv-leaks-more-details/)，WireGuard 已经移植了他们的 Android 应用程序，使其可以在电视上运行，界面简单易用。这将允许用户在电视内通过 VPN 运行网飞等应用程序。

你可以从[谷歌 Play 商店](https://play.google.com/store/apps/details?id=com.wireguard.android)或者 [F-Droid](https://f-droid.org/en/packages/com.wireguard.android/) 那里获得应用程序。

Android 智能手机上的 WireGuard 应用程序为股票非 rooteded 用户提供了一个普通的基于 VpnService 的后端，为 root 用户提供了一个基于内核的后端。现在，由于 XDA 公认的开发者的努力，预建的内核模块可以用于像谷歌像素系列这样的流行设备。这样，有库存但有根的用户也可以利用这些内核模块，而不需要在有 WireGuard 支持的自定义 ROM 上。内核模块可以从应用程序中获得。感兴趣的开发者可以[通过 GitHub](https://github.com/wireguard/android-wireguard-module-builder/) 添加更多支持的 rom。

另一个我们最喜欢的应用程序， [Tasker，也在今年早些时候获得了 WireGuard 支持](https://www.xda-developers.com/tasker-5-9-3-beta-4-contact-via-app-wireguard-integration/)。

XDA 知名开发者 zx2c4 也告诉我们，WireGuard 的代码库也有所改进，并进行了相当大的更新。该项目现在分为两个模块:用户界面的 UI 模块和隧道模块，这是一个独立的 API，允许任何应用程序嵌入到 WireGuard 中。隧道模块可以从 JCenter 导入[，并附带](https://bintray.com/wireguard/wireguard-android/wireguard-android/_latestVersion)[丰富的文档](https://javadoc.io/doc/com.wireguard.android/tunnel)。这种拆分有几个好处。首先，开发人员现在可以通过一行简单的代码将 WireGuard 直接添加到他们的应用程序中，比如 implementation '*com . wire guard . Android:tunnel:$ WireGuard tunnelversion*'。隧道模块是用 Java 编写的，很容易嵌入到 Java 和 Kotlin 应用程序中。UI 模块也在 Kotlin 中完全重写，同时利用了 Jetpack 和 Kotlin 协同程序等工具。应用程序上的操作完全是异步的。

**[WireGuard 内核/ROM 集成- XDA 线程](https://forum.xda-developers.com/android/development/wireguard-rom-integration-t3711635)**

这些代码库改进的原因之一是为了吸引新的开发人员。WireGuard 项目正在积极为其 Android 应用寻找新的维护者。如果你想帮助这个开源项目，请联系 WireGuard 开发团队，他们的联系方式在他们网页的[底部。](https://www.wireguard.com/#email-contact)