# 非官方的无系统曝光可用-允许在线旅行社，安卓支付

> 原文：<https://www.xda-developers.com/unoffical-systemless-xposed-is-now-available-otas-and-pay-unaffected/>

# 非官方无系统曝光现已可用-在线旅行社和支付不受影响！

一个新构建的 Xposed 可以让你在你的 ROM 上获得 OTA，在 XDA 找到如何安装它！

公认的贡献者 [topjohnwu](http://forum.xda-developers.com/member.php?u=4470081) 已经修改了 Xposed 框架(V.85.1)来与 Chainfire 的无系统 SuperSU 一起工作，以便在不修改系统分区的情况下也能运行。

这意味着您可以在运行 stock ROM 的根设备上安装 Xposed 模块，并继续接收 OTA。一些用户甚至报告说，Android Pay 使用这种方法工作，包括 OP，但是像往常一样，您的 milage 可能会有所不同。

> “我在 systemless 上实现 Android Pay 的方法是，ramdisk 中的 mount 脚本将检测 Xposed installer 创建的禁用文件。如果该文件存在，它不会装载 app_process，但仍会装载其余的艺术库和二进制文件，因此艺术缓存在禁用时不会重新构建。

对于 Arm、Arm64 和 x86 设备，存在无系统 Xposed 构建，但是，无系统 root 目前仅在 Marshmallow 和更高版本上可用，因此，如果您正在运行您的股票 ROM 和 Xposed，但错过了 OTA 接收您的更新，那么现在就前往线程并尝试一下。请务必仔细阅读线程，并做好备份！

[**Head over to the thread**](http://forum.xda-developers.com/xposed/unofficial-systemless-xposed-t3388268)