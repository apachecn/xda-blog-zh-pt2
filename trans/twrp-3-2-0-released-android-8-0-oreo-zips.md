# TWRP 3.2.0 发布，更好地支持安装 Android 8.0 拉链

> 原文：<https://www.xda-developers.com/twrp-3-2-0-released-android-8-0-oreo-zips/>

# TWRP 3.2.0 发布，更好地支持安装 Android 8.0 奥利奥拉链等

针对大多数设备的 TWRP 3.2.0 已经发布。它对安装基于 Android 8.0 的 zip、各种小错误修复和调整等有更好的支持。

TWRP 是 Android 上最受欢迎的自定义恢复，它的受欢迎程度还在继续增长，因为如果用户想要刷新自定义 rom、内核、mod 等，设备需要 TWRP 支持。最近，我们已经看到 TWRP 支持添加到更多设备中，包括小米 Mi A1 和华硕 ZenFone 4 变种。谷歌 Pixel 2 和 Pixel 2 XL [首先收到了定制恢复的 alpha 版本](https://www.xda-developers.com/twrp-recovery-alpha-pixel-2-xl-available/)，后来[升级为 beta 版本](https://www.xda-developers.com/twrp-beta-2-pixel-2-and-pixel-2-xl/)。

现在， [XDA 资深公认开发者](https://forum.xda-developers.com/member.php?u=912474) *Dees_troy* 宣布发布适用于大多数设备的 TWRP 3.2.0。自定义恢复的最后一个版本是 3.1.0 版— [于 3 月](https://www.xda-developers.com/twrp-v3-1-0-is-now-rolling-out-with-support-for-adb-backup-ab-ota-zips-and-more/)发布，支持 ADB 备份、A/B zip 等。3.2 版本仍然是一个点版本，所以没有添加任何主要功能。然而，这些变化仍然是受欢迎的，因为它们改善了用户体验。变更日志声明:

*   允许在 TWRP GUI (bigbiff)中恢复 adb 备份
*   修复 adb 备份中的 gzip 备份错误(bigbiff)
*   修正了 TWRP 备份程序中偶尔损坏备份文件的错误(nkk71)
*   更好地支持安装基于 Android 8.0 的拉链，由于传统的道具(nkk71)
*   在 8.0 固件(nkk71)中支持使用 keymaster 3.0 解密 vold
*   像素 2 合成密码的解密(Dees_Troy)
*   在 libtar (Dees_Troy)中支持更新的 ext4 FBE 备份和恢复策略
*   v2 fstab 支持(Dees_Troy)
*   将 TWRP 带到安卓 8.0 AOSP 基地(Dees_Troy)
*   各种其他小的错误修复和调整

最显著的变化包括允许用户在 TWRP GUI 中恢复 ADB 备份，以及更好地支持 Android 8.0 Oreo zips。Pixel 2 支持合成密码的解密。(之前， [*Dees_troy* 详细介绍了为实现解密](https://www.xda-developers.com/twrp-beta-2-pixel-2-and-pixel-2-xl/)对 Pixel 2 所做的工作量)。自定义恢复现在支持 v2 fstab，并且它已被带到 Android 8.0 AOSP 基地。

*Dees_troy* 注意到很多设备没能构建 TWRP 3.2.0。构建错误应该在未来几周内得到修复，我们肯定会在不久的将来看到更多的设备得到官方支持。

* * *

[**来源:Dees _ troy【Google+】**](https://plus.google.com/+DeesTroy/posts/PhAUQHMXnJK)