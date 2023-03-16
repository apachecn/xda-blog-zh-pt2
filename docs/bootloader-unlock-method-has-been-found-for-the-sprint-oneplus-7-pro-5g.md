# 发现了 Sprint 一加 7 Pro 5G 的引导加载器解锁方法

> 原文：<https://www.xda-developers.com/bootloader-unlock-method-has-been-found-for-the-sprint-oneplus-7-pro-5g/>

# 发现了 Sprint 一加 7 Pro 5G 的引导加载器解锁方法

Sprint 一加 7 Pro 5G 发现了一种非官方的引导加载器解锁方法。这款手机于 8 月份在 Sprint 的 5G 网络上推出。

2019 年 8 月，[一加推出了](https://www.xda-developers.com/sprint-5g-phone-oneplus/)售价 840 美元的 Sprint 一加 7 Pro 5G。这款手机是一加 7 Pro 的 5G 版本，4 个月前的 5 月份发布。它具有相同的内部规格，不同之处仅在于调制解调器。Sprint 一加 7 Pro 5G 使用第一代高通骁龙 X50 调制解调器在 Sprint 的中频段 5G 网络上提供低于 6GHz 的 5G 连接。无锁版 4G 一加 7 Pro 和 Sprint 一加 7 Pro 5G 的另一个主要区别是软件。与 4G 解锁版本不同，Sprint 版本没有官方可解锁的引导加载程序。 [T-Mobile 4G 版本](https://www.xda-developers.com/t-mobile-oneplus-7-pro-international-firmware-install/)允许用户在支付设备费用后立即解锁引导程序，但 Sprint 版本不能。然而，现在已经为 Sprint 一加 7 Pro 5G 手机找到了一种非官方的 bootloader 解锁方法。

非官方 bootloader unlock 背后的团队曾运营一项邮寄服务，通过批准用户请求来非官方地解锁 Sprint 一加 7 Pro 设备的 bootloader。然而，由于最近的发展，这种方法现在已经停止，因为该团队现在已经获得了一个 MSM 工具，允许解锁 Sprint 模型上的引导加载程序，而不需要邮寄设备或远程做任何事情。

建议用户谨慎对待这种非官方的引导加载程序方法，因为不能保证事情不会出错。一旦他们的设备被解锁，他们将无法使用 OTA 更新。他们将不得不通过快速启动来刷新更新，或者重置他们的设备来存储并锁定启动加载程序以再次通过 OTA 来更新。

在 Sprint 一加 7 Pro 5G 上非正式解锁引导程序的步骤如下所示。

1.  从这里下载解锁 MSMDownloadTool。
2.  重新启动到 EDL 模式(音量增大+音量减小+ USB)。
3.  允许 MSMTool 运行完成，同时保持警惕。
4.  MSMTool 一结束，就会重启手机。这里重要的一步是不要让它引导到系统。用户必须通过输入 fastboot 来中断引导。
5.  立即运行“快速启动闪烁解锁”。
6.  用户现在应该有一个解锁的引导加载程序。

这是一个非官方的引导加载解锁漏洞，一加可能会在未来修补这个漏洞。如需了解更多信息，用户应[参考论坛主题](https://forum.xda-developers.com/oneplus-7-pro/how-to/bootloader-unlock-sprint-oneplus-7-pro-t4042145)。

* * *

[**XDA 论坛线程为非官方 bootloader 解锁为冲刺一加 7 Pro 5G**](https://forum.xda-developers.com/oneplus-7-pro/how-to/bootloader-unlock-sprint-oneplus-7-pro-t4042145)