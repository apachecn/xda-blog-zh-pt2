# 小米 Mi 10 和 Mi 10 Pro 现已推出非官方 TWRP

> 原文：<https://www.xda-developers.com/unofficial-twrp-is-now-available-for-the-xiaomi-mi-10-and-mi-10-pro/>

小米 2020 年的 mi 系列旗舰产品-Mi 10 和 Mi 10 Pro -由[高通骁龙 865](https://www.xda-developers.com/qualcomm-snapdragon-865-processor-specifications-features/) SoC 加上 LPDDR5 RAM 和 UFS 3.0 存储驱动。得益于[骁龙 X55 调制解调器](https://www.xda-developers.com/qualcomm-snapdragon-x55-5g-modem-2019-android-smartphones/)，米 10 系列还支持双模(SA/NSA) 5G。小米甚至在他们国家的[发布会](https://www.xda-developers.com/xiaomi-launches-mi-10-90hz-screen-108mp-camera-snapdragon-865/)后不久[就发布了设备二人组的内核源代码](https://www.xda-developers.com/xiaomi-mi-10-kernel-source-code/)。如果你打算购买 Mi 10 或其 Pro 版本来探索售后市场发展，你应该很高兴知道他们现在已经收到了一个统一的、非官方的 TWRP 版本。

**[米 10 XDA 论坛](https://forum.xda-developers.com/xiaomi-mi-10) ||| [米 10 亲 XDA 论坛](https://forum.xda-developers.com/xiaomi-mi-10-pro)**

Mi 10 家族自带 Android 10，这使得为他们编译一个完全可用的 TWRP 版本相当困难。受欢迎的定制恢复项目正在进行大规模重组，原因是随着 Android 10 的发布，谷歌对 AOSP 恢复环境进行了大量的改变。TWRP 团队正忙着重写各种内部模块以支持搭载 Android 10 的设备，但是还没有关于稳定版本的具体时间表。

尽管面临所有这些障碍，XDA 资深成员 [simonsmh](https://forum.xda-developers.com/member.php?u=7141309) 还是设法为这些智能手机编译了一个实验性的 TWRP 版本。统一版基于 TWRP 3.3.1，自定义恢复可以通过读取`ro.boot.hwversion`属性的值无缝确定底层设备。“数据”分区的解密正在工作，您甚至可以挂载“系统”、“供应商”和“产品”分区，尽管是在只读模式下。非工作组件的列表预计会很长，比如坏的 ADB 侧加载、缺少 USB OTG 支持以及无法格式化现有分区。幸运的是，大多数错误都不是特定于设备的，一旦 TWRP 开发人员开始合并适当的上游提交，这些错误就会被修复。

**TWRP 下载讨论线程:[米 10](https://forum.xda-developers.com/xiaomi-mi-10/development/experimental-unofficial-twrp-mi-10-t4106381)| |[米 10 Pro](https://forum.xda-developers.com/xiaomi-mi-10-pro/development/experimental-unofficial-twrp-mi-10-10-t4106385)**

请注意，出于稳定性原因，TWRP 映像不应在目标设备上永久闪烁。相反，建议用户选择使用快速启动界面临时启动 IMG 文件。为了鼓励开源开发的精神，开发者的 GitHub 档案中提供了[设备树](https://github.com/simonsmh/android_device_xiaomi_umi)和[恢复源](https://github.com/simonsmh/android_bootable_recovery)。