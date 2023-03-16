# 小米米 5s 非官方获得项目高音兼容性

> 原文：<https://www.xda-developers.com/xiaomi-mi-5s-project-treble-compatibility-unofficially/>

Project Treble 是 Android 的重大改进，我们一直密切关注着它的发展。最大的潜在好处是，它允许制造商更快地推出更新。然而，这项优势的影响要到今年晚些时候才能得到验证(届时将有更多的 Android 手机推出三重支持)。

第二个好处是对定制开发社区很重要的。它允许基于 Android Oreo 的 AOSP 通用系统映像(GSI)在 Treble 兼容设备上闪现。[我们一直在为您更新 Project Treble](https://www.xda-developers.com/tag/project-treble/) 的进展，包括对[如何在理论上增强定制 ROM 开发](https://www.xda-developers.com/how-project-treble-revolutionizes-custom-roms-android-oreo/)的解释。尽管缺乏内核源代码或 TWRP 支持，但拥有 Project Treble 支持使得[一款不起眼的联发科 Android 手机能够运行 AOSP Android Oreo](https://www.xda-developers.com/obscure-mediatek-phone-kernel-source-android-oreo-project-treble/) 。

在我们的论坛中，一个更令人兴奋的发展是努力将 Project Treble 兼容性非正式地带到不支持它的设备上。我们已经看到了第一个成功的报道，因为[小米 Redmi Note 4 被制作成 Project Treble 兼容](https://www.xda-developers.com/xiaomi-redmi-note-4-project-treble/)。现在，XDA 资深成员 [MZO](https://forum.xda-developers.com/member.php?u=6304619) 也同样让小米 Mi 5s 高音兼容，为其他**小米/msm8996-common** 设备兼容铺平了道路。这份名单包括小米 5、小米 5s Plus 和其他产品。

Project Treble 兼容性意味着小米米 5s 可以运行 AOSP 安卓奥利奥的通用系统映像(GSI)。更重要的是，这意味着更新到 Android P 的可能性对开发者来说更容易。

用户可以使用非官方的项目 Treble 端口来安装通用系统映像，如 XDA 资深成员 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 的 [Phh-Treble](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/experimental-phh-treble-t3709659) 。这样做的说明是:

*   下载项目 Treble zip，并将其解压缩到您的系统中。
*   基于您的系统运行脚本(sh 用于 Linux，bat 用于 Windows)。
*   刷新通用系统映像。

RIL、摄像头、Wi-Fi、蓝牙等重要硬件都可以在高音端口正常工作。但是，还是有 bug。具体来说，硬件按钮灯没有工作，SELinux 被设置为许可。

开发者还指出，Treble 端口不会对小米 Mi 5s 的 LineageOS 兼容性产生任何影响。这是因为 SELinux 在 Treble 端口中设置为 permissive，这是 LineageOS 所不允许的。

小米 5s 的非官方项目 Treble compatibility 是一个好消息，尽管许多人可能不认为有必要，因为我们的论坛上有太多基于 AOSP 的定制 rom 可供小米设备使用。当 Android P 发布时，我们预计 Treble 兼容性将对未来的定制 ROM 开发有巨大的帮助。

* * *

[**小米米 5S**](https://forum.xda-developers.com/mi-5s/development/oreo-project-treble-capricorn-t3756463) 下载项目高音 ZIP