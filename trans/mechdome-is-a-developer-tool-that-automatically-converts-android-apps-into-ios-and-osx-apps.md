# MechDome 是一款开发者工具，可以自动将 Android 应用转换成 iOS 和 OSX 应用

> 原文：<https://www.xda-developers.com/mechdome-is-a-developer-tool-that-automatically-converts-android-apps-into-ios-and-osx-apps/>

跨平台开发多年来一直是大多数独立开发人员面临的主要挑战。通常，为了将你的应用移植到另一个平台，学习一门新的编程语言会花费太多的时间和资源。

多年来，由于更有利可图的市场，这种资源分配的事实促使许多开发者将主要精力放在 iOS 上。然而，多亏了像 [Xamarin](https://www.xamarin.com/) 这样的项目，熟悉 C#的开发者已经能够在 iOS、Android 和 Windows Mobile 上推广他们的项目。但是 Android 开发人员最熟悉用 Java 编写，所以使用 Xamarin 需要开发人员熟悉一种新的语言并构建平台。我们已经报道了一个项目，旨在通过为 Java 开发人员提供一个交叉开发平台来弥合移动操作系统之间的差距——[英特尔的多操作系统引擎](http://www.xda-developers.com/intels-multi-os-engine-lets-you-make-android-or-ios-apps-using-java/)——但是还不知道这个项目将走向何方。这就是 **[机甲](https://www.mechdome.com/)** 的用武之地。

MechDome 是一家总部位于加利福尼亚州的初创公司，于今年 1 月成立，开发了一种转换工具，可以从你的 Android 应用程序自动创建原生 iOS 和 OS X 应用程序。无需学习如何使用新的 IDE 或 API。你需要做的只是向 MechDome 发送一个 APK 文件(不需要向他们发送你的源代码)，全自动工具将在几秒钟内为 iOS 和 OS X 编译一个独立的二进制文件，然后开发者可以在苹果的应用商店上分发。我们采访了 MechDome 的创始人兼首席执行官马里奥·科斯米斯卡斯(Mario Kosmiskas ),观看了该工具的运行演示——而且它**确实有效。**尽管由于 iOS 和 Android 操作方式的根本差异(我们将在下面讨论)而存在一些限制，但该工具已经在苹果应用商店上制作了一些实时应用，如[开源](https://github.com/QuantumBadger/RedReader) Reddit 客户端 [RedReader](https://itunes.apple.com/us/app/redreader-b/id1089788044?mt=8) 和[开源](https://code.google.com/archive/p/sudoku-pro-android/source) [数独](https://itunes.apple.com/us/app/sudoku-pro-o/id1142448897?mt=8)客户端，以证明其工作正常。

* * *

**装有 MechDome 的 iOS 上的 Android 应用**

MechDome 的既定目标是允许开发者将未经修改的 Android 应用转换为原生的 iOS 或 OS X 应用。与英特尔的多操作系统引擎或 Xamarin 等技术相比，Android 开发人员不需要知道如何绑定 Objective-C 库，因为该工具会为您处理。也不需要使用 UI 生成器来修改您的 Android 应用程序，因为 MechDome 会处理所有 Android UI 元素的转换。是的，即使是 Android 平板电脑应用程序也能很好地转换成适合 iPads 的格式。

MechDome 最大的承诺是，转换后的 Android 应用程序将以目标操作系统用户熟悉的方式运行。例如，Android 共享菜单将被 iOS 中的原生共享表所取代，如果适用的话，还将包括使用隔空投送的功能。在 Android 中发布通知的应用程序将在 iOS 的通知中心显示通知。某些意图比如在 Android 上打开摄像头确实会在 iOS 设备上打开摄像头，Android 上的 URL 意图会调用 iOS 上的 Safari。Android 上访问联系人或日历的内容提供商将转而访问相关的 iOS 或 OS X 数据库来获取这些信息。

不过一般来说，使用 Android 应用程序所需的所有硬件功能都将直接映射到 iOS 中的相关硬件。不过，软件功能可以分为 3 个不同的类别:1)iOS 上不存在的功能(如 toast 消息)将直接实现，2)iOS 和 Android 上都存在的功能将被相关的 iOS 方法替换，3)iOS 上存在但 Android 上不存在的功能(如苹果的 3D Touch 库)不能转换，但可以通过使用库来实现。MechDome 的创始人表示，大多数活动、视图、服务、祝酒词和基本内容提供商应该可以从 Android 转换到 iOS。

但是如前所述，这个工具确实有一些限制，这是由 iOS 的工作方式决定的。寻求将应用程序转换到 iOS 的 Android 开发者面临的最大挑战之一是如何处理后台服务。无论好坏，iOS 对第三方应用程序可以运行的后台服务的时间和种类的要求要严格得多。此外，Android 中允许应用程序间通信的丰富意图系统在 iOS 中基本上不存在。最后，目前不支持 Google Play 服务 API，因此任何依赖 Google 服务的应用程序都将无法运行。因此，开发人员将主要限于通过手动用户输入直接访问的功能，这对大多数游戏或应用程序来说不应该构成重大问题。

* * *

**正在使用的机械罩**

在一个私人演示中，这个工具看起来确实像宣传的那样起作用。科斯米斯卡斯演示了如何将几个功能齐全的安卓应用程序编译成可以运行的 iOS 和 OSX 应用程序。Toast 通知、通知中心中的通知、webview、位置访问、文本输入和 UI 元素的一般功能都在演示中工作。运行在 iOS 上的 AOSP 计算器的外观和功能与任何 Android 设备上的完全一样。

还展示了更新应用程序并为 iOS 重新编译它，这个过程相当简单。在这种情况下，开发人员 Kosmiskas 先生演示了如何在 Android Studio 中更改文本框以显示“XDA 开发人员”。然后，他导出了应用程序，生成了签名的 APK，并在几秒钟内从 MechDome 服务器编译了 iOS 和 OS X 二进制文件。当使用模拟器启动 iOS 应用程序时，Android Studio 中所做的更改就会出现。

目前，MechDome 正在进行一项免费的公开测试计划。开发者可以[在 MechDome 网站上注册他们的应用](https://www.mechdome.com/signup.html)来接收邀请，以测试转换他们的 Android 应用。不幸的是，这项服务的价格信息还没有公布。尽管如此，如果你是一名 Android 开发者，希望最终在苹果的生态系统中掀起波澜，而无需自己付出太多努力，这仍然是一个值得关注的有趣项目。