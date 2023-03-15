# 修复一加 8 系列、7T Pro 等产品的指纹注册问题

> 原文：<https://www.xda-developers.com/fix-fingerprint-enrollment-issues-broken-persist-partition-oneplus-8-pro/>

Android 驱动设备上的主存储模块[被分成几个分区](https://www.xda-developers.com/how-a-b-partitions-and-seamless-updates-affect-custom-development-on-xda/)。对于售后开发，Android modding 社区主要处理一些分区，如“/system”、“recovery”、“cache”等。另一方面，原始设备制造商通常使用不太知名的分区来[存储有趣的参数](https://www.xda-developers.com/how-to-discover-hidden-fastboot-commands/)，比如[引导加载程序的锁定/解锁状态](https://www.xda-developers.com/unlock-bootloader-zte-phones/)。一个这样的分区是“/persist”，它通常包含内部传感器的校准数据，在某些情况下，还包含像 Wi-Fi 芯片的 MAC 地址这样的唯一标识符。

由于它的独特性，不能简单地通过恢复通用转储来修复损坏的持久分区。以类似的方式，即使在完全固件刷新之后，也几乎不可能正确地重写“持久”的内容。这就是为什么一加 8，一加 8 专业版和一加 7T 专业版迈凯轮版的一些用户很难修复与损坏的持久分区相关的指纹注册错误。

**[一加 7T Pro 论坛](https://forum.xda-developers.com/7t-pro)**| |**|[一加 7T Pro 迈凯轮版](https://forum.xda-developers.com/7t-pro-mclaren)**

**[一加 8 XDA 论坛](https://forum.xda-developers.com/oneplus-8) ||| [一加 8 职业 XDA 论坛](https://forum.xda-developers.com/oneplus-8-pro) ||| [一加 8 职业 XDA 评论](https://www.xda-developers.com/oneplus-8-pro-review-never-settle-on-hardware/)**

腐败背后的确切原因尚未查明。我们知道，一加 8 系列和一加 7T Pro 上的指纹传感器可能会在某些特定情况下停止工作(比如在刷新了不同的区域固件之后)。从您的单元刷新持久分区的已知工作转储后，可以修复指纹注册的异常。并不是所有的最终用户都期望这样做，因此该解决方案实际上并不可行。

## 修复一加 8 专业版

幸运的是，XDA 资深会员 antnyhills 已经找到了一种相当通用的方法来修复一加 8 Pro 上损坏的持久分区。想法是从具有损坏的持久分区的目标设备中提取现有的指纹校准数据，并在清理的持久分区之上恢复它。假设您在一加 8 Pro 上拥有 root 访问权限，那么来自终端仿真器或 ADB shell 的具有 root 权限的以下命令应该会创建持久分区的 1:1 备份。

```
 dd if=/dev/block/bootdevice/by-name/persist of=/sdcard/persist.img 
```

备份部分至关重要，所以不要放错你创建的转储。我们建议对分区映像进行设备外备份。**您不能使用另一个用户**的分区映像。

备份分区后，必须在一加 8 Pro 上执行[低级 EDL 刷新](https://www.xda-developers.com/oneplus-8-pro-unbrick-tool-now-available/)，以确保没有固件不匹配。此时，用户应[解锁设备上内置的【工厂模式】](https://forum.xda-developers.com/oneplus-8-pro/how-to/guide-unlock-factory-mode-root-t4118527)，并尝试重新校准指纹传感器。测试预计会失败，这已经不是什么大事了。您只需恢复指纹扫描仪先前备份的校准数据。如果一切正常，你应该可以进入设置并添加你的指纹。

**[【XDA 教程】修复一加 8 Pro](https://forum.xda-developers.com/oneplus-8-pro/how-to/guide-fix-persist-img-loss-finger-print-t4125909)** 上损坏持久分区导致的指纹注册问题

如果你觉得以上帖子中描述的所有步骤都很难，这里有一个由 [antnyhills](https://forum.xda-developers.com/oneplus-8-pro/how-to/guide-fix-persist-img-loss-finger-print-t4125909) 创建的分步视频指南，让事情变得更简单。

## 修复其他一加手机

如果你在另一部一加手机上遇到这个问题，请查看 XDA 论坛，看看是否有适用于你的手机的指南。以下是一些引起我们注意的线索:

**一加 7T Pro 迈凯轮版** : [【导读】用“腐败”坚持 15 分钟修好指纹扫描仪！](https://forum.xda-developers.com/7t-pro-mclaren/how-to/how-to-fix-fingerprint-scanner-corrupt-t4129711)

**一加 8** : [【导读】修复坚持。IMG 指纹传感器丢失](https://forum.xda-developers.com/oneplus-8/how-to/guide-fix-persist-img-loss-finger-print-t4126455)

* * *

***您在一加设备上遇到过指纹注册故障吗？请在下面的评论中告诉我们！***