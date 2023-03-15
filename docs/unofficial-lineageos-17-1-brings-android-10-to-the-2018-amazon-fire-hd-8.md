# 非官方的 LineageOS 17.1 将 Android 10 带到了 2018 亚马逊 Fire HD 8

> 原文：<https://www.xda-developers.com/unofficial-lineageos-17-1-brings-android-10-to-the-2018-amazon-fire-hd-8/>

# 非官方的 LineageOS 17.1 将 Android 10 带到了 2018 亚马逊 Fire HD 8

基于 Android 10 的 LineageOS 17.1 的非官方版本现已用于 2018 年亚马逊 Fire HD 8，这是由 XDA 知名开发商 Kaijones23 提供的。

亚马逊的 Fire 系列平板电脑可能会提供很多价值，但该公司为了实现这些价格标签，走了很多捷径。以亚马逊 Fire HD 8 为例——2018 版[推出](https://www.xda-developers.com/amazon-fire-hd-8-android-nougat/)搭载 Fire OS 6(基于安卓牛轧糖！)，但这款平板电脑尚未获得一次重大的操作系统更新。虽然你可以[将 Google Play 服务和谷歌 Play 商店](https://www.xda-developers.com/amazon-fire-hd-8-google-play-store/)加载到设备上，[禁用一系列软件强加的限制](https://www.xda-developers.com/amazon-fire-toolbox-helps-install-google-apps-change-launchers-and-more-on-amazon-fire-tablets/)，但亚马逊定制的 Android 软件在许多情况下都存在不足，根本不可能进行修补。幸运的是，你可以利用漏洞解锁 Fire HD 8 (2018) [的引导加载程序，并随后安装 TWRP，这意味着 Fire OS 可以被替换为接近库存的 Android 版本。](https://www.xda-developers.com/208-amazon-fire-hd-8-unlocked-rooted/)

**[亚马逊 Fire HD 8 XDA 论坛](https://forum.xda-developers.com/hd8-hd10)**

XDA 公认的开发者 [Kaijones23](https://forum.xda-developers.com/member.php?u=9605864) 已经为 2018 年的 Fire HD 8 [编译了非官方的 LineageOS 构建了一段时间](https://forum.xda-developers.com/hd8-hd10/orig-development/rom-lineage-16-0-t3981685)，现在他已经为这款平板电脑提供了**第一个基于 Android 10 的 LineageOS 17.1 ROM** 。请记住，Fire HD 8 内部的[联发科 MT8163](https://www.mediatek.com/products/tablets/mt8163) 芯片并不强大，硬件支持的解码目前在 ROM 中被打破，所以你可能会偶尔遇到延迟。尽管 SoC 支持 64 位，但该型号上的 Android 操作系统运行在 32 位模式下。因此，在刷新 ROM 之后，你必须选择谷歌应用套件的 ARM 版本。

根据开发者的说法，LineageOS 17.1 在平板电脑上的当前迭代应该被视为测试版。虽然大多数功能都工作正常，但在推荐用作日常驱动程序之前，ROM 仍需要进行一些改进。用于构建这个 ROM 的[内核源代码](https://github.com/mt8163/android_kernel_amazon_karnak)和[设备树](https://github.com/mt8163/android_device_amazon_karnak/)被托管在 GitHub 上，因此其他开发者可以提交补丁并修复现有的 bug。尽管如此，如果你仍然想在 2018 Fire HD 8 上试用 Android 10，你可以前往下面链接的 XDA 线程，找到安装说明和下载链接。

**[非官方 LineageOS 17.1 为 2018 亚马逊 Fire HD 8——XDA 线程](https://forum.xda-developers.com/hd8-hd10/orig-development/rom-lineage-17-1-t4134829)**