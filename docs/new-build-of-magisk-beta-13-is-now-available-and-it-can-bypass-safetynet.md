# Magisk Beta 13 的新版本现已推出，它可以绕过 SafetyNet

> 原文：<https://www.xda-developers.com/new-build-of-magisk-beta-13-is-now-available-and-it-can-bypass-safetynet/>

最近围绕 Magisk 有很多新的。本月初[谷歌从 Play Store](https://www.xda-developers.com/magisk-manager-removed-from-play-store-developer-responds-on-the-future-of-magisk/) 移除了 Magisk Manager，原因是该应用的设置方式。XDA 认可开发者和贡献者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 然后就在上周开始测试版本 13 的测试版[这是一个完整的重写，所以它可能是一个统一的二进制](https://www.xda-developers.com/magisk-v13-0-beta-available-to-test-brings-unified-binary-manual-injection-and-more/)。本周，我们注意到谷歌已经更新了安全网，因此 Magisk 无法绕过新的检查。

有些人可以通过禁用 Magisk 模块并将 Magisk 管理器设置为仅核心模式来解决这个问题，所以这在当时是一个很好的解决方法。 [topjohnwu 花时间写了一些关于篡改检测的文章](https://www.xda-developers.com/magisk-developer-assures-next-magisk-beta-will-pass-safetynet-again/)以及 Magisk 和 SafetyNet 的未来。目前，他们能够绕过谷歌实施的新变化。可悲的是，谷歌已经在 Pixel 设备上做了大量工作，以强化这些类型的检查。

昨天下午晚些时候，我们看到 topjohnwu 发布了一个关于 Magisk beta 版本 13 的新版本。当刷新时，它与 Magisk Manager 版本 5.0.2 捆绑在一起，开发人员谈到了与这些新版本的一些兼容性问题。因此，Magisk v13 及更高版本将与低于 5.0.0 的任何 Magisk Manager 版本不兼容。我们在我们的论坛上看到来自那些尝试过的人的关于强制关闭的报告。

topjohnwu 在 Magisk Beta 线程中简要介绍了这一更新，并表示可能有一种方法可以隐藏 Magisk Manager，使其不被其他搜索它的应用程序发现(他们在篡改检测帖子中谈到了这一点)。完整的更新日志会在下面，但是你可以在这里下载新的测试版更新。

### 神奇 v13 测试版变更日志

*   [BETA]v 13.0(96 F8 EFC)-[修复]使用 busybox 作为旧 Android 版本的后备
*   [BETA]v 13.0(a90e8b 6)-[magis hide]更新隐藏策略，启用最新 SafetyNet 更新上的模块将通过 CTS- [Fix]调整的闪存脚本以仅使用/system 组件
*   [BETA]v 13.0(b3da 28 e)-[修复]修复 Magic Mount 中一个小但相当关键的 bug，使用多个模块现在应该可以了-[修复]不要为 libsqlite.so 编译 shell.c
*   [BETA]v 13.0(1e 87780)-[修复]修复自定义恢复中无法链接可执行文件的问题-[修复]修复由于“e2fsck”工具在每个设备上的输出不同而导致的守护程序崩溃-[修复]修复导致添加文件到/system 和/vendor root 崩溃的魔法挂载错误-[修复]修复某些极端组合中的另一个潜在的魔法挂载错误
*   [BETA]v 13.0(0b4baad)-[修复]修复/data encrypted 设备上的守护进程崩溃- [MagiskSU]添加名称空间模式选项支持
*   [BETA] v13.0(0980cb6)- [General]将 MagiskSU、magiskhide、resetprop、magiskpolicy 合并为一个二进制- [General]添加 Android O 支持(在 DP2 上测试)- [General]动态链接 libselinux.so、libsqlite.so 从系统中大大减少二进制大小- [General]解锁所有实际的块设备以获得读写支持，而不仅仅是 emmc(只是发现并非所有设备都使用 emmc lol)- [General]通过二进制管理 ext4 映像- [MagiskSU]不会为每个请求派生新的进程 防止编写不良的 su 应用程序对性能造成影响- [MagiskSU]多个设置从 prop 检测移到数据库- [resetprop]更新到最新的 AOSP 上游，支持从 5.0 到 Android O 的 props-[reset prop]重命名所有函数以防止从外部 libc 调用函数- [magiskpolicy]更新了来自官方 SELinux repo 的 libsepol- [magiskpolicy]添加了 xperm 补丁支持(为了使 Android O 正常工作)-[magiskpolicy]更新了 Android O 的规则，以及 Liveboot 支持-[magiskphide]删除伪许可模式 改为直接隐藏许可状态- [MagiskHide]删除不可靠的列表文件监视器，更改为守护程序请求模式- [Magic Mount]放弃基于 shell 脚本的挂载，使用正确的 C 程序来解析和挂载文件。 速度显著提高

[**在我们的论坛**](https://forum.xda-developers.com/apps/magisk/beta-magisk-v13-0-0980cb6-t3618589/post72686834#post72686834) 查看 Magisk v13 测试版