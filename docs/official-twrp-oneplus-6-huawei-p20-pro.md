# TWRP 官方恢复适用于 OnePlus 6、华为 P20 Pro 等

> 原文：<https://www.xda-developers.com/official-twrp-oneplus-6-huawei-p20-pro/>

# TWRP 官方恢复适用于 OnePlus 6、华为 P20 Pro 等

OnePlus 6、华为 P20 Pro、HTC Desire 830、努比亚 M2、PDA 双子星和 Vanzo A315 现已获得官方 TWRP。

在定制的 rom、内核和对设备的修改变得可用之前，用户需要一种方法来备份以防出错。幸运的是，这正是 TWRP 的用武之地。流行的自定义恢复使修改你的设备变得容易，而不用担心把事情搞得太糟(只要你定期备份。)TWRP 现可用于 OnePlus 6。自我们上一篇文章以来，其他设备包括华为 P20 Pro、HTC Desire 830、努比亚 M2、PDA 双子星和 Vanzo A315 最近也获得了支持。最后，LG G4 的 TWRP 已统一用于所有型号。

## 一加 6 的 TWRP

[Dees_Troy](https://twitter.com/Dees_Troy) 发布了设备的定制恢复。由于 A/B 分区方案和专用恢复分区的缺乏，闪存指令与您在以前的一加设备上可能习惯的略有不同。

以下是在 OnePlus 6 上安装 TWRP 的方法:

1.  你需要安装 ADB/Fastboot。如果你不知道它是什么或者你没有安装它，请看这篇文章。
2.  首先，你需要从这里直接下载 twrp-installer-enchilada-3 . 2 . 1-0 . zip 到你的设备[。](https://dl.twrp.me/enchilada/)
3.  然后从这里下载 twrp-3.2.1-0-enchilada.img 到你的 PC [(注意文件格式，因为链接是一样的)。](https://dl.twrp.me/enchilada/)
4.  现在，关闭您的设备。
5.  按住音量键+电源键启动进入引导加载程序。
6.  通过 USB 电缆将您的设备连接到 PC。
7.  打开一个命令提示符。
8.  导航到您的 twrp-3.2.1-o-enchilada.img 所在位置并执行`fastboot boot twrp-3.2.1-0-enchilada.img`。
9.  现在你暂时进入了 TWRP。要永久安装它，进入 install 部分并选择我们之前下载的 twrp-installer-enchilada-3 . 2 . 1-0 . zip。
10.  (可选)如果您之前在设备上安装了 Magisk，现在再次刷新 Magisk。
11.  就是这样！现在你已经在全新的 OnePlus 6 上安装了 TWRP。

MTP 支持目前在 TWRP 被禁用，因为它会导致股票内核崩溃。也许将来的更新会解决这个问题。

## 华为 P20 Pro 和其他产品的 TWRP

您可以通过下面的链接下载上述其他设备的 TWRP。每页上还包括安装说明。

[**TWRP 为华为 P20 Pro**](https://forum.xda-developers.com/huawei-p20-pro/development/recovery-twrp-3-2-1-0-touch-recovery-t3779336)

[**TWRP 对宏达的渴望 830**](https://twrp.me/htc/htcdesire830.html)

[**TWRP 为努比亚**M2 为 ](https://twrp.me/nubia/nubianx52.html)

[**TWRP 为双子星**PDA](https://twrp.me/planet/planetgeminipda.html)

[**TWRP 为万佐 A315**](https://forum.xda-developers.com/android/general/recovery-twm-amazing-x3s-zte-blade-a315-t3744802)

[**统一 TWRP 所有 LG G4 变种**](https://forum.xda-developers.com/g4/development/recovery-twrp-3-touch-recovery-t3442424)