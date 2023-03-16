# Android P 将最终限制应用程序监控你的网络活动

> 原文：<https://www.xda-developers.com/android-restrict-apps-monitor-network-activity/>

一个持续多年的隐私漏洞将最终在 Android 上终结。这是一个你可能从未听说过的问题，但却是你绝对应该关注的问题。目前，Android 上的应用程序可以**完全访问你设备上的网络活动**——**，甚至无需请求任何敏感权限**。这些应用程序无法检测*你网络通话的内容*，但是它们可以通过 TCP/UDP 嗅探任何传出或传入的连接，以确定你是否连接到某个服务器。例如，一个应用程序可以检测到您设备上的另一个应用程序何时连接到金融机构的服务器。不相信我？只需[在 Play Store 上下载众多 netstat 应用程序中的一个](https://play.google.com/store/search?q=netstat)并亲自体验。

Netstat Plus 应用程序检测到我的手机连接到大通银行。

任何应用程序都可以检测到**你的设备上还有哪些应用程序连接到互联网**，而且它们还可以告诉**这些应用程序何时连接到互联网**以及**它们在哪里连接到互联网**。显然，这是谷歌最终解决的一个严重的隐私漏洞，但恶意软件的影响也相当严重(为了不给任何人任何想法，我们不会深入细节。)我听说过 Play Store 上的一些可疑应用程序使用这种方法来检测你何时连接到他们不同意的服务。脸书、推特和其他社交媒体应用程序可以在你不知情的情况下利用这个来追踪你的网络活动。

* * *

## Android P 即将修复

Android 开源项目中出现了一个新的 commit 来“启动锁定 proc/net 的过程”/proc/net 包含了内核中与网络活动相关的一系列输出。目前对访问/proc/net 的应用没有限制，这意味着他们可以从这里读取(尤其是 TCP 和 UDP 文件)来解析你设备的网络活动。可以在手机上安装一个终端 app，输入`cat /proc/net/udp`自己看。

但是由于 Android 的 SELinux 规则有了新的变化，对这些信息的访问将会受到限制。特别是，这一变化适用于 Android P 的 SELinux 规则，这意味着只有指定的 VPN 应用程序才能访问其中的一些文件。系统将审核寻求访问的其他应用程序。出于兼容性的考虑，似乎针对 API 等级< 28 的应用程序现在仍然可以访问。这意味着[直到 2019 年，应用程序必须以 API 等级 28 为目标](https://www.xda-developers.com/play-store-updated-requirements-api-level-64-bit/)，大多数应用程序仍然可以不受限制地访问。

我们可能会在未来的 Android P 开发者预览版中看到这一变化。如果你使用的是自定义 ROM，比如 [CopperheadOS](https://copperhead.co/android/docs/usage_guide#network-connection-information--statistics) ，那么你已经很安全了，因为这些 SELinux 的改动在几年前就已经完成了。我们很高兴看到 Google 在多年的无限制访问之后终于限制了对/proc/net 的访问。这是一个非常小的变化，用户不太可能注意到，但对用户隐私的影响将是巨大的。我们只是希望这个补丁能被移植到早期的 Android 版本中，这样它就可以在每月的安全补丁更新中应用。

更正:这篇文章的最初版本报道了 Android 7.1+将会进行修复。在与精通 SELinux 的开发人员讨论后，这一变化似乎适用于运行在 Android P 上的针对 API 级别 28 的应用程序