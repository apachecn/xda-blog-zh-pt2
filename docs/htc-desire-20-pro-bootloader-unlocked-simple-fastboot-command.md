# HTC Desire 20 Pro 可以通过一个简单的快速启动命令解锁引导加载程序

> 原文：<https://www.xda-developers.com/htc-desire-20-pro-bootloader-unlocked-simple-fastboot-command/>

# HTC Desire 20 Pro 可以通过一个简单的快速启动命令解锁引导加载程序

无需生成任何设备特定的令牌-您可以使用常规的 Fastboot 命令解锁 HTC Desire 20 Pro 的引导加载程序。请继续阅读！

HTC 最近在本国推出了两款中档智能手机，试图在智能手机市场卷土重来。HTC Desire 20 Pro 就是其中之一，它采用了略旧的[高通骁龙 665 SoC](https://www.xda-developers.com/qualcomm-snapdragon-665-snapdragon-730g/) ，带有 48MP 主传感器的四摄像头阵列，以及支持快速充电 3.0 的 5,000 mAh 大电池。该公司还保留了 3.5 毫米耳机插孔，而在 128GB 内置存储旁边还有一个额外的 microSD 卡插槽。人们也可以解锁 HTC Desire 20 Pro 的引导加载程序，这要归功于 OEM 长期以来允许大多数型号的引导加载程序解锁的传统。好消息是，HTC 显然不再强制用户在解锁前获得解锁令牌，至少在 Desire 20 Pro 的情况下是这样。

**[HTC Desire 20 Pro XDA 论坛](https://forum.xda-developers.com/htc-desire-20-pro)**

对于那些不熟悉 HTC 的 bootloader 解锁过程的人来说，该公司曾经要求你在他们的开发者门户网站上创建一个帐户，即首先是[HTCdev.com](https://www.htcdev.com/)，然后[为你的型号生成一个设备特定的 ID 令牌](https://www.htcdev.com/bootloader/preview_unlock_process)。与谷歌的 Pixel 系列不同，用户不能简单地使用标准的 Fastboot 命令来解锁 HTC 设备的引导加载程序。然而，XDA 初级成员 [otack](https://forum.xda-developers.com/member.php?u=2748311) 已经[发现](https://forum.xda-developers.com/htc-desire-20-pro/how-to/guide-how-to-unlock-bootloader-t4129991/)在 HTC Desire 20 Pro 上不再需要`get_identifier_token`命令来执行解锁过程。您只需在下载模式下将设备连接到 PC，并执行以下命令:

```
 fastboot flashing unlock 
```

如果正确安装了必要的驱动程序，此时您应该会在手机屏幕上看到提示。使用音量摇杆选择“解锁引导程序”,然后按下电源按钮确认选择。

当然，解锁引导加载程序将导致您的设备上的数据被完全擦除，所以请确保您事先备份了所有重要的数据。您可能仍然需要一个额外的命令，比如`fastboot flashing unlock_critical`，才能获得对低级固件分区的写访问，尽管通过通用的快速启动命令进行 [S-OFF](https://www.xda-developers.com/tag/s-off/) 访问是极不可能的。