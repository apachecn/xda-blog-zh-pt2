# Realme X3 超级变焦得到非官方的引导加载程序解锁方法，而 Realme C3 收到它的官方

> 原文：<https://www.xda-developers.com/realme-x3-superzoom-gets-unofficial-bootloader-unlock-method-realme-c3-receives-official/>

Realme 通常为他们的手机提供可解锁的引导加载程序，但你不能简单地使用典型的快速启动解锁命令来完成任务。除非你在处理[的 Realme 2 或 C1](https://www.xda-developers.com/realme-2-c1-coloros-bootloader-unlock/) ，否则你必须首先安装一个名为**深度测试**的特定型号应用程序，以验证引导加载程序解锁的资格。该应用程序从目标设备向 Realme 服务器发送一组唯一标识符，以生成解锁令牌。在成功的服务器端验证之后，应用程序本身会在手机上安装令牌，然后只有您可以继续使用`fastboot flashing unlock`来执行剩余的解锁过程。然而，似乎在某些情况下，现有的*深度测试*应用程序可以强制在不支持的模型上运行。“黑客”足够稳定，可以解锁 Realme X3 SuperZoom 的引导加载程序。

在[回顾 Realme X3 SuperZoom](https://www.xda-developers.com/realme-x3-superzoom-review-an-actual-flagship-killer/) 时，我们自己的 [Zachary Wander](https://www.xda-developers.com/author/zacharywander/) ，在论坛上更为人所知的是 XDA 认可的开发者[zachare 1](https://forum.xda-developers.com/member.php?u=7055541)，发现[为 Realme 6 Pro](https://www.xda-developers.com/realme-6-pro-bootloader-unlock-tool-unofficial-twrp-now-available/) 设计的*深度测试*应用程序也可以用于执行 X3 SuperZoom 的引导加载程序解锁。该应用程序可能会抛出一些关于设备不兼容的错误，但你可以很容易地[改变你的 Realme X3 SuperZoom](https://forum.xda-developers.com/x3-superzoom/how-to/guide-switch-software-region-to-allow-t4136341) 上的区域设置来绕过它们。解锁引导程序将会重置你的设备，但是如果你希望[启动你的设备](https://forum.xda-developers.com/x3-superzoom/how-to/guide-root-realme-x3-superzoom-magisk-t4136333)，这是绝对必要的。

**[Realme X3 SuperZoom XDA 论坛](https://forum.xda-developers.com/x3-superzoom)** **[指南解锁 Realme X3 SuperZoom 的 boot loader](https://forum.xda-developers.com/x3-superzoom/how-to/guide-unlock-bootloader-realme-x3-t4136325)**

根据 Zachary 的说法，这个技巧可能也适用于普通的 Realme X3，同时我们可以发现 T2 关于 Realme 6 bootloader 解锁的报告是相互矛盾的。原始设备制造商尚未公布 Realme X3 系列的内核源代码，因此，即使你设法解锁了引导程序，也不要指望这款设备会有源代码定制的 ROM。

Realme C3 也获得了引导程序解锁支持，尽管是通过官方渠道。公司[在四月份发布了这款设备](https://www.xda-developers.com/kernel-sources-for-the-realme-6-6-pro-c3-and-5i-are-now-available/)的内核源代码，现在他们终于发布了 Realme C3 的深度测试 APK。我们希望内核源代码和 bootloader unlocker 应用程序的可用性应该对这款手机上的 kickstart 开发有用。

**[下载 Realme C3 深度测试 APK](https://download.c.realme.com/flash/Unlock_tool_IN/DeepTest_realme_C3.apk) ||| [Bootloader 解锁指南](https://c.realme.com/in/post-details/1285562681092210688)**

**[Realme C3 XDA 论坛](https://forum.xda-developers.com/realme-c3)**