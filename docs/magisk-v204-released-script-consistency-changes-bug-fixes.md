# Magisk v20.4 发布，包含脚本一致性更改和错误修复

> 原文：<https://www.xda-developers.com/magisk-v204-released-script-consistency-changes-bug-fixes/>

# Magisk v20.4 发布，包含脚本一致性更改和错误修复

Magisk (v20.4)的最新稳定更新已经发布。从这个版本开始，默认情况下不再启用 MagiskHide。继续阅读，了解更多信息！

Magisk 在这一点上基本上已经成为 Android 上 root 访问的代名词。最受欢迎的定制 ROM 发行版之一 LineageOS 甚至[放弃了对自己的 addonsu 二进制文件](https://www.xda-developers.com/lineageos-dropping-superuser-addonsu-implementation-favor-magisk-manager/)的支持，转而支持这个由 XDA 知名开发商 *[topjohnwu](https://forum.xda-developers.com/member.php?u=4470081)* 开发的无系统解决方案。开发人员最近谈到了*magis hide*组件的[潜在缺点](https://www.xda-developers.com/magisk-no-longer-hide-bootloader-unlock-status/)，源于谷歌安全网认证 API 的一些变化。虽然[谷歌可能需要一段时间](https://twitter.com/topjohnwu/status/1238514375150850048)才能完全实施新规则，但 *topjohnwu* 现在已经发布了 Magisk 的另一个稳定版本，默认情况下 *MagiskHide* 被禁用。标记为 v20.4 的最新版本只专注于核心组件，因为 Magisk Manager 的[重新设计的 UI](https://www.xda-developers.com/magisk-manager-redesigned-ui-latest-canary-update/)“*还没有完全准备好迎接黄金时间*”。

发布在 GitHub 上的发布说明非常强调 BusyBox 独立模式以提高脚本一致性，这主要是针对开发者和 Magisk 模块维护者的。从这个版本开始，Magisk 强制每个脚本使用内部的 BusyBox 二进制，这是由 XDA 公认的开发者 [*osm0sis*](https://forum.xda-developers.com/member.php?u=4544860) 增强的。然而，用户仍然可以选择在 BusyBox 之外调用命令，但是他们需要使用完整的路径。

这是 Magisk v20.4 的官方变更日志:

*   [MagiskInit]修复仅限 A 的 2SI 设备中潜在的引导环路
*   [MagiskInit]正确支持 Tegra 分区命名
*   【常规】动态加载 libsqlite.so，这样就不需要在 Android 10+上使用包装器脚本了
*   [常规]在某些设备上使用回退方法检测 API 级别
*   [常规]解决方法 x86 内核 readlinkat 系统调用中可能存在的错误
*   [BusyBox]启用 SELinux 特性。添加 chcon/runcon 等。、和“-Z”选项
*   [BusyBox]引入独立模式。发行说明中的更多详细信息
*   [magis hide]默认情况下禁用 magis hide
*   [magis hide]添加更多潜在的可检测系统属性
*   [magis hide]添加小米设备 bootloop 在跨区域 rom 上启用 magis hide 时的变通方法
*   [MagiskBoot]支持修补特殊的 Motorolla DTB 格式
*   [MagiskPolicy]支持“genfscon”策略规则
*   [脚本]支持基于 NAND 的启动映像(/dev/block 中的字符节点)
*   [脚本]更好的 addon . d(v1 和 v2)支持
*   [脚本]支持 Android 10+的血统恢复

**[从 GitHub](https://github.com/topjohnwu/Magisk/releases/tag/v20.4) 下载 Magisk v20.4】**

谷歌可能会严厉打击 Magisk 向应用程序隐藏引导程序解锁状态的能力，但这并没有锁定其他潜力。从[实现真正的双引导](https://www.xda-developers.com/unofficial-twrp-enables-true-dual-boot-oneplus-7-pro-5g/)到[破解 iPhone](https://www.xda-developers.com/jailbreak-apple-iphone-using-checkra1n-rooted-android-phone/) ，Magisk 仍然被改装社区积极使用。

* * *

**来源:[GitHub](https://github.com/topjohnwu/magisk_files/blob/598fee44ab7528205b7088716d1197dd8e38532d/notes.md)**