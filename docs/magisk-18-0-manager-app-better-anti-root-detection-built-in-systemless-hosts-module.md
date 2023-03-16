# Magisk 18.0 发布了新的管理器应用程序，以实现更好的反 root 检测

> 原文：<https://www.xda-developers.com/magisk-18-0-manager-app-better-anti-root-detection-built-in-systemless-hosts-module/>

# Magisk 18.0 发布了新的管理器应用程序，以实现更好的防根检测和内置的无系统主机模块

Magisk 已经更新到 v18.0 稳定版，带来了一个更新的 Magisk Manager 应用程序和其他几项改进。继续阅读，了解更多信息！

Magisk 仍然是确定多个设备的根并进行/系统修改的首选方法，同时仍然保持对依赖 SafetyNet 检测根访问和系统修改的应用程序的访问。

Magisk 现在已经[更新到版本 18.0，作为稳定版](https://github.com/topjohnwu/magisk_files/blob/2ef99925eb85fc961100aea88e70dec499343047/notes.md)。这个版本对 Magisk Hide 进行了改进，进程监视器现在匹配组件名而不是进程名。这反过来允许 Magisk Hide 将隐藏列表上的应用程序派生的所有进程作为目标。Magisk 还在这个新版本中为所有 Android 7.0+设备上的 [procfs 安全漏洞](https://www.xda-developers.com/procfs-leak-lg-oneplus-huawei-xiaomi-asus/)打补丁，现在它已经转移到基于 C++的新代码库，而不是旧的基于 C 的代码库。Magisk Manager 也将更新到 6.1.0 版，以完全支持新的 Magisk 版本。

v18 版本的[完整变更日志](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445/post78368595#post78368595)如下:

### 神奇 v18.0

*   [常规]将所有代码库迁移到 C++
*   [常规]本机修改数据库，而不是通过 Magisk 管理器
*   [General]不推荐使用路径/sbin/。核心，请开始使用/sbin/。马吉斯克
*   [常规]引导脚本从 <magisk_img>/移出。核心/ <stage>。<stage>开发署。d</stage></stage></magisk_img>
*   [常规]删除本机无系统主机(Magisk Manager 更新了内置的无系统主机模块)
*   [常规]允许模块 post-fs-data.sh 脚本禁用/删除模块
*   [magis hide]使用组件名而不是进程名作为目标
*   [magis hide]在 SDK 24+上添加 procfs 保护(牛轧糖)
*   [magis hide]删除文件夹/。备份以防止检测
*   [magis Hide]隐藏列表现在存储在数据库中，而不是图像中的原始文本文件
*   [magis hide]将“- status”选项添加到 CLI
*   [magis hide]停止卸载与非定制相关的挂载点
*   [MagiskSU]在广播中添加 FLAG_INCLUDE_STOPPED_PACKAGES 以强制唤醒 Magisk Manager
*   [MagiskSU]修正了一个导致 SIGWINCH 不能被正确检测的错误
*   [MagiskPolicy]支持新的 av 规则:type_change，type_member
*   [MagiskPolicy]在修补 sepolicy 后删除所有 AUDITDENY 规则，以记录用于调试的所有拒绝
*   [MagiskBoot]正确支持引导头中的 extra_cmdline
*   [MagiskBoot]尝试修复损坏的 v1 启动映像头
*   [MagiskBoot]添加新的 CPIO 命令:" exists "

### Magisk Manager v6.1.0

*   引入新的下载方法:不再使用错误的系统下载管理器
*   引入许多新的通知以获得更好的用户体验
*   添加对 Magisk v18.0 的支持
*   隐藏(重新打包)后将应用程序名称更改为“管理器”，以防止应用程序名称检测
*   添加内置无系统主机模块(在设置中访问)
*   隐藏(重新打包)和恢复 Magisk Manager 后，自动启动新安装的应用程序
*   修复了导致模块中的不完整模块.道具具有不正确的用户界面的错误

Magisk 和 Magisk Manager 的新更新可以从 [Magisk XDA 线程](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)下载。