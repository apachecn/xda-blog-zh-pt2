# TWRP 现可用于小米 Mi Max 3 和 HTC U12+

> 原文：<https://www.xda-developers.com/twrp-xiaomi-mi-max-3-htc-u12/>

XDA 论坛最大的吸引力之一是丰富的定制 rom、内核和修改。随着 [Android Pie](https://www.xda-developers.com/android-pie-google-pixel-google-pixel-2/) 的发布，开发者们正在努力将来自 AOSP 的最新 Android 版本[移植到他们的设备上。在定制开发在我们的论坛上真正起飞之前，必须克服两个主要的障碍:引导加载器解锁和移植定制恢复。没有前者，甚至考虑改装你的设备都没有意义，这就是为什么社区对](https://www.xda-developers.com/android-pie-source-code-aosp/)[华为最近的决定](https://www.xda-developers.com/xda-huawei-decision-stop-bootloader-unlocking/)感到不安。如果没有后者，对大多数用户来说，修改他们的设备太危险了，因为如果你不能访问库存图像，你可能最终会使你的设备无法操作。自定义恢复，尤其是团队胜利恢复项目(TWRP)，对自定义开发至关重要，这就是为什么小米 Mi Max 3 和 HTC U12+的 TWRP 官方支持在各个社区都很重要。

既然这两款设备都获得了 TWRP 的支持，开发就可以安全地开始了。HTC U12+的内核源代码[已经可用](https://www.htcdev.com/devcenter/downloads)，但[我们仍在等待](https://github.com/MiCode/Xiaomi_Kernel_OpenSource/branches/all)小米 Mi Max 3 的内核源代码。由于小米[上个月刚刚发布了 Mi Max 3](https://www.xda-developers.com/xiaomi-mi-max-3-specifications-pricing-availability/)，我们应该很快就会看到“氮”分支下的源代码弹出。无论如何，由于小米发布了大量类似的设备，如果使用其他小米设备的 BLOBs 的端口弹出来，不要感到惊讶。多亏了 Project Treble 的支持，你应该能够[闪现一个基于 AOSP Android 8.1 Oreo 的 GSI](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/) ，甚至是基于谷歌 Pixel 的 Android Pie 系统映像的“[半 GSI](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/rom-android-p-developer-preview-t3816659) ”。至于 HTC U12+对定制 ROM 的支持，限制因素是它的受欢迎程度:我们不确定有多少开发者购买了这款设备。不过，请留意我们的论坛。

## 小米 Mi Max 3

[**TWRP 为小米 Mi Max 3** 下载 ](https://twrp.me/xiaomi/xiaomimimax3.html)

[**小米 Mi Max 3 论坛**](https://forum.xda-developers.com/mi-max-3)

[**XDA 支持小米 Mi Max 3** 线程 ](https://forum.xda-developers.com/mi-max-3/development/official-twrp-3-2-x-xiaomi-mi-max-3-t3825561)

由于 Mi Max 3 是仅支持 A 的设备，安装 TWRP 需要以下一般步骤:

1.  从小米网站获取引导加载程序解锁代码
2.  解锁引导加载程序
3.  重新启动引导程序
4.  将 TWRP 闪存到恢复分区:`fastboot flash recovery name_of_twrp_image.img`

## HTC U12+

[**【TWRP】下载为 HTC U12+**](https://twrp.me/htc/htcu12+.html)

[**HTC U12+论坛**](https://forum.xda-developers.com/u12-plus)

[**【XDA】支持线程为 HTC U12+**](https://forum.xda-developers.com/u12-plus/development/recovery-unofficial-twrp-3-2-2-0-htc-t3819343)

由于 U12+是一个 [A/B 设备](https://www.xda-developers.com/how-a-b-partitions-and-seamless-updates-affect-custom-development-on-xda/)(它[支持无缝更新](https://www.xda-developers.com/list-android-devices-seamless-updates/))，安装 TWRP 将需要这些一般步骤:

1.  解锁设备的引导加载程序
2.  重新启动引导程序
3.  启动 twrp:t0
4.  到达 TWRP 后，启用亚行侧载
5.  侧装 TWRP 安装程序脚本:`adb sideload name_of_twrp_installer_script.zip`

## 更新 TWRP

保持最新版本的自定义恢复的最简单方法是从谷歌 Play 商店下载并安装官方应用程序。如果你是根用户，它可以用最新版本自动修补启动映像。否则，它会从恢复/快速启动下载您需要安装的最新版本。