# TWRP 增加对小米 Mi Note 10 和 Mi Mix 3 5G 的支持

> 原文：<https://www.xda-developers.com/xiaomi-mi-note-10-mi-mix-3-5g-official-twrp-support/>

# TWRP 增加对小米 Mi Note 10 和 Mi Mix 3 5G 的支持

小米 Mi Note 10 和 Mi Mix 3 5G 现在由 TWRP 官方支持，这使得这些设备的所有者更容易尝试定制的 rom 和 mod。

用像 TWRP 这样的定制恢复取代库存恢复，让用户可以选择试用售后模块，并通过安装定制的 rom 和内核来定制他们的 Android 设备。除了像完整数据备份和恢复这样的常规功能，TWRP 还可以进一步修改以支持[真正的双引导](https://www.xda-developers.com/unofficial-twrp-enables-true-dual-boot-oneplus-7-pro-5g/)。该项目是开源的，因此社区开发者很乐意扩展支持设备的列表。现在，小米 Mi Note 10 和 Mi Mix 3 5G 增加了官方支持。

以相机为中心的小米 Note 10 只不过是小米中国独家[小米 CC9 Pro](https://www.xda-developers.com/xiaomi-mi-cc9-pro-108mp-penta-rear-camera-50x-zoom-snapdragon-730g-china-launch/) 的翻版。这款手机采用五后置摄像头设置，以 [108MP 三星 ISOCELL 亮 HMX 传感器](https://www.xda-developers.com/samsung-isocell-bright-hmx-108mp-camera-sensor-xiaomi/)为主。小米在内核源代码的[发布方面做得很好，帮助 XDA 高级成员](https://www.xda-developers.com/xiaomi-mi-note-10-cc9-pro-kernel-sources-android-9/) [mauronofrio](https://forum.xda-developers.com/member.php?u=4712355) 在 2019 年 12 月迅速为小米 Note 10 建立了 TWRP 的工作版本。从那以后，开发人员通过添加对 Android 10 的支持和正确的解密对它进行了微调。官方版本是由同一个人维护的，尽管你可以查看[讨论线程](https://forum.xda-developers.com/mi-note-10/development/recovery-unofficial-twrp-xiaomi-mi-note-t4015805)来获取带有最新修正的非官方版本。

**[糜注 10 TWRP](https://twrp.me/xiaomi/xiaomiminote10.html) || [糜注 10 XDA 论坛](https://forum.xda-developers.com/mi-note-10)**

一年多前，5G 版本的 Mi Mix 3 作为普通版 Mi Mix 3 的升级版[亮相](https://www.xda-developers.com/xiaomi-mi-mix-3-5g-qualcomm-snapdragon-855/)。这款手机还没有尝到 MIUI 11 和 Android 10 的味道，[不像它的 4G 版](https://www.xda-developers.com/download-xiaomi-mi-mix-3-receives-stable-android-10-update-with-miui-11/)。然而，小米[发布了](https://www.xda-developers.com/redmi-k20-pro-5g-xiaomi-mi-mix-3-kernel-sources/)Mi Mix 3 5G 的内核源代码，这是我们论坛上该设备可用的定制 rom 的基础。虽然收藏相当有限，但随着官方 TWRP 的面世，情况可能会有所好转。再一次，mauronofrio 是幕后的人，他也在我们的论坛上提供了一个[讨论主题](https://forum.xda-developers.com/mi-mix-3/development/recovery-unofficial-twrp-xiaomi-mi-mix-t3941867)。

**[米 Mix 3 5G TWRP](https://twrp.me/xiaomi/xiaomimix35g.html) || [米 Mix 3 5G XDA 论坛](https://forum.xda-developers.com/mi-mix-3/xiaomi-mi-mix-3-5g-andromeda)**

上述设备都没有使用 [A/B 分区方案](https://www.xda-developers.com/google-virtual-ab-seamless-updates-android-11/)，所以用户应该坚持使用标准的闪存方法，即`fastboot flash recovery twrp.img`命令。当然，在刷新之前，你需要解锁引导程序([，这可能是一个漫长的步骤](https://www.xda-developers.com/xiaomi-2-month-wait-unlock-bootloader/))。