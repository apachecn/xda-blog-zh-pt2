# Android 13 终于通过 HTTPS 增加了对 DNS 的原生支持

> 原文：<https://www.xda-developers.com/android-13-dns-https-support/>

Android 从 Android 9.0 Pie 开始就支持 DNS-over-TLS (DoT)。它可以在你的手机的网络和互联网设置下的名称为私人 DNS。去年 9 月，在安卓开源项目(AOSP)中发现的一个代码变化表明，谷歌正计划在安卓 13(T1)中添加 DNS over HTTPS 支持。现在终于正式宣布了。

正如斯珀的米沙·拉赫曼所发现的，Android 13 终于增加了对 HTTPS 域名系统的原生支持。在最基本的层面上，DoT 和 DoH 都做同样的事情:加密 DNS 流量。TLS 上的 DNS 使用 TLS(也称为 SSL)来加密流量，而 HTTPS 上的 DNS 使用 HTTP 或 HTTP/2 协议来发送 DNS 查询和响应。

但是，使用 DoH 代替 DoT 有一些优点。DoT 使用一个专用端口，在这个端口上，网络层的任何人都可以看到传入和传出的流量——然而，内容本身仍然是加密的。另一方面，DoH 使用端口 443，这是 HTTPS 流量的标准端口。因此，通过 DoH 发送的请求和流量可以隐藏在其余的 HTTPS 流量中，使得攻击者或网络管理员几乎不可能监控或阻止 DoH 查询。像 Mozilla Firefox 和 Google Chrome 这样的流行浏览器已经提供了对 HTTPS 域名的支持。

目前，在运行 Android 13 DP2 的设备上，似乎没有通过 HTTPS 访问 DNS 的面向用户的设置。但是，斯珀报告说，它可以通过“netd_native”命名空间下的 device_config 布尔标志“doh”来启用。

AOSP 最近的代码变化表明，谷歌正在考虑在 Android 13 中默认启用 DoH 支持，尽管这还不是最终决定。

Android 13 带来了大量新功能，包括自动主题化图标、每应用程序语言支持、对蓝牙 LE 音频的完全支持、通知的运行时权限等等。此外，最新版本还在 Camera2 API 中启用了 [HDR 视频支持，并引入了新的](https://www.xda-developers.com/android-13-hdr-vide-stream-use-case-camera2-api/)[游戏 API，可以显著减少游戏加载时间](https://www.xda-developers.com/android-13-game-loading-mode-improvements/)。

* * *

**来源** : [斯珀](https://www.blog.esper.io/android-13-deep-dive/#dns_over_https)