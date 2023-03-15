# EFIDroid:使用 UEFI 固件进行多重引导的第二阶段引导加载程序[XDA 聚焦]

> 原文：<https://www.xda-developers.com/efidroid-is-a-second-stage-bootloader/>

很长一段时间以来，双引导和多 ROM 实现一直是 Android 开发者的主要挑战。以前的解决方案通常需要大量的[设备专用开发](https://github.com/Tasssadar/multirom/wiki/Porting-MultiROM)和 rom 开发者的进一步支持。即使这样，对于普通的 ROM 用户来说，它们也往往比它们的价值更复杂。 [EFIDroid](http://forum.xda-developers.com/android/software-hacking/efidroid-t3447466) 寻求补救这一切。

EFIDroid 以前被称为 GRUB4Android，由 XDA 公认的开发者和贡献者 [m11kkaa](http://forum.xda-developers.com/member.php?u=3530648) 创建，作为一种有效地允许**几乎任何 ROM 被多重引导的手段，而无需修改**期望的 ROM 或当前恢复。这意味着没有内核补丁，没有 [kexec](http://forum.xda-developers.com/showthread.php?t=2104706) ，没有 ROM 不兼容问题，也没有让 ROM 用户或开发者头疼的问题。

* * *

### **什么是 EFIDroid？**

EFIDroid 是一个**二级引导加载程序**，旨在允许设备的原始引导加载程序代码自己处理硬件接口，从而简化将该应用程序移植到不同设备所需完成的工作。这是基于英特尔的 [EDK II](http://www.tianocore.org/edk2/) 项目，该项目有一个完善的代码库，并提供了大量的可扩展性。这个实现利用了高通的开源引导程序，**小内核(LK)** ，因此，支持**目前仅限于骁龙设备**。

安装非常简单，只需从根设备上的谷歌 Play 商店下载 [EFIDroidManager 应用程序](https://play.google.com/store/apps/details?id=org.efidroid.efidroidmanager)，前提是你的设备支持合并到项目的 [github 库](https://github.com/efidroid)中。如果您的设备受支持，该应用程序将下载相关代码，让您安装、卸载、重新安装和修复 EFIDroid，并允许您在多引导配置中管理您的 rom。一旦安装了 EFIDroid，rom 就可以安装在你选择的位置(通常是某个地方，比如*/data/media/0/multiboot/NAME*)。

目前，只有少数设备得到支持，包括 [Moto E(秃鹰)](http://forum.xda-developers.com/moto-e)、 [Moto G 4G(游隼)](https://forum.xda-developers.com/moto-g)、[诺基亚 X2](https://forum.xda-developers.com/nokia-x2) 、 [OnePlus One](http://forum.xda-developers.com/oneplus-one) 、Vega Iron 2 和 [Fairphone 2](http://forum.xda-developers.com/fairphone-2) 。然而，m11kkaa 正在**寻找开发者来帮助将 EFIDroid** 移植到其他设备上—[一些已经获得了“非官方支持”](https://github.com/efidroid/projectmanagement/wiki/Device-Maintainers)如果您能够让 EFIDroid 在另一个设备上工作，那么将它合并到应用程序中的过程只需要**向 EFIDroid git** 存储库发送一个 pull 请求。M11kkaa 还告诉我们，他未来计划扩展该应用程序，以潜在地支持引导插件和 UEFI 应用程序(尽管请记住，在这一点上这些只是计划)。

* * *

### **工作原理**

EFIDroid 利用 LK 作为抽象层与设备硬件进行交互。该应用程序使这些组件能够被 UEFI 的广泛功能充分利用——其中包括以

后面一点。

EFIDroid 利用 Linux 内核库将 Linux 内核编译成软件库。这使得 UEFI 能够使用文件系统驱动程序来读取和写入多个引导分区，并使其能够引导到多个 rom 或恢复环境。EFIDroid 还可以显示以前引导失败的错误消息。创作者甚至提到将来可能使用 Linux 内核库来增加触摸屏支持。

所有这些当然需要 root 访问权限和设备上的解锁引导程序**，但不需要定制内核**。

![](img/6c61ed5dce10bbad5dbc2cdd8bcf8386.png) ![](img/830fb3e24d26f6fdd3cd58e6ba5825e1.png)

*[图片来源:EFIDroid](http://efidroid.org)*

* * *

### **不止是多重引导**

UEFI 引导加载程序的实现为 Android 设备带来了许多可能性。各种插件，包括 Memtest86 之类的诊断，打开命令行，甚至游戏，在 UEFI 环境中都是可能的。虽然需要支持来实现这些可能性，但 EFIDroid 目前仍为兼容设备提供一些关键功能。无论是简单地用作可能缺少恢复选项的设备的替代引导加载程序，还是用作管理和故障排除多个 rom 或恢复环境的工具，该工具都提供了上述所有功能，并通过用户友好和直接的 UI *来引导*。

如需进一步讨论，请前往[论坛主题](http://forum.xda-developers.com/android/software-hacking/efidroid-t3447466)或通过以下链接关注该项目！

Github 上的[**EFI droid**](https://github.com/efidroid)

[**EFIDroid 官网**](http://efidroid.org)

[**EFIDroid 的 Slack 社区**](http://join-efidroid.rhcloud.com)

* * *

你以前试过 EFIDroid 吗？您希望看到对您的设备的支持吗？请在下面的评论中告诉我们！