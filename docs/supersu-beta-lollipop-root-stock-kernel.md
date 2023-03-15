# SuperSU BETA:将 Android Lollipop 放在股票内核上

> 原文：<https://www.xda-developers.com/supersu-beta-lollipop-root-stock-kernel/>

到目前为止，如果你想在 Android 5.0 上获得 root，你需要在你的设备上刷新一个修改过的内核，以绕过一些 SELinux 限制。XDA 资深公认开发者 [Chainfire](http://forum.xda-developers.com/member.php?u=631273) 最近发布了之前必需的 [CF-Auto-Root](http://www.xda-developers.com/android/chainfire-releases-cf-auto-roots-for-nexus-line/) 包，对内核 ramdisk 做了必要的修改，从 AOSP 上的 install-recovery.sh 脚本中删除了 SELinux 限制。然而，今天早上，Chainfire 给许多人带来了笑容，因为他[在 Twitter](https://twitter.com/ChainfireXDA/status/535253476021116928) 上宣布，未来将不再需要这样做。

直到今天，Chainfire 一直计划发布一个自动化的基于 ZIP 的补丁工具，从 TWRP 恢复中自动修补内核映像，直到他找到一个合适的方法来消除这种需要。

这一发现意味着 Android 5.0 用户不再需要运行修改后的内核来通过 SuperSU(或其他 root 解决方案)获得 root 访问权限。虽然在带有可解锁引导加载程序的 Nexus 设备上这不是一个大问题，但是对于许多引导加载程序锁定设备的用户来说，修改 ramdisk 的需求是值得关注的，因为这些设备没有解锁功能(是的，不幸的是它们确实存在)。他们祈祷的答案现在就在这里，我们可以对所需的改变给出一个独家的解释。至少目前(直到/除非谷歌对此进行修补)，有可能获得 root 访问权限，然后在一台普通 Android 5.0 设备上安装和使用 SuperSU，而无需对内核 ramdisk 进行任何调整。这样做的原因是需要 SuperSU 以 root 身份运行服务，以允许在受 SELinux 保护的设备上进行不受限制的 root 访问。

以前，SuperSU 会利用预装的 AOSP *flash_recovery* 服务(在 AOSP 用于在 OTA 安装后更新恢复)来启动 SuperSU 守护进程(它实际上为请求它的应用程序提供 root 权限)。随着 Lollipop 的发布，这个服务已经被添加到一个受限的 SELinux 上下文中，这意味着它不再能够完全访问系统。之前的内核修改试图从这个脚本中删除 SELinux 限制。

Chainfire 的 SuperSU 最新测试版通过使用核心的“Zygote”服务(负责启动所有 Java 服务，从而启动设备上安装的所有应用程序)解决了这一问题。由于 Zygote 是 Android L 上仅有的可用服务之一，它是在无限制的“init”SELinux 上下文中作为 root 启动的，这使得它成为 SuperSU 操作中使用的主要目标。启动后，Zygote 服务将其 SELinux“init”上下文转换为其最终(受限)的“Zygote”上下文。Chainfire 已经成功地修改了 Zygote 文件，以便在不受限制的“init”上下文中以 root 用户身份运行代码，从而将 SuperSU 带回 Android L，而无需修改内核。

这不是 Chainfire 第一次求助于 Zygote 来解决这些问题；早期的 2.23 测试版使用 Zygote 作为一种手段，可能规避一些其他 SELinux 问题(这些问题导致 root 应用程序在 Android L 上崩溃)。这使得一些(但不是全部)不起作用的应用程序能够运行——其余的需要开发者进行一些更新。不幸的是，当 5.0 AOSP 代码被查阅时，谷歌已经打破了接管 Zygote 服务的方法。鉴于他之前所有接管受精卵的尝试都失败了，这是一个充满希望的进步。

Chainfire 敏锐地指出，SuperSU 长期以来一直能够在运行的系统上修改 SELinux 策略(并警告 OEM 可以轻松地禁用这一功能，并真正阻止有意义和简单的根访问)，以及对 Zygote 的任何修改都必须小心谨慎，因为该服务是从各种不同的上下文中运行的，用于不同的任务，这增加了许多(令人讨厌的)微妙故障的可能性。这个新的 SuperSU beta 2.27 是一个供发烧友和其他技术人员玩的版本，可以发现哪些地方出了问题。手指交叉——没有意外的节目停止错误，这是一个可行的前进方向。

请注意——即使这个测试版成功了，Zygote 是获得 root 访问权限的首选途径，向前发展，整个过程只需一行代码就可以被谷歌破解，这将使打补丁的内核 ramdisks 成为 Android 上 root 访问权限的未来(从而排除了 bootloader 锁定设备的 root 访问权限)。事实上，作为一个提醒，由于过去几个月中一些相当大的 SELinux 变化，新的过程甚至可能无法在完全最新的 AOSP 版本上工作，这些变化没有包括在零售设备中，但毫无疑问会在未来的版本中出现。不过，看起来 root 迟早需要修改内核内存磁盘，但这个新的测试版可能会在我们必须朝着这个方向前进之前提供一个短暂的暂停执行。

查看[发布说明](https://plus.google.com/113517319477420052449/posts/K7n4e1q5SMD)以获得更多关于测试所涉及风险的信息，以及相关链接。开发人员也应该知道，Chainfire 目前正在努力编写[【如何使用 SU】指南](http://su.chainfire.eu/)(针对 Android 5.0 进行了全面更新)，应该会在未来几天内发布。

非常感谢 Chainfire 在这里所做的工作，以及在准备这篇文章时给予的帮助。]