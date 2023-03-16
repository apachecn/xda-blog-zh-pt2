# Magisk v16.6 增加了对三星 Galaxy S9 和 Project Treble GSIs 的支持

> 原文：<https://www.xda-developers.com/magisk-v16-6-samsung-galaxy-s9-project-treble-gsi-root-loss/>

如果你曾经关注过你的 Android 设备，你可能在某个时候听说过 Magisk。这是一个无系统的 root 开源解决方案，最著名的是它通过 SafetyNet 的能力——允许你在 root 状态下使用 Google Pay 和 Pokemon Go 等应用程序。它是由 XDA 知名开发商 topjohnwu 开发的，他最近在台湾完成了强制性的军事训练。在那段时间里，我们仍然看到一些更新，其中[改进了 MagiskHide 并添加了 Android P 支持](https://www.xda-developers.com/magisk-16-4-magiskhide-android-p/)和[绕过了“认证设备”问题](https://www.xda-developers.com/magisk-16-3-fixes-pokemon-go-uncertified-devices/)，但现在我们得到了更好的东西。Magisk v16.6 (Beta)现在与[Project Treble Generic System Images](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/)(GSIs)和三星 Galaxy S9 更加兼容，神秘的“root loss”问题已经修复。

更新是朝着正确方向迈出的一大步，因为闪烁项目高音 GSI 或在 GSI 之间切换经常需要擦除/数据。但是，由于 Magisk 依赖于/data 中的文件才能工作，因此您需要重新安装它才能工作。在最近的更新中，如果没有检测到管理器，将安装嵌入 magiskinit 的新存根管理器 APK。然后，存根下载完整的应用程序，然后重新构建根环境。因此，重新安装将由脚本处理，而您不必采取一堆额外的步骤！

接下来，用户报告了一个神秘的问题，root 访问权限会突然丢失。topjohnwu 发现了一个边缘案例，并实施了一个修复来防止根丢失问题的发生。此外，他还实现了修复来处理守护进程崩溃导致的根丢失。

如果你想阅读变更日志的其余部分，那么看看下面。

### 神奇 v16.6 (Beta 版)变更日志

*   Magisk Manager 将在应用程序内升级时保留随机包名称。magisk 将不再偏好包名 com.topjohnwu.magisk 而不是重新打包的(隐藏的)Magisk 管理器，以防止恶意软件针对这个特定的包名。如果您安装了重新打包的 Magisk 管理器，com.topjohnwu.magisk 将被强制拒绝 root 访问。可以在设置中使用**恢复 Magisk Manager** ，或者卸载重新打包的 Magisk Manager 解锁 com.topjohnwu.magisk。
*   ext4 映像中计算空闲空间的逻辑被新的非常精确的方法所取代，希望不会再发生由映像导致的模块安装失败。所有使用 template 1500 的模块将自动受益于 Magisk v16.6+上新的可用空间计算方法，无需额外更改。
*   正式增加对三星 Galaxy S9/三星 Galaxy S9+的支持。
*   Magisk v16.4 切换到仅 32 位二进制文件，导致一些应用程序出现问题。添加了一个新的包装器脚本来消除所有可能的问题。
*   项目 Treble GSIs(例如 phh AOSP)有时需要替换 ramdisk 中的 adbd，并用于与 Magisk 冲突。现在这个问题已经解决，亚行将在使用三重 GSIs 项目时充分发挥作用。
*   LineageOS 向 A/B 分区设备引入了 addon.d-v2，addon.d 脚本被更新为 A/B 感知的(我这边没有测试)

这是管理器应用程序的变更日志。现在可以在应用程序中查看 changelog，方法是转到侧边栏的“关于”部分。

### Magisk Manager v5.8.0 Changelog

*   在重新打包的 Magisk 管理器中升级时保持隐藏
*   新功能:支持在检测到错误时重建正确的 Magisk 环境(例如，在工厂重置后)
*   新的卸载方法:下载卸载程序，完全删除 Magisk + Magisk 管理器，然后重新启动。
*   隐藏的应用程序现在显示在 MagiskHide 片段列表的顶部
*   大量的 bug 修复和改进

如果你有兴趣安装它，那么[看看官方线程](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)。关于发布的更多细节，请看他的[官方公告帖](https://forum.xda-developers.com/showpost.php?p=77014053&postcount=43)。我们很想知道这个版本如何在您的设备上运行。如果你经常刷新 GSIs，让我们知道新的更新对你来说怎么样。此外，如果你有一个可解锁的三星 Galaxy S9 引导程序，也请让我们知道最新的更新是否能在你的设备上正常工作。