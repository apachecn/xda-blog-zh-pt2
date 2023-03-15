# 谷歌拉后，闪光短信 DoS 信息 HushSMS

> 原文：<https://www.xda-developers.com/google-pulls-hushsms-after-flash-sms-dos-info/>

不久前，我们谈到了影响当前 Nexus 设备阵容的[Flash SMS(0 级)DoS 漏洞](http://www.xda-developers.com/android/google-nexus-devices-vulnerable-to-dos-attacks-protect-yourself-with-simple-app/ "Google Nexus Devices Vulnerable to DoS Attacks, Protect Yourself with Simple App")。罗马尼亚安全研究人员波格丹一世·亚历克发现了这一漏洞，即快速连续发送的 Flash SMS(0 类)消息会在各种 Nexus 设备上导致意外行为。奇怪的是，这个漏洞只影响了 Nexus 设备用户。

幸运的是，这个漏洞从来没有那么具有破坏性。毕竟，迄今为止看到的最糟糕的结果是由于设备重启导致的数据丢失。也就是说，该漏洞肯定会让用户受到恼人的恶作剧和垃圾邮件的影响，从而影响基本的工作效率。

现在，该漏洞已经取得了第一次重大胜利，尽管是以一种有点出乎意料的方式。不，不存在基于漏洞的恶意攻击。应用程序开发者 Michael Mueller 的 HushSMS 已被 Google Play 商店删除，原因是“违反了内容政策的危险产品条款以及开发者分发协议的第 4.3 和 4.4 节。”这是为了一个已经在 Play store 中可用了大约 10 个月的应用程序，以及一个“可以根据 3GPP 规范 23.040‘短消息服务的技术实现’和一些其他规范(如 OMA WAP)发送消息”的应用程序，如穆勒本人所述。

虽然我们中的许多人都期待着即将到来的 Android 4.4.1 的官方修复，但我们不禁认为这是谷歌对这个问题的一个相当奇怪的“解决方案”。作为参考，HushSMS Play 商店列表的[谷歌缓存页面仍然可用。可以在下面的源代码链接中找到来自开发人员的更多信息。](http://webcache.googleusercontent.com/search?q=cache:-0DoJaZ4GCUJ:https://play.google.com/store/apps/details%3Fid%3Dcom.silentservices.hushsms%26hl%3Den+&cd=1&hl=en&ct=clnk&gl=us)

*【来源:[软儿科](http://news.softpedia.com/news/Google-Removes-SMS-App-After-Researcher-Presents-Details-of-Flash-SMS-Flaw-405550.shtml)*