# Kindle Fire 的 Firekit LiveUSB 修复套件

> 原文：<https://www.xda-developers.com/firekit-liveusb-repair-kit-for-kindle-fire/>

有时候，Windows 就是做不到。许多开发人员在大部分工作中使用 Linux 发行版，虽然比大多数 Mac 用户要好，但 Windows 有能力引起巨大的麻烦。

对于一些亚马逊 Kindle Fire 用户来说尤其如此，他们报告说在 Windows 上使用 ADB 和 Fastboot 驱动程序有问题。

XDA 资深会员 pokey9000 来拯救我们了，他设计了一种方法来绕过这个问题，让 Kindle Fire 用户恢复到他们头疼的自由方式。他解释了它到底是什么:

> Firekit 将 Kindle Fire recovery 的所有命令行工具与 Ubuntu LiveUSB 结合在一起。你所需要的只是一个 u 盘和一台可以启动的电脑。所有文件都保存在记忆棒上，因此您电脑上的内容不会改变。

虽然这需要一些关于创建 Ubuntu LiveUSB 的知识，但是一旦你通过了，这是一个相对简单的过程。在你创建了你的 Ubuntu LiveUSB 并把文件放在那里之后，你可以使用命令行做任何事情，从恢复你的 Fire 到修复混乱的分区表。以下是命令的完整列表(将在命令行中输入):

> 安装 fff 和 twrp，而在股票 Android。使用 fbmode 重新启动。使用它在 6.2.1 stock OS 上安装 FFF/TWRP。
> 
> install_fff_twrp:在快速启动时安装 fff 和 twrp。很好，如果你被困在快速启动，你想 FFF/TWRP。
> 
> fix_parts 在快速启动时将分区表恢复到库存。如果你正在快速启动，而你的分区表被搞砸了，就这么做。
> 
> normal_boot:设置 bootmode 来引导 android，并在快速启动时重新启动。如果你被 Kindle Fire 的 logo 卡住了，试试这个。
> 
> usb_boot_twrp:不安装的 usb 启动 twrp。如果你尝试开机时 Kindle 黑屏，请启动 TWRP。需要 USB 启动模式技巧。
> 
> usb_install_fff_twrp: USB 启动 fff，安装 FFF 和 twrp。安装/恢复引导加载程序和恢复，如果他们被打破。需要 USB 启动模式技巧。
> 
> USB _ fix _ parts _ and _ install _ fff _ twrp:USB 启动 fff，恢复分区表到库存，安装 FFF 和 twrp。如果你把分区表搞砸了，而你的屏幕又不能打开，那就把一切都修好。需要 USB 启动模式技巧。

如果你想尝试这种强大的替代方式来通过 Windows 工作，你可以查看一下[原始线程](http://forum.xda-developers.com/showthread.php?t=1430038)以获得更多的说明、使用指南和下载链接。pokey9000 似乎也计划对此提供更多支持，因为他确实在第一篇帖子的底部列出了他打算修复和改进的事情的待办事项。