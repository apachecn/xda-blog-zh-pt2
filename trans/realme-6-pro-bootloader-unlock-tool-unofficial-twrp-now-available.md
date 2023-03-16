# Realme 6 Pro bootloader 解锁工具和非官方 TWRP 现已上市

> 原文：<https://www.xda-developers.com/realme-6-pro-bootloader-unlock-tool-unofficial-twrp-now-available/>

Realme 6 Pro 提供了一些可靠的规格，例如[高通骁龙 720G](https://www.xda-developers.com/qualcomm-snapdragon-720g-662-460-navic/) SoC，高达 8GB 的 LPDDR4X RAM，以及高达 128GB 的 UFS 2.1 存储，价格非常诱人。该设备采用 90Hz 打孔显示屏，同时配备 4,300mAh 电池，支持 30W 快速充电。软件方面，手机开箱运行基于 Android 10 的 Realme UI。该公司已经[发布了该设备的内核源代码](https://www.xda-developers.com/kernel-sources-for-the-realme-6-6-pro-c3-and-5i-are-now-available/)，以符合 GNU 通用公共许可证 v2，但如果没有解锁的引导加载程序，售后市场开发基本上是不可能的。

**[Realme 6 Pro XDA 评测:一款拥有一些高端功能的全面平价智能手机](https://www.xda-developers.com/realme-6-pro-review/)**

就像大多数其他 Realme 手机一样，Realme 6 Pro 的引导加载程序必须在解锁前使用独特的设备特定解锁应用程序进行验证(通常称为“深度测试”)。尽管还没有正式发布，该社区已经设法获得了 Realme 6 Pro 的引导加载器解锁应用程序，这是由 XDA 成员 [barakcodam](https://forum.xda-developers.com/member.php?u=10757359) 和 XDA 成员 [Rizezky](https://forum.xda-developers.com/member.php?u=5457987) 提供的。

[realme 6 pro xd 论坛](https://forum.xda-developers.com/realme-6-pro)

感兴趣的用户可以从以下镜像下载 APK，并将其侧载以申请深度测试，以便有资格使用 Fastboot 解锁引导加载程序。如果你正在寻找一个详细的教程来解锁引导程序以及禁用这部手机上的 Android 验证引导，XDA 成员 [nullxception](https://forum.xda-developers.com/member.php?u=10333947) 已经[为你提供了](https://forum.xda-developers.com/realme-6-pro/how-to/guide-unlocking-bootloader-disabling-t4104045)。

**下载 Realme 6 Pro 深度测试(Bootloader 解锁)APK:[Google Drive](https://drive.google.com/file/d/16az-7SHoPyJhDIi4p4x7wj1cRUcsPwCM/view)| |[MEGA](https://mega.nz/file/xshHHC4Q#kJINQ--_bSSBS8CxohNqB9iIHUldz-FpQSJOZb3ehQE)**

由于内核源代码和解锁引导程序的存在，XDA 成员 [nullxception](https://forum.xda-developers.com/member.php?u=10333947) 也为该设备编译了一个非官方版本的 TWRP。基于 TWRP 3.3.1，当前版本在智能手机的 **RMX2061** 变种上进行测试。用户可以通过这个 TWRP 解密“数据”分区和 flash stock Realme UI 更新包(OZIP ),尽管目前还不支持格式化现有分区。请注意，Realme 不提供 flash 工具，所以要小心。

**[Realme 6 Pro TWRP — XDA 下载讨论线程](https://forum.xda-developers.com/realme-6-pro/development/rmx2061-unofficial-twrp-realme-6-pro-t4107907)**