# 开发者将 LineageOS 移植到面向儿童的 LeapFrog Epic 平板电脑上

> 原文：<https://www.xda-developers.com/developers-port-lineageos-leapfrog-epic-tablet-for-children/>

# 开发人员将 LineageOS 移植到...LeapFrog 儿童史诗平板电脑，为什么不呢？

一名开发人员在 LeapFrog Epic 上实现了启动 LineageOS 14.1 的惊人壮举，leap frog Epic 是一款最初搭载 Android 4.4 的儿童平板电脑。

Android 平板电脑可以有各种形状和尺寸，但 2015 年在 XDA 发布的 [LeapFrog Epic](https://store.leapfrog.com/en-us/store/p/leapfrog-epic-7-kids-tablet-with-16gb-memory-and-quadcore-processor/_/A-prod31576) 未能成为头条新闻。作为一款面向儿童的“教育”平板电脑，这款设备运行在高度贴肤的 Android 4.4 KitKat 版本上。这个玩具内部是一个四核联发科处理器，1 GB 内存，16GB 卡插槽和 7 英寸 1024×600 显示屏。本质上，它类似于那个时代的亚马逊 Fire 平板电脑，有一堆软件强加了限制。现在——在发布近 5 年后的——这款平板电脑获得了一系列的好评。

XDA 资深成员 [blakegriplingph](https://forum.xda-developers.com/member.php?u=4092918) 已经与开发者 [mac2612](https://forum.xda-developers.com/member.php?u=3404943) 、 [R0rtiz](https://forum.xda-developers.com/member.php?u=8978978) 、 [Kai2000](https://forum.xda-developers.com/member.php?u=9605864) 和[合作，限定](https://forum.xda-developers.com/member.php?u=8184192)为 LeapFrog Epic 带来 LineageOS 14.1(基于 Android 牛轧糖)的非官方端口，以寻求通过提供接近库存的 Android 体验来重新定位这些平板电脑。要安装 ROM，您需要解锁 Epic 的引导加载程序，并安装一个兼容的自定义恢复映像。由于 LeapFrog 没有官方的 bootloader 解锁工具，开发者甚至[想出了一个*破解*的解决方案](https://forum.xda-developers.com/showpost.php?p=83474783&postcount=245)。由于非官方解锁方法的性质，建议在修改事件之前[为您的设备创建一个完整的 eMMC 备份](https://huckleberrypie57.blogspot.com/2018/12/and-i-came-in-for-another-leapfrog-epic.html)。

如果你对此感兴趣的话，有几个注意事项。首先，这个 ROM 的电池寿命相对来说比股票软件差。此外，由于缺少硬件加速解码支持，视频录制会使相机应用程序崩溃，1080p 视频播放滞后很多。NVRAM 无法正确处理，这可能是因为缺少 SELinux 权限。诚然，这远不是一个稳定的蛙跳史诗定制 rom，但它很好地为一个容易过时并因此被丢弃的设备注入了新的生命。前往下面链接的线程，获得闪烁的指令。

**[非官方线报 14.1 为越级史诗——XDA 线报](https://forum.xda-developers.com/android/development/rom-lineageos-14-1-leapfrog-epic-t4161311)**