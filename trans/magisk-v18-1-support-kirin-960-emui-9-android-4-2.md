# Magisk v18.1 发布，支持麒麟 960、EMUI 9、Android 4.2 等

> 原文：<https://www.xda-developers.com/magisk-v18-1-support-kirin-960-emui-9-android-4-2/>

XDA 公认的开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 的 [Magisk](https://www.xda-developers.com/tag/magisk/) 最初是一个无系统的 root 方法，多年来已经发展成为一个比普通 root 更加多样化和强大的工具。但即使在今天，如果您需要 root，为您的设备推荐的 root 方法很可能会提到为 root 安装 Magisk。

[Magisk 现在已经更新到 v18.1](https://forum.xda-developers.com/showpost.php?p=78829088&postcount=49) ，带来了对华为 EMUI 9 和麒麟 960 的支持，同时还将支持一直扩展到 Android 4.2(2012 年发布，只是为了刷新你的记忆)。

## 神奇 v18.1 变更日志

*   [常规]支持 EMUI 9.0
*   [常规]支持麒麟 960 设备
*   [常规]支持低至 Android 4.2
*   [常规]主要代码库的底层现代化

即使华为已经停止提供官方的 bootloader 解锁服务，但是有付费服务可以解锁 bootloader。这种情况类似于以前的 HTC 设备，必须通过非官方的付费服务解锁 bootloader，不同的是华为设备确实卖得很好。在 v18.1 中，Magisk 现在支持 EMUI 9 和麒麟 960。但是，由于华为对分区进行了更改，因此采用了特殊的解决方法来提供支持。您可以在本说明页的[上找到更多详细信息和说明。](https://topjohnwu.github.io/Magisk/install.html)

Magisk 现在也支持 Android 版本，一直到 Android 4.2 Jellybean。Kitkat 4.4 和更高版本的设备将启用所有功能，而 Android 4.4 和 Android 4.2 之间的设备可以利用 Magisk 作为根解决方案，因为 MagiskHide 和 resetprop 功能在 Jellybean 上是不可能的，而 Magic Mount/modules 暂时被禁用。

Magisk Manager 也已更新到 7.0.0 版，其变更日志如下。

## Magisk Manager v7.0.0 Changelog

*   重大 UI 重新设计！
*   原生渲染 Markdown(不再有错误的 WebView！)
*   支持低至 Android 4.1(原生 Magisk 仅支持 Android 4.2)
*   显著提高 Magisk 日志显示性能
*   修复 A/B 设备的 OTA 后脚本
*   验证和签名启动映像时减少内存使用
*   不再支持低于 v18.0 的 Magisk

顺便提一下，一些用户报告 Magisk Manager v7 无法直接将 Magisk 从 v18.0 升级到 v18.1。如果您遇到这个问题，您应该在更新前尝试取消隐藏 Magisk Manager。我们还想强调备份的重要性(因为我们大多数人经常认为 Magisk 的稳定性是理所当然的)，所以在尝试更新之前一定要做好充分的备份。

[**从 XDA 论坛**下载 Magisk](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)