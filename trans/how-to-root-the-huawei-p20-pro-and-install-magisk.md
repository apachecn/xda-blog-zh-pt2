# 如何 root 华为 P20 Pro 并安装 Magisk

> 原文：<https://www.xda-developers.com/how-to-root-the-huawei-p20-pro-and-install-magisk/>

# 如何 root 华为 P20 Pro 并安装 Magisk

用户现在可以在华为 P20 Pro 上 root 并安装 Magisk，因为 XDA 高级成员 LastStandingDroid 发布了一个修补的 ramdisk 映像。

华为 P20 和 P20 Pro [作为华为最新的旗舰智能手机](https://www.xda-developers.com/huawei-announces-huawei-p20-p20-pro-p20-lite/)于 3 月发布。华为 P20 Pro 是迄今为止最贵的华为智能手机。其高端规格列表包括海思麒麟 970 片上系统，6GB 内存搭配 128GB 存储，6 英寸全高清+ (2244x1080)有机发光二极管缺口显示屏，长宽比为 18.7:9，三个 40MP (RGB) + 20MP(单色)+ 8MP(长焦)后置摄像头，24MP 前置摄像头，以及 4000mAh 电池。这款手机在 Android 8.1 Oreo 的基础上搭载了 EMUI 8.1。

P20 和 P20 Pro 都由麒麟 970 SoC 提供动力。这款 SoC 也为华为 Mate 10 和 Mate 10 Pro 以及 Honor View 10 提供动力。二月，XDA 知名开发商 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 发布了 [Magisk 最新项目三倍华为设备，包括 Honor View 10](https://www.xda-developers.com/magisk-16-bootloop-crash-fix-huawei-honor-support/) 。官方对于 Honor View 10/华为 Mate 10/华为 Mate 10 Pro 的 Magisk 安装方法是需要获取一个 bootloader 解锁码，解锁 bootloader，打补丁股票 ramdisk 镜像，用 ADB 拉出来，然后通过 fastboot 进行闪存。

TWRP 尚未发布华为 P20 和 P20 Pro。到目前为止，还不能启动 P20 Pro，因为还没有启动映像被转储。

随着 XDA 资深成员 [LastStandingDroid](https://forum.xda-developers.com/member.php?u=4435346) 发布了华为 P20 Pro 的补丁 ramdisk 映像，这种情况现在发生了变化。这允许 P20 Pro(设备名称:CLT-L29)的用户引导他们的设备并安装 Magisk。这样做的说明是:

1.  从华为获取 bootloader 解锁代码。
2.  解锁引导加载程序。
3.  带 fastboot 的 flash ramdisk flash ramdisk CLT-L29-magisk . img，重启。

[LastStandingDroid](https://forum.xda-developers.com/member.php?u=4435346) 提到这种方法已经在华为 P20 Pro 的演示设备上进行了测试。Magisk 被证实可以工作，他还表示他将很快发布一个华为 P20 的补丁启动映像。

* * *

[**来源:XDA 论坛**](https://forum.xda-developers.com/huawei-p20/how-to/magisk-root-p20-pro-t3773781)