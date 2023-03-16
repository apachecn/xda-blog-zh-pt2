# Magisk 19.3 改进了 MagiskHide 中的过程监控，因为 Magisk Manager 7.2.0 获得了 UI 更新

> 原文：<https://www.xda-developers.com/magisk-19-3-process-monitoring-magiskhide-magisk-manager-7-2/>

# Magisk 19.3 改进了 MagiskHide 中的过程监控，因为 Magisk Manager 7.2.0 获得了 UI 更新

topjohnwu 发布了 Magisk 19.3，改进了 MagiskHide 中的进程监控，Magisk Manager 7.2.0 获得了一些 UI 更新。

在这一点上，我确信你们大多数人至少听说过 Magisk。是 XDA 知名开发商 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 的生根解决方案。该方法在不接触系统分区的情况下工作，因此更新软件和解除设备根是一个无缝的过程。开发者总是积极努力完善生根解决方案。刚才他发布了解决方案和 Magisk Manager 应用程序的新版本。变更日志是微妙但非常重要的，所以让我们深入了解它。

首先，也可能是最重要的一点是，MagiskHide 现在有了一个更好的过程监控系统。这解决了效率问题，这意味着在此过程中 CPU 不会 100%工作。守护进程崩溃也不太可能发生。这一幕后的改变应该会极大地改善幕后流程。MagiskInit 的大修也在进行中，它修复了许多设备上的引导错误。Magisk 19.3 还支持华为新的面向 Android 的文件系统，可扩展的只读文件系统，简称 EROFS。这将提高基于 EMUI 9.1 的 Android 系统的兼容性，因此大多数华为和 Honor 设备都采用了最新的固件。

Magisk 管理器也得到更新。7.2.0 版本对用户界面做了一些调整(如上)。如果你错过了，Magisk [的开发者在一个月前](https://twitter.com/topjohnwu/status/1116360618750226434)宣布，一名新的开发者将致力于 Magisk Manager，以改善该应用的 UI 和整体功能。看起来他一直在努力完善申请。吴炯还承诺未来会对这款应用进行更多的改动。

* * *

### **Magisk v19.3 和 Magisk Manager v7.2.0 变更日志**

*   神奇 v19.3
    *   [magis hide]极大地改进了进程监视器的实现，希望不会再导致 100%的 CPU 和守护进程崩溃
    *   [MagiskInit]等待分区为早期安装做好准备，应该可以修复少数设备上的引导问题
    *   [MagiskInit]支持 EMUI 9.1 中使用的 EROFS
    *   [MagiskSU]正确实现挂载名称空间隔离
    *   [MagiskBoot]标头 v2 的正确校验和计算
*   Magisk Manager v7.2.0
    *   巨大的用户界面革新
    *   未来会有更多甜蜜的改变！

* * *

你可以[导航到这个线程](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445/)来下载这两个并刷新/安装 Magisk 的 root 解决方案和管理器应用程序。确保在线程中查找说明和兼容性注释。