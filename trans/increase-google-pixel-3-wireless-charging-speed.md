# 改装者想出了如何提高谷歌 Pixel 3 的无线充电速度，但这可能有风险

> 原文：<https://www.xda-developers.com/increase-google-pixel-3-wireless-charging-speed/>

# 改装者想出了如何提高谷歌 Pixel 3 的无线充电速度，但这可能有风险

XDA 资深成员 k0rner 公布了一个 mod，可以将 Pixel 3 的无线充电电流提高到高达 1.290mA

与电缆充电相比，无线充电通常较慢，但最近一些原始设备制造商已经在其设备中实现了更快的无线充电。三星在这一点上是众所周知的，如果你使用 [Pixel 支架](https://www.xda-developers.com/google-pixel-3-google-pixel-3-xl-specs-features-pricing-availability/)和其他来自 *Made for Google* 计划的认证设备，Pixel 3 和 Pixel 3 XL 实际上将充电 10W(Belkin 去年年底宣布了其 10W 充电器)。然而，如果您使用的是未经认证的 Qi 无线充电器，那么默认情况下，您通常会获得大约 750mA 的充电电流。

[**像素 3 XDA 论坛**](https://forum.xda-developers.com/pixel-3)

这是出于多种原因(如发热)，但一些改装者已经找到了一种提高 Pixel 3 无线充电速度的方法。XDA 资深成员[科尔纳](https://forum.xda-developers.com/member.php?u=2309157)在周末公布了这一模型，并表示他能够将无线充电电流提高到 1290 毫安。这是通过将`/sys/class/power_supply/wireless/voltage_max`的值更改为 9000000(从默认的 5000000)来实现的。

这种改变需要在设备无线充电时进行，因为一旦充电会话结束，它将重置为默认状态。但是，这个设置可以通过使用[高级充电控制 Magisk 模块](https://forum.xda-developers.com/apps/magisk/module-magic-charging-switch-cs-v2017-9-t3668427)永久化(只要你进去修改代码添加`onPlugged=./wireless/voltage_max:9000000`)。

警告:任何干扰充电的修改都是有风险的。您应该始终为您的设备使用高质量的充电器。

[**在我们的 Pixel 3 论坛**](https://forum.xda-developers.com/pixel-3/development/mod-pixel-3-fast-wireless-charge-t3889374/) 中阅读更多关于这个 mod 的信息