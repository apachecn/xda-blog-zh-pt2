# 一个动漫游戏的根检测是如何导致 LG、一加、华为、小米等公司的手机发现安全漏洞的

> 原文：<https://www.xda-developers.com/procfs-leak-lg-oneplus-huawei-xiaomi-asus/>

普通消费者和技术爱好者每月在超过 20 亿台设备上使用移动 Android 操作系统。尽管与 Android 用户的总体人口相比，解锁引导加载程序并启动智能手机的人数相对较少，但在 XDA 和 Reddit 等论坛上仍有很多人。Magisk 是修补社区不可或缺的工具。它提供无系统的 root 访问，并拥有 MagiskHide 等工具，使 root 用户能够继续使用他们喜欢的应用程序、游戏和服务，而不受限制。然而，一款流行的动漫游戏一直在巧妙地滥用一个系统安全漏洞来绕过 Magisk 的反 root 检测。这是如何工作的，以及哪些设备受到这个安全漏洞的影响。

*   一个游戏用一个 bug 来检测一个设备是否被 rooted 了。如果设备是根用户，游戏会阻止用户玩游戏。
*   该漏洞允许一个应用程序读取内存中其他应用程序的状态，而不需要任何特殊权限。该漏洞不允许应用程序从其他应用程序窃取任何数据。这种小毛病并不严重，而且相当无害。
*   谷歌已经意识到这个问题，并更新了他们的测试工具，以确保所有设备都得到保护。

## 背景

一个叫做命运/大秩序的流行动漫游戏阻止了根用户尝试玩这个游戏。XDA 认出了开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) ，Magisk 的首席开发者，之前[发现了绕过 Fate/Grand Order 的根检测的方法](https://www.xda-developers.com/fate-grand-order-fortnite-mobile-magisk/)，但是尽管他尽了最大努力，他的解决方案在他的 OnePlus 6 上并不起作用。这位开发人员决心不放弃，他分析了 Fate/Grand Order 来弄清楚它是如何在他的一加设备上检测到 root 的。正如他在他的[媒体帖子](https://medium.com/@topjohnwu/from-anime-game-to-android-system-security-vulnerability-9b955a182f20)中解释的那样，这让他发现了一个安全漏洞，Fate/Grand Order 似乎正在滥用这个漏洞来继续检测一加设备上的 root 访问。

## Procfs 和 Android

在基于 Unix 的操作系统上，有一个称为“procfs”的特殊文件系统，它包含进程(比如应用程序)的信息，比如它们的内存使用情况(比如 RAM)、状态(进程是否正在运行、是否处于睡眠状态等等。).在大多数基于 Unix 的操作系统上，用户和应用程序可以很容易地访问 procfs，以查看他们的系统上正在运行什么类型的应用程序和服务(就像 Window 的任务管理器一样)。)然而，谷歌从 Android 7.0 牛轧糖开始[锁定对 procfs](https://issuetracker.google.com/issues/37091475) 的访问。在 Android Nougat 之前，SystemPanel 等应用程序可以收集正在运行的应用程序的数据，而不需要任何特殊权限。在 Android Nougat 之后，应用程序需要使用像 [UsageStats](https://developer.android.com/reference/android/app/usage/UsageStats) 或 [AccessibilityService](https://developer.android.com/reference/android/accessibilityservice/AccessibilityService) 这样的 API，这两者都受到权限的限制，必须由用户授予权限。

Google 通过使用标志“hidepid=2”挂载/proc 来防止应用程序通过 procfs 读取其他应用程序的状态。通过使用 hidepid=2 挂载 procfs，应用程序只能看到自己进程的状态。因此，应用程序需要使用 UsageStats 或 AccessibilityService 等公认的 API 来获取设备上正在运行的应用程序和服务的信息。

## 弱点

如果 procfs 没有挂载 hidepid=2 怎么办？那么，应用程序将能够自由地读取系统上运行的其他应用程序(和挂载点)的状态，而不需要任何额外的权限*。Google 在自己的设备上挂载 hidepid=2 的 procfs，但是他们不会在其他厂商的设备上强制执行这个要求。LG、一加、华为/Honor、小米和其他公司的几款设备尚未安装 hidepid=2 的 procfs，这是 Fate/Grand Order 等应用程序用来检测 Magisk 是否存在于设备上的功能。

* Android 9 Pie 中的一个安全变化阻止了应用程序读取自己的“SELinux 上下文”之外的信息，因为每个应用程序现在都是单独隔离的。SELinux 是一个内核模块，充当某种看门人的角色，阻止应用程序和服务访问它们不应该访问的文件。SELinux 上下文就像一个文件的标签，其中包含用户和角色等信息。如果没有为 procfs 启用 hidepid=2 标志，具有相同 SELinux 上下文的应用程序可以读取相同上下文中其他应用程序的信息。在运行 Android 9 Pie 的设备上，只有针对 Android Pie 构建的应用程序才会应用 Android Pie 的新 SELinux 更改。以 Android 8.1 Oreo 或更低版本为目标的应用程序将使用旧的 SELinux 规则，允许它们在相同的 SELinux 上下文中访问有关进程的信息，只要 procfs 安装时没有 hidepid=2。由于新的 Google Play 要求，在你的设备上运行的大多数应用程序至少应该针对 Android 8.0 Oreo，但许多应用程序还没有更新到针对 Android Pie。

下面的截图显示了不挂载 hidepid=2 的 procfs 的后果。

## 这有多糟糕？

如果我们将这个系统漏洞与类似[【fuseégelée】](https://www.xda-developers.com/nvidia-tegra-x1-google-pixel-c-nvidia-shield/)[blue borne](https://www.xda-developers.com/bluetooth-vulnerability-blueborne-impacts-android-ios-windows-and-linux-devices/)[KRACK](https://www.xda-developers.com/wpa2-wifi-protocol-vulnerability-krack/)和 [Meltdown/Spectre](https://www.xda-developers.com/chromebook-meltdown-spectre-how-to-check/) 的漏洞进行比较，那么这个 bug 相比之下就相形见绌了。**应用程序无法利用这一点获得 root 访问权限或窃取您的密码。您的银行账户和信用卡都很安全。一个应用程序所能做的最糟糕的事情就是判断另一个应用程序是否正在你的设备上运行，这种用途非常有限。请记住，这是许多 GNU/Linux 发行版的标准行为，Google 只是最近才开始用 Android Nougat 阻止对 procfs 的访问。这个 bug 允许应用程序绕过需要某些权限来监控其他进程，但它们仍然无法打破 Android 的沙箱，并从其他应用程序中窃取数据。无论如何，这是无意的行为，破坏了 Android 的隐私功能，因此必须修复。**

## 我的设备受到影响了吗？

以下是我们发现的无法使用 hidepid=2 挂载 procfs 的设备列表:

| 

设备原产商

 | 

设备

 | 

安卓版本

 | 

procfs 泄漏

 |
| --- | --- | --- | --- |
| 华硕 | ZenFone 5Z | 安卓 8.0 奥利奥 | 是 |
| 黑莓 | 按键 2 | 安卓 8.0 奥利奥 | 不 |
| 必要的 | PH-1 | 安卓 9 派 | 不 |
| 谷歌 | 像素 2 | 安卓 9 派 | 不 |
| 谷歌 | 像素 3 | 安卓 9 派 | 不 |
| 谷歌 | 像素 3 XL | 安卓 9 派 | 不 |
| 荣耀 | 魔法 2 | 安卓 9 派 | 是 |
| 常简称为 HTC 或宏达电 | U12+ | 安卓 8.0 奥利奥 | 是 |
| 华为 | Mate 20 X | 安卓 9 派 | 是 |
| 水平规ˌ水准仪(Level Gauge) | G7 ThinQ | 安卓 8.0 奥利奥 | 是 |
| 水平规ˌ水准仪(Level Gauge) | V40 ThinQ | 安卓 8.1 奥利奥 | 是 |
| 摩托罗拉 | Moto G4 | 安卓 8.1 奥利奥 | 不 |
| 诺基亚（总部设在芬兰） | 7.1 | 安卓 8.1 奥利奥 | 不 |
| 一加 | 6 | 安卓 8.1 奥利奥/安卓 9 派 | 是 |
| 一加 | 6T | 安卓 9 派 | 是 |
| 雷蛇 | 电话 2 | 安卓 8.1 奥利奥 | 是 |
| 三星电子 | Galaxy Note 8 | 安卓 8.0 奥利奥 | 不 |
| 三星电子 | Galaxy Note 9 | 安卓 8.1 奥利奥/安卓 9 派 | 不 |
| 三星电子 | 银河 S7 | 安卓 8.0 奥利奥 | 不 |
| 三星电子 | 银河 S8 | 安卓 8.0 奥利奥 | 不 |
| 三星电子 | 银河 S9 | 安卓 9 派 | 不 |
| 三星电子 | Galaxy S9+ (Exynos) | 安卓 8.0 奥利奥 | 是 |
| 索尼 | Xperia XZ1 | 安卓 9 派 | 不 |
| 小米 | 米 Mix 2S | 安卓 9 派 | 是 |
| 小米 | POCO F1 | 安卓 8.1 奥利奥 | 是 |

## 如何检查您的设备是否受到影响

很容易检查您的设备是否向其他应用程序泄漏了进程信息(换句话说，procfs 没有使用 hidepid=2 挂载)。虽然您可以像我们一样使用 shell 命令，但是您也可以使用 topjohnwu 开发的应用程序进行检查。如果你的手机是 rooted 的，他的应用程序还允许你用 hidepid=2 重新安装 procfs。

[**下载 ProcGate**](https://github.com/topjohnwu/ProcGate/releases)

## 会有解决办法吗？

**是的，这个问题会在**解决。Google 现在将要求所有设备安装 hidepid=2 的 procfs。他们将通过[更新](https://android-review.googlesource.com/c/platform/cts/+/833984)兼容性测试套件(CTS)来加强这一点，所有设备都必须通过一系列测试才能使用 Google Play 应用和服务。所有 OEM 厂商(希望销售预装了谷歌 Play 商店的设备)必须在不久的将来发布一个更新来重新安装 hidepid=2 的 procfs。由于一加设备是第一个发现此问题的设备，**一加已经意识到此问题，并正在努力解决**。如果其他 OEM 对这个错误发表评论，我们会更新这篇文章，但没有必要怀疑您的设备的 OEM 是否会发布更新。如果他们希望他们的更新通过 CTS，那么他们必须修复这个 bug。