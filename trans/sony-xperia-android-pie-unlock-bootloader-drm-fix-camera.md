# 解锁引导加载程序不再损坏运行 Android Pie 的索尼 Xperia 设备上的相机

> 原文：<https://www.xda-developers.com/sony-xperia-android-pie-unlock-bootloader-drm-fix-camera/>

索尼移动是开源和开发者友好程度最高的原始设备制造商之一，拥有像英雄开源开发者和索尼开放设备这样的程序。索尼发布了如何[构建 Linux 4.4 内核](https://www.xda-developers.com/xperia-open-devices-linux-4-4-kernel/)或[最新安卓版本](https://www.xda-developers.com/sony-builde-aosp-android-pie-xperia-devices/)的指南，甚至是如何[解锁他们设备的引导程序](https://www.xda-developers.com/sonys-open-device-program-releases-an-updated-guide-for-unlocking-bootloader-of-the-xperia-devices/)。不幸的是，解锁任何索尼 Xperia 设备的引导加载程序都会导致很多不良后果。例如，相机完全坏了，结果除了绿色的图片什么也没有。其他软件功能，如索尼的视频和音频增强功能也坏了，即使你坚持使用股票的 ROM。失去索尼的视频和音频调整是一回事，但不得不处理一个坏掉的相机是许多人不愿意做出的权衡。幸运的是，Android Pie 更新似乎不再损坏带有未锁定 bootloaders 的 Xperia 设备上的摄像头。

对于上下文，索尼 Xperia 设备有一个 trim area (TA)分区，其中包含 DRM 密钥和其他设备特定的信息，如 IMEI、序列号、MAC 地址等。解锁引导加载程序会清除 TA 分区中的 DRM 密钥。一旦数据被擦除，没有备份就无法恢复(除非您已经有了 root 用户，否则无法进行备份)。没有 DRM 密钥，索尼专有的音频和视频功能(X-Reality 视频增强、DSEE HX、ClearAudio+等。)对股票 ROM 不起作用。然而，解锁引导加载程序也*顺便提一下*破坏了相机的功能，因为可能的错误涉及无法读取 DRM 密钥(这个问题仍然没有得到很好的理解)。(*感谢 XDA 知名开发商[本人](https://forum.xda-developers.com/member.php?u=3816568)和 [Luk1337](https://forum.xda-developers.com/member.php?u=5075128) 的讲解。*)索尼甚至在解锁引导程序之前警告你:

> #### “由于删除了 DRM 安全密钥，您设备上的某些预装内容也可能无法访问。对于运行最新软件版本的设备，例如 Xperia Z3，删除 DRM 安全密钥可能会影响高级相机功能。例如，降噪算法可能会被删除，在弱光条件下拍照的性能可能会受到影响。”- [索尼移动](https://developer.sony.com/develop/open-devices/get-started/unlock-bootloader/)

您可能会失去的 DRM 相关功能包括一些相机后处理功能、色域配置文件、白平衡、X-Reality 视频增强、DSEE HX、ClearAudio+和 Widevine L1 对高清网飞的支持。随着时间的推移，一些聪明的开发人员，如 XDA 的高级成员[托拜厄斯.瓦尔德沃格尔](https://forum.xda-developers.com/xperia-z5/development/root-automatic-repack-stock-kernel-dm-t3301605)、 [mbc07](https://forum.xda-developers.com/member.php?u=5604590) 、[蒙杰尼](https://forum.xda-developers.com/member.php?u=4120742)和其他人，发现了通过修改核心系统库[或](https://www.xda-developers.com/restore-lost-functionality-unlocked-xperia/)[模拟没有根的锁定设备](https://forum.xda-developers.com/xz-premium/development/hack-mod-sony-xperia-xz-premium-twrp-t3695171)来恢复失去的功能的方法。索尼可能打算在解锁引导程序后破坏 DRM 相关的功能，但尚不清楚拍摄绿色照片的相机是否是故意的。

尽管如此，使用技巧可能不再是必要的，至少让相机工作，因为 XDA 资深成员[缪斯东](https://forum.xda-developers.com/member.php?u=4756773)和[其他人在更新他们的设备到 Android Pie 后发现](https://forum.xda-developers.com/xz-premium/how-to/android-pie-9-firmware-47-2-0-306-t3865226)。XDA 资深会员[lazer 10 rd](https://forum.xda-developers.com/member.php?u=7836278)好心地为我们录制了一段视频，展示了他根深蒂固的运行 Android 9 Pie 的索尼 Xperia XZ Premium 仍然能够使用相机。他还测试了哪些功能可以正常工作，哪些功能仍然被索尼破坏:

*   **什么有效**:色域配置文件，相机不再拍摄绿色图片(质量不保证相同，但至少有效)，白平衡，Camera2API(后置摄像头全无 RAW，前置摄像头有限)
*   **什么不起作用** : X-Reality 视频增强，DSEE HX，ClearAudio+，威德文 L1

总之，所有与 DRM 相关的音频和视频功能仍然不工作，但相机不再是坏的，这是索尼用户的一个大问题。

我们不确定是什么让索尼决定在解锁引导加载程序时不再损坏相机，但我们希望这不仅仅是他们的设备更新到 Android Pie 时的一个错误。我们不明白为什么索尼觉得有必要限制解锁引导程序的用户访问他们的摄像头、视频和音频功能，特别是因为这迫使一些社区成员转向第三方付费服务。Android Pie 目前可用于以下索尼 Xperia 设备，所以如果你有下面列出的设备之一，那么你应该能够享受定制的 rom 而不完全牺牲相机。

*   索尼 Xperia XZ Premium
*   索尼 Xperia XZ1
*   索尼 Xperia XZ1 紧凑型
*   索尼 Xperia XZ2
*   索尼 Xperia XZ2 紧凑型
*   索尼 Xperia XZ2 高级版
*   索尼 Xperia XZ3(引导加载程序解锁尚不可用)

*本文于美国东部时间上午 10:08 更新，以使 DRM 定位和相机之间的区别更加清晰。*