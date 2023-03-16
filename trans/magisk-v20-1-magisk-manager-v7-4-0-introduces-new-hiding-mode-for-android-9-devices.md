# Magisk Manager v7.4.0 为 Android 9+设备带来了新的隐藏模式

> 原文：<https://www.xda-developers.com/magisk-v20-1-magisk-manager-v7-4-0-introduces-new-hiding-mode-for-android-9-devices/>

# Magisk v20.1 和 Magisk Manager v7.4.0 为 Android 9+设备引入了新的隐藏模式

Magisk v20.1 和 Magisk Manager v7.4.0 为运行 Android 9 和更高版本的设备提供了更新的隐藏模式以及错误修复。

Magisk 对于 Android 发烧友来说是一个不可思议的工具。这是一个由 XDA 公认的开发者 *[topjohnwu](https://forum.xda-developers.com/member.php?u=4470081)* 创建的无系统界面，可用于不仅仅是为你的设备生根发芽。该界面帮助用户修改系统设置，而无需实际更改系统文件。除了允许安装广泛的模块，Magisk 非常受欢迎，因为它能够绕过谷歌的安全网，防止游戏，OTT 和银行应用程序等在根设备上运行。上个月， [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 推出了完全兼容 Android 10 的 [Magisk V20.0，包括只支持 A 分区方案的设备。现在，他们发布了 v20.1 和 Magisk Manager 7.4，其中包含一个错误修复日志和一个新的隐藏模式，适用于运行 Android 9 Pie 和更高版本的设备。](https://www.xda-developers.com/magisk-v20-stable-release-android-10-support/)

Magisk Manager v7.4.0 新增的隐藏模式部分通过"*高度模糊的存根 APK* "确保相关包不被检测到运行管理器所需的资源将被下载到存根应用程序的内部文件中，并在您需要使用完整的管理器应用程序时加载。您也可以在隐藏应用程序时更改其名称。

开发者指出，由于这种隐藏模式需要“*一种特殊的方式来与应用程序*进行通信，因此它可能无法在某些自定义 Android 皮肤或覆盖的情况下工作。因此，更新后的版本有一个新的功能，检查新的隐藏模式的兼容性。

此次更新还修复了之前版本的一些错误，以下是完整的更新日志:

**神奇的 v20.1**

*   [MagiskSU]支持组件名称不可知的通信(用于存根 APK)
*   [MagiskBoot]在启动映像头中设置正确的 header_size(修复 Samsung 设备上的 vbmeta 错误)
*   [magis hide]多次扫描受精卵
*   [MagiskInit]支持不带/sbin/recovery 二进制文件的恢复映像。这将修复某些 A/B 设备在刷新 Magisk 后无法启动恢复的问题
*   [常规]移动帐户以防止守护程序被终止
*   [常规]确保"- remove-modules "将在删除后执行 uninstall.sh

**Magisk Manager v7.4.0**

*   在 Android 9.0+上隐藏带有存根 apk 的 Magisk 管理器
*   隐藏 Magisk 管理器时允许自定义应用程序名称
*   生成随机密钥来签署隐藏的 Magisk 管理器，以防止签名检测
*   修复指纹 UI 无限循环

要使用新的隐藏模式，你必须更新 Magisk 和管理器应用程序。如果你已经隐藏了管理器，从你的应用抽屉中点击一个名为“取消隐藏 Magisk 管理器”的应用，更新应用，然后重启智能手机。

* * *

**来源 1: [XDA 论坛线程](https://forum.xda-developers.com/showpost.php?p=68966755&postcount=2) /来源 2: [GitHub](https://github.com/topjohnwu/magisk_files/blob/6f94236b1407bd0c162647db75dfa2ac956163ca/notes.md)**