# Android 5.0.2 和 Nexus 7 (Wi-Fi)的新出厂图像可用

> 原文：<https://www.xda-developers.com/android-5-0-2-factory-images-nexus-7-wifi/>

# Android 5.0.2 和 Nexus 7 (Wi-Fi)的新出厂图像可用

谷歌推出了其移动操作系统的另一个小更新。Android 5.0.2 带来了几项主要针对平板电脑的改进。

自 11 月初以来，Android 5.0 已经公开发布[，安装谷歌最新操作系统的设备数量与日俱增。在发布后的最初几周，谷歌专注于稳定性，并发布了相当多的更新版本。现在，是时候进行一次小小的数字提升了，因为 Android 5.0.2 刚刚被推送到谷歌的 AOSP 回购中。](http://www.xda-developers.com/android/android-5-0-lollipop-source-complete/)

Android 5.0.1 [是相当小的更新](http://www.xda-developers.com/android/android-5-0-1_r1-source-images/)，只有一些显著的变化。Android 5.0.2 肯定更大，但还是不大。谷歌设法解决了 *MountService* 的一些问题，现在应该在 *performBootDexOpt* 之前开始。这修复了之前在[问题跟踪器](https://code.google.com/p/android/issues/detail?id=79264)中报告的一个错误。与 NAND 相关的其他一些变化也已推出。Android 4.3 中引入的 Fstrim 在 Lollipop 上引起了一些严重的问题。根据 XDA 知名开发商 cybojenix 提供的日志[,当晚关机的设备在启动 fstrim 时出现了问题。谷歌解决了这个问题，现在使用慢速 NAND 的设备应该有明显的性能提升。](https://gist.github.com/anonymous/8bc6a5ea7a6f113167b6)

Nexus 7 (Wi-Fi)和 Nexus 7(移动数据)设备树已更新。因此，Nexus 7 (2012)的新出厂映像和更新的二进制文件已经推出。像往常一样，你可以从 Android 开发者页面获得它们。罗非鱼的更新设备树是一个好迹象，因为它是尚未收到官方更新的两个设备之一。隧道尽头有一盏灯，预示着谷歌最终将尽快为失踪的设备带来官方的棒棒糖。

如果您想自己构建 Android 5.0.2，可以通过执行以下命令来更新您当前的源代码:

`repo init -b android-5.0.2_r1 && repo sync`