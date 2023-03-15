# BraveDNS 是一个 DNS-over-HTTPS 客户端、防火墙和广告拦截器

> 原文：<https://www.xda-developers.com/bravedns-open-source-dns-over-https-client-firewall-adblocker-android/>

用售后 ROM 取代工厂安装的操作系统不仅仅局限于 Android 生态系统。早在 Android 智能手机兴起之前，人们就开始改造基于 Linux 的无线路由器和接入点，以实现包过滤、防火墙或广告拦截等功能，这些功能在普通固件中并不存在。不出所料，Android 世界也非常需要这样的功能。虽然自 Android Pie 以来，可以配置私有 DNS(或 HTTPS DNS)并随后阻止 Android 设备上的广告，但最终用户仍然需要依赖第三方应用来设置适当的防火墙。如果你正在寻找一款集防火墙、广告拦截器、甚至 HTTPS 域名系统客户端于一身的应用，BraveDNS 可能会让你感兴趣。

“BraveDNS”这个名字听起来像是另一个 DNS 解析服务，但它肯定不止于此。这款免费开源的应用程序将自己描述为“一个受[open snick](https://github.com/evilsocket/opensnitch)启发的防火墙和网络监视器+一个受 [pi-hole](https://github.com/pi-hole/pi-hole) 启发的带有黑名单的 HTTPS 客户端 DNS”。DoH 客户端模块主要基于另一个流行的开源项目 [Intra](https://github.com/Jigsaw-Code/intra) ，使用自己的广告、跟踪器和间谍软件拦截 DNS 端点。开发团队还提供他们自己的 DNS 解析服务，作为那些需要定制阻止列表、允许列表、存储 DNS 日志以供以后分析等功能的人的付费选项。

以下是该应用目前提供的功能列表:

1.  HTTPS 的 DNS(规避审查，防止互联网服务提供商和其他人对 DNS 日志的监视)。
2.  查看 DNS 日志。
3.  由 [oisd_dbl](https://dbl.oisd.nl/) 和[激活保护](https://energized.pro/)支持的 BraveDNS 广告、跟踪器和间谍软件拦截 DNS 端点
4.  按应用类别划分的防火墙。
5.  防火墙单个应用。
6.  当应用程序在后台(非活动使用)时设置防火墙。
7.  设备锁定时的防火墙。

Google Play 和网站上的 BraveDNS 最新版本至少需要 Android 8 Oreo，但开发者计划在不久的将来让它兼容所有 Android 棉花糖。此外，对双模 DNS 和防火墙执行的支持承诺将被反向移植到传统的 Android 版本。

你可以从下面的 Play Store 链接下载 BraveDNS 应用程序，或者从[他们的官方网站](https://www.bravedns.com/)获取[APK](https://download.bravedns.com/)。

**勇敢者:[github rest](https://github.com/celzero/brave-android-app/)| |[xda 论坛线程](https://forum.xda-developers.com/android/apps-games/app-bravedns-anti-censorship-adblocker-t4144243)**

(app box Google play " com . celzero . bravedns ")