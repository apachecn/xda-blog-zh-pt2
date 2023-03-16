# 内核辅助超级用户(KernelSU)——安全网的最后边界和一个重要的开发工具

> 原文：<https://www.xda-developers.com/kernel-assisted-superuser-kernelsu/>

根对我们 XDA 来说非常特殊。它允许用户控制他们的设备，并添加一些并非总是可用的功能，如通话录音、主题和高级电池监控。这些年来已经有了一些根实现，最流行的可能是 SuperSU。不过最近，随着安全网的推出和对 root 设备的限制越来越多，Magisk 已经成为首选的 root 实现，因为它的 Magisk Hide 功能允许用户有效地隐藏他们拥有网飞和谷歌支付等应用的 root 的事实。然而，Magisk Hide 的实现和功能在很大程度上是谷歌修补它和 Magisk 围绕该修补程序工作的猫鼠游戏。

Magisk 运行在所谓的用户空间。这也是你手机上大多数程序运行的地方，无论是游戏、音乐播放器还是健身追踪器。它是设备操作系统面向用户的“空间”。用户空间也是 Magisk Hide 大部分战斗发生的地方。不幸的是，随着时间的推移，谷歌修补了越来越多的 Magisk Hide 的方法，剩下的隐藏空间越来越少。将来，Magisk 可能会完全失去隐藏 root 的能力。

为这种可能性做准备，XDA 认可开发人员 [zx2c4](https://forum.xda-developers.com/member.php?u=5434776) (杰森·唐恩菲尔德)，他因[在 WireGuard](https://www.xda-developers.com/wireguard-vpn-project-support-android-roms/) 上的工作和[一加引导程序漏洞](https://www.xda-developers.com/oneplus-6-bootloader-protection-exploit-physical-access/)的发现而在 XDA 出名，他创造了[内核辅助超级用户](https://git.zx2c4.com/kernel-assisted-superuser/about/) (KernelSU)。

与 Magisk 不同，KernelSU 将获得 root 的能力嵌入到内核本身。在这里，它劫持系统调用来欺骗 shell 以为`/system/bin/su`存在于设备上，而实际上它并不存在。然后，它执行使用`su`运行的命令，就像它们是普通命令一样，但是具有 root 权限。SELinux 无法阻止这个过程——如果内核愿意，它甚至可以禁用 SELinux——对用户空间隐藏根状态的能力几乎是无限的，因此对 SafetyNet 也是如此。

然而，KernelSU 还远未完成。目前，还没有合适的访问控制机制(想想 Magisk Manager)。正因为如此，KernelSU 目前对内核开发者的帮助最大，而不是用户。构建内核的过程需要开发人员不断地重新构建和加载引导映像，以测试和修复错误和功能，而拥有 root 用户使这变得容易得多。但是，对于 Magisk 或 SuperSU 这样的 root 选项，每次构建后都必须修补引导映像，这样 root 才能正常工作，这会极大地影响开发过程。另一方面，KernelSU 意味着在构建时集成，不需要构建后打补丁。为了使 KernelSU 集成对开发人员来说更容易，可以使用一个简单的一行命令:

```
 curl -LsS "https://git.zx2c4.com/kernel-assisted-superuser/plain/fetch-and-patch.sh" | bash - 
```

一旦执行完毕，KernelSU 就可以作为正常构建过程的一部分构建到内核中。这意味着开发人员可以轻松地构建和测试他们的内核，而不必担心添加 root。

虽然 KernelSU 还处于早期，还需要做更多的工作来使它具有完整的特性，但这是一个有趣的项目。我们采访了[Magisk](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)-创建者，XDA 认可的开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) ，关于 KernelSU，他也觉得很有趣，他说，由于 KernelSU 在内核级运行，如果添加 Magisk Hide 的功能将更加可靠，并且它将是一个“实现起来很有趣的事情”

如果你是一个对 KernelSU 感兴趣的内核或 ROM 开发者，请查看 [XDA 线程](https://forum.xda-developers.com/android/software/root-backdoor-android-kernel-development-t3870559)和[项目的主页](https://git.zx2c4.com/kernel-assisted-superuser/about/)以了解更多信息。