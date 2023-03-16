# 越狱你的 iPhone 使用一个根 Android 手机，并检查 ra1n

> 原文：<https://www.xda-developers.com/jailbreak-apple-iphone-using-checkra1n-rooted-android-phone/>

我们很多人在 XDA-Developers.com 的时候第一次偶然发现了这个论坛，当时我们正在寻找我们的 Android 设备。毕竟，[我们的论坛](https://forum.xda-developers.com/)在这一点上已经超过 17 年，目前拥有超过 1000 万成员，这些年来已经创建了超过 340 万个线程和 7700 万个帖子——为帮助爱好者扎根他们的设备并充分利用它们创造了宝贵的社区资源。根深蒂固的 Android 手机为发烧友社区打开了大量的机会，为各种疯狂的事情打开了大门——例如，破解你的 iPhone。

越狱 iPhone 类似于在其核心概念中扎根 Android 设备——你本质上是授予自己升级的权限，并禁用 OS、iOS 和 Android 分别内置的许多保护。虽然由于合作的原始设备制造商，让几款流行的 Android 手机扎根已经在很大程度上成为一件小事，但由于苹果及其围墙花园的方法，越狱 iPhone 仍然是一个不断变化的挑战。每次发布越狱，苹果都会努力修补导致越狱发生的漏洞，为未来的设备和未来的软件更新关闭相同解决方案的大门。因此，越狱往往是非常具体的手机和 iOS 版本，也需要非常具体和非常特殊的步骤才能取得成功。

Checkra1n 是一个越狱解决方案，被认为是运行 iOS 13 的苹果设备的第一个越狱。它还可以在各种苹果硬件上运行。因为它利用了针对苹果硬件启动 ROM 中的缺陷而不是 iOS 中的漏洞的漏洞，所以它也被认为是唯一可以在易受攻击的手机上跨软件更新工作的解决方案之一。然而，作为缺点，Checkra1n 是一种半束缚越狱，这意味着每次重启设备时都需要重新越狱。更不方便的是，越狱最初[只能通过 MacOS v10.10+](https://ios.cfw.guide/installing-checkra1n) 实现——如果你的手机不按计划重启，这极大地限制了你的选择。

不过最近， [Checkra1n 获得了对 Linux](https://twitter.com/checkra1n/status/1224992759473496064?s=21) 的支持，使得使用 Linux 电脑越狱 iOS 13 设备成为可能。显然，这扩大了你可以使用的可能平台，但正如 [Reddit 用户/u/stblr 发现的](https://www.reddit.com/r/jailbreak/comments/fctkfp/news_it_is_possible_to_run_checkra1n_from_an/)，这也可以通过让你使用一部根深蒂固的 Android 智能手机越狱来解决半束缚越狱的不便之处！

Reddit 用户/u/stblr 注意到一些先决条件:

1.  当然，首先你需要一台兼容 Checkra1n (iPhone 5s 到 iPhone X，iOS 12.3 及以上)的 iPhone 或 iPad。
2.  具有 root 访问权限的 Android 设备，最好是较新的 Linux 和 Android 版本。视频演示使用的是索尼 Xperia XZ1 Compact，运行在 Android 10 上，采用 Linux 内核 4.14，并以 Magisk 为根。
3.  Android 手机上的终端应用程序。
4.  连接两部手机的方法。苹果的一些 USB-C 到 Lightning 的电缆无法工作，因为它们缺少将 iDevice 置于 DFU 模式的引脚。

与 iOS 社区过去见过的一些更复杂的方法相比，越狱的步骤出奇的简单:

1.  [下载用于 Linux 的 Checkra1n 二进制文件](https://checkra.in/releases/#all-downloads)，注意您的 Android 设备的正确 arch:
    1.  您可以在连接手机的情况下，通过在计算机上运行以下 ADB 命令来检查手机的架构:

        ```
         adb shell getprop ro.product.cpu.abi 
        ```

        输出将是您手机的架构。
2.  将下载的二进制文件放到你的 Android 手机的/data 中。您可以[在我们的子论坛](https://forum.xda-developers.com/)中搜索您的设备，了解找到它的最佳方法。
3.  将您的 iDevice 连接到您的 Android 手机。
4.  打开终端 app，通过输入“ *su* 命令获得 root 权限。
5.  键入" *lsusb* "检查您的 iDevice 是否被识别。显示的 USB ID 应该是“ *05ac:12a8* ”。
6.  将您的设备置于 DFU(设备固件升级)模式。你可以在这里找到[特定于设备的指令](https://www.theiphonewiki.com/wiki/DFU_Mode)。
7.  使用“ *lsusb* ”检查您的 iDevice 是否仍被识别。现在显示的 USB ID 应该是“ *05ac:1227* ”。
8.  使用命令"*"在 CLI 模式下运行 checkra1n。/checkra1n -c* ”。
9.  你的设备现在应该越狱了。但是，该方法并不完全可靠，因此您可能需要重试这些步骤才能成功。

这些步骤看起来令人望而生畏，但事实并非如此。如果你有一个根设备，我们可以假设你对按照说明输入几个命令感到舒服。尽管如此，请记住，越狱和生根设备有其自身的风险，所以在没有完全了解你在做什么之前，不要尝试任何一种。