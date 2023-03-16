# 亚马逊消防电视棒 4K 现在可以启动加载解锁

> 原文：<https://www.xda-developers.com/amazon-fire-tv-stick-4k-bootloader-unlock-root-install-twrp-magisk/>

亚马逊 Fire 电视棒 4K 是亚马逊最受欢迎的流媒体加密狗之一。它不仅为连接的设备解锁 4K 视频功能，还支持 HDR10+、杜比视界和杜比全景声。今年早些时候，该设备甚至[通过更新获得了对 Miracast 屏幕镜像](https://www.xda-developers.com/amazon-fire-tv-stick-4k-miracast-screen-mirroring-support-update/)的支持，现在，开发人员已经能够成功解锁其引导加载程序，开辟了更多的可能性。

在最近的一篇[帖子](https://forum.xda-developers.com/fire-tv/orig-development/unlock-fire-tv-stick-4k-mantis-t3978459)中，XDA 资深成员 [k4y0z](https://forum.xda-developers.com/member.php?u=7104332) 重点介绍了一个漏洞，利用这个漏洞你可以解锁你的 Fire TV Stick 4K 的引导程序。然而，这个过程并不像你想象的那么简单。这种方法利用了 XDA 资深会员 [xyz](https://forum.xda-developers.com/member.php?u=9667509) 发现的引导 ROM 漏洞，要求你打开加密狗并做一些硬件改动。

该漏洞的工作方式非常类似于 Fire TV Stick 第二代使用的[漏洞，首先你必须打开设备，移除没有天线一侧的隔热板，然后在电路板上短接特定的点。此外，你需要在你的电脑上安装一个补丁的 Linux 内核，它已经方便地包含在一个 live-ISO 中。您可以从 post 下载 ISO，并将其刻录到 CD 或 USB 闪存驱动器，然后再继续操作说明。](https://forum.xda-developers.com/fire-tv/development/unlock-fire-tv-stick-2nd-gen-tank-t3907002)

简而言之，这个过程包括下载 ISO，用 USB 线将 Fire TV Stick 连接到计算机，并运行一些命令。短路本质上是将设备置于一种能够接收所述命令的状态，并且可以通过拿着导电的东西到达上图中标有 DAT0 的点来容易地实现。

由于这个过程有点棘手，需要物理修改，可以肯定地说，它不适合初学者，并且肯定会使保修无效。开发者还建议用户应该[禁用 OTA 更新](https://forum.xda-developers.com/showpost.php?p=80453643&postcount=37)，尽管 TWRP 将允许安装完整更新，不会有任何问题。用户也被建议避开从 FireOS 内部刷新启动和恢复镜像的应用程序和方法。该主题中的用户已经报告了通过 Magisk 进行根操作的成功。

**[解锁 Bootloader，安装 TWRP 并 Root 亚马逊 Fire 电视棒 4K - XDA 线程](https://forum.xda-developers.com/fire-tv/orig-development/unlock-fire-tv-stick-4k-mantis-t3978459)**