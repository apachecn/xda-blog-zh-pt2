# 谷歌相机 HDR+端口增加了对 LG 智能手机广角镜头的支持

> 原文：<https://www.xda-developers.com/google-camera-hdr-lg-v30-wide-angle-lens/>

非官方谷歌相机 HDR+端口[的第一个版本于 8 月](https://www.xda-developers.com/google-camera-hdr-ported/)发布。它使谷歌相机的 HDR+技术可用于非 Nexus 和 Pixel 设备，并已被证明在许多情况下[显著提高图像质量](https://www.xda-developers.com/google-camera-hdr-xiaomi-redmi-note-3/)。从那以后，该端口接收了许多更新，包括 [RAW 支持](https://www.xda-developers.com/google-camera-hdr-customization-raw-support/)，支持运动照片，支持[人像模式](https://www.xda-developers.com/google-camera-mod-portrait-mode-lens-blur-4k-video/)，等等。事实上，它正迅速成为基于高通的设备最受欢迎的 mod 之一(并且[它现在也可以在一些基于 Exynos 的设备上运行](https://www.xda-developers.com/google-camera-mod-exynos-portrait-mode-galaxy-s8-s7-note-8/))。

然而，港口并没有摆脱它的问题。它在 OnePlus 5 等一些设备上仍然存在漏洞，而且它的一些配置在相当多的设备上无法工作。更值得注意的是，该端口不支持任何设备上的双摄像头。

Android 设备上的双摄像头[可以有几种类型](https://www.xda-developers.com/a-brief-history-of-the-past-present-and-future-of-dual-camera-smartphones/)。一些设备具有 RGB +单色双后置摄像头，而其他设备则使用广角和长焦镜头。其他人仍然使用辅助摄像头来进行深度感测。第四类双摄像头是普通+广角镜头。这类相机在很多 LG 手机中使用，如该公司在 G5，V20，G6 和 V30 上的广角辅助相机。

例如， [LG V30](https://www.xda-developers.com/lg-v30-specs-snapdragon-835-released/) 有一个 1600 万像素的主摄像头，配有索尼 IMX351 传感器、1.0 微米像素和 f/1.6 光圈。它具有光学图像稳定功能(OIS)，以及 71 度的视角。辅助摄像头是广角 1300 万像素摄像头，视角为 120 度，像素为 1.0 微米，光圈为 f/1.9。辅助广角相机是 LG 旗舰智能手机的一个独特的差异化功能，因为它可以拍摄其他智能手机相机无法拍摄的照片。因此，非官方的谷歌摄像头端口不支持它是一个耻辱。

然而现在，XDA 资深成员 [cstark27](https://forum.xda-developers.com/member.php?u=2712580) 发布了他自己的谷歌相机 HDR+端口版本，支持 LG G5、LG G6、LG V20 和 LG v30 的广角相机。它需要通过 Camera2 API 报告广角镜头，因此，它不一定支持 Galaxy Note 8、Nokia 8、小米 Mi A1 或 Essential Phone 等所有设备。

 <picture>![Google Camera LG V30 Wide Angle Lens](img/b33ea71396b349fadbe5a89ebc272430.png)</picture> 

Credits: XDA Junior Member [metartur](https://forum.xda-developers.com/member.php?u=5811475)

如果你有 LG G5，G6，V20 或 V30，你可以前往源代码链接下载支持广角镜头的谷歌相机 HDR+端口的测试版，并亲自查看。

[**下载谷歌相机 HDR+端口带广角镜头支持**](https://forum.xda-developers.com/lg-v30/how-to/google-camera-port-hdr-v30-t3696066/post75364454#post75364454)

据开发者称，这篇文章被更新以反映这一事实，即该 mod 也适用于 LG G5、LG G6 和 LG V20。