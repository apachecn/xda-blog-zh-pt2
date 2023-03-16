# HMD Global 的诺基亚 4.2 和诺基亚 3.2 现在可以在不拆卸的情况下解锁引导程序

> 原文：<https://www.xda-developers.com/hmd-global-nokia-4-3-2-bootloader-unlocked-without-disassembly-android-10/>

# HMD Global 的诺基亚 4.2 和诺基亚 3.2 现在可以在不拆卸的情况下解锁引导程序

似乎你可以在 Android 10 更新后使用常规的快速启动命令解锁诺基亚 3.2 和诺基亚 4.2 的引导程序。请继续阅读！

诺基亚 3.2 和诺基亚 4.2 于 2019 年 2 月在 MWC[发布。像 HMD Global 产品组合中的大多数其他设备一样，这些 Android One 供电的手机没有官方的引导加载器解锁机制。没有一个解锁的引导装载程序，典型的 mods -包括根和自定义 ROMs 变得不可能实现。不过，还是有一线希望的，因为在 Android 10 更新后，这两部手机的所有者显然可以使用常规的快速启动命令来解锁引导加载程序。](https://www.xda-developers.com/nokia-1-plus-32-42-android-one-mwc-launch/)

**[诺基亚 3.2 XDA 论坛](https://forum.xda-developers.com/nokia-3-2) || [诺基亚 4.2 XDA 论坛](https://forum.xda-developers.com/nokia-4-2)**

值得一提的是，社区确实发现了[一个非官方的诺基亚 3.2/4.2](https://www.xda-developers.com/nokia-3-2-nokia-4-2-bootloader-unlock-method/) 的 bootloader 解锁方法，但是这个过程对于没有经验的用户来说太繁琐了。要将`get_unlock_ability`参数的值设置为`1`，必须首先拆卸目标设备。通过短路被称为“测试点”的引脚触发手机的 [EDL 模式](https://www.xda-developers.com/exploit-qualcomm-edl-xiaomi-oneplus-nokia/)后，人们不得不通过被称为**消防软管**的底层协议修改“配置”分区。

[根据用户报告](https://forum.xda-developers.com/nokia-3-2/how-to/how-to-unlock-bootloader-disassembling-t4096623)，稳定的 Android 10 更新为[诺基亚 3.2](https://www.xda-developers.com/samsung-galaxy-j6-nokia-3-2-receive-stable-android-10-update/) 和[诺基亚 4.2](https://www.xda-developers.com/nokia-4-2-receives-official-android-10-update/) 实际上不赞成前述方法。自从更新以来，引导程序[可以非常简单地解锁](https://twitter.com/yashinatsu/status/1268628110511009792)，而不需要经历任何奇怪的麻烦和变通办法。你所需要做的就是在开发者选项中启用“OEM 解锁”,然后通过 Fastboot 解锁，就像解锁谷歌 Pixel 或一加手机一样。[与诺基亚 8](https://www.xda-developers.com/hmd-global-allegedly-killed-off-official-nokia-bootloader-unlock/) 不同，你甚至不需要放一个服务器生成的解锁令牌。

### 嗯，有一个陷阱！

早在 2 月份，一些诺基亚 4.2 用户[报告](https://forum.xda-developers.com/nokia-4-2/how-to/2020-jan-security-patch-alternate-t4044867)他们可以切换 OEM 解锁选项，并在基于 Pie 的软件版本 V1.41H 上连续解锁引导加载程序。这可能是诺基亚方面的一个错误，稍后可能会被修补，就像最初一批诺基亚 6.2 和诺基亚 7.2 [附带了一个可解锁的引导加载程序](https://www.xda-developers.com/nokia-7-2-unlockable-bootloader/)，但该漏洞很快被关闭。HMD Global 这次是不是故意为诺基亚 3.2/4.2 提供 bootloader 解锁功能？我们不知道，我们甚至可能会在未来几天内看到 OTA 推出一个快速的“错误修复”来逆转“无意的错误”。