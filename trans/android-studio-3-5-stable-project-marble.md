# Android Studio 3.5 随着来自 Project Marble 的所有修复和增强变得稳定

> 原文：<https://www.xda-developers.com/android-studio-3-5-stable-project-marble/>

早在 2018 年 11 月，谷歌就向 Android 工作室推出了一种名为“ [Project Marble](https://www.xda-developers.com/android-studio-3-3-stable-release-project-marble/) ”的东西。不过，这不是另一款消息应用。相反，谷歌通过改进 Android 应用程序开发工作流程，做了一些前所未有的事情。

如果你错过了，大理石项目并不是真正的单一产品或服务。更确切地说，这是一个总括术语，指的是谷歌在改善 Android Studio 稳定性方面的工作，Android Studio 是谷歌的 Android 应用程序开发程序的选择。在 Project Marble 的生命周期中，谷歌一直更专注于修复 Android Studio 的漏洞和提高性能，而不是引入新功能。

在测试版更新几个月后，谷歌发布了 Android Studio 3.5 的稳定版本，标志着大理石项目的结束(但不是错误修复的结束)。以下是该版本带来的一些显著特性和改进:

### 用户界面冻结

如果你经常使用 Android Studio，你可能会注意到这个问题。在看似随机的时间，Android Studio 会简单地冻结 1 秒到 1 分钟，甚至直到你强制关闭它。显然，当你试图开发一个应用程序时，这是一件非常烦人的事情。

随着 Android Studio 3.5 的推出，谷歌努力改善这种情况。它并不完美，但迄今为止所做的肯定是值得赞赏的。在 XML 中编辑数据绑定表达式现在可以更快地减少延迟。

### 构建速度

Android 应用程序开发的另一个长期问题是构建应用程序所需的时间。除非你有一个非常强大的计算机，编译可能需要 3 分钟以上。如果你只是为了调试一个问题而做一些小的改动，那就需要很长时间了。

这个新版本的 Android Studio 为应用程序编译带来了两个显著的改进。第一个是注释处理器的增量编译。如果你在应用中使用 Dagger 和 Realm 这样的库，你应该会注意到构建时间变短了。

第二个改进与 Windows 上的磁盘 I/O 有关。Windows Defender(现在称为 Windows Security)具有实时扫描文件(在创建或修改文件时)的功能，以保护您免受恶意软件的攻击。但是，这种扫描会显著降低应用程序的构建速度。Android Studio 3.5 现在将显示一个提示，告诉你可以采取哪些步骤来将你的项目目录从这个实时保护中排除，以加快构建速度。

### 应用更改

Android Studio 3.5 中另一个值得注意的变化是引入了 Apply Changes，它取代了旧的即时运行框架。Instant Run 的本意是让你更容易对你的应用程序进行小的修改和测试，但通常情况下，它会导致问题。

为了解决这个问题，谷歌已经完全放弃了即时运行，并从头开始构建应用更改。它应该比即时运行更可靠、更快。

* * *

如果你是使用 Android Studio 3.4 或更早版本的 Android 开发者，这个更新绝对值得一试。您应该会注意到总体性能和稳定性的显著提高。要获得 Android Studio 3.5，要么[从谷歌网站](https://developer.android.com/studio/)下载，要么检查当前版本的更新。

**来源:[安卓开发者](https://android-developers.googleblog.com/2019/08/android-studio-35-project-marble-goes.html)**