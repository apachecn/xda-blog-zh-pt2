# 基于 Android Pie 的 MIUI 10 移植到 OnePlus 6 和一加 6T 上

> 原文：<https://www.xda-developers.com/miui-10-android-pie-ported-oneplus-6-6t/>

# 基于 Android Pie 的 MIUI 10 移植到 OnePlus 6 和一加 6T 上

小米的 MIUI 10 ROM 已经创造了大量的追随者，现在 OnePlus 6 和一加 6T 的用户可以尝试这种固件。

我们经常看到为各种智能手机设计的普通 AOSP 端口。然而，很少看到 OEM ROMs 移植到其他设备上。我们通常不会在 Pixel 3 或 LG G7 等设备上看到三星的体验，但 MIUI 10 现在有数百万人在使用。小米的 OEM ROM 已经创造了大量的追随者，现在一加 6 和一加 6T 的用户可以尝试固件，这要归功于 XDA 高级成员的工作。

这个 MIUI 10 端口是基于小米 8.11.23 版本的 Android Pie，它需要你的 OnePlus 6 或一加 6T 安装 OB8(或更新版本)固件才能安装。由于这是一个端口，我们希望看到一些功能正常工作，而其他功能则不正常。例如，开发人员告诉我们，到目前为止已经报告了以下错误:

*   NFC(正在开发中)
*   手电筒开关(第三方手电筒应用程序工作正常)
*   股票 MIUI 相机不工作，所以只使用最新的谷歌相机或 OxygenOS 相机。
*   Mi 帐户(主题、壁纸、铃声等工作正常)
*   警报滑块
*   自动旋转开关会冻结你的设置，所以不要碰它。如果不小心改了，再改一次就可以解冻你的设置了。

然而，MIUI 的 AOD 功能作品，主题，壁纸(静态和动态)，铃声作品，全屏手势作品，以及 Mi AI 作品。因此，如果你是 MIUI 10 的粉丝，或者只是想在你的 OnePlus 6 或一加 6T 上尝试一下，那么在 TWRP 创建一个备份，并在你的设备上测试这个端口。

* * *

[**在我们的 OnePlus 6 论坛**](https://forum.xda-developers.com/oneplus-6/development/rom-miui-10-pie-8-11-23-t3876955) 查看这个 MIUI 10 端口