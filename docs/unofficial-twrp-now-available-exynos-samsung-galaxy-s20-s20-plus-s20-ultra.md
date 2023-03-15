# 三星 Galaxy S20、S20+和 S20 Ultra 获得非官方 TWRP 版本

> 原文：<https://www.xda-developers.com/unofficial-twrp-now-available-exynos-samsung-galaxy-s20-s20-plus-s20-ultra/>

# 非官方 TWRP 现可用于 Exynos 三星 Galaxy S20、S20+和 S20 Ultra

你现在可以下载三星 Galaxy S20、S20+和 S20 Ultra 的非官方 TWRP 恢复版本，但只能下载 Exynos 版本。

三星的 Galaxy S20 系列自带 Android 10 开箱即用，OEM 现在已经承诺给[三代 Android OS 更新](https://www.xda-developers.com/samsung-galaxy-devices-3-generations-android-updates/)给他们。作为 Galaxy S 系列最新旗舰产品的所有者，你可能不准备在短期内选择在手机上安装定制 rom，但我们的改装社区有不同的想法。flash 爱好者应该很高兴知道，银河 S20/S20+/S20 Ultra 的 TWRP 的统一版本已经出现在我们的论坛上。

**[三星 Galaxy S20/S20+/S20 超 XDA 论坛](https://forum.xda-developers.com/galaxy-s20)**

XDA 资深会员 geiti94 是这个非官方的 TWRP 港口的幕后策划人。 [S20 的股票内核源代码](https://www.xda-developers.com/samsung-galaxy-s20-kernel-source-code-available-exynos-models/)的可用性确实在 TWRP 在这些手机上的到来背后发挥了至关重要的作用，但有一个问题。当前版本基于 [TWRP 3.4.0](https://www.xda-developers.com/twrp-3-4-0-enables-ozip-decryption-realme-oppo-devices-support-legacy-devices-upgraded-android-10/) ，只能在 Galaxy S20 系列的国际版本上运行，这些版本由三星内部的 [Exynos 990](https://www.xda-developers.com/samsung-exynos-990-5g-modem-5123-7nm/) SoC 驱动。装载高通骁龙 865 的美国和加拿大版本的智能手机不允许启动加载程序解锁，因此为它们建立 TWRP 映像是不可行的。

**[从亚马逊](https://www.amazon.in/Samsung-Galaxy-Storage-Additional-Exchange/dp/B086KFMC6Y/?tag=xdaportalin-21)购买三星 Galaxy S20 Ultra】**

即使你可以解锁 Exynos Galaxy S20 的引导加载程序，请记住，这个过程不可逆转地触发了 KNOX 保修位(**因此取消了保修**)以及**禁用后续 OTA 更新**。此外，你必须清除你的手机的整个用户数据分区，以摆脱股票加密，所以**做了事先备份**。开发者已经承诺在不久的将来提供一个自动化的加密移除器来简化这一部分。

如果你想查看 Galaxy S20 的详细的一步一步的 TWRP 闪光指南，请点击下面的链接。值得一提的是，MTP 在最初的构建中是坏的，但你可以在 TWRP 挂载设置中禁用 MTP，并使用 ADB 将文件从电脑推送到手机(反之亦然)。

**[非官方 TWRP 为三星 Galaxy S20/S20+/S20 超](https://forum.xda-developers.com/galaxy-s20/development/recovery-twrp-galaxy-s20-s20-s20-ultra-t4149911)**