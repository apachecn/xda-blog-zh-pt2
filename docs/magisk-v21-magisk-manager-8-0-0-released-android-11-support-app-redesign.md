# Magisk v21 和 Magisk Manager 8.0.0 发布，支持 Android 11、应用程序重新设计等

> 原文：<https://www.xda-developers.com/magisk-v21-magisk-manager-8-0-0-released-android-11-support-app-redesign/>

# Magisk v21 和 Magisk Manager 8.0.0 发布，支持 Android 11、应用程序重新设计等

XDA 资深公认开发人员 topjohnwu 现在发布了 Magisk v21 和 Magisk Manager v8.0.0，支持 Android 11，重新设计了应用程序，等等。

由 XDA 资深公认开发人员 *[topjohnwu](https://forum.xda-developers.com/member.php?u=4470081)* 开发的 Magisk 无疑是 Android 设备最受欢迎的根解决方案。有了 Magisk，在 TWRP 这样的定制恢复中刷新一个. zip 文件并安装 Magisk Manager 应用程序，就可以轻松地为您的 Android 设备找到根。但是由于 Magisk 必须进行修改以适应无系统根，所以它需要[升级以兼容每一个新的 Android 版本](https://www.xda-developers.com/latest-magisk-canary-release-adds-support-for-android-11/)。现在 Android 11 已经开始在一些设备上推出， *topjohnwu* 发布了 Magisk v21 和 Magisk Manager v8.0.0，支持 Android 11，重新设计了应用程序，等等。

**[Magisk XDA 论坛](https://forum.xda-developers.com/apps/magisk)**

Magisk 的最新版本旨在与所有运行 Android 11 的设备配合使用。然而，根据 *topjohnwu 的* Magisk v21 公告推特上的回复，[一些用户正面临最新版本的问题](https://twitter.com/Tathaga74078643/status/1312357300883996673)。Magisk v21 也[目前似乎无法与几款联发科驱动的设备](https://twitter.com/topjohnwu/status/1312519081581400065)兼容。如果你有兴趣在你的设备上试用这个版本，你可以从下面的链接下载 Magisk 和 Magisk Manager 的最新版本，并按照这篇文章中的说明来引导你的设备。如果你遇到任何问题，你可以在[项目的 GitHub 库](https://github.com/topjohnwu/Magisk/issues)上提交一份错误报告。查看以下部分，获取最新 Magisk 和 Magisk Manager 版本的完整变更日志。

### 变更日志

神奇的 v21:

*   【通用】支持 Android 11🎉
*   [常规]添加安全模式检测。当设备启动到安全模式时，禁用所有模块。
*   [常规]将文件系统后数据模式超时从 10 秒增加到 40 秒
*   [MagiskInit]从头开始重写 2SI 支持
*   不存在/sbin 文件夹时的[MagiskInit]支持(Android 11)
*   [MagiskInit]将 fstab 从设备树转储到 rootfs，并强制 Init 将其用于 2SI 设备
*   [MagiskInit]为 2SI 剥离 AVB，因为它可能会导致引导环路
*   [模块]从头开始重写模块安装逻辑
*   【MagiskSU】对于 Android 8.0+，使用了全新的策略设置。这减少了 Android 沙盒中的妥协，为 root 用户提供了更多的策略隔离和更好的安全性。
*   [MagiskSU]隔离的挂载命名空间现在将首先从父进程继承，然后将其自身与外界隔离
*   [MagiskSU]使用 Magisk 管理器更新通信协议，以便与强化的 SELinux 设置一起工作
*   [MagiskPolicy]优化匹配所有规则。这将显著减小策略二进制文件的大小，节省内存并提高一般内核性能。
*   [MagiskPolicy]支持声明新的类型和属性
*   [MagiskPolicy]使政策声明更贴近股票*。te 格式。有关更多详细信息，请查看更新的文档或 magiskpolicy - help。
*   [MagiskBoot]支持压缩的额外 blobs
*   [MagiskBoot]用零填充启动映像包到原始大小
*   [magis hide]操作其他供应商属性

Magisk Manager v8.0.0:

*   100%全 app 重写！将在下面重点介绍功能变化。
*   在主屏幕中添加详细的设备信息以帮助用户安装
*   支持 Magisk v21.0 通信协议
*   支持修补现代三星 AP.tar

**t1【下载魔法 v21】T2**

**[Download Magisk Manager v8.0.0](https://github.com/topjohnwu/Magisk/releases/tag/manager-v8.0.0)**