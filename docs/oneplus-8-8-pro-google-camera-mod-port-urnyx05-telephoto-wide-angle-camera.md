# OnePus 8 和 8 Pro 的谷歌摄像头端口可以使用其他摄像头

> 原文：<https://www.xda-developers.com/oneplus-8-8-pro-google-camera-mod-port-urnyx05-telephoto-wide-angle-camera/>

一加 8 和一加 8 Pro 于今年 4 月发布。虽然[一加 8(回顾)](https://www.xda-developers.com/oneplus-8-xda-review/)延续了去年的类似相机，但[一加 8 Pro(回顾)](https://www.xda-developers.com/oneplus-8-pro-review-never-settle-on-hardware/)在相机方面比去年的[一加 7T](https://www.xda-developers.com/oneplus-7t-pro-xda-review/) 系列有了显著改进。这些变化包括更大的 48MP 索尼 IMX689 主传感器，而另一个 48MP 传感器用作超广角摄像头。如果你想将一加 8 系列设备上的摄像头与谷歌丰富的摄影技能配对，下面链接的这个谷歌摄像头端口不仅可以帮助你使用这两款手机上的主摄像头，还可以使用非主摄像头。

**[一加 8 论坛](https://forum.xda-developers.com/oneplus-8)** ||| **[一加 8 Pro 论坛](https://forum.xda-developers.com/oneplus-8-pro)购买:一加 8([₹41,999 首发](https://www.amazon.in/Test-Exclusive-547/dp/B078BNQ318/?tag=xdaportalin-21) ) |||一加 8 pro([₹54,999 首发](https://www.amazon.in/b/ref=s9_acss_bw_cg_oneplus_4d1_w?node=21152978031) )**

谷歌相机的非官方端口在过去的几年中变得非常受欢迎，因为它们将谷歌计算摄影的好处添加到了非谷歌设备中。然而，由于 Pixel 设备已经推出了最多两个摄像头，开发人员需要修改谷歌摄像头端口，以添加对辅助摄像头(即主摄像头以外的摄像头)的支持，如广角或长焦摄像头。

XDA 资深会员 *[Urnyx05](https://forum.xda-developers.com/member.php?u=9040262)* 为一加 8 系列最新推出的谷歌相机端口，可以在旗舰智能手机上实现长焦和超广角传感器。更重要的是，这个 Google Camera mod 不需要添加任何配置 XML 就可以工作。

XDA 的 Max Weinbach 在他的一加 8 Pro 上试用了谷歌相机模式，结果如下所示:

*用 stock Camera 应用程序拍摄的图像在左边，而用 mod 拍摄的图像在画廊的右边*

谷歌相机显然捕捉到了更自然的色彩和更好的对比度。谷歌相机图像中的高光和阴影看起来并不夸张，色彩噪声也较少。谷歌相机模式不会错误地裁剪 3 倍远摄图像，也可以反转任何鱼眼效果，在超广角相机上呈现自然的外观，而不是扭曲的外观

这种模式有一些限制，首先是图像是在 12MP 分辨率下捕捉的，即来自 48MP 传感器(两款手机的主传感器和一加 8 Pro 的广角传感器)的 4 合 1 像素宁滨之后，没有办法以全分辨率捕捉图像。虽然像素宁滨通常是有利的，因为它增加了更多的光线和图像的清晰度，一些用户可能希望捕捉全分辨率的图像，这在这里是无法实现的。此外，目前国防部不支持一加 8 上的微距相机。最后，超广角相机没有防失真功能，所以照片的边缘会扭曲。

如果你拥有这两种设备中的任何一种，你可以从下面的链接下载改装的谷歌摄像头端口。请注意，这个相机模块可能会/可能不会与该公司的旧设备。

[下载一加 8/8 Pro 的谷歌相机端口](https://www.celsoazevedo.com/files/android/google-camera/dev-urnyx05/)

为了启用对辅助相机的支持，该 Google Camera mod 的包名称已被设置为" **org.codeaurora.snapcam** "，这是一个白名单包，位于 devices' build.prop 中的"**vendor . Camera . aux . package list**"属性下。然而，要使用辅助相机，它们必须由 OEM 向 Camera2 API 公开。

* * *

**Via:[Reddit(r/一加)](https://www.reddit.com/r/oneplus/comments/hb9m5p/gcam_can_now_take_advantage_of_auxiliary_cameras/)**