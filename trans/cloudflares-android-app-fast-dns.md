# CloudFlare 的新 Android 应用程序让您可以轻松启用他们的快速 DNS

> 原文：<https://www.xda-developers.com/cloudflares-android-app-fast-dns/>

今年早些时候， [CloudFlare 向公众推出了自己的 DNS 服务](https://www.xda-developers.com/cloudflare-dn-magisk-module/)，名为“1.1.1.1”。CloudFlare 的 DNS 解析器不同于您的 ISP 或其他 DNS 替代方案，如 Google Public DNS 和 Cisco OpenDNS，因为它首先关注隐私和速度。您的 IP 地址不会被记录或保存在 CloudFlare 的服务器上，根据 CloudFlare 的说法，通过多项优化，1.1.1.1 比其他 DNS 解决方案快 28%。它也有助于对抗审查——众所周知，土耳其和委内瑞拉等国家会审查和屏蔽新闻媒体、社交网络和成人网站，一种替代的 DNS 解析器有助于克服这种限制。1.1.1.1 也可以在 Android 手机上使用，但对于 Android Oreo 和更低版本的设备来说，这并不是一个简单的过程。幸运的是，CloudFlare 推出了一款应用程序来简化这一过程。

过程很简单:只需下载应用程序，打开它，点击切换按钮，使用 CloudFlare 的 1.1.1.1 DNS，并通过它进行导航。它也相当轻便，只有 7.8 MB。最棒的是。它不需要 root 或任何其他修改:只需打开它，点击，然后去。唯一的缺点是？该应用程序使用 Android 的 VPN API 来连接替代的 DNS 解析器。这意味着如果你使用 1.1.1.1，你将无法同时使用一个真正的 VPN 提供商。

如果你在 Android Pie 上，那么你不需要这个应用程序，因为 Android Pie 支持 TLS 上的 DNS。要使用 CloudFlare 的 DNS，只需执行以下操作:

*   转到设置应用程序并点击网络和互联网。
*   选择“专用 DNS 模式”。
*   对于专用 DNS 提供商主机名，输入:1dot1dot1dot1.cloudflare-dns.com
*   保存。

如果你没有 Android Pie，也不想使用这个应用，你就必须使用 root 方法:[有一个 Magisk 模块](https://www.xda-developers.com/cloudflare-dn-magisk-module/)用于使用 1.1.1.1 DNS。

最后，如果你没有根和/或你不介意使用第三方应用程序，那么 CloudFlare 的新应用程序应该会创造奇迹。点击下面的链接查看。

* * *

[**来源:CloudFlare**](https://blog.cloudflare.com/1-thing-you-can-do-to-make-your-internet-safer-and-faster/)