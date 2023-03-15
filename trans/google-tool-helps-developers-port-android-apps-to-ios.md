# 谷歌工具帮助开发者将 Android 应用移植到 iOS

> 原文：<https://www.xda-developers.com/google-tool-helps-developers-port-android-apps-to-ios/>

如果你是一个为 Android 开发了[应用程序并把它们放在 Google Play 上的应用程序开发者，你无疑已经看到了为最大的移动操作系统开发应用程序的优势。也许你想和其他移动操作系统的用户“分享爱”,但是你不熟悉 Objective-C，所以你选择远离它。](http://forum.xda-developers.com/forumdisplay.php?f=524)

有许多工具可以帮助您将 JAVA 转换成 Objective-C，并产生不同的结果。鉴于 JAVA 和 Objective-C 几乎是两个不同的世界，尝试移植或转换可能很耗时，因为您必须筛选字节码和错误输出。然而 Google 已经创建了一个工具，叫做 [J2ObjC](http://google-opensource.blogspot.com/2012/09/j2objc-java-to-ios-objective-c.html) ，它将把你的 JAVA 类转换成 Objective-C 类，从而直接利用 iOS 基础框架。本质上，该工具允许 JAVA 代码成为 iOS 应用程序的一部分。

以下是他们对此的看法:

> J2ObjC 是 Google 的一个开源命令行工具，它可以将 Java 代码翻译成 Objective-C，用于 iOS(iPhone/iPad)平台。该工具使 Java 代码成为 iOS 应用程序构建的一部分，因为不需要编辑生成的文件。目标是用 Java 编写应用程序的非 UI 代码(比如数据访问或应用程序逻辑)，然后由网络应用程序(使用 [GWT](https://developers.google.com/web-toolkit/) )、[安卓](https://www.android.com/)应用程序和 iOS 应用程序共享。

该工具支持大多数 JAVA 语言和运行时特性，但不保证能与所有可能的 JAVA 使用方式一起工作。该工具没有为开发人员提供独立于平台的 UI 工具包，所以您仍然需要使用原生的 iOS UI 代码，但对于希望开发跨平台应用程序的开发人员来说，这是一个很大的进步。请务必访问[项目页面](https://code.google.com/p/j2objc/)了解关于使用该工具的信息。