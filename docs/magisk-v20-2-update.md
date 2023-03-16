# Magisk v20.2 允许模块包含自定义策略修补程序，并引入了新的模块安装程序格式

> 原文：<https://www.xda-developers.com/magisk-v20-2-update/>

# Magisk v20.2 允许模块包含自定义策略修补程序，并引入了新的模块安装程序格式

Magisk (v20.2)的最新更新现在允许模块包含自定义的 sepolicy 修补程序，并引入了新的模块安装程序格式。

Magisk 是 Android 用户释放设备全部潜力的最佳工具之一。这是一个由 XDA 知名开发商 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 开发的无系统界面，可以用于从给你的设备找根到给它添加独特功能的任何事情。使用它最好的一点是，它允许用户修改系统设置，而不需要实际修改系统文件。它受欢迎的另一个原因是它能够绕过谷歌的[安全网](https://forum.xda-developers.com/apps/magisk/guide-magisk-troubleshooting-t3641417/post73145987#post73145987)，该安全网阻止某些应用在根设备上运行。去年年底，topjohnwu [推出了 Magisk v20.1](https://www.xda-developers.com/magisk-v20-1-magisk-manager-v7-4-0-introduces-new-hiding-mode-for-android-9-devices/) 和 Magisk Manager v7.4.0，对界面进行了一些有趣的更新。现在，他们发布了 v20.2，其中包括更多的变化和 Magisk 和 Magisk Manager 的错误修复。

根据我们论坛上发布的发行说明，此次更新改进了根请求提示，支持修补 dtb/dtbo 分区格式，支持模块中的预初始化 sepolicy 修补程序，以及旨在使创建新模块更容易的新模块安装程序格式。

这是 Magisk v20.2 的官方变更日志:

*   [MagiskSU]正确处理守护程序和应用程序之间的通信(root 请求提示)
*   [MagiskInit]修复 kmsg 中的日志记录
*   [MagiskBoot]支持修补 dtb/dtbo 分区格式
*   [常规]支持模块中的预初始化策略修补程序
*   [脚本]更新 magisk 库存图像备份格式
*   Magisk Manager v7.5.0:
    *   支持新的 MagiskSU 通信方法(ContentProvider)
    *   修复隐藏存根 APK 的几个问题
    *   支持使用生物计量提示(面部解锁)

有关模块的预初始化 sepolicy 补丁和新模块安装程序格式的更多信息，可以访问下面链接的 GitHub 源代码。如果你对使用更新的安装程序格式创建新的 Magisk 模块感兴趣，你可以按照 [topjohnwu 的指南](https://topjohnwu.github.io/Magisk/guides.html)学习如何使用新的模块模板。

* * *

**来源: [XDA 论坛](https://forum.xda-developers.com/showpost.php?p=81364297&postcount=57)， [GitHub](https://github.com/topjohnwu/magisk_files/blob/de0ebcfdf314133118e1fd4bbbf12db9ae7f4613/notes.md) ，**