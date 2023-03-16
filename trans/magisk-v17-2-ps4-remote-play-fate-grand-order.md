# Magisk v17.2 远程游戏混淆，修复命运/大订单

> 原文：<https://www.xda-developers.com/magisk-v17-2-ps4-remote-play-fate-grand-order/>

# Magisk v17.2 增加了 PS4 远程游戏的混淆，命运/大订单的变通办法，等等

Magisk v17.2 在这里，它增加了 PS4 远程游戏的混淆，命运/大订单和堡垒之夜等的变通办法。

Magisk 是给你的手机找根的最好方法之一，这不仅仅是因为它是在大多数设备上唯一这样做的方法之一。Magisk 完全在不修改/system 分区的情况下进行修改，旨在绕过 SafetyNet 等检测方法。除了堡垒之夜和 PS4 Remote Play 等少数游戏外，它运行得非常好，但 Magisk v17.2 实际上也增加了对这些应用程序的支持！你可以在下面查看完整的变更日志。以前，玩这些游戏的唯一方法是使用 Magisk 的 [canary 版本，除非你是开发人员，否则不推荐使用。](https://www.xda-developers.com/fate-grand-order-fortnite-mobile-magisk/)

*   [ResetProp]更新到 AOSP 上游以支持序列化系统属性
*   [MagiskInit]随机化 Magisk 服务名称以防止检测(例如 FGO)
*   [MagiskSU]与 Magisk 管理器通信的新通信方案

这些变化不仅确保 Magisk 不会被检测到，而且还修复了 Android Pie 出现的一些问题。最值得注意的是，resetprop 已得到修复，允许您对 build.prop 进行无系统的更改。resetprop 最有用的一个好处是，你可以改变你设备的指纹来通过 CTS，比如在 OnePlus 6[Android Pie open beta](https://www.xda-developers.com/pass-safetynet-beta-android-pie-oneplus-6/)上。Magisk 管理器的通信方法也被完全重写，使得应用程序几乎不可能检测到它是否存在。

该更新可以从 XDA 的 Magisk 线程下载(如下),并在您的设备上刷新。您需要更新 Magisk Manager，因为旧版本与新的通信方法不兼容。它不是完全模糊的，以便仍然与 Magisk v17.1 一起工作。这个更新将对那些在手机上玩游戏或在 Android Pie 上的人有用。

* * *

[t1 下载魔法 v 17.2T3](https://forum.xda-developers.com/showpost.php?p=77678063&postcount=46)