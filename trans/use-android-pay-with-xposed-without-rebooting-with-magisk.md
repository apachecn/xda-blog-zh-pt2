# 使用 Android Pay with Xposed 无需重启 Magisk

> 原文：<https://www.xda-developers.com/use-android-pay-with-xposed-without-rebooting-with-magisk/>

在许多第一世界的问题中，有一个问题引起了许多 XDA 居民的共鸣。一方面，Android 着眼于未来，推出了类似 Android Pay 的解决方案——允许你用手机在物理终端上支付，而不需要你的钱包。这很方便，也很有效(如果你在受支持的地区)。

另一方面，像 Xposed 这样的修改和允许提升应用程序的 SU 权限的能力允许大量的定制。对我们来说，Android 是让你的手机成为我们自己的，而像这样的修改才是真正可能的。因此，Android Pay 和 Xposed 很难共存。我们知道为什么，但这并不能阻止人们去尝试。

以前，如果你想使用 Android Pay，你必须保持完全库存和无根。然后出现了 SuperSU 和 Xposed 的无系统版本，如果用户禁用 Xposed 并重启，他们就可以使用 Android Pay。里程确实因手机、安卓版本和更多变量而异。但这无疑是从零兼容性的前几个阶段的进步。

今天的新闻更进了一步。公认的贡献者[topjohnwu](http://forum.xda-developers.com/member.php?u=4470081),[非官方无系统曝光改装](http://www.xda-developers.com/unoffical-systemless-xposed-is-now-available-otas-and-pay-unaffected/)的开发者，创造了[Magisk](http://forum.xda-developers.com/android/software/mod-magisk-v1-universal-systemless-t3432382)——通用无系统接口。正如 dev 所说:

> Magisk 是一个无系统改变系统的魔术面具。

Magisk 本身有很大的潜力。它挖掘了进行无系统修改的潜力，同时消除了与之相关的复杂性。无系统的 mods 很复杂，很难维护，并且在一般使用中有局限性和不可行性。Magisk 消除了这些困难，并为每个人，包括开发者和用户，创建了一个通用的界面来使用和开发无系统 mods。

Magisk 有很多超越 Android Pay 兼容性的功能。其中之一是 Magic Mount，它不仅允许你替换/system 中的文件，甚至允许你添加新的文件和目录。这本身就为所有现有的暴露的 mod 打开了无系统工作的可能性。如果这不符合您的意愿，Magisk 还承诺在引导期间为脚本运行提供多个入口点。Magisk Manager 允许您管理您的 root 挂载状态，这将我们带到第一个问题的解决方案:使用 Android Pay 和 root 和 Xposed！

要安装 Magisk，开发人员建议从 100%的库存系统和引导映像状态开始。然后你需要闪 Magisk 就大功告成了。如果你不是 100%的股票系统和启动图像，开发人员已经制定了一些指示，你可以按照成功安装。

想了解更多的特性，想了解更多关于 mod 本身的信息，请前往[论坛主题](http://forum.xda-developers.com/android/software/mod-magisk-v1-universal-systemless-t3432382)。

### 那么，如何在 root 和 Xposed 下使用 Android Pay 呢？

首先，你需要安装 Magisk。然后，您需要确保您使用的是兼容 Magisk 的 phh 开源超级用户(可以从 Magisk 线程下载)。对于 Xposed，您需要 Magisk 兼容的 systemless Xposed(在 Magisk 线程中链接)。然后，您需要打开随 Magisk 自动安装的 Magisk 管理器，并单击 unmount root。你瞧，Android Pay 现在应该可以工作了，你甚至不需要重启！这是因为这个选项实际上是暂时**完全解除你的设备的 root**，所以任何需要 root 的东西都没有 root，结果是使用安全网检查的应用程序也无法检测到 root。

要恢复 root，只需重新安装 root，就可以了。简单易行，无需重启。

如果您选择的超级用户权限管理工具是 Chainfire 的 SuperSU，则不能保证 100%的兼容性。开发人员已经创建了一个方便的图表，它会告诉您如果您偏离了推荐的操作过程，可以做什么和不可以做什么。

> 如果你因为想让 Android Pay 与 Xposed 一起工作而被迫使用 phh 的 root，但你也想使用不兼容的应用程序(需要 secontext live patching)，这里我在“Magisk Manager”中提供了一个开关，让你将 SELinux 设置为许可。这将提供最大的兼容性(这将允许任何事情发生)。请注意，我不建议让 SELinux 永久切换到许可模式。仅在必要时使用！

Magisk 还有很多内容超出了本文的范围。开发者在他的[论坛线程](http://forum.xda-developers.com/android/software/mod-magisk-v1-universal-systemless-t3432382)中已经涵盖了很多信息，建议大家去看看。开发人员也要求用户不要在 SuperSU 与 Magisk 的兼容性请求上出现问题，因为开发人员会在适当的时候自己处理。

现在，是时候回到#BackToStock，然后进行无系统的修改。如果你试用过 Magisk，请在下面的评论中告诉我们你的体验！请在下面的评论中确认 Android Pay 是否可以在你的设备上使用！**闪了！**