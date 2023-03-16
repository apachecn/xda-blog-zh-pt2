# 小米 Mi 5 非正式获得 Project Treble 兼容性

> 原文：<https://www.xda-developers.com/xiaomi-mi-5-receives-project-treble-compatibility-unofficially/>

Project Treble 需要在任何使用 Android 8.0 Oreo 及更高版本的手机上支持。然而，搭载旧版本 Android [的设备不需要更新 Project Treble 支持](https://www.xda-developers.com/why-current-oneplus-nokia-phones-wont-be-project-treble-certified/)。这意味着没有更新 Project Treble 支持的旧设备无法利用 [Project Treble](https://www.xda-developers.com/tag/project-treble/) 提供的任何好处，例如能够在没有任何内核修改的情况下刷新 AOSP Android Oreo 的通用系统映像(GSI)。

这就是开发社区的用武之地。当[项目 Treble 成功带到小米 Redmi Note 4](https://www.xda-developers.com/xiaomi-redmi-note-4-project-treble/) 上时，我们看到了第一个成功的报道，这是开发中的一个重要里程碑。紧接着，小米 Mi 5s(设备代号:capricorn) [也非正式获得了 Project Treble compatibility】。](https://www.xda-developers.com/xiaomi-mi-5s-project-treble-compatibility-unofficially/)

现在，轮到小米米 5 了。米 5(设备代号:gemini)是 2016 年小米旗舰智能手机。它有一系列高端规格，包括高通骁龙 820 片上系统、3GB/4GB 内存和 32GB/64GB/128GB 存储空间、5.15 英寸全高清(1920x1080) 16:9 IPS 显示屏、16MP 后置摄像头、4MP 前置摄像头和 3000mAh 电池。它在 Android Marshmallow 之上附带了 MIUI 7，最近它收到了 MIUI 9 更新。基于 Android Oreo 的 MIUI 全球测试版 ROM [也已经为设备](https://www.xda-developers.com/xiaomi-mi-5-android-oreo-miui-beta/)发布。

Project Treble compatibility 已经由 JDCTeam 带到了小米 Mi 5 上。它使用未使用的 CUST 分区(这是用于为 Redmi Note 4 带来高音的相同方法)。开发人员提到这个项目的状态是 alpha，工作列表还没有指定。

对 Mi 5 的三重支持带来了两个分区:**系统**和**厂商**。系统分区包含通用系统映像(GSI)，而供应商分区包含启动和运行电话所需的设备特定文件。由于 Treble，Mi 5 用户可以轻松地更改系统映像，并使用相同的内核和供应商分区运行不同的系统映像。

需要注意的是，小米 Mi 5 是 A 专用设备。关于通用系统镜像，用户需要下载 ARM64 和 A-only 镜像(如 XDA 资深会员 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 的 [Phh-Treble](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/experimental-phh-treble-t3709659) )。开发人员提到，Phh-Treble 的最新版本正在与 Treble gemini zip 项目合作。

在小米米 5 上安装 alpha Project Treble zip 的说明是:

*   下载项目 Treble zip。
*   下载一个仅限 A 的 GSI 图片。
*   重启以恢复(开发人员提到需要 TWRP 3.2.1-1)。
*   擦除系统/数据/缓存/Dalvik 分区。
*   闪光高音双子座拉链。
*   刷新 GSI 系统映像，然后重新启动。

很高兴看到 Project Treble 被非正式地带到小米设备上。我们预计当 Android P 的最终版本发布时，三重兼容性将是对开发的巨大推动，因为它将使开发变得更加容易。

* * *

[**小米 5**](https://forum.xda-developers.com/mi-5/development/jdcteam-treble-support-project-t3761296) 下载项目高音 ZIP