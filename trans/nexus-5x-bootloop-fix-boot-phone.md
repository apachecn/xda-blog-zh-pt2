# Nexus 5X Bootloop 修复终于让你启动手机

> 原文：<https://www.xda-developers.com/nexus-5x-bootloop-fix-boot-phone/>

你的 LG/谷歌 Nexus 5X 停止启动了吗，或者更确切地说，陷入了无休止的启动序列？这就是我们所说的“引导循环”,它可能因为各种原因而发生。大多数引导回路可以通过刷新固件或工厂重置来修复，但在硬件引导回路的情况下，除了对手机进行 RMA 之外，通常你什么也做不了。如果你的谷歌 Nexus 5X 一直拒绝启动，并且你尝试过的任何方法都无法修复它，你并不孤单。Nexus 5X bootloop 问题在社区中臭名昭著，但直到最近才找到修复方法。

## Nexus 5X Bootloop 修复-上下文

在过去的几年里，LG 的智能手机因其 bootloop 问题获得了一些声誉。一个似乎始于 LG G4 的问题随着公司发布的每一款新设备变得越来越普遍。我们最近谈到了一种[解决华为 Nexus 6P](https://www.xda-developers.com/nexus-6p-bootloop-fix/)boot loop 问题的方法，现在有一种适用于 [Nexus 5X](https://forum.xda-developers.com/nexus-5x/) 的解决方案，该方案源自我们之前写的指南。

对这些修复的普遍共识似乎表明，骁龙 808/810 芯片组被高通匆忙淘汰，已经退化到部分损坏的地步。骁龙 810 的[发热问题并不是什么新鲜事，但当谈到是什么导致了引导错误时，808 似乎也有类似的问题。LG 最初声明](https://www.xda-developers.com/opinion-the-810-held-back-a-generation-with-deliberate-apologism-damage-control/)[LG G4 引导系统的问题确实与硬件有关](https://www.xda-developers.com/xda-external-link/lg-admits-g4-bootloop-problem-is-a-hardware-fault-will-repair-affected-devices/)，但从未详细说明情况。

一些人认为这是由于他们使用的焊料，在设备的寿命期间，它最终会因为加热和冷却次数过多而破裂。不管这是不是真的，**我们仍然不确定问题背后的原因是什么，但这次对 Nexus 5X 引导循环的修复似乎确实解决了这个问题。因此，今天我们为您提供了一个指南，将带您了解如何修复 Nexus 5X bootloop 问题。虽然在这篇文章底部的链接论坛帖子的标题确实说它未经测试，但社区中的许多人都报告了这种方法的成功。**

不过，与往常一样，您的收获可能会因这种变通办法而异。

* * *

## 辅导的

**要求**:

*   在引导循环开始之前可解锁的引导加载程序，因为你不能引导到 Android，也不能在之后启用解锁引导加载程序所需的设置。如果你能够简单地启动手机，那么进入开发者选项，勾选“启用 OEM 解锁”就可以了。

1.  下载最新的 [ADB 和 Fastboot 二进制文件](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/)，并将它们解压缩到计算机上一个易于访问的文件夹中。
2.  下载并安装[谷歌的 USB 驱动](https://developer.android.com/studio/run/win-usb.html)(针对运行 Windows 的用户)。
3.  下载 [N2G47Z_4Cores.img](https://www.dropbox.com/s/tm7qt98r6d7q2a6/N2G47Z_4Cores.img?dl=0) 文件，并将其保存在 ADB 和 Fastboot 二进制文件所在的目录下。
    *   可选:如果您想在您的固定 Nexus 5X 上使用 TWRP 恢复，这需要您使用 TWRP 的修改版本。所以下载 [TWRP3_1_1_5X.img](https://www.dropbox.com/s/levla3p5npe24pw/TWRP3_1_1_5X.img?dl=0) 并保存在 ADB 和 Fastboot 二进制文件所在的文件夹中。
    *   可选 2:如果你想加速你的固定 Nexus 5X，你可以刷新 XDA 认可的开发者 [flar2](https://forum.xda-developers.com/member.php?u=4684315) 的 Elemental X 内核的修改版本。将 [EX4_10_5X.zip](https://www.dropbox.com/s/172ey8346e5du6l/EX4_10_5X.zip?dl=0) 文件下载到您的 Nexus 5X 上，这样它就会存储在默认的下载目录中。

4.  用 USB 线将 Nexus 5X 连接到电脑。
5.  继续，在保存 ADB 和 Fastboot 二进制文件的同一个目录中启动命令提示符或终端。Windows 用户，您可以通过按住 shift 并右键单击，然后选择“在此打开命令提示符”来完成此操作 Windows 10 用户将看到一个 PowerShell 选项，取代了命令提示符选项。
6.  将 Nexus 5X 引导至快速引导模式(有些人也称之为引导装载模式)。
7.  在命令提示符下执行以下命令:`fastboot devices`
8.  如果您看到您的设备的序列号，您就可以继续了。如果没有，那么由于某种原因，USB 驱动程序没有完全安装。
9.  如果您的引导加载程序尚未解锁，但您之前已经在开发者选项中启用了 OEM 解锁，您现在可以通过输入:`fastboot flashing unlock`来解锁引导加载程序。然后，按照屏幕上的说明解锁引导加载程序。请注意，这将清除您手机上的所有数据。
10.  现在在命令提示符下输入以下命令来替换当前的引导映像:`fastboot flash boot N2G47Z_4Cores.img`
    *   可选:如果你想刷新修改后的 TWRP，然后输入以下命令:`fastboot flash recovery TWRP3_1_1_5X.img`

11.  通过输入`fastboot reboot` 重启你的手机
12.  几分钟后(可能需要一段时间)，你应该会看到你的手机启动动画，最终锁屏。恭喜你，你救了你的手机！
13.  可选:如果你想提高性能，并且按照步骤安装了修改版的 TWRP，将修改后的 Elemental X 内核复制到你手机的存储器中，启动进入 TWRP，刷新自定义内核。你甚至可以选择在设置过程中对**小集群**进行超频，从而让你的手机获得更高的性能。

* * *

### 说明

就像我们在 Nexus 6P 指南中向您展示的如何修复其 bootloop 问题一样，原因与 SoC 的大集群 CPU 核心有关。根据 XDA 成员 [XCnathan32](https://forum.xda-developers.com/member.php?u=5288606) 在测试该进程期间的日志，该问题是由 VLL 无法获得 A57 内核的锁引起的。到目前为止，我们还不能 100%确定是什么导致了这个问题，但我们的解决方法实际上是禁用这些损坏的 A57 内核，这样我们就可以完全绕过这个问题。

一个更优雅的解决方案可能会在未来出现，但现在我们感谢开发人员社区提出一个允许人们的智能手机再次启动的解决方案。如果有人已经处理这个问题有一段时间了，至少他们可以有一个音乐播放器，dash cam 等功能设备。那些还没有经历过这个问题的人至少在他们第一次经历 bootloop 时会有一个可用的解决方案。

如上所述，我们已经看到社区中的许多人(在我们的官方 XDA 线程中)报告说，这个 Nexus 5X bootloop 解决方案确实有效。然而，我们也至少有一个人说它不适合他们。Nexus 5X bootloop 问题可能有多种原因，因此本指南可能不适合所有人。如果你的 Nexus 5X 目前正在引导，尝试一下肯定没有坏处，因为如果你想恢复所有这些修改过的文件，你可以随时闪现谷歌提供的股票图像。

* * *

[**在我们的 Nexus 5X 论坛**](https://forum.xda-developers.com/nexus-5x/general/untested-nexus-5x-bootloop-death-fix-t3641199) 查看原帖