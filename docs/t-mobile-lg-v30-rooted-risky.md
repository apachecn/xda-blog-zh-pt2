# T-Mobile LG V30 已经扎根，但程序有风险

> 原文：<https://www.xda-developers.com/t-mobile-lg-v30-rooted-risky/>

LG 移动每年都损失数百万美元，他们锁定某些运营商设备的方式对发烧友群体没有帮助。在美国，无线运营商出售的老款 LG 设备像往常一样被锁定，但 T-Mobile 的变种有容易解锁的引导加载器。这种情况随着 T-Mobile LG G5 的出现而停止。虽然您可以解锁引导加载程序并引导到快速引导模式，但没有任何命令可以让您安装 TWRP 作为根和自定义 ROM。一名开发者社区成员努力保持这种可能性，他们的最新工作向我们展示了如何获得 T-Mobile LG V30 的 root 访问权限。

T-Mobile LG 智能手机的粉丝可能会认出 XDA 公认的开发商 [runningnak3d](https://forum.xda-developers.com/member.php?u=3167089) ，因为他们能够在今年早些时候通过 T-Mobile LG G6 绕过[这一限制。开发者本月再次为 T-Mobile LG V30 (H932)开发了一种方法，该方法将引导您在手机上使用 LAF，然后允许您在设备上安装 TWRP，然后通过向您展示如何安装 Magisk 来结束，这样您就可以完全 root 访问 LG V30 的 T-Mobile 版本。](https://forum.xda-developers.com/tmobile-g6/how-to/root-h872-to-including-11g-t3775518)

正如我们在标题中提到的，这个过程是有风险的，如果你不严格按照描述的步骤去做，最终可能会很难把你的智能手机变成砖头。如果你在除 H932 之外的 LG V30 的任何型号上尝试这种方法，那么你最终会导致你的智能手机启动。据我们所知，这种在非 H932 LG V30 版本上的特定引导循环是永久的，因为你将会清除下载模式，并且没有办法恢复。尽管如此，这个过程对 H932 来说也是有风险的，但幸运的是 runningnak3d 已经足够好地将它分成多个逐步指南。这从将您的固件降级到 v10d 开始，以刷新 Magisk 结束，这样您就有了 root 访问权限。

除了 runningnak3d 所做的工作之外，他们还对 Lekensteyn 在 LG G2 和 LG G3 上所做的工作给予了肯定。XDA 认可的开发者[standover x](https://forum.xda-developers.com/member.php?u=5545101)因添加功能、测试疯狂的想法、 [FWUL](https://www.xda-developers.com/forget-windows-use-linux-is-a-usb-bootable-distro-for-your-android-recovery-needs-xda-spotlight/) 等等而受到感谢。tuxuser 帮助 runningnak3d 提高了他们的 Python 知识，最后，感谢 XDA 成员 [smitel](https://forum.xda-developers.com/member.php?u=6556954) 对 LG UP 的原始逆向工程。

同样，在遵循下面链接的说明时要小心。请务必从头到尾通读整个教程，然后再开始做任何事情，因为今年早些时候有许多类似方法的 LG G6 设备。runningnak3d 向我们保证，他们“已经升级到奥利奥，然后降级到 10d，并测试了 4 次”，所以他们知道这个过程是可行的，但“让 H933 laf 进入你的手机是危险的”，所以请注意你在做什么。

[**在我们的 LG V30 论坛**](https://forum.xda-developers.com/lg-v30/how-to/root-h932-lafploit-1-5-to-v20a-t3842550) 查看这个有风险的 root 方法