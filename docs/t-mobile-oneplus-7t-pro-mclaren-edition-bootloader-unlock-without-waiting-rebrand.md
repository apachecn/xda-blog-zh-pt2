# T-Mobile 一加 7T - Bootloader 解锁，无需等待和品牌重塑

> 原文：<https://www.xda-developers.com/t-mobile-oneplus-7t-pro-mclaren-edition-bootloader-unlock-without-waiting-rebrand/>

# T-Mobile 一加 7T，7T 专业迈凯轮版现在可以启动加载程序解锁，无需等待，7T 更名也是可能的

XDA 资深会员 Superboy58 分享了一种无需 SIM 解锁即可引导加载程序解锁 T-Mobile 一加 7T 和 7T Pro 迈凯轮版的方法。

T-Mobile 品牌的一加智能手机上的引导加载器解锁体验与解锁版本非常不同。一旦你付清合同并在网络上使用该设备至少 40 天，你就有资格执行 [SIM 解锁](https://www.t-mobile.com/support/plans-features/t-mobile-device-unlock-app)。SIM 解锁后，你需要[生成一个唯一的解锁令牌](https://support.oneplus.com/app/answers/detail/a_id/588/~/how-to-unlock-bootloader-for-oneplus-smart-phone)才能解锁引导程序。除了启动加载器解锁的复杂性，较慢的更新频率和无法参与 OxygenOS [开放测试版](https://www.xda-developers.com/tag/open-beta/)和[开发者预览版](https://www.xda-developers.com/download-oneplus-8-oneplus-8-pro-oxygenos-11-android-11-developer-preview-3/)计划是人们更喜欢将其 T-Mobile 一加手机“更名”为国际(即非 T-Mobile)固件的一些主要原因。如果你有 T-Mobile 一加 7T，并想摆脱运营商固件，那么你会有兴趣了解 XDA 高级成员 [Superboy58](https://forum.xda-developers.com/member.php?u=2625583) 已经设法找到一种方法来转换这种变体到国际没有传统解锁引导加载程序/SIM 卡解锁。

**[一加 7T 论坛](https://forum.xda-developers.com/oneplus-7t)**

诀窍是从[官方 unbrick 包](https://www.xda-developers.com/oneplus-7t-development-update-first-custom-rom-kernel-and-unbrick-tool-released/)中修补 OPS 文件，以这样的方式引导加载程序忽略令牌生成部分，并允许用户用标准的 Fastboot 命令解锁它。一旦你解锁了引导程序，为一加 7T 选择[快速引导-可刷新的全局固件，然后](https://forum.xda-developers.com/oneplus-7t/how-to/rom-stock-fastboot-roms-oneplus-7t-t3979213)[刷新一次](https://forum.xda-developers.com/oneplus-7t/how-to/guide-t-mobile-brand-conversion-to-t4019495)以完成品牌重塑过程。更多说明请点击下面的链接。

**[将 T-Mobile 一加 7T 更名为国际固件— XDA 线程](https://forum.xda-developers.com/oneplus-7t/how-to/t-mobile-7t-conversion-to-international-t4153943)**

如果你有 T-Mobile 一加 7T 专业迈凯轮版，有一个类似的模块来解锁引导加载程序，无需等待。唯一的问题是，**你不能像另一个模型那样重新命名它**。T-Mobile 版本支持 5G，而一加 7T Pro 5G 的国际版本根本不存在。你不可能用另一个官方的 OxygenOS ROM 来替换库存的 T-Mobile 迈凯轮版固件。不过，你可以选择专门为这款车打造的[定制光盘](https://forum.xda-developers.com/7t-pro-mclaren/development)。

**[Bootloader 解锁 T-Mobile 一加 7T Pro 迈凯伦版无需等待](https://forum.xda-developers.com/7t-pro-mclaren/how-to/t-mobile-7t-pro-5g-mclaren-bootloader-t4154441)**

**[T-Mobile 一加 7T Pro 迈凯伦版论坛](https://forum.xda-developers.com/7t-pro-mclaren)**