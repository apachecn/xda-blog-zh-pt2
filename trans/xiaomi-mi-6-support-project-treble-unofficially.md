# 小米 6 是最新一个非正式支持 Project Treble 的产品

> 原文：<https://www.xda-developers.com/xiaomi-mi-6-support-project-treble-unofficially/>

很少有 Android 设备制造商选择为旧设备发布 Project Treble 支持的更新。华为是选择用三重支持更新旧设备的公司之一。基本包括高音支持在 [Android 8.1 奥利奥更新的基本手机](https://www.xda-developers.com/essential-phone-android-8-0-oreo-beta-2/)也。但是，到了小米米 6，情况就不一样了。他们选择不在官方 Android Oreo 更新中包含三重支持(仍在进行中)。

即将推出的搭载 Android 8.0 Oreo 及以上版本的小米设备被要求拥有 [Project Treble](https://www.xda-developers.com/tag/project-treble/) 支持，但这并不意味着旧设备被完全排除在外。开发社区的辛勤工作导致[小米 Redmi Note 4 获得非官方项目三重支持](https://www.xda-developers.com/xiaomi-redmi-note-4-project-treble/)，这是通过使用未使用的 **cust** 分区实现的。这意味着该设备的用户可以闪现 AOSP 安卓奥利奥的通用系统映像(GSI)。

同样的方法被用于[给小米米 5s](https://www.xda-developers.com/xiaomi-mi-5s-project-treble-compatibility-unofficially/) (代号:摩羯座)和[小米米 5](https://www.xda-developers.com/xiaomi-mi-5-receives-project-treble-compatibility-unofficially/) (代号:双子座)带来非官方项目高音支持。现在，最新获得非官方高音支持的小米设备是小米 Mi 6。它还使用了与使用 **cust** 分区完全相同的方法。

小米 Mi 6(代号:sagit)于 2017 年 4 月上市。它有一系列高端规格，包括高通骁龙 835 片上系统，4GB/6GB 的内存与 64GB/128GB 的存储空间，5.15 英寸全高清(1920x1080) 16:9 IPS 显示屏，双 12MP + 12MP 广角+长焦后置摄像头，8MP 前置摄像头和 3350mAh 电池。该设备在 Android Nougat 的基础上推出了 MIUI 8，并在 11 月获得了 MIUI 9。小米还为设备发布了基于 Android Oreo 的 MIUI 全球稳定 ROM。

非官方项目三重支持带来两个分区:**系统**和**厂商**。系统分区包含通用系统映像，而供应商分区包含启动和运行电话所需的设备特定文件。Treble 支持允许用户更改系统映像，并使用相同的内核和供应商分区运行不同的系统映像。

小米 6 是一款仅支持 A 的设备，因此希望闪存通用系统映像(如 XDA 资深成员 [phhusson 的](https://forum.xda-developers.com/member.php?u=1915408) Phh-Treble)的用户需要下载 ARM64 和仅支持 A 的系统映像。Mi 6 的 Treble ZIP 文件包含一个引导映像(内核)和一个供应商映像( **cust** 分区)。

开发人员提到目前不工作的东西包括 VoLTE。SeLinux 也被设置为 permissive。

在 Mi 6 上闪烁项目高音 ZIP 的说明如下:

*   下载项目 Treble ZIP 文件。
*   下载通用系统映像(ARM64 和仅限 A 的版本)。
*   重启恢复 [**(此恢复需要**](https://androidfilehost.com/?fid=818070582850499029) **)。**
*   擦除系统/数据/供应商/缓存/Dalvik 分区。
*   小米 6 的闪光高音拉链。
*   刷新通用系统映像，然后重新启动。

我们预计，当 Android P 的最终版本发布时，非官方项目 Treble compatibility 将有助于小米设备的开发。

* * *

[**小米 6**](https://forum.xda-developers.com/mi-6/development/sagit-project-trouble-t3763762) 下载项目高音 ZIP