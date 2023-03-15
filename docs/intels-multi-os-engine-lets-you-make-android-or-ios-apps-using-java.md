# 英特尔的多操作系统引擎允许开发人员使用 Java 创建原生 iOS 或 Android 应用

> 原文：<https://www.xda-developers.com/intels-multi-os-engine-lets-you-make-android-or-ios-apps-using-java/>

我们中的许多人可能都遇到过不同平台上的应用程序，这让我们感到奇怪:*“为什么我现在还不能下载这个呢？”*

我相信你已经听说过一个最近风靡一时的应用， [Prisma](http://prisma-ai.com/) 。Prisma 于 6 月 11 日在 iOS 上推出，立即红极一时。一个多月后， [Prisma 终于在 Android 上公开发布](http://www.xda-developers.com/xda-external-link/prisma-publicly-released-on-android/)。一个月的周转时间并不算太糟糕，但是许多流行的应用程序需要更长的时间才能转移到另一个平台。但是为什么呢？很多时候，这只是由于资源分配。与 Android 用户相比，iOS 用户[在应用内购买方面仍然领先。因此，如果你是一家试图赚钱的企业，而你投资开发应用的资金有限，那么最初专注于 iOS 是有意义的。](https://www.appsflyer.com/resources/state-app-spending-global-benchmarks-data-study)

然而，随着时间的推移，已经发布了几个开发工具集来简化跨平台开发。其中一个流行的工具集叫做 [Xamarin Platform](https://www.xamarin.com/) ，最近被[微软](https://blog.xamarin.com/xamarin-for-all/)收购，它使拥有 C#技能的开发者能够在他们的 Mac 或 Windows PC 环境中为 Android、iOS 或 Windows Mobile 创建移动应用。最熟悉 Java 的开发人员曾期待使用 RoboVM 为 iOS 编写代码，直到今年四月 T4 项目被关闭。那么 Java 开发者还能用什么呢？幸运的是，英特尔在过去的几个月里一直致力于一个名为"[多操作系统引擎](https://software.intel.com/en-us/multi-os-engine/details)"的项目，目前仅作为技术预览版提供，旨在使 **Java 开发人员**能够轻松地为 iOS 和 Android 进行交叉开发。

* * *

**了解英特尔的多操作系统引擎**

根据英特尔的说法，使用多操作系统引擎进行移动应用程序开发有很多优势。首先，如果你使用服务器，你可以在 Mac 或 Windows 上开发应用程序。Multi-OS Engine 是一个独立的插件，集成了 Android Studio。希望为 iOS 编写代码的开发人员可以在 Android Studio 中为 Android 应用程序启动一个项目，然后使用 Multi-OS Engine 的工具将该项目配置为 iOS 应用程序。您可以访问许多特定于 iOS 的平台 API，这些 API 在 Java 中是不可用的，并且您可以创建绑定来为通用的 Objective-C 和 C 库生成 Java 代码。您编写的代码将被编译成本机 ARM 或 x86 代码。不需要了解目标 C。

英特尔声称，使用多操作系统引擎创建的应用程序的性能与原生应用程序相当。至于创建应用程序的用户界面，英特尔表示，Android 开发者应该继续通过 Android Studio 工作，而 iOS 应用程序可以使用多操作系统引擎中提供的用户界面设计器来设计。鉴于 RoboVM 的消亡，许多开发人员担心该项目可能很快被放弃，这将使任何可能投入大量时间和精力支持该项目的用户感到沮丧，这是可以理解的。英特尔声称其多操作系统引擎已经准备好作为一个开源项目发布，但是消息来源还没有下降。至少现在，这个项目是免费的。

* * *

任何对使用英特尔新的多操作系统引擎感兴趣的开发者都可以[在这里](https://registrationcenter.intel.com/en/forms/?productid=2586)注册技术预览，或者在这里查看更加[详细的文档。](https://software.intel.com/en-us/node/633225)