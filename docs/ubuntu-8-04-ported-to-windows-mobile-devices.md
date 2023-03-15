# 移植到 Windows Mobile 设备的 Ubuntu 8.04

> 原文：<https://www.xda-developers.com/ubuntu-8-04-ported-to-windows-mobile-devices/>

与致力于将 ANDROID 移植到广受欢迎的 Windows Mobile 设备(如 Raphael、Blackstone、Rhodium 和 Diamond)的 [XDANDROID](http://forum.xda-developers.com/showthread.php?t=601751 "XDANDROID Raphael thread") 项目非常相似，该论坛的各个成员一直在共同努力，将完整的 Ubuntu Linux 发行版移植到一系列手机上。

这源于 [fatsal](http://forum.xda-developers.com/member.php?u=434568) 对索尼爱立信 XPERIA X1 的移植，但支持和开发已经大幅增长，该操作系统现在可以在其他几个设备上工作(具有不同程度的功能)。

该端口的操作与 Android 非常相似。用户必须将相关的系统文件放入 SD 卡的根目录下，并运行 haret.exe 来引导进入 Linux。所有设备的 WiFi 支持应该是固定的，但触摸屏必须像触控板一样使用才能移动光标。显然，不能通过 Ubuntu 打电话和发短信，因为它是作为一个完整的 PC 操作系统设计的，而不是移动操作系统。

对于您自己的设备，请查看相应的主题，仔细阅读给定的说明(因为它们在不同的设备之间有所不同),并记住下载适当的 zImage:

> **[fatsal 的线程为 XPERIA X1](http://forum.xda-developers.com/showthread.php?t=631437)**
> 
> **[【jesusfreak 316】拉斐尔的线与钻石](http://forum.xda-developers.com/showthread.php?t=635770)**
> 
> **[dsfreak0109 的螺纹为黄玉](http://forum.xda-developers.com/showthread.php?t=644539&highlight=ubuntu)**
> 
> **[sebbo90 的 Rhobuntu 线为铑](http://forum.xda-developers.com/showthread.php?t=640785)**
> 
> Rhodium 用户还应该阅读 RhodiumT3 的 Ubuntu 上的 [W **iki 条目**](http://wiki.xda-developers.com/index.php?pagename=RhodiumUbuntu)

如果你的设备目前还没有出现，不要担心:该项目仍在发展，很可能在未来几周内扩展到其他设备。