# 革命性的 VPN 项目 WireGuard 增加了对 Android ROMs 的支持

> 原文：<https://www.xda-developers.com/wireguard-vpn-project-support-android-roms/>

很难想象没有 VPN 的现代互联网。多年来，VPN 将专用网络扩展到了整个公共网络，使用户能够通过共享或公共网络发送和接收数据，就像他们的计算设备直接连接到专用网络一样。因此，这产生了允许用户绕过特定地理限制以及保持数据安全的效果。然而，VPN 软件的前景有无数的问题，WireGuard，一种新的安全隧道协议，旨在解决这些问题。

* * *

## OpenVPN、IPsec 及其问题

现在 Android 上比较知名的 VPN 解决方案是 OpenVPN 和 IPsec，但也不是没有问题。OpenVPN 的流行有点道理，因为它比 IPsec 更容易配置，并且已经存在很长时间了。虽然这个项目对大多数用户来说是一个可以接受的解决方案，但是它的复杂性是压倒性的。OpenVPN 包含大约 120，000 行代码。如此大量的代码使得项目几乎不可能被审计和保护，正如过去几年中大量的安全漏洞所证明的那样。OpenVPN 也存在于用户空间中，这使得它非常慢，因为每个包都必须被复制几次，并导致几次上下文切换。IPsec、IKEv2、L2TP、PPTP 和相关的 90 年代技术也非常流行，但同样存在问题，它们是庞大的代码库——strong swan 大约有 430，000 行代码，此外，还有整个内核 XFRM 层——并且基于过时的 90 年代加密智慧。这些协议的日常使用也非常“闲聊”，发送不必要的流量，导致笔记本电脑和移动电话的电池寿命缩短。

* * *

## 一个激动人心的新 VPN 项目:WireGuard

最近，我们有幸与我们公认的开发人员之一 zx2c4 进行了交谈。在现实生活中，他是 Jason Donenfeld，是下一代 VPN 隧道 **WireGuard** 的作者，该隧道可能很快会取代 OpenVPN 和 IPsec。于 2015 年推出的 [WireGuard](https://www.wireguard.com/) 提供了最先进的加密技术，更容易审计，因为它**不到 4000 行代码**，并且非常容易使用。

WireGuard 是一种新颖的 VPN，它运行在 Linux 内核中，利用了最先进的加密技术。它的目标是比 IPSec 更快、更简单、更精简、更有用，同时避免令人头痛的问题。它的性能比 OpenVPN 高得多。WireGuard 被设计为一个通用的 VPN，可以在嵌入式接口和超级计算机上运行，适用于许多不同的环境。它在 UDP 上运行。

WireGuard 在安全社区和内核社区内的反响都非常积极，Linux 内核的稳定维护者 Greg KH 在彻底的代码审查后[认可了它](http://plus.google.com/+gregkroahhartman/posts/jD6N4BzToa3)。《T2》已经在世界各地上演，其中[的福斯德姆的演出](http://video.fosdem.org/2017/Janson/wireguard.mp4)可能与 XDA 的读者特别相关。WireGuard [白皮书](https://www.wireguard.com/papers/wireguard.pdf)也通过了学术界的同行评审。

该协议非常适合移动电话，因为它是作为“秘密 VPN”开发的，默认情况下不发送任何数据包，除非有实际数据要发送。这使得**不会像其他 VPN 客户端那样耗尽电池**。此外，WireGuard 允许在不同的 IP 地址之间自由漫游，这意味着您可以在 WiFi 和蜂窝连接之间转换，或在任何其他类型的连接之间转换，而不必建立任何连接；这是完全无缝的。

**的速度是同类**中最好的，提供 SSSE3、AVX、AVX2、AVX512 和 NEON 加速的算法实现。它使用 ChaCha20 意味着它在几乎所有硬件上都非常快。在测试中，WireGuard 轻松击败了其他协议。

[WireGuard](https://www.wireguard.com/) 不仅是该领域最快的 VPN，而且加密技术也已经过[正式验证](https://www.wireguard.com/formal-verification/)，这意味着有数学证据表明其加密结构在符号模型中是安全的。虽然密码学是现代的，但它也是保守的，是偏执的错误，而不是轻率的错误。从安全角度来看，结合其微小且易于审计的代码库，WireGuard 非常可靠。

* * *

## WireGuard 和 Android 支持

虽然 WireGuard 主要是作为 Linux 的优化内核模块开发的，但用户空间可移植版本正在开发中，因此它可以在 Play Store 的应用程序中分发，而无需 root 访问。然而，尽管用户空间的实现仍然比竞争对手更快，但当使用本机内核模块时，WireGuard 的许多神奇之处都大放异彩。因此，XDA 开发社区对 WireGuard 的主要兴趣在于将内核模块直接集成到 rom 中。

事实上，WireGuard 已经进入了一些 rom。最值得注意的是，它被集成到了 Sultanxda 为 OnePlus 3/3T 开发的流行 rom 中，其他开发者肯定会跟进。修补程序非常简单，只需几个简单的步骤就可以完成。找到参考资料的最好地方是 [android_kernel_wireguard git 库页面](https://git.zx2c4.com/android_kernel_wireguard/about/)以及 [zx2c4 关于将其添加到 rom](https://forum.xda-developers.com/android/development/wireguard-rom-integration-t3711635)的 XDA 线程。

目前正在开发的 Android 应用程序如果可用的话，会有机会使用内核模块，否则就退回到使用用户空间实现。该应用程序有一个 GUI 来定义 VPN 隧道，检查状态，并非常好地在通知区域添加了一个切换开关来打开和关闭隧道。下面你可以看到该应用早期版本的简单切换界面。

WireGuard 开发团队目前正在招募 Android GUI 开发人员，与他们一起工作，推动核心技术的进步。如果任何 XDA 开发者感兴趣，他们应该毫不犹豫地联系 zx2c4。WireGuard 项目是完全开源和透明的。

总体而言，WireGuard 似乎是 VPN 和安全网络隧道的未来，它包含坚如磐石的现代密码术、安全的可审计代码库和非常适合智能手机的创新协议。它在 Linux 服务器和桌面上的使用已经得到了高度重视，正在稳步向主流 Linux 前进。我们 XDA 期待着看到 WireGuard 进入 Android 和我们的 rom。

如果您急于在您的设备上测试 WireGuard，请联系您的 ROM 开发者，或者自行重新编译 ROM。你也可以从[官方线程](https://forum.xda-developers.com/android/development/wireguard-rom-integration-t3711635)或 [Google Play 商店](https://play.google.com/apps/testing/com.wireguard.android)获取该应用的 alpha 版本。

* * *

[**访问 XDA** 上的 WireGuard 线程](https://forum.xda-developers.com/android/development/wireguard-rom-integration-t3711635)