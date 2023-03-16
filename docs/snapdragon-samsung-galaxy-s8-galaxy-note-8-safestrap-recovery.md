# 骁龙三星 Galaxy S8/S8+和 Galaxy Note 8 现在可以安装安全带恢复功能

> 原文：<https://www.xda-developers.com/snapdragon-samsung-galaxy-s8-galaxy-note-8-safestrap-recovery/>

美国骁龙三星 Galaxy 设备在定制开发方面几乎没有希望，因为运营商要求三星不得发布官方引导加载程序解锁工具。这些设备获得 root 访问权限的唯一方法是找到漏洞。对于三星 Galaxy S8、三星 Galaxy S8+和三星 Galaxy Note 8 来说，这正是发生在 [SamFail 漏洞利用](https://www.xda-developers.com/samsung-galaxy-note-8-root-samfail/)上的事情。利用 root 权限，XDA 资深会员 [afaneh92](https://forum.xda-developers.com/member.php?u=4770483) 为三台设备创建了一个安全带恢复。安全带恢复就像 TWRP，但它与锁定的引导加载程序一起工作。

Safestrap 是带锁定引导程序的手机的恢复**。它基于 TWRP 3.2.1，并使用当前可用于 SamFail 漏洞利用的 root 进行工作。它的工作原理是当你重启手机时显示一个闪屏，允许你启动到安全恢复或系统。恢复允许你有多达 4 个 ROM 插槽旁边的股票 ROM。**

当刷新文件时，您可以选择要刷新的 ROM 插槽，然后返回刷新文件、备份、恢复备份或擦除分区，就像解锁引导程序的手机的普通 TWRP 一样。除了普通 TWRP 的所有功能，开发者还添加了一个引导选项菜单，允许你创建虚拟 ROM 插槽。这些存储在数据分区中，所以 rom 越多，可用的存储空间就越少。

如果你在三星 Galaxy S8、Galaxy S8+或 Galaxy Note 8 上安装了 Safestrap，请注意**它将仅限于 Android 牛轧糖**。这也将限制你 80%的电池，因为根方法使用。遗憾的是，在 Galaxy S8、S8+和 Note 8 上获得 root 访问权限的唯一已知方法是通过 SamFail 漏洞，该漏洞已被修补。目前，您可能无法安装完全定制的基于 AOSP 的 rom，如 LineageOS 14.1，但这可能很快就会实现。

* * *

## 如何在三星 Galaxy S8/S8+和三星 Galaxy Note 8 上安装 Safestrap 恢复功能

[**根为骁龙三星 Galaxy Note 8**](https://forum.xda-developers.com/galaxy-note-8/development/root-samfail-galaxy-note8-t3685340)

[**根为骁龙三星 Galaxy S8**](https://forum.xda-developers.com/galaxy-s8/development/root-partcyborgrom-aqi6-deodexed-t3702988)

[**根为骁龙三星银河 S8+**](https://forum.xda-developers.com/galaxy-s8+/development/root-partcyborgrom-aqk3-samfail-odin-t3717702)

要进行 flash Safestrap 恢复，您需要使用上述 Galaxy S8、S8+或 Note 8 的 root 方法之一来启动您的手机。在你的手机生根之后，你需要去谷歌 Play 商店安装一个 busybox 安装程序，然后安装 busybox。

安装完成后，您需要在您的设备上安装 APK 安全带。

[**三星 Galaxy Note 8 的 Safestrap 恢复**](https://forum.xda-developers.com/galaxy-note-8/development/recovery-locked-nougat-7-1-1-safestrap-t3772765)

[**骁龙三星 Galaxy S8**T3【安全带恢复】](https://forum.xda-developers.com/galaxy-s8/development/recovery-locked-nougat-7-0-safestrap-t3772760)

[**【骁龙三星 Galaxy S8+】**](https://forum.xda-developers.com/galaxy-s8+/development/recovery-locked-nougat-7-0-safestrap-t3772761)

在 Safestrap 应用程序中，您必须同意条款，然后选择“**安装恢复”**按钮。当应用程序中显示的状态变为“已安装”时，您就会知道它已安装。一旦安装，你可以重启你的手机，你应该会看到启动画面。最后，要访问 Safestrap recovery，请选择闪屏上的菜单按钮。进入菜单后，您将可以访问 Safestrap。