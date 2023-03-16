# 最新的 AOSP GSI 增加了对小米 9 的显示扫描仪的支持

> 原文：<https://www.xda-developers.com/xiaomi-mi-9-custom-aosp-gsi-in-display-fingerprint-scanner/>

# 最新定制的 AOSP GSI 增加了对小米 Mi 9 的显示指纹扫描仪和 2019 年 4 月安全补丁的支持

显示指纹扫描仪一直是定制 ROM 开发商的一个挑战，但最新的 AOSP GSI 应该没有问题的米 9

更新的技术总是令人兴奋。无边框显示器(及其实现前置摄像头的各种方法)、显示器内指纹扫描仪和 3D 人脸扫描技术只是过去两年中推出的一些东西，它们让我们深入了解了智能手机的未来。但通常情况下，这些技术实际上对开发人员社区构成了挑战，特别是对定制 ROM 开发，因为在 AOSP 定制 ROM 中实现这些新技术并不是一个简单的过程。造成这种情况的原因有很多，包括这些技术的前沿性质(可能 AOSP Android 本身一开始就不支持这些技术)以及缺乏适当的文档。

[**小米米 9 XDA 论坛**](https://forum.xda-developers.com/Mi-9)

这些障碍最终被定制 ROM 开发者所克服。最近，我们得知一加 6T 定制 rom 将很快开始[全面支持手机的显示指纹扫描仪](https://www.xda-developers.com/first-oneplus-6t-custom-rom-working-in-display-fingerprint-scanner/)，使这款手机的 rom 向完全稳定的状态迈进了一大步。现在，轮到小米 Mi 9 了，它还带来了光学显示指纹扫描仪。XDA 知名开发商 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 最新的[定制 AOSP GSI](https://www.xda-developers.com/custom-aosp-project-treble-gsi-updated-march-security-patch/) 包括对小米 Mi 9 指纹传感器的支持，允许用户轻松解锁他们的设备，就像在 MIUI 上一样。

phhusson 的 AOSP GSI 上的小米 9 的显示指纹扫描仪。

此次 GSI 中包括的其他变化包括[4 月安全补丁](https://www.xda-developers.com/april-2019-android-security-google-pixel-essential-phone/)，对一些联发科驱动的设备的杂项音频修复，允许使用 Android Pie 供应商映像的三星设备启动，等等。你可以在这里查看整个 T2 的变更日志。如果你想在你的 Mi 9 上或者任何其他兼容 Treble 的设备上测试这个 GSI，你可以从[这里](https://github.com/phhusson/treble_experimentations/releases/tag/v112)下载它，但是记住，作为一个非常通用的，一刀切的 rom，你可能会遇到一些意想不到的问题。