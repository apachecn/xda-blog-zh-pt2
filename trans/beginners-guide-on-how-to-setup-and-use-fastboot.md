# 关于如何设置和使用 Fastboot 的初学者指南

> 原文：<https://www.xda-developers.com/beginners-guide-on-how-to-setup-and-use-fastboot/>

快速启动是我们直接从电脑上刷新映像的最重要的工具之一。几乎所有使用 HTC 或 Nexus 设备的人都使用过它，要么是通过命令行，要么是通过利用 fastboot 的自动化工具。

毕竟，这就是我们如何在 Nexus 设备上执行我们都知道并喜爱的 *fastboot oem unlock* 命令。然而，您可以使用 fastboot 做更多的事情。现在多亏了 XDA 公认的贡献者[德姆特](http://forum.xda-developers.com/member.php?u=4334383)，我们有了一个简单且非常容易理解的指南，教你如何设置快速启动，它能做什么，你如何使用它，以及为什么你会想使用它。

在与 ADB 进行比较并向初学者简要介绍了它能做什么之后，初始设置包括两个选项:通过 Android SDK 手动设置，或者使用更自动化的工具来获得必要的二进制文件。在此之后，基本的快速启动命令将被涵盖，如擦除现有分区或用映像刷新它。提供了示例输出文本，以便您第一次自己动手时知道会遇到什么情况。

如果你是一个从未使用过 fastboot 的新用户，现在是学习的好时机。前往[导丝](http://forum.xda-developers.com/showthread.php?t=2277112)了解更多信息。