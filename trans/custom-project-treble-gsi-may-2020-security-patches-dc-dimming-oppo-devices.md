# 定制 AOSP 项目 Treble GSI 构建获得 2020 年 5 月安全补丁

> 原文：<https://www.xda-developers.com/custom-project-treble-gsi-may-2020-security-patches-dc-dimming-oppo-devices/>

一些三星设备[开始](https://www.xda-developers.com/samsung-galaxy-s20-galaxy-fold-updates-may-2020-security-patches/) [接收【2020 年 5 月的安全补丁，甚至在](https://www.xda-developers.com/samsung-galaxy-note-10-receives-update-with-may-2020-security-patches/)[谷歌发布当月的安全公告](https://www.xda-developers.com/may-2020-android-security-patches-google-pixel/)并推出兼容 Pixel 设备的相应 OTA 更新之前。即使你没有谷歌 Pixel 手机或三星旗舰手机，你仍然有机会通过更新的[通用系统镜像](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/) (GSI)来提升你的设备的安卓安全补丁级别(SPL)，前提是设备本身符合 [Project Treble](https://forum.xda-developers.com/project-treble) 并且引导程序是可解锁的。事实上，XDA 认可的开发者 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) ，第三方 GSI 开发社区中的知名人士，最近更新了他的定制 AOSP 项目 Treble GSI，又名*嘎嘎 Phh-Treble* ，提供了 2020 年 5 月的安全补丁以及几个特定于 OEM 的修复。

**[呱呱 Phh——高音——XDA 螺纹](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/aosp-10-0-quack-phh-treble-t3992559)**

作为一个快速复习，开发者已经在小米手机上添加了对双击唤醒手势的支持，并在最近几个版本的*嘎嘎 Phh 高音* 中添加了 Realme 的显示屏下指纹传感器[。除了新的安全补丁，定制 GSI 的最新版本( *v216* )现在完全兼容运行 Android 10 的三星设备上的超声波指纹传感器。phhusson 还合并了几个与高通供应商实现相关的修复，这可能会导致骁龙平台上更高的摄像机录制分辨率。](https://www.xda-developers.com/custom-project-treble-gsis-get-updated-with-the-april-2020-security-patches-and-fixes-for-xiaomi-realme-devices/)

关于 OEM 特定的增强功能，新版本现在可以正确识别不同的参数，如一些诺基亚手机上的电池状态和自动亮度。另一方面，从现在开始，DC 调光应该可以在这款定制 GSI 上的兼容 OPPO 设备上工作。对于那些不熟悉这个术语的人来说，DC 调光是一种行业标准方法，在某些情况下[调光 OLED 面板以减少屏幕闪烁](https://www.xda-developers.com/oneplus-dc-dimming-optional-feature-future-update/)。

完整的变更日志可以在下面找到:

*   2020 年 5 月安全补丁
*   修正三星 [Galaxy A30](https://forum.xda-developers.com/galaxy-a30) 的开机问题
*   为[红米 6A](https://forum.xda-developers.com/redmi-6a) 和[红米 6](https://forum.xda-developers.com/redmi-6) 修复奥利奥供应商的长靴
*   在三星 Q 厂商上固定超声波指纹传感器
*   修复牙线变体上的最近按钮
*   将手电筒固定在 [S10 Lite](https://forum.xda-developers.com/galaxy-s10-lite) 上
*   修正小米双击唤醒[红米 Go](https://forum.xda-developers.com/t/xiaomi-redmi-go)
*   新的覆盖层(修复电池状态，自动亮度，...)
*   开发者端:
    *   清除在硬件覆盖中使用 IMS
    *   为供应商媒体配置文件提供更多更改
*   高音设置:
    *   高通设备:添加使用供应商媒体配置文件的选项。这可以实现更高的相机记录分辨率。
    *   高通设备:添加一个选项来使用供应商音频策略。这可能会修复一些音频问题，但可能会产生一些其他问题。
    *   添加一个选项来禁用音频效果。这可能会修复一些音频问题。
    *   Oppo:增加一个启用 dc 明帝的选项。
    *   navbar 的反转逻辑:navbar 默认启用，但可以禁用。

**[下载呱呱 Phh-高音 v216](https://github.com/phhusson/treble_experimentations/releases/tag/v216)**

在闪烁自定义 GSI 之前，您应该使用下面链接的 Treble Info 应用程序确定您的设备型号。刷新过程将要求您重置设备的出厂设置，因此在继续之前，请确保您已准备好丢失应用程序数据。我们建议你选择设备外备份(比如在你的电脑或 SD 卡上)，以防万一。

[app box Google play " tk . hack 5 . treble check "]