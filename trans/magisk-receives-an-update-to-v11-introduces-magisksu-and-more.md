# Magisk 收到了 v11 的更新，介绍了 MagiskSU 等

> 原文：<https://www.xda-developers.com/magisk-receives-an-update-to-v11-introduces-magisksu-and-more/>

XDA 公认的开发者和贡献者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 最近一直在努力工作，刚刚推出了 Magisk Android mod 的重大更新。这里最大的新特性是增加了 MagiskSU，因为这将 Magisk 变成了自己的根解决方案。这个新特性的代码是基于 phh 更新 CM 超级用户的方法，但是据说其重要性足以成为它自己的解决方案。这里的目标是实现 SuperSU 标准，开发者认为功能应该与*几乎等同。*

现在唯一担心的是兼容性，这将在未来的后续更新中解决。对于那些仍然想坚持

[Chainfire's](https://forum.xda-developers.com/member.php?u=631273)

根解决方案，Magisk 11 仍将与 SuperSU 一起工作(并已通过 SuperSU v2.79-SR3 测试)。为了配合新的 MagiskSU 根解决方案，topjohnwu 说他们已经重新分解了 Magisk 的 sepolicy-inject 工具。在 Chainfire 文档的帮助下，Magisk 现在应该遵循与 SuperSU 的 supolicy 工具相同的语法。

为了增加 Magisk 与定制 rom 的兼容性，并为社区提供额外的选项，Magisk v11 提供了 topjohnwu 所说的伪 SELinux Enforce 模式。这将是设置菜单中的一个选项，它将 SELinux 设置为许可，同时使状态显示为强制。尽管有些人认为将此设置为 permissive 是一种不好的做法，但一些自定义 rom 要求这样设置。所以现在用户可以选择将 SELinux 设置为强制，或者假装它设置为强制。

回到 Magisk 的第 4 版，topjohnwu 删除了使用通用引导脚本的能力，因为他们希望人们使用每个模块的脚本。这个特性现在已经恢复，脚本应该放在/magisk/中。core/post-fs-data.d 和/magisk/。对于那些感兴趣的人，这里是 Magisk 版本 11 的完整变更日志。。。

*   [魔法坐骑]支持替换符号链接。符号链接不能作为绑定装载的目标，因此它们被视为新文件
*   [魔法挂载]修正了文件/文件夹名包含空格的问题
*   [BusyBox]更新到 1.26.2 版。应该可以修复 FlashFire 的黑屏问题
*   [resetprop]支持读取属性值中包含空格的属性文件
*   [MagiskSU]使通信适应 Magisk 管理器；剥离未使用的数据传输
*   [MagiskSU]实现超级用户访问选项(Disable，APP only，ADB Only，APP & ADB) phh 超级用户应用程序有此选项，但该功能不在 SU 二进制文件中实现
*   [MagiskSU]修复了 su -c“命令”(使用 root 运行命令)的所有问题。该功能应该只允许一个选项，但显然 adb shell su -c“命令”不能以这种方式工作
*   许多根应用程序不遵守规则。su 二进制文件现在会将-c 之后的所有内容都视为命令的一部分。
*   [MagiskSU]移除了 TiBack 的传统上下文攻击，它目前所做的是减慢调用速度
*   [MagiskSU]调用 SU 后保留当前工作目录以前 phh 超级用户在获得 root shell 后会将路径更改为/data/data。现在，它将保留在您
*   苏
*   [MagiskSU]守护进程现在也可以在 u:r:su:s0 上下文中运行
*   [MagiskSU]删除了一个不必要的分支，减少了运行过程并加快了调用速度
*   [MagiskSU]将-cn 选项添加到二进制文件中不确定这是否仍然相关，也不确定是否正确实现，但是嘿，它在这里
*   [sepolicy-inject]完全重写命令行选项，现在几乎匹配 supolicy 语法
*   [sepolicy-inject]支持几乎每个操作的所有匹配模式(使伪强制成为可能)
*   [sepolicy-inject]修复了一个古老的错误，即分配的内存不会重置
*   [uninstaller]现在作为一个独立的脚本运行，可以在启动时执行完全支持恢复，无需/数据访问，使用 Magisk Manager 卸载 Magisk
*   【附加】Busybox、MagiskHide、hosts 设置现在可以即时应用；不需要重启
*   [添加]添加 post-fs-data.d 和 service.d
*   [附加]添加禁用 Magisk 的选项(MagiskSU 仍将启动)

[**来源:XDA**](https://forum.xda-developers.com/showpost.php?p=70897029&postcount=12)