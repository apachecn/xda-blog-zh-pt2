# 亲身体验 OnePlus 6 的非官方 LineageOS 15.1 GSI 版

> 原文：<https://www.xda-developers.com/unofficial-lineageos-15-1-oneplus-6/>

在 Project Treble 之前，新的智能手机问世后，有时需要几周或几个月的时间才能为该手机开发出稳定、实用的定制 ROM。使用 Project Treble，理想情况下，应该可以在发布当天将通用系统映像(GSI)闪存到启用 Treble 的设备上，并使其发挥最大功能。虽然我们不认为基于 AOSP 的定制 rom 会花太多时间到达[新发布的](https://www.xda-developers.com/oneplus-6-specifications-pricing-availability/) OnePlus 6，但我们想看看 [LineageOS](https://www.xda-developers.com/lineageos-15-1-resurrection-remix-available-project-treble/) 通用系统映像(GSI)在一加[第一个支持高音的设备](https://www.xda-developers.com/why-current-oneplus-nokia-phones-wont-be-project-treble-certified/)上运行得如何。

然而，对于 OnePlus 6 来说，试图简单地[将 GSI](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/) 刷新到系统分区会导致设备启动并冻结成带有白色通知 LED 的黑屏，或者无休止地重新启动。XDA 成员 [ProtoDeVNan0](https://forum.xda-developers.com/member.php?u=5203734) 花了大约一周时间在[上发布了一个关于如何让 GSI 在 OnePlus 6](https://forum.xda-developers.com/oneplus-6/how-to/guide-how-to-flash-treble-roms-oneplus-6-t3797858) 、**上启动的帖子，然而它似乎只对 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 的** **[AOSP GSI](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/experimental-phh-treble-t3709659)** 有效。让 AOSP GSI 启动的秘密是通过带有`--disable-verity`和`--disable-verification`标志的 fastboot 刷新库存 vbmeta 映像，这应该允许非库存 rom 启动。然而，即使在这个过程之后，其他可用的 GSI 如[linegeos 或 resurrence Remix](https://www.xda-developers.com/lineageos-15-1-resurrection-remix-available-project-treble/)也会导致引导循环。幸运的是， [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 发布了 OnePlus 6 上启动的 LineageOS 和复活混音的更新[版本，XDA 成员](https://forum.xda-developers.com/oneplus-6/development/experimental-lineage-t3801281/) [Exelios](https://forum.xda-developers.com/member.php?u=5930599) 发布了关于如何正确闪光图像的[说明](https://forum.xda-developers.com/showpost.php?p=76740118&postcount=2)。

**2018 年 6 月 14 日**更新:XDA 资深成员 joemossjr】发布了一款工具，让闪现 GSI 方式的过程变得更加简单。

首先要测试的是所有的硬件功能:Wi-Fi、蓝牙、无线电、GPS、指南针、加速度计、触觉、摄像头和麦克风。除了 NFC、VoLTE 和 [Dash Charging](https://www.xda-developers.com/oneplus-dash-charge-rebrand-amazon/) 之外，其他都工作正常。附带的应用程序运行正常，附带的 AudioFX 功能也是如此。看一眼 Profile GPU 渲染图，ROM 似乎不像 stock OxygenOS 那样[平滑，这是一个没有专门为 OnePlus 6 优化的通用系统映像所预期的，但它也不慢。也许到目前为止最值得注意的问题是缺乏对 notch 的支持，它穿过状态栏并稍微进入应用程序的操作栏。如果通知和系统图标胆敢闯入 notch 的域，它们也会消失在 notch 中。OnePlus 6 显示屏圆角的状态栏也缺少填充。一旦基于 Android P 的 GSIs 可用，缺乏适当的 notch 支持可能会得到解决。](https://www.xda-developers.com/oneplus-6-speed-gaming-review/)

关于设置和 [LineageOS 功能](https://www.xda-developers.com/lineageos-15-feature-list-overview-screenshots-video/)，我尝试的所有设置似乎都工作正常，除了 LiveDisplay 和在显示设置下更改样式。系统配置文件看起来也很正常，但是为系统配置文件设置蓝牙触发器会破坏设置。似乎还缺少一些重要的功能，如自适应亮度，一加手势，如双击唤醒，以及显示颜色配置文件。然而，有[的变通办法来重新启用自适应亮度](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/overlay-enable-night-light-adaptive-t3741965)，并通过根 ADB 在不同的颜色配置文件之间切换。

要切换其他[显示配置文件](https://www.xda-developers.com/oneplus-6-display-analysis-compared-oneplus-5t/)，您需要将您的 OnePlus 6 连接到带有 ADB 的计算机:

1.  通过导航到设置→系统→关于电话启用开发者选项，向下滚动并重复点击“内部版本号”直到“开发者选项”被启用。
2.  通过导航到设置→系统→开发者选项，向下滚动到“Root access”并选择“ADB only”来启用 Root 访问。
3.  在你的电脑上，打开终端/命令提示符，键入`adb root`并按回车键。
4.  根据您要切换的颜色配置文件，复制并粘贴以下内容之一，然后按 enter 键:
    *   对于 sRGB: `adb shell "echo 1 > /sys/devices/platform/soc/ae00000.qcom,mdss_mdp/drm/card0/card0-DSI-1/SRGB"`
    *   对于 P3 的 DCI:`adb shell "echo 1 > /sys/devices/platform/soc/ae00000.qcom,mdss_mdp/drm/card0/card0-DSI-1/DCI-P3"`
    *   对于自适应模式:`adb shell "echo 1 > /sys/devices/platform/soc/ae00000.qcom,mdss_mdp/drm/card0/card0-DSI-1/adaptive_mode"`

颜色配置文件不会在重新启动后保持不变，因此您每次都必须这样做。

总之，在运行非官方生产线的 OnePlus 6 上，**不起作用的**或缺失的东西是 GSI:

*   回
*   国家足球联盟
*   [破折号充电](https://www.xda-developers.com/oneplus-dash-charge-rebrand-amazon/)
*   现场展示/夜灯
*   线性地理样式
*   系统配置文件蓝牙触发器
*   自适应亮度(适用于变通方法)
*   一加手势
*   颜色配置文件(适用于变通方法)

值得注意的是，**在运行非官方生产线的 OnePlus 6 上做的其他事情**GSI:

*   指纹扫描仪
*   通知 LED
*   亮度滑块(不适用于 AOSP GSI)
*   AudioFX

在 OnePlus 6 这样的设备上，我们建议你等待一个合适的基于 AOSP 的定制 ROM 发布。虽然看到这个 GSI 的功能令人印象深刻，但它没有 LineageOS 的官方版本稳定。如果你真的想满足闪现 AOSP ROM 的冲动，并且不介意处理我们上面提到的一些问题，那么请随意尝试一下。现在有了官方的 TWRP，你就不用担心事情会出错。