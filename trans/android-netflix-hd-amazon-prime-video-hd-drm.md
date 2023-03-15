# 一些旗舰 Android 手机不支持高清网飞/亚马逊 Prime 视频

> 原文：<https://www.xda-developers.com/android-netflix-hd-amazon-prime-video-hd-drm/>

如果你曾经试图在某些设备上观看[网飞](https://www.xda-developers.com/netflix-app-user-interface-redesign/)或其他付费视频流媒体服务，你可能会注意到，即使你的计划支持高清流媒体视频，视频质量也不会超过 480p。这不一定是你的网速问题，也不一定是网飞应用程序的问题。相反，这完全可能是你的设备本身的问题。

这是因为网飞和亚马逊 Prime Video 等其他服务受到数字版权管理(DRM)服务的保护，在 Android 上需要谷歌 Widevine DRM 解决方案的最安全级别( **Widevine Level 1** )才能向 Android 设备提供高清(720p+)视频内容。缺乏对 Widevine L1 的支持可能会导致高清视频在你的 Android 设备上无法正常播放，无论你的设备有多强大，屏幕分辨率有多高。

今天，我们将了解什么是 Widevine，以及如何检查您的设备是否缺少网飞或亚马逊 Prime Video 高清播放所需的 Widevine L1。

* * *

### Widevine 简介

 <picture>![](img/6c048bc6fec60de558b83f64d3fc0f84.png)</picture> 

Widevine Technologies logo.

Widevine 是最古老、使用最广泛的 DRM 解决方案之一，也是保护数字内容最有效的解决方案之一。它是多平台和多格式的，可用于全球近 40 亿台设备，包括桌面 PC 和设备、运行 Android 或 iOS 的移动设备、电视、蓝光播放器、机顶盒和游戏控制台。Widevine 由 Widevine Technologies 开发，该公司成立于 1999 年，2010 年 12 月被谷歌以 1.6 亿美元收购。

网飞的内容催生了大量的电视剧、电影、纪录片，甚至像《纸牌屋》、《橙色是新的黑色》和《更奇怪的东西》这样的原创系列，这些内容受到 DRM 和加密措施的保护，以避免盗版和录音被用户自由分发。为此，他们使用多种 DRM 解决方案，包括 Google 的 Widevine DRM，因为这是他们支持的平台中很大一部分选择的 DRM 措施。Widevine 也被其他付费流媒体服务使用，如亚马逊 Prime Video。

### 不同的级别，不同的安全等级

虽然所有 Android 设备都支持某种形式的 Widevine，但并不是所有手机都支持相同的级别。有几个不同的级别:第 3 级是最底层的安全层，用于保护标清(480p 及更低)视频和标准质量媒体，然后是第 1 级，用于提供高质量媒体，如高清/FHD/QHD/4K 视频。级别 1 需要硬件支持的 DRM 措施来处理受保护的内容。为了让设备显示来自 Widevine 支持的服务的高清视频，所述设备**必须**支持 L1: L3 将只显示标清视频，而不管您的订阅或设备能力如何。

这给我们带来了另一个问题:并不是所有的旗舰设备都支持 L1，因此不能从网飞输出高清视频。尽管有硬件能力，但旗舰手机不支持 Widevine L1 的一些例子包括**任何一加手机和中兴 Axon 7/M，它们由 Widevine L3** 而不是 L1 支持。谷歌 Pixel 2 XL 等其他旗舰产品确实完全支持 Widevine L1。

目前还不清楚为什么一加和中兴选择跳过 Widevine L1 的认证程序，特别是谷歌 T2 不需要任何授权费用。然而，随着认证的消失，这是一个很容易解决的软件问题。一名一加发言人告诉 *The Verge* 更新将很快在 Widevine L1(以及网飞高清)的支持下推出。

### 让高清网飞开始工作

如果你有三星 Galaxy S8、Galaxy Note8、LG G6、LG V30 等受欢迎的旗舰产品，你应该不会受到影响。然而，如果你的设备，无论什么品牌，不能在网飞或其他应用程序上输出高清视频，你不妨去 Play Store 下载 DRM Info，看看 Widevine 是否是罪魁祸首。

如果 DRM Info 在 Google Widevine DRM 的安全级别下显示“L1 ”,则您的设备能够在网飞和其他应用程序上显示高清视频。如果它仍然不显示高清视频，尽管有完整的 Widevine L1 支持，那么这可能是网飞不得不将你的设备列入白名单，以实现全分辨率视频播放的问题。

不幸的是，这意味着手动修补网飞的应用程序，让它运行。XDA 资深成员[陈小龙](https://forum.xda-developers.com/member.php?u=4277844)已经为[整理了一份指南，让高清网飞在这些设备上工作](https://forum.xda-developers.com/showpost.php?p=65001865&postcount=12)，XDA 初级成员 [GuillaumeBarberousse](https://forum.xda-developers.com/member.php?u=5607337) 为[制作了一个 Ubuntu 脚本](https://forum.xda-developers.com/android/apps-games/app-netflix-hd-widevine-drm-l1-devices-t3307241)，用于自动修补网飞 APK。

另一方面，如果 DRM Info 显示“L3”，那么你就不走运了，因为你的设备目前不支持 Widevine L1。上面的教程对你也不起作用，因为它们是为支持 Widevine L1 的设备设计的，但由于某种原因，它们不支持网飞高清。因此，这是一个向您的 OEM 报告所述问题的问题，他们应该看看是否可以对此采取一些措施。对一加车主来说，至少在不久的将来，一个解决方案正在路上。

现在还不清楚为什么原始设备制造商没有从一开始就通过威德文 L1 的认证程序。这可以归结为他们没有时间为 Widevine L1 认证他们的设备，或者只是不想这样做。几乎每一款 2017 年旗舰设备都支持 Widevine L1 的硬件，因此我们希望明年的手机越来越多地采用它。