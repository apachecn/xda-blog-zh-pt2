# Transformer TF300T 上的 ArchLinux

> 原文：<https://www.xda-developers.com/archlinux-on-the-transformer-tf300t/>

在 Android 上运行 Linux 是一个[古老的最爱](http://www.xda-developers.com/android/samsung-galaxy-nexus-gets-linux-on-android-support/)。从完全安装到不太复杂的 *chroot* 方法，新旧项目都有，用户可以在各种设备上运行 Linux。唯一的限制是你可以加载的 Linux 发行版。大多数情况下，它是 Ubuntu 或其他基于 Debian 的发行版。现在，[华硕变压器 TF300T](http://forum.xda-developers.com/forumdisplay.php?f=1578) 车主可以安装 Arch 了。

这种方法已经存在一段时间了，但是已经通过更新得到了完善。XDA 论坛成员 [cb22](http://forum.xda-developers.com/member.php?u=374382) 发布了方法。尽管它并不完美，但绝对是一个坚实的开端。以下是当前工作的列表:

> 安卓双开机。
> 
> 内部存储和 MicroSD 卡
> 
> X11，带合成
> 
> 声音的
> 
> 鼠标和键盘，以及坞站热插拔。
> 
> 触摸屏
> 
> 播放视频(全 1080P 效果很棒。)使用 Xfce 的媒体播放器
> 
> 传感器(光、指南针、加速度计、陀螺仪)。这些都暴露在 sysfs 下。
> 
> 充电/坞站充电。这似乎是由内核管理的。
> 
> USB 小工具(作为通过 USB 访问网络的 RNDIS 设备)
> 
> CPU 频率缩放/ Tegra LP 内核。LP 内核是自动使用的，您可以在/sys/kernel/cluster/active 中看到它的状态(当该文件读取 LP 时),它的用途就是当前 CPU1 的用途。
> 
> WiFi，带网络管理器
> 
> 3G，在 TF300TG 型号上，带网络管理器
> 
> Xfce 中的电池(和坞站)状态
> 
> 坞站上的 USB 端口
> 
> 一些明智的按键重映射(后退->退出，搜索-> Alt，Home -> Super)

目前不起作用的大东西是从 Linux 重启、蓝牙和双指滚动。这些也恰好在计划要修复的事情的短列表上。还有很多是未经检验的。

有关安装说明和更多细节，请查看[原始螺纹](http://forum.xda-developers.com/showthread.php?t=1918849)。