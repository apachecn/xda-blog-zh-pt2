# Android 4.4 KitKat 工厂映像和驱动程序二进制文件现可用于 Nexus 4、7(全部)和 10

> 原文：<https://www.xda-developers.com/android-4-4-kitkat-factory-images-and-driver-binaries-now-available-for-nexus-4-7-all-and-10/>

自从 [Android 4.4 KitKat 发布](http://www.xda-developers.com/android/new-in-android-4-4-kitkat-everything-you-need-to-know/ "New in Android 4.4 KitKat: Everything You Need to Know")以来，问题很快变成了除了[谷歌 Nexus 5](http://forum.xda-developers.com/google-nexus-5) 之外的设备[何时能看到商品](http://www.xda-developers.com/android/android-4-4-coming-soon-to-the-nexus-4-7-10-moto-x-new-droids-htc-one-and-sgs4-gpe-not-gnex/ "Android 4.4 Coming Soon to the Nexus 4, 7, 10, Moto X, New Droids, HTC One and SGS4 GPe; No 4.4 for the Galaxy Nexus")。我们已经看到各种非官方版本的不支持设备弹出。事实上，我们已经为一些目前可用的更受欢迎的设备突出了相当多的高功能版本。但直到昨天，如果你想以官方身份享受 Android 4.4 KitKat，你需要拥有一台 Nexus 5。

随后，谷歌[为](http://www.xda-developers.com/android/official-android-4-4-kitkat-available-for-nexus-7-and-10-nexus-4-soon/ "Official Android 4.4 KitKat Available for Nexus 7 and 10, Nexus 4 Soon") [Nexus 7](http://forum.xda-developers.com/nexus-7) (仅 WiFi)[Nexus 7(2013，仅 WiFi)](http://forum.xda-developers.com/nexus-7-2013)和 [Nexus 10](http://forum.xda-developers.com/nexus-10) 推送了官方 KitKat OTA 更新，并且 [OTA 链接很快被抓取](http://www.xda-developers.com/android/android-4-4-ota-updates-captured-for-nexus-10-and-7-both/ "Android 4.4 OTA Updates Captured for Nexus 10 and 7 (Both)")。然而， [Nexus 4](http://forum.xda-developers.com/nexus-4) (以及带有移动数据的 Nexus 7 变种)的时间表仍然悬而未决，唯一的官方声明是它将很快到来。显然，“很快”实际上是指第二天。为此，官方的 Android 4.4 KitKat 恢复映像现在可用于 Nexus 4、Nexus 7(所有变体和两年)和 Nexus 10。与此同时，专有的驱动程序二进制文件使 ROM 开发人员能够为这些设备创建全功能的版本。奇怪的是，Nexus 4 的 OTA 更新还没有开始进入手机。也就是说，我们无法想象这款设备的 KitKat 图像已经发布了太久。

如果您是最终用户，安装就像下载映像并执行 *flash-all.bat* 文件一样简单。或者，您可以通过执行命令 *fastboot <分区名称> <镜像名称和路径>* ，提取可用的归档文件并通过 fastboot 逐段刷新它们。这将使您能够在不丢失数据的情况下进行闪存。

您可以通过访问 [Nexus 工厂映像](https://developers.google.com/android/nexus/images)和 [Nexus 驱动程序二进制文件](https://developers.google.com/android/nexus/drivers)页面开始。

更新:看起来谷歌网站上的一些更新链接目前已经关闭。我们认为这是因为它们可能被上传到网站上。请不时尝试，因为我们相信它们很快就会上线。

非常感谢读者 Sampo S .寄来的提示！]