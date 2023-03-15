# Moto G4 Plus 支持 64 位定制 rom

> 原文：<https://www.xda-developers.com/moto-g4-plus-64-bit-custom-roms/>

# Moto G4 Plus 支持 64 位定制 rom

Moto G5 Plus 在我们的论坛上获得了对定制 rom 的 64 位支持，现在 Moto G4 Plus 也获得了同样的待遇。

智能手机制造商有时会做出奇怪的决定。例如，摩托罗拉发布了搭载 [32 位安卓操作系统](https://www.xda-developers.com/developer-brings-64-bit-rom-support-moto-g5-plus/)的 [Moto G4 Plus](http://xda-developers.com/tag/g4-plus) 和 [Moto G5 Plus](http://xda-developers.com/tag/moto-g5-plus) ，尽管事实上这两种处理器都能够运行 64 位软件。这从来没有多大意义——大多数 Android 应用程序需要 64 位软件支持，包括流行的[谷歌摄像头 HDR+端口](https://www.xda-developers.com/google-camera-hdr-customization-raw-support/)。但还是有希望的:XDA 认可的开发商 [vache](https://forum.xda-developers.com/member.php?u=1829889) 为 Moto G5 Plus 带来了 64 位支持，现在 XDA 认可的开发商 [Dreamstar](https://forum.xda-developers.com/member.php?u=6158043) 已经为 Moto G4 Plus 提供了 64 位解决方案。

这些说明相当简单，发布在 XDA 的 Moto G4 Plus 论坛上，同时发布的还有 64 位 LineageOS 15.1 的下载链接、设备树、内核树、供应商树和 64 位启用的 [TWRP](http://xda-developers.com/tag/twrp) 。在 Moto G4 Plus 和 Moto G5 Plus 的 64 位环境中，除了系统服务器 *app_process* 之外的所有系统进程都在 64 位模式下运行。(app_process 在 32 位模式下运行，因为当它在 64 位模式下运行时，手机的传感器无法正常工作。)64 位模式允许更好的能效，理论上来说，[更好的性能](https://www.xda-developers.com/developer-brings-64-bit-rom-support-moto-g5-plus/)。

如果你对在 Moto G4 Plus 上运行 64 位应用程序的前景感兴趣，请查看论坛线程。不过，请注意，由于软件的性质，它很可能有问题——这种类型的端口往往比大多数端口更难，因为定制 ROM 开发人员无法在没有一点尝试和错误的情况下编辑设备驱动程序和供应商 blob[。](https://www.xda-developers.com/cameras-custom-roms-developers-make-hardware-work-without-source-code/)

* * *

[**查看 Moto G4 Plus 的 64 位 rom！**](https://forum.xda-developers.com/moto-g4-plus/development/dev-64-bit-roms-kernel-twrp-t3724261)