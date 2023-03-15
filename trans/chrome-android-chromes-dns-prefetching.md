# Chrome for Android 将很快支持 Chrome 的 DNS 预取，以加快网页浏览速度

> 原文：<https://www.xda-developers.com/chrome-android-chromes-dns-prefetching/>

2018 年 1 月 29 日更新:由于一个未指明的错误，异步 DNS 功能[已被恢复](https://chromium-review.googlesource.com/c/chromium/src/+/881206)。

Chrome for Android 将很快支持 DNS 预取，这是一种允许更快浏览网页的技术。

DNS 预取也称为异步 DNS，[自 2012 年](https://plus.google.com/+FrancoisBeaufort/posts/JXcvYw1yCkH)以来一直作为桌面 Chrome 中的一个标志存在，当时它是作为一个实验性功能推出的，默认情况下是禁用的。从那以后，它得到了一些开发人员的关注，在某些情况下，现在可以将页面加载时间缩短几秒钟。

它是这样工作的:当你使用任何网络浏览器访问网页时，你的浏览器查询域名服务器(DNS)以获得该网页的 IP 地址。这是为了消除记住不同网站的 IP 地址号码的需要——想象一下，每次你想访问谷歌时，都必须在浏览器的地址栏中键入“209.85.203.94 ”!这是不切实际的，一个简单得多的替代方法是给网页分配名称，并将这些名称解析回 IP 地址。

世界各地的 DNS 服务器保存着网站及其相关 IP 的数据库，但有一个问题:当你浏览网页时，DNS 查找过程在某些情况下可能需要几秒钟。这使得拥有完美连接能力的人们等待服务器完成域名解析并返回网站的 IP 地址，这就是 Chrome 的异步 DNS 功能的用武之地。

Android 上的谷歌 Chrome 启用了 DNS 预取标志，Chrome 扫描页面中的可点击链接，并将 URL 解析为 IP 地址。当你进入任何一个页面时，它们的地址将会被返回到你的设备上，从而缓解任何 DNS 速度问题——唯一的瓶颈是你自己的连接。(可选地，它将使用你的设备自己的 DNS 服务器，不会接触谷歌的，除非你希望它这样做。)

DNS 预取应该很快就会出现在 Google Chrome for Android 的稳定分支中。