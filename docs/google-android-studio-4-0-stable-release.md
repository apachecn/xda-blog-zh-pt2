# 谷歌发布 Android Studio 4.0 稳定版，新增开发者功能

> 原文：<https://www.xda-developers.com/google-android-studio-4-0-stable-release/>

仿佛就在昨天(如果昨天是二月的话), [Android Studio 3.6 发布了](https://www.xda-developers.com/android-studio-3-6-stable-release/),提供了许多有用的补充和必要的修复。现在，一天(三个月)后，谷歌已经将 Android Studio 4.0 推向稳定，增加了更多有用的功能和必要的修复。请继续阅读，了解更多新内容。

## 运动编辑器

我们要讨论的第一个特性是运动编辑器。近几年来， [AndroidX](https://www.xda-developers.com/googles-androidx-aosp/) 拥有了一个名为 MotionLayout 的 ConstraintLayout 子类。MotionLayout 的目的是帮助您更轻松地在布局状态之间制作动画。唯一的问题是，您必须自己用 XML 创建转换。在 Android Studio 4.0 中，有一个新的运动编辑器界面，让您可以在 MotionLayout 中可视化地创建和编辑过渡和动画。不管怎样，所有这些都以一个 XML 文件结束，但是您不再需要自己写出来。

## 新布局检查器

Android Studio 有一个非常有用的工具是布局检查器。在可调试的应用程序上，它让你确切地看到你的应用程序是如何在屏幕上布局的，以及它们的各种属性。在 Android Studio 4.0 中，新的和改进的布局检查器扩展了旧版本。虽然您仍然可以使用它进行简单的视图树检查，但它现在包括了像实时刷新这样的功能。与至少运行 Android 10 的设备配对，你可以获得更多功能，如更详细的视图属性和屏幕上的 3D 显示。

## 布局验证

可以说，设计一个应用程序最困难的方面之一是创建布局。您可能会使用 Android Studio 中的内置预览创建一个布局，但在实际的手机或平板电脑上看起来很糟糕。虽然可以在预览中切换不同的屏幕尺寸和分辨率，但这可能会很麻烦。如果这是困扰你的事情，你很幸运！Android Studio 4.0 增加了布局验证视图，让你一次看到你的布局在各种不同的屏幕尺寸和分辨率下会是什么样子。

## 所有 API 的 Java 8 去糖

为 Android 开发的另一个恼人的部分是试图使用 Java 8 的特性。也许你找到了一些实现流的代码，或者你想使用 lambda 函数。也许你甚至需要一个不切实际的 Java 8 API。一段时间以来，Android Gradle 插件已经能够将一些 Java 8 功能编译到旧的 API，但从 Android Studio 4.0 开始，所有 Java 8 功能现在都应该得到支持。

* * *

这个列表远非详尽无遗。这些只是 Android Studio 4.0 中一些更有趣的新增功能。以下是由 Google 提供的最新版本中引入的主要新增强功能和特性的摘要:

## Android Studio 4.0 变更日志概述

**设计**

*   运动编辑器:创建、编辑和预览`MotionLayout`动画的简单界面
*   升级的布局检查器:实时和更直观的调试体验
*   布局验证:跨多个屏幕维度比较您的用户界面

**开发&简介**

*   CPU Profiler 更新:改进使用户界面导航更直观，数据更容易理解
*   R8 规则更新:代码收缩器规则的智能编辑器功能，如语法突出显示、完成和错误检查
*   IntelliJ IDEA 2019.3 平台更新，提高了性能和质量
*   实时模板更新:为您的 Kotlin 代码提供 Android 专用的实时模板
*   cland 支持:默认情况下打开 cland 和 Clang-Tidy

**建造**

*   构建分析器:理解并解决构建中的瓶颈
*   Java 8 语言支持更新:无论应用程序的最低 API 级别如何，您都可以使用 API
*   特性对特性的依赖性:定义动态特性模块之间的依赖性
*   buildFeatures DSL:启用或禁用离散的构建功能，如数据绑定
*   Kotlin DSL:对 Kotlin DSL 脚本文件的基本支持

如果你想了解关于这次更新的更多信息，请务必[查看谷歌的博客文章](https://android-developers.googleblog.com/2020/05/android-studio-4.html.)和[的发布说明](http://d.android.com/studio/releases#4-0-0)以了解全部细节，或者观看下面嵌入的视频以获得可视化概述。