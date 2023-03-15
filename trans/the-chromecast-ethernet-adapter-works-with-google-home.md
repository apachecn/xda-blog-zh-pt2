# Chromecast 以太网适配器可与 Google Home 配合使用

> 原文：<https://www.xda-developers.com/the-chromecast-ethernet-adapter-works-with-google-home/>

在去年谷歌 I/O 2016 上宣布谷歌 Home 个人助理设备几周后，有报道称[谷歌 Home 只不过是塞在扬声器里的 Chromecast](https://www.xda-developers.com/xda-external-link/google-home-reported-to-be-a-chromecast-inside-of-a-speaker/) 。该报道来自 The Information，并声称这是真的，因为他们与 [Chromecast](https://forum.xda-developers.com/android-tv/chromecast) 共享相同的微处理器和 WiFi 芯片。Chromecast 真的没有那么多东西，所以谷歌需要做的只是添加一个扬声器、麦克风、LED 灯和一个塑料外壳，然后嘣，你就有了 Google Home。

然后在去年 11 月， [iFixit 发布了他们对 Google Home](https://www.xda-developers.com/ifixit-tears-down-google-home-gives-it-an-8-out-of-10/) 的拆除，并证实这两款设备共享相似的硬件。我们了解到，Google Home 与 2015 年的 Chromecast 共享相同的 CPU、闪存和 RAM。这是一款非常受欢迎的产品，自首次发布以来，谷歌已经售出了数千万台。谷歌甚至为 Chromecast 配备了一个[以太网适配器，可以从谷歌商店以 15 美元的价格购买。](https://store.google.com/product/ethernet_adapter_for_chromecast)

Reddit 用户 LeonJWood 在将他们的 Google Home 设备连接到他们可用的无线网络时遇到了问题。似乎 Google Home 连接 802.1x (WPA2 企业)WiFi 网络有困难，除非你设置了 MAC Auth 来自动允许设备连接。自然，这在一些工作和学校环境中是不允许的，所以他们被迫走另一条路。他们意识到 Chromecast 和 Google Home 产品共享相似的硬件，所以他们从谷歌购买了以太网适配器，看看它是否能工作。

确实有效！你所要做的就是通过后面的端口(被扬声器格栅隐藏)将以太网适配器连接到 Google Home，它就能工作了。他们警告你，网络上的任何人都可以看到并控制你的谷歌主页。他们还注意到，从智能手机向它播放流媒体音乐会导致它不时中断。这可能是由其他问题引起的，因此可能不仅限于此以太网适配器。

[**来源:/r/GoogleHome**](https://www.reddit.com/r/googlehome/comments/5qioz9/hardwired_google_home/dcziy22/)