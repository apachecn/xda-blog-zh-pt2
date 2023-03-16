# 索尼 Xperia XZ Premium 像 Razer 手机一样具有隐藏的 120Hz 屏幕模式

> 原文：<https://www.xda-developers.com/sony-xperia-xz-premium-hidden-120hz-screen-mode-razer-phone/>

**2018 年 4 月 8 日更新:我们已经了解了更多关于这种隐藏屏幕模式的信息。见下文。**

嗯，这里有些有趣的东西。索尼 Xperia XZ Premium 是 2017 年的旗舰产品，最引人注目的是它的 4K HDR 显示屏，但它还有另一个隐藏的技巧:它的显示面板实际上支持像 Razer 手机一样的高帧率 120Hz 模式。关于这种隐藏屏幕模式[的传言自该设备发布之时起就在互联网](https://gazyekichi.com/2017/07/26/%E7%94%BB%E9%9D%A2%E3%81%95%E3%81%8F%E3%81%95%E3%81%8F%EF%BC%81%E3%80%8Cxperia-xz-premium%E3%80%8D%E3%81%AF%E3%80%8C120hz%E3%80%8D%E3%81%AB%E5%AF%BE%E5%BF%9C%E3%81%97%E3%81%A6%E3%81%84%E3%82%8B/)上流传，但因为它需要修改内核才能启用，所以没有多少用户能够实际测试它。然而最近，[我们听说](https://www.reddit.com/r/Android/comments/8a6kkn/this_aosp_81_for_the_xperia_xz_premium_seems_to/)许多用户已经开始测试这种隐藏屏幕模式...不幸的是，结果很不一致。

作为背景，Xperia XZ Premium 显示面板支持 3 种屏幕模式:1080p@60fps，2160p@60fps，最后是禁用的 1080p@120fps 模式。这种禁用的高帧速率模式可以通过在内核源代码中将该提交恢复为显示面板配置来启用。

感谢索尼开放设备程序支持 [Xperia XZ Premium](https://www.xda-developers.com/xperia-xz-premium-open-devices/) 用于其[最新 Android Oreo](https://www.xda-developers.com/sony-android-oreo-open-devices-program/) [发布](https://www.xda-developers.com/android-oreo-sony-xperia-xz-premium/)(甚至在 [Linux 内核版本 4.4](https://www.xda-developers.com/xperia-open-devices-linux-4-4-kernel/) ！)，开发人员为设备构建一个功能性的 AOSP ROM 是相当容易的。(不幸的是，有一个挥之不去的问题，当解锁引导加载程序时，DRM 密钥被擦除，导致劣质的相机性能。)使用最新的资源，XDA 成员 [uditrawat](https://forum.xda-developers.com/member.php?u=8946654) 为 XZ Premium 编译了 [Android 8.1 Oreo，支持 120Hz 屏幕模式。](https://forum.xda-developers.com/xz-premium/how-to/aosp-8-1-t3752708)

根据我们论坛中测试过这个版本的成员所说，结果是不一致的。有人说它有效，有人说它只是安慰剂。我个人认为，如果成功了，人们会很容易注意到。也许 AOSP 本身不支持高帧率显示，而是需要额外的框架补丁。一名为 [Razer 手机](https://www.xda-developers.com/list-android-devices-project-treble-support/)闪存了[linegeos 15.1](https://www.xda-developers.com/lineageos-15-1-resurrection-remix-available-project-treble/)的[通用系统映像](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/)版本的测试人员报告称，这款手机的运行频率为 90Hz(这是该手机内核中指定的默认刷新率)，所以我不太确定它不能用于索尼 Xperia XZ Premium 的原因。

不管怎样，这是一个非常有趣的发展。索尼 Xperia XZ Premium 不允许开箱即用的 120Hz 刷新率肯定有一个很好的原因。我不认为这与性能有关，因为该设备使用与 Razer 手机相同的片上系统(高通骁龙 835)，所以我倾向于 Android 兼容性或显示面板不一致。希望开发者能够解决这里的问题，让索尼 Xperia XZ Premium 稳定在 120Hz，或者希望 Android P 将正式添加对高帧率显示器的支持。鉴于索尼向 AOSP 提交上游更改的记录，我认为如果该公司真的希望 XZ Premium 支持高帧速率模式，我们应该已经在 AOSP 看到对它的支持了。

## 更新:更多设备，更多信息

事实证明，有更多的索尼设备被内核禁用了隐藏的 120Hz 显示模式。XDA 认可开发者 [Myself5](https://forum.xda-developers.com/member.php?u=3816568) 深挖来源向我们确认索尼 Xperia X、索尼 Xperia X Performance、索尼 Xperia XZ、索尼 Xperia XZ1、索尼 Xperia XZ1 Compact、索尼 Xperia XA2、索尼 Xperia XA2 Ultra 都支持这种屏幕模式。基本上，除了索尼 Xperia X Compact 之外，任何新的索尼手机都应该支持这种模式。

然而，屏幕模式目前在为这些设备编译的 AOSP rom 上不起作用，因为模式之间的切换不起作用。不过，这并不意味着屏幕模式本身不起作用，因为 Myself5 声明将内核默认设置为该屏幕模式会起作用。如果或当这些索尼设备的 8.1 版本支持高帧率屏幕模式时，CarbonROM 和其他基于 AOSP 的 ROM 将开始集成这些补丁。