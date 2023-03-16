# LineageOS 15.1 现可用于三星 Galaxy Note 9 (Exynos)

> 原文：<https://www.xda-developers.com/samsung-galaxy-note-9-lineageos-15-1-exynos/>

# LineageOS 15.1 现可用于三星 Galaxy Note 9 (Exynos)

三星 Galaxy Note 9 已经很棒了，现在又有了面向 Exynos 机型的 LineageOS 15.1 预官方版本。

Android 社区中的许多人目前都在大肆宣传谷歌 Pixel 3 和 Pixel 3 XL，但今年已经有许多优秀的智能手机发布。见鬼，[还有更多优秀的智能手机](https://www.xda-developers.com/xiaomi-mi-mix-3-10gb-ram-5g-support/)[也计划在今年晚些时候发布](https://www.xda-developers.com/oneplus-6t-announced-october-30/)。不管你是不是三星的粉丝，都很难去争论 Galaxy Note 9 有多好。它避免了 notch 的崩溃，有一个 3.5 毫米的耳机端口，为喜欢记东西的人配备了一支手写笔，现在有一个用于 Exynos 型号的 LineageOS 15.1 的预官方版本。

Galaxy Note 9 于 8 月中旬推出，并于当月晚些时候上架。三星很快[发布了 Exynos 变体](https://www.xda-developers.com/samsung-galaxy-note-9-exynos-kernel-source/)的内核源代码，但由于美国运营商的参与，这是大多数开发者社区关注的焦点。骁龙版本(除了在中国销售的版本)有一个锁定的引导加载程序，所以我们不能做太多，除非一个漏洞出来。有一些情况下，当一个工程内核发布时，可以帮助我们获得 root 访问权限，但完整的 TWRP 安装和定制 ROM 支持已被证明对这些骁龙 Galaxy Note 设备很少。

Galaxy Note 9 的内核源代码发布几天后，TWRP 的一个[非官方端口可用，第一个定制 ROM](https://www.xda-developers.com/samsung-galaxy-note-9-twrp-custom-rom/) 也可用。我们仍然没有该设备的 TWRP 官方版本，但社区开发者的支持已经有所增加，正如在该设备的 XDA 官方论坛上看到的[。现在，由于 XDA 公认的开发者和贡献者](https://forum.xda-developers.com/galaxy-note-9/development) [jesec](https://forum.xda-developers.com/member.php?u=6371894) 的工作，我们有了 Exynos Galaxy Note 9 (N960F/FDS/N)的 LineageOS 15.1 的预官方版本。

构建还不是正式的，但工作仍在继续，可能会在不久的将来到来。虽然它不是官方的，但这意味着有些事情可行，有些事情不可行。这是 jesec 给我们的一份清单。在 XDA 主题的原始帖子中，开发者还为那些想要在他们的设备上安装这个预官方版本的人提供了具体的说明。

**什么在起作用**

*   这个建筑是一个正式的线性地质建筑。强制并保证符合我们的[设备支持要求](https://github.com/LineageOS/charter/blob/master/device-support-requirements.md)。这意味着包括但不限于这些硬件将会起作用:
*   无线保真
*   蓝牙
*   移动网络(通话、数据等。)
*   声音的
*   通用串行总线
*   全球（卫星）定位系统
*   照相机
*   指纹传感器
*   国家足球联盟
*   等等。查看[设备支持要求](https://github.com/LineageOS/charter/blob/master/device-support-requirements.md)了解更多信息。

**什么不起作用:**

*   在[设备支持要求](https://github.com/LineageOS/charter/blob/master/device-support-requirements.md)中授予的适用例外。
*   显然三星自己的功能如 Samsung Pay、KNOX、主题中心、游戏启动器等。不会移植到 LineageOS。不过，我们可能有自己的类似功能的实现。
*   虹膜传感器不工作，因为 AOSP 上游还不支持。
*   IMS 服务(VoLTE、VoWiFi 等)。三星有自己的专有实现。很难将其移植到 LineageOS。

* * *

[**看看这款为银河 Note 9**](https://forum.xda-developers.com/galaxy-note-9/development/official-lineageos-t3855550) 打造的 LineageOS 15.1