# WireGuard VPN 协议进入 Linux 内核 5.6

> 原文：<https://www.xda-developers.com/wireguard-vpn-linux-kernel-5-6/>

虚拟专用网络(VPN)可能是数字时代的重要工具。由于日益增长的隐私问题或简单的地理定位障碍，越来越多的用户正在利用他们信任的 VPN 所提供的增强的隐私和多功能性。随着新冠肺炎迫使数百万工人呆在家里，许多人被迫使用公司拥有的 VPN 远程工作。在过去的几年里，一种新的 VPN 实现方式已经在技术爱好者中生根发芽，并且在不久的将来，它最终将会被数百万用户所使用。这个新实现的名字叫做 [WireGuard](https://www.xda-developers.com/wireguard-vpn-project-support-android-roms/) ，由 Jason Donenfeld 开发，他在我们的论坛上使用的用户名是 [zx2c4](https://forum.xda-developers.com/member.php?u=5434776) 。昨天，他宣布[wire guard 1.0 版](https://www.wireguard.com/known-limitations/)是 Linux 内核 5.6 的一部分(via [*ArsTechnica*](https://arstechnica.com/gadgets/2020/03/wireguard-vpn-makes-it-to-1-0-0-and-into-the-next-linux-kernel/) )。

与 OpenVPN、IPSec 和其他流行的 VPN 实现相比，WireGuard 具有相当小的代码库，从而减少了攻击面。它易于配置，并且比 OpenVPN 具有更快的连接协商。性能和能效也有所提高。然而，这个协议有一些限制。尽管如此，由于它带来的好处，Linux 内核社区已经开始支持它。在将加密实现[放入内核](https://lwn.net/Articles/802376/)之后，WireGuard 现在可以在 Linux 内核 5.6 的树中使用。任何运行 Linux 内核 5.6 发行版的用户都可以开始使用 WireGuard 客户端。虽然像 Arch 和 Gentoo 这样的前沿发行版会很快升级到 Linux 内核 5.6，但其他专注于稳定性的发行版如 Ubuntu 或 Debian 将需要一些时间来进行升级。然而，Donenfeld 先生表示，WireGuard 已经反向移植到 Ubuntu 20.04“Focal Fossa”和 Debian Buster，他还在维护反向移植到 Linux 内核版本 5.4.y 和 5.5.y。

至于 Android，大多数用户需要等待一段时间才能使用 WireGuard VPN 隧道。尽管 Android 是建立在 Linux 内核之上的，但是运行在大多数 Android 设备上的内核已经相当过时了。例如，我运行 Android 11 的 Pixel 3 是基于 2016 年发布的 Linux 内核 4.9 构建的。供应商可以将 WireGuard 所需的内核补丁移植到设备的旧内核树中，但不知道这是否会发生。最有可能的是，我们将不得不等待谷歌为最新的 Linux 内核版本启动一个新的 Android 公共内核分支，然后硅制造商基于新版本生产新的 SOC，但这可能需要一些时间才能发生。与此同时，期待在我们的论坛上看到 WireGuard 在定制内核中日益流行。

虽然将 WireGuard 集成到主流 Linux 内核中肯定是一个受欢迎的举措，会让许多系统管理员和一些用户兴奋不已，但我们希望看到新的 VPN 协议能够进入更多的平台。截至目前，WireGuard 的 Windows 版本为 0.1.0 测试版。自其最初的预览版发布以来，WireGuard 0.1.0 for Windows 对性能和稳定性进行了重大改进，因此我们应该有望在不久的将来看到一个稳定的版本。