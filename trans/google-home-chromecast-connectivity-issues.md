# 这就是为什么许多 Google Home 和 Chromecast 设备会导致网络问题

> 原文：<https://www.xda-developers.com/google-home-chromecast-connectivity-issues/>

**2017 年 1 月 18 日更新:**谷歌已经开始通过 Google Play 服务 11.9.74 测试版推出针对 Cast Wi-Fi 漏洞的补丁。如果你还没有注册 Google Play 服务测试版，你可以在[这里](https://developers.google.com/android/guides/beta-program)注册——最新版本将自动安装在与你的 Google 账户相关的 Android 设备上。

**2017 年 1 月 17 日更新:**谷歌周三发布了一个[支持页面](https://support.google.com/googlehome/answer/7634752?hl=en&ref_topic=7071995)，详细说明了问题的原因。“在某些情况下，Android 手机上的 Cast 软件中的一个错误可能会错误地发送大量网络流量，从而降低速度或暂时影响 Wi-Fi 网络，”该页面称。“对网络的具体影响因路由器而异。”这家搜索巨头将于 1 月 18 日发布一个修复程序，并建议在此期间，有问题的人应该尝试重启他们的 Android 手机，并检查以确保他们的路由器运行的是最新的固件版本。

* * *

如果你在拿起[谷歌 Chromecast](https://www.xda-developers.com/google-chromecast-apple-tv-amazon/) 或[谷歌 Home](https://www.xda-developers.com/google-home-sales-top-6-million/) 音箱的时候开始遇到 Wi-Fi 连接问题，你并不孤单。正如 TP-Link 的工程师最近详述的那样，谷歌的“ [Cast](https://developers.google.com/cast/) 协议和使用该协议的无线网络的不稳定性之间存在潜在的必然结果。

随着 TP-Link Archer C1200 路由器的新测试固件(硬件版本 1、2 和 3)，TP-Link 工程师发布了他们发现的 Google Cast 网络漏洞的完整解释。Android 手机和平板电脑以及支持 Cast 的谷歌应用程序，如 YouTube、Google Play Movies & TV 和 Google Photos，通过所谓的 MDNS 数据包或“多播域名服务器”数据包与谷歌 Home 和谷歌 Chromecast 设备保持活跃的连接。MDNS 将设备的主机名(即分配给这些设备的网络名称)解析为 IP 地址，通常用于没有 DNS 服务器的本地网络。它们通常每 20 秒左右发送一次，但当一些支持谷歌 Cast 的设备进入睡眠状态时，它们会继续排队发送新的数据包，直到被唤醒并解锁。这可能会在短时间内导致超过 100，000 个数据包的激增——发送的数据包数量与设备保持休眠状态的时间成正比。这当然会导致连接问题，但也会导致 Wi-Fi 路由器崩溃，并影响其许多核心服务。唯一的解决办法就是重启无线路由器。

这个错误不仅限于 Archer C1200 用户。TP-Link Archer C7 [用户](https://productforums.google.com/forum/#!msg/googlehome/MmnsVnSxdQc/qBJF2KJ1AQAJ)报告了同样的崩溃，Synology 和 Linksys 路由器的[所有者](https://www.reddit.com/r/Android/comments/7qb3k3/having_wifi_issues_lately_router_problems_linked/)也报告了同样的崩溃。

如果你遇到了这个问题，TP-Link 建议现在禁用 Android 手机和/或平板电脑上的 Cast 功能。或者，它建议断开所有支持 Cast 的设备与 Wi-Fi 网络的连接，直到谷歌发布修复程序。

您可以在源链接上查看 TP-Link 的故障，以及用于 Archer C1200 的修复该问题的测试版固件更新。

* * *

[**来源:TP-Link**](http://www.tp-link.com/us/faq-2050.html)[**Via:Reddit**](https://www.reddit.com/r/Android/comments/7qk7rq/tplink_engineer_explains_wifi_disconnections_tied)