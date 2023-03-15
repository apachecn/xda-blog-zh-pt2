# Nexus 6P Bootloop 修复已被发现-以下是它的工作原理

> 原文：<https://www.xda-developers.com/nexus-6p-bootloop-fix/>

你被死神的 Nexus 6P Bootloop 影响过吗？如果你是少数几个把 Nexus 6P 藏在某个抽屉里的不幸者之一，你会很高兴地知道，已经找到了一个修复方法，可以让你再次完全启动你的设备。

这是通过禁用该设备的 Snapdragon 810 SoC 的大集群来实现的，然后允许该设备最终到达其锁屏。为了复活你的 Nexus 6P，[你需要刷新 XDA 会员](https://forum.xda-developers.com/nexus-6p/general/guide-fix-nexus-6p-bootloop-death-blod-t3640279) [XCnathan32](https://forum.xda-developers.com/member.php?u=5288606) 提供的修改文件(在 XDA 资深会员 [rchtk](https://forum.xda-developers.com/member.php?u=4533695) 的帮助下[才能让你的 ROM 和恢复再次工作。](https://forum.xda-developers.com/nexus-6p/general/boot-images-bootloop-t3633723)

* * *

### 语境

在 2016 年底，我们看到了来自多名用户的大量报告，声称他们的 Nexus 6P 设备莫名其妙地进入随机引导，这个问题似乎与大约同一时间困扰手机的[提前关机](https://www.xda-developers.com/some-nexus-6ps-are-shutting-down-at-early-battery-percentages/)无关。这是不同的，虽然减少电池寿命肯定是不好的，但靴带基本上把智能手机变成了镇纸。

面临这一问题的用户很快陷入绝望，因为看不到补救措施。无论擦除多少数据或重新刷新工厂映像似乎都无法解决问题，这表明该问题与硬件有关，可能是 SoC 中的问题。这并不是谷歌的设备第一次进入毁灭性的砖块或引导回路状态:Nexus 7 在收到其最初的棒棒糖 OTA 后出现了广泛的砖块，LG 制造的 [Nexus 5X](http://forum.xda-developers.com/nexus-5x) 也遭受了与许多具有硬件相关引导回路的 LG 手机相同的命运。

Nexus 6P bootloop 问题已经得到了谷歌代表的确认，他建议用户应该联系他们的购买地，以获得保修或维修选项。用户试图从谷歌那里获得更好的解决方案，通过在 [AOSP 问题追踪器](https://issuetracker.google.com/issues/37130791)中开始对话来寻求帮助，然后我们开始听说[因早期关机和 bootloop 问题对谷歌和华为提起的潜在诉讼](https://www.xda-developers.com/google-facing-potential-lawsuit-over-nexus-6p-early-shutdown-and-bootloop-issues/)。一场集体诉讼最终被提起，然后被修改，原告遍及十多个州。虽然谷歌和华为显然已经意识到这个问题，但除了更换保修期内的 Nexus 6p bootloop 设备，我们还没有看到他们解决这个问题。

* * *

## 死亡的 Nexus 6P Bootloop，绕过

XDA 成员 [XCnathan32](https://forum.xda-developers.com/member.php?u=5288606) 发布了一份指南和修改文件，据报道修复了 Nexus 6P bootloop 问题。这些指令非常简单，它们只涉及刷新修改后的 boot.img 映像和修改后的 TWRP 版本，这样你就可以在以后刷新其他文件。这些版本已被更改为仅使用 Snapdragon 810 SoC 的小集群，有效地禁用了似乎阻止设备启动的 A57 性能核心。虽然我们不会猜测这是为什么，但这确实意味着你会遇到明显的延迟，尽管 A53 小内核也更省电。这是一个很大的权衡，但肯定比没有好。

许多用户报告说，在开篇文章中提供的修改后的图像正在工作，并允许设备启动，我自己在 Nexus 6P bootloop 设备上尝试了一下，以证实这一点。我用这种方法让我弟弟的 Nexus 6P 复活了，即使谷歌的出厂映像不起作用。如果您希望恢复设备，可以遵循以下说明:

## 辅导的

1.  下载最新的 [ADB 和 Fastboot 二进制文件](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)，并将它们解压到计算机上一个容易访问的文件夹中。
2.  如果你运行的是 Windows，下载并安装[谷歌 USB 驱动](https://developer.android.com/studio/run/win-usb.html)。
3.  下载 [N2G48B_4Cores.img](https://www.dropbox.com/s/65newjmcul32ylw/N2G48B_4Cores.img?dl=0) 并保存到保存 ADB 和 Fastboot 二进制文件的同一个目录。
    *   可选:如果您想在您的固定 Nexus 6P 上使用 TWRP 恢复，您将需要使用修改后的版本。下载 [twrp3_1_1_4Cores.img](https://www.dropbox.com/s/bf9ug30v6uji1gt/twrp3_1_1_4Cores.img?dl=0) 并保存到保存 ADB 和 Fastboot 二进制文件的目录下。
    *   可选:如果你想加速你的固定 Nexus 6P，你可以刷新 XDA 认可的开发者 [flar2](https://forum.xda-developers.com/member.php?u=4684315) 的 Elemental X 内核的修改版本。下载 [EX4_1_1_4Cores.zip](https://www.dropbox.com/s/e3l8fjks15hf9zg/EX4_1_1_4Cores.zip?dl=0) 并保存到你的下载目录。
4.  把你的手机接到电脑上。
5.  在保存 ADB 和 Fastboot 二进制文件的同一目录中打开命令提示符或终端。在 Windows 上，您可以通过按住 shift 键并右键单击，然后选择“在此打开命令提示符”来轻松实现这一点
6.  输入以下命令:`fastboot devices`
7.  如果您看到您的设备的序列号，您就可以继续了。否则，您需要尝试重新安装驱动程序。
8.  **重要提示**:您手机的引导程序必须解锁，才能刷新这些修改过的图像。如果您的引导程序已经解锁，请跳过以下 2 个步骤。
9.  通过输入以下命令启动解锁手机引导程序的过程:`fastboot flashing unlock`
10.  使用音量和电源键，确认您要解锁引导加载程序。这将会清除手机内存中的所有内容。但是，要么这样，要么买一块几百美元的砖头。你的选择！
11.  现在输入以下命令来刷新修改后的引导映像:`fastboot flash boot N2G48B_4Cores.img`
    *   可选:如果你想闪现 TWRP，那么输入:`fastboot flash recovery twrp3_1_1_4Cores.img`
12.  通过输入`fastboot reboot` 重启你的手机
13.  几分钟后(可能需要一段时间)，你应该会看到你的手机启动动画，最终锁屏。恭喜你，你救了你的手机！
14.  可选:如果你想提高性能，并且刷新了 TWRP，把修改后的 Elemental X 内核复制到你手机的存储器中，启动进入 TWRP，刷新自定义内核。您可以选择在设置期间超频这个小集群，以便从您的手机中挤出更多的性能。

XCnathan32 确实注意到 root 在 TWRP 是通过闪现 SuperSU 来工作的。他还提供了一些提高设备性能的建议，比如禁用动画或将 CPU 调控器改为主动调控器。虽然他在普通 ROM 上测试了修改后的 boot.img，但 PureNexus 等其他 ROM 应该也能工作。你只需要确保你运行的内核被修改成使用四个小内核。

这是一个令人印象深刻的发展，Nexus 6P 用户现在可以恢复他们优秀的设备，即使这种解决方案有所妥协。鉴于许多用户无法在保修期内更换手机，他们现在可以好好利用手机，而不是让它死死地躺在角落或抽屉里。

我们建议你也完整地阅读下面的帖子，并在发帖前搜索你可能有的任何问题。感谢 [XCnathan32](https://forum.xda-developers.com/member.php?u=5288606) ，如果可以的话，[帮助他调试](https://forum.xda-developers.com/nexus-6p/help/dev-help-debugging-ramoops-bootlooping-t3640826)引导循环 Nexus 6P，因为他正在寻找让大内核也工作的方法。

* * *

在我们的 Nexus 6P 论坛中检查引导加载程序修复！