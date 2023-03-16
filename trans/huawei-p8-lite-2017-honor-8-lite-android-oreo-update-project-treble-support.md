# 华为 P8 Lite 2017/Honor 8 Lite 安卓奥利奥更新带来项目高音支持

> 原文：<https://www.xda-developers.com/huawei-p8-lite-2017-honor-8-lite-android-oreo-update-project-treble-support/>

华为 P8 Lite 2017 和 Honor 8 Lite 是同一款手机的不同名称。两款手机都有相同的规格列表，包括海思麒麟 655 片上系统，3GB 内存搭配 16GB 存储或 4GB 内存搭配 64GB 存储，5.2 英寸全高清(1920x1080) IPS 显示屏，12MP 后置摄像头，8MP 前置摄像头和 3000mAh 电池。华为 P8 Lite 2017 于 2017 年 1 月发布，EMUI 5.0 基于 Android 7.0 牛轧糖。几个月后，Honor 8 Lite 面向不同市场发布。

最近几个月，我们已经看到过去的华为和 Honor 设备在 [Project Treble](https://www.xda-developers.com/tag/project-treble/) 支持下正式更新。华为 Mate 9、华为 P10 和 P10 Plus、Honor 8 Pro、 [Honor 7X](https://www.xda-developers.com/honor-7x-android-oreo-beta-emui-8-0-project-treble/) 以及更多产品通过其 Android Oreo 更新获得了 Project Treble 支持。现在，华为 P8 Lite 2017/Honor 8 Lite 加入了官方更新的支持 Project Treble 的华为手机名单。

华为 P8 Lite 2017 PRA 的用户必须重新命名他们的设备，以支持 8 Lite AL00C/AL00X/TL10C B220。然后，他们可以为 Honor 8 Lite 安装基于测试版中文 Android Oreo 的 EMUI 8 更新，这带来了 Project Treble 支持。XDA 资深会员 [Fr0nk](https://forum.xda-developers.com/member.php?u=7186719) 给出了安装测试版更新的指南:

*   下载[这张 TWRP 图片](http://www.hassanmirza01.blogspot.it/p/elite-twrp.html)。
*   从[这里](http://www.pro-teammt.ru/firmware-database/?firmware_model=pra-al00&firmware_page=0)下载最后一个 Android Oreo update.zip，放在外部存储器上。
*   下载 [nocheck 恢复](http://www.drive.google.com/open?id=1LKMjje29u0X7xLjalMCZImZRGGTqJOrJ)。
*   从引导加载程序闪存 TWRP。
*   启动到 TWRP >点击安装>选择镜像安装>选择 nocheck.img 并安装在恢复分区。
*   在 TWRP 菜单中，单击高级>选择终端，然后键入不带引号的' ' echo-update _ package =/SD card/update . zip >/cache/recovery/command ' '。
*   在 TWRP 终端键入“重启恢复”。它应该会自动重启并完成安装。
*   开机前，华为恢复库存并执行一次数据格式化，然后重启。

在安装了测试版 Android Oreo 更新后，华为 P8 Lite 2017/Honor 8 Lite 用户可以选择继续使用 EMUI 8.0。他们可以通过下载并刷新 Android 奥利奥 TWRP，安装 GMScore.apk(这将导致设备自动重启)，然后安装 Play Store 和谷歌服务 APKs，在 EMUI 中安装 Play Store。

或者，用户可以选择刷新 Android Oreo 的通用系统映像(GSI)。他们可以闪现一个 AOSP GSI，比如 XDA 知名开发商 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 的 [Phh-Treble](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/experimental-phh-treble-t3709659) 。(通过 XDA 资深会员 Fr0nk)的操作说明如下:

*   为设备下载安卓奥利奥 TWRP 。
*   下载通用系统映像。
*   闪光 TWRP 奥利奥。在 TWRP，点击安装>选择安装镜像并安装到系统镜像分区。
*   进行出厂重置，然后重启。

XDA 公认的贡献者 [haky 86](https://forum.xda-developers.com/member.php?u=4883214) 也发布了华为 P8 Lite 2017 的非官方项目高音启用 LineageOS 15.1(基于 Android 8.1 Oreo)。在 P8 Lite 2017 上安装非官方 LineageOS 15.1 的说明如下:

*   下载 tar.gz 档案。
*   使用归档管理器提取 system.img。
*   重新启动到快速启动模式并运行:快速启动闪存系统 system.img &&快速启动重新启动。
*   重新引导至 TWRP 并运行出厂重置以引导 linegeos-15.1。

目前，NFC 在非官方的 LineageOS 15.1 ROM 中不工作，信号总是被报告为低。开发人员声明他正计划修复这两个错误。

* * *

[**来源 1: XDA 论坛**](https://forum.xda-developers.com/p8lite/p8-lite-2017-discussion/guide-holy-emui8-treble-rom-pra-lx1-t3773216) [**为华为 P8 Lite 2017**](https://forum.xda-developers.com/p8lite/p8-lite-2017-development/rom-lineageos-15-1-huawei-p8-lite-2017-t3774331) 下载 LineageOS 15.1(项目高音使能)