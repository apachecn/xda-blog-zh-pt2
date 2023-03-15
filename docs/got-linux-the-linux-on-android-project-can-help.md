# 有 Linux 吗？Android 上的 Linux 项目可以提供帮助

> 原文：<https://www.xda-developers.com/got-linux-the-linux-on-android-project-can-help/>

Linux——我相信你们大多数人对它都很熟悉。如果你不是，这里有一个快速的[视觉指南](https://lh3.googleusercontent.com/-9BOXH-32RFY/T8TEcCTeVUI/AAAAAAAARd4/aAKdvxNy-PI/Mac%2B%2BWindows%2BLinux.jpg)。由于 Android 操作系统和 Linux 之间的紧密联系，有几种不同的方法可以在 Android 设备上运行基于 Linux 的操作系统。然而，我想在这里讨论的是最简单的一个，目的是让尽可能多的设备可以访问 Linux。

Android 上的 Linux 项目是 XDA 知名开发者 zacthespack 的创意，它是一种在你的 Android 设备上运行各种 Linux 发行版的简单且非破坏性的方法。它使用众所周知的方法 *[chroot](http://en.wikipedia.org/wiki/Chroot) ，*，并在你设备上的一个虚拟机中运行发行版。这样做的主要好处是，除了明显占用一些存储空间之外，您的设备上没有任何更改或覆盖，您的当前设置保持不变。可以使用 VNC 来访问你选择的发行版的 GUI。或者，如果您是一个经验丰富的 linux 用户，您可以使用终端。目前支持的 Linux 发行版有 Ubuntu、Debian 和 Backtrack。

附带的应用程序，被称为“[完整的 Linux 安装程序](https://play.google.com/store/apps/details?id=com.zpwebsites.linuxonandroid&feature=more_from_developer#?t=W251bGwsMSwxLDEwMiwiY29tLnpwd2Vic2l0ZXMubGludXhvbmFuZHJvaWQiXQ..)”，本质上是一个工具，它将指导你尽可能简单地设置一切。当我说简单的时候，我是认真的。该应用程序将让您立即启动并运行。对于方法论和项目运行的更详细的描述，然后查看原始的[论坛帖子](http://forum.xda-developers.com/showthread.php?t=1585009)。

您可能已经猜到，这需要 root 访问权限。它应该可以在大多数中/高规格设备和大多数 rom 上工作。开发者也渴望听到你们中任何一个拥有 Nexus 7 并想测试它的人的意见。他非常希望能够支持该设备，但目前他自己无法获得，需要~~豚鼠~~测试员。因此，如果你有一个 Nexus 7，并想测试这个方法，请停止线程，让他知道它是如何工作的。