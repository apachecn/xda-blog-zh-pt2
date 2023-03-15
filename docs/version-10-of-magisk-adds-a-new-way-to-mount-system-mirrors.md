# Magisk 的第 10 版增加了一种装载系统镜像的新方法

> 原文：<https://www.xda-developers.com/version-10-of-magisk-adds-a-new-way-to-mount-system-mirrors/>

# Magisk 的第 10 版增加了一种装载系统镜像的新方法

广受欢迎的 Magisk mod 版本 10 增加了一个通用的无系统接口，允许用户将文件绑定到他们选择的任何目录。

在过去的中，我们已经在 XDA [这里](https://www.xda-developers.com/magisk-updated-to-v7-now-completely-open-source/)[多次讨论过 Magisk](https://www.xda-developers.com/magisk-receives-an-update-to-v9-prepares-itself-for-multirom-support/) ，自从它被首次引入以来，看到这种改进的发展真是太棒了。Magisk 的目标是克服 Android 平台无系统 mods 的局限性。通过创建一个通用的无系统接口，这使得开发者和用户能够以不干扰系统分区的方式应用软件模块。

Magisk 的第 9 版上个月刚刚发布，它带来了许多新的变化，比如移除了后 fs 模块的接口，并为多 ROM 支持做好了准备。尽管 MultiROM 支持仍在开发中，你可以[观看一个概念验证视频](https://www.youtube.com/watch?v=uN6pgG0IJz0)来了解该功能如何工作。

Magisk 的第 10 版提供了一种新的挂载系统(供应商)镜像的方法，一种处理/vendor 分区的通用方法，以及将任何文件添加到任何分区的能力。魔法挂载现在将使用符号链接来镜像目录(如果可能的话)，这减少了添加文件的绑定挂载。它还将检查 init 名称空间和 zygote 名称空间，以防止 Magic Mount 中断。Magisk Hide 现在会发送 SIGSTOP 来立即暂停一个目标进程，这样如果卸载太晚，就会导致崩溃。隐藏现在也可以在任何条件下工作，甚至在添加库和/system root 时。

昨天，我们看到了 10.2 版本的快速更新，也增加了 Magisk 的一些新变化。更改日志提到从白名单中删除 apps/priv-app 作为崩溃的修复，它还附带了对 phh 二进制文件过期的修复。最后，它修复了在 Magisk Manager 中升级时导致 root 访问权限消失的错误。

您可以找到下面列出的这两个更新的完整更改日志:

* * *

**v10.2**

*   从白名单中删除应用程序，应该可以修复所有的崩溃
*   [phh]修复二进制过时问题
*   [脚本]修复在 Magisk 管理器中升级时根消失的问题

**v10**

*   [Magic Mount]使用一种新的方式来装载系统(供应商)镜像
*   [魔装]使用通用方式处理/厂商，处理两者分开的分区与否
*   [魔法挂载]现在正式支持在任何地方添加任何东西(包括/系统根和/厂商根)
*   [Magic Mount]如果可能，使用符号链接进行镜像，减少添加文件的绑定装载
*   [Magisk Hide]检查 init 命名空间和 zygote 命名空间，以防止魔法座架损坏(也称为根丢失)
*   [Magisk Hide]发送 SIGSTOP 以尽快暂停目标进程，以防止在卸载太迟的情况下崩溃
*   隐藏可以在任何条件下工作，包括添加库和/系统根目录等。
*   [phh]如果没有检测到正确的根，则对设备进行根操作
*   [phh]将/sbin 移动到/sbin_orig 并链接回来，修复 Samsung no-suid 问题
*   [脚本]改进 SuperSU 集成，现在使用 sukernel 来修补 ramdisk，支持 SuperSU 内置于 ramdisk 恢复
*   [template]添加 PROPFILE 选项以加载 system.prop

* * *

[**来源:XDA 论坛**](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)