# OnePlus 5T 现已推出官方 TWRP

> 原文：<https://www.xda-developers.com/official-twrp-oneplus-5t/>

在 OnePlus 5T 发布后不久，我们为社区提供了 TWRP 的[非官方版本。这个版本是通过将 OnePlus 5 的 TWRP 映像与 OnePlus 5T 的内核重新打包而成的，然而，这并不是一个完美的解决方案，因为并不是所有东西都保证可以工作。](https://www.xda-developers.com/unofficial-twrp-oneplus-5t-released/)

然而，这一次，由于 XDA 认可的开发人员 [simonsickle](https://forum.xda-developers.com/member.php?u=4973732) 、XDA 认可的高级开发人员 [Dees_Troy](https://forum.xda-developers.com/member.php?u=912474) 和 XDA 认可的高级开发人员 [bigbiff](https://forum.xda-developers.com/member.php?u=2638973) 的工作，TWRP 的正式版本已经从源代码构建并发布。我们被告知一切正常，这意味着您可以开始刷新[自定义内核](https://www.xda-developers.com/blu-spark-oneplus-5t/)和[rom](https://forum.xda-developers.com/oneplus-5t/development/rom-omnirom-8-x-t3713775)，但是如果启用了基于文件的加密，从备份中恢复数据分区将会导致启动问题(这只是 FBE 工作方式的一个副作用)。

对于一加设备，闪烁指示始终是相同的。首先，在开发者选项中启用 OEM 解锁。然后，重新启动引导程序，打开命令提示符或终端，并键入:

```
 fastboot oem unlock 
```

根据提示解锁您的引导加载程序，这将擦除内部存储。下载一加 5T 的[官方 TWRP。最后，在命令提示符窗口或终端中将目录更改为存储该文件的位置，然后键入:](https://dl.twrp.me/dumpling/)

```
 fastboot flash recovery twrp-3.2.0-0-dumpling.img 
```

当你启动恢复，你应该看到 TWRP 弹出。要获得更详细的指南，包括一步一步的指导以及如何根化你的设备的指导，你应该看看 XDA 公认的贡献者 Funk Wizard 的这篇文章。

请记住，如果您正在刷新一个[oxygen OS OTA](https://www.xda-developers.com/oxygenos-v4-7-4-update-oneplus-5t/)，那么 TWRP 将被库存恢复覆盖，除非您随后立即再次刷新 Magisk 或 TWRP。对于那些喜欢运行 OxygenOS 但拥有 root 访问权限的人来说，这是一个有用的技巧。

* * *

[**在我们的 OnePlus 5T 论坛**](https://forum.xda-developers.com/oneplus-5t/development/recovery-twrp-oneplus-5t-t3715834) 下载官方 TWRP