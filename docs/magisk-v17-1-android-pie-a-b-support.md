# Magisk v17.1 发布，提供更好的 Android Pie 和 A/B 设备支持

> 原文：<https://www.xda-developers.com/magisk-v17-1-android-pie-a-b-support/>

# Magisk v17.1 发布，提供更好的 Android Pie 和 A/B 设备支持

Magisk v17.1 已经发布，更好地支持 Android Pie 和 A/B 分区设备。你可以在这里获得完整的 changelog 并下载 Magisk！

当谈到植根于你的 Android 智能手机时，每个人都指出 XDA 公认的开发者/公认的贡献者 Magisk 是开始的最佳地方。这是给你的 Android 智能手机加根的最简单的方法之一，它也完全支持 Magisk 模块。这些模块允许您无系统地替换设备/系统分区上的文件。Magisk 最大的卖点在于它是一种隐藏 root 用户的方法。这使得用户即使在手机解锁和开机的情况下也能玩像 Pokemon Go 这样的游戏。

Magisk v17.1 现已发布，更好地支持 [A/B 分区设备](https://www.xda-developers.com/how-a-b-partitions-and-seamless-updates-affect-custom-development-on-xda/)和运行 Android Pie 的智能手机。这还不是全部，因为 Magisk v17.1 还支持三星 Galaxy S9、三星 Galaxy S9+和三星 Galaxy Note 9。您可以查看以下 Magisk 和 Magisk Manager 的完整变更日志。

## 神奇 v17.1 变更日志

*   [常规]将安装带回到 A/B 设备上 OTA 的非活动插槽
*   [脚本]删除 addon.d 中基于系统的根目录
*   [Script]添加适当的 addon.d-v2，以便在 A/B 设备的自定义 rom 上保留 Magisk
*   [Script]当设备使用 system_root_image 时启用 KEEPVERITY
*   [脚本]添加 hexpatch 删除新奥利奥内核中的三星 defex
*   [守护程序]支持镜像的非 ext4 文件系统(系统/供应商)
*   [MagiskSU]使 pts 套接字始终在 dev _ pts secontext 中运行，为所有终端仿真器根 shell 提供与 adb shells 相同的功能[MagiskHide]终止所有与目标具有相同 UID 的进程，以解决 OOS 胚胎优化问题
*   [MagiskInit]在初始化前移动所有 sepolicy 修补程序，以防止 Pixel 2 (XL)启动服务崩溃

## Magisk Manager v5.9.1 Changelog

*   没有更多的启动通知
*   支持在 A/B 设备上为 OTA 安装到非活动插槽的新机制
*   修复 Android P 上的恢复 Magisk 管理器设置
*   验证现有的文件校验和，以防止不必要的重新下载
*   更新 SNET 扩展以使用新的 Google API，修复“无效响应”错误
*   将指纹设置移动到 magisk 数据库，以防止设置被轻易删除
*   指纹设置现在受到指纹认证的保护，然后才能被更改
*   禁止将任何文件下载到/sdcard/MagiskManager

在所有这些特性之上，它还隐藏了应用程序子服务的根。一个重新打包的 MagiskHide 的根丢失也已经被修复，所以你也不应该遇到这些问题。这基本上是一个巨大的错误修复更新，使你的 Android 智能手机的整个过程变得平滑。这也是 A/B 支持发挥作用的地方，因为现在您实际上可以保留您的 Magisk 安装。在 GitHub [这里](https://github.com/topjohnwu/Magisk/blob/master/docs/tips.md#ota-installation-tips)可以找到完整的指南，这样你就可以在不失去 root 访问权限的情况下进行更新。

如果您已经更新了，但陷入了引导循环，只需刷新卸载程序并更新到版本 17.1。这些引导错误是由 16.0 版本的数据库不兼容问题引起的，所以卸载并重新安装 Magisk 是唯一的选择。其他值得注意的增加包括在 Magisk Manager 中重新引入 SafetyNet checker，以及一个新的模块模板，因为它与基于文件的加密(FBE)有冲突。当然，也有大量的错误修复和改进，但这些都是主要的变化。可以看看下面的帖子下载一下！

[t1 下载魔法 v 17.1T3](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)