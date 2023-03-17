# Google Pixel 3 和 Pixel 3 XL 工厂图像和内核源代码上线

> 原文：<https://www.xda-developers.com/google-pixel-3-factory-images-kernel-source-code/>

上周，谷歌终于通过[宣布这两款设备](https://www.xda-developers.com/google-pixel-3-google-pixel-3-xl-specs-features-pricing-availability/)结束了 Pixel 3 的泄露流。尽管有许多泄漏，但仍有一些细节等待被发现。我们在[对这款设备的初步评测](https://www.xda-developers.com/google-pixel-3-xl-camera-software-design-pixel-stand/)是积极的:谷歌继续在计算摄影方面表现出色，Pixel 3 是他们成功的证明。虽然普通消费者关注的是 Pixel 3 的相机性能，但许多 Android 爱好者喜欢 Pixel，因为它干净，接近 Android 的版本。我们已经看到[实时壁纸被移植](https://www.xda-developers.com/download-google-pixel-3-live-wallpapers-port/)，开发者已经在尝试[将夜视和谷歌镜头建议](https://www.xda-developers.com/pixel-3-google-camera-port-night-sight-live-google-lens/)移植到其他设备上。现在工厂图像和内核源代码已经发布，开发者将能够开始对 Pixel 3 的软件进行更多的修改。

### 工厂图像

随着工厂图像的发布，开发者现在可以安全地尝试修复设备并刷新 TWRP 了。我个人一直在等待这些，因为没有启动映像备份，就没有办法从拙劣的 Magisk 安装中恢复。但对于那些一直在等待 Pixel 3 的应用程序和其他系统文件的开发者来说，工厂图像让你可以访问设备上的一切。期待在几天或几周内看到 Magisk 模块为您的设备添加一系列 Pixel 3 功能。

| 

设备

 | 

版本

 | 

下载链接

 |
| --- | --- | --- |
| 谷歌像素 3(蓝线) | 9 月安全修补程序的 9.0.0 (PD1A.180720.03X) | [链接](https://developers.google.com/android/images#blueline) |
| 谷歌像素 3 XL(交叉线) | 9 月安全修补程序的 9.0.0 (PD1A.180720.03X) | [链接](https://developers.google.com/android/images#crosshatch) |

### 内核源代码和 DTS

内核源代码和设备树源代码已经上传，因此开发人员很快就可以开始为设备构建 TWRP 和定制内核。我知道 XDA 认可的开发者 Dees_Troy 将很快收到他的设备，所以我们将从该项目的主要开发者那里得到一个正常工作的官方 TWRP 版本。对于其他内核开发人员来说，Pixel 3 的内核源代码是一个很好的方式来研究谷歌是如何让新的 Pixel 如此高性能的。我们将在评测的第二部分测试 Pixel 3 XL 的性能，敬请关注！

设备树源代码和内核源代码可以在下面的链接中找到。

[**查看谷歌 Pixel 3 和 Pixel 3 XL 的设备树来源**](https://android.googlesource.com/device/google/crosshatch/)

[**查看谷歌 Pixel 3 和 Pixel 3 XL 的内核源码**](https://android.googlesource.com/kernel/msm/+/android-9.0.0_r0.31/)

* * *

最后，要了解这两款设备的最新发展，请务必查看下面的设备论坛。

[**访问谷歌 Pixel 3 论坛**](https://forum.xda-developers.com/pixel-3)

[**访问谷歌 Pixel 3 XL 论坛**](https://forum.xda-developers.com/pixel-3-xl)

*本文在美国东部时间下午 5:39 更新，以反映 DTS 和内核源代码已经完全上传。*