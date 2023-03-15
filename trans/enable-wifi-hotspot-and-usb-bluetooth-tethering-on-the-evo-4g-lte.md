# 在 EVO 4G LTE 上启用 WiFi 热点和 USB /蓝牙共享

> 原文：<https://www.xda-developers.com/enable-wifi-hotspot-and-usb-bluetooth-tethering-on-the-evo-4g-lte/>

全新的 EVO 4G LTE 是 HTC 在 EVO 产品线中的最新产品。显而易见，EVO 系列设备中最有用和最受欢迎的 mod 之一迟早会出现。通过简单的 *build.prop* 编辑(或者方便的 flash 化 *update.zip* ，感谢 XDA 资深会员 [smw6180](http://forum.xda-developers.com/member.php?u=670396) )你现在可以启用原生 USB 和蓝牙网络共享，以及解锁你设备上的原生 WiFi 热点。

XDA 公认的开发者 [aamikam](http://forum.xda-developers.com/member.php?u=1278360) 发现该编辑可与新的 EVO 4G LTE *build.prop* 一起工作，并通过高级成员 [kaos420](http://forum.xda-developers.com/member.php?u=746545) 到达我们的社区。奇怪的是，mod 在你的 *build.prop* 中增加了一行，这一行以前在最初的 EVO 4G 上发现过，在新的 EVO 上也有效。

> ro.tether.denied=false

那些喜欢使用可恢复闪存的人应该继续使用[修改线程](http://forum.xda-developers.com/showthread.php?t=1704991)。在更改你的 *build.prop* 文件之前，请务必阅读整篇文章并备份你的整个设备。