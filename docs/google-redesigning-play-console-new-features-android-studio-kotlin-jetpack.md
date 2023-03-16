# Google Play 控制台、Android Studio、Kotlin 和 Jetpack 获得新功能

> 原文：<https://www.xda-developers.com/google-redesigning-play-console-new-features-android-studio-kotlin-jetpack/>

Android 11 测试版可能刚刚发布，但如果你是一名开发人员，还有更多值得兴奋的事情。随着 Android 11 的推出，谷歌为开发者推出了一系列好东西，包括新的 Google Play 控制台设计，新版本的 Android Studio，以及一系列 AndroidX 和 Kotlin 更新。

## Google Play 控制台重新设计

首先，我们来谈谈新的 Google Play 主机。自从引入新的材料设计准则以来，谷歌一直(慢慢地)更新其各种应用程序和网站，以适应新的设计语言，最终包括 Play 控制台。在设计更新的基础上，事情已经重新组织了一点。谷歌表示，有一个新的用户管理系统来帮助你处理你邀请到你的控制台帐户的人，以及一些其他功能来“帮助你在 Google Play 上茁壮成长”。

你可以在下面看到一些新设计的截图。

## Android Studio 4.1 和 4.2

下一个新事物是 Android Studio。谷歌发布了两个新版本:4.1 测试版和 4.2 加那利版。这些版本中有大量的新特性，所以我们只讨论一些更有趣的特性。

如果你做过很多开发(或修补)，你可能知道无线 ADB。ADB 的这一功能允许您使用 IP 地址而不是电缆连接到您的设备。不幸的是，它很难被启用。你要么需要摆弄正常的 ADB，要么有一个根设备。嗯，有了 Android Studio 4.2，你需要的只是一台运行 Android 11 或更高版本的设备，你马上就能运行无线 ADB。

Android 模拟器现在是 Android Studio 的一部分。在撰写本文时，还不清楚这意味着什么，但谷歌表示，它将实现更快、更集成的自动化测试。

最后(对于这个子列表)，运行 Android 11 或更高版本的设备的应用构建应该更快。

下图显示了两个版本中的新功能。

## 科特林和安卓

现在我们来谈谈[科特林](https://www.xda-developers.com/tag/kotlin/)和[安卓克斯](https://www.xda-developers.com/android-jetpack-components-kotlin-android-studio-3-2/)。Kotlin 可能已经成为 Android 开发中最流行的语言。它比 Java 更简洁，有各种助手方法，支持扩展功能，还有很多其他的功能，使它比 Java 更容易使用。由于所有这些优势，Google 官方推荐 Kotlin 作为 Android 开发使用的语言。

首先，Kotlin 本身有一些新功能。Android Studio 现在支持 Kotlin 1.4，它带来了一大堆新东西。1.4 的主要特性之一是 Kotlin 接口的 SAM 转换。一段时间以来，Kotlin 已经自动将单方法 Java 接口转换为 lambdas，以获得更好的可读性。然而，这种转换不适用于在 Kotlin 中声明的接口；在 1.3 中，即使只有一个单一方法的 Kotlin 接口，您也必须写出整个实现。在 Kotlin 1.4 中，这不再是必要的。只需用`fun`修饰符标记你的单方法 Kotlin 接口，你就能以 lambda 的形式使用它们。

你可以在这里和这里阅读更多关于科特林 1.4 [的内容。](https://blog.jetbrains.com/kotlin/2020/03/kotlin-1-4-m1-released/)

然而，这还不是全部。Kotlin 有一个强大的特性，叫做协程。协同程序类似于 Android 的[现在已经废弃的 AsyncTask](https://www.xda-developers.com/asynctask-deprecate-android-11/) ，但是有更多的特性，更好的语法，更容易阅读。三个 AndroidX 库，Lifecycle、WorkManager 和 Room，现在都支持 Kotlin 的协同程序，这使得在使用这些库时更容易处理异步逻辑。

## Jetpack 复合

如果你错过了谷歌发布的各种公告，Jetpack Compose 是一种在原生 Android 项目中设计布局的新方法。Compose 不是命令式的 XML 布局设计，而是一个完全用 Kotlin 编写的声明性框架。它的第一个开发者预览版已经有一段时间了，但是从今天开始，你将可以试用它的第二个开发者预览版。这个版本中有许多新功能，包括:

*   与原生 Android 视图的互操作性
*   动画片
*   基于适配器的列表
*   布局更改的实时预览(以前需要重建项目)
*   代码完成

谷歌希望在今年夏天的某个时候发布 Compose 的 alpha 版本，完整版本预计在 2021 年的某个时候发布。

* * *

这就是我们今天的全部！并非所有的新东西都在这篇文章中，所以请务必查看谷歌的官方声明以了解更多细节。你可以在【YouTube 播放列表中看到谷歌刚刚发布的所有 12 场演讲，在谷歌的“【Android 11 周”期间每周了解新的开发者内容，并在[在线 Android 11 社区聚会](http://d.android.com/android11/meetups)期间相互学习。