# 通过 TWRP 协调员从 Android 内部控制 TWRP

> 原文：<https://www.xda-developers.com/control-twrp-from-within-android-with-twrp-coordinator/>

你可能还记得几年前 TWRP2 [推出](http://www.xda-developers.com/android/team-win-recovery-project-updated-to-2-1/ "Team Win Recovery Project Updated to 2.1")时，它带来了开源开放恢复系统(ORS)。借助 ORS，专门构建的应用程序能够直接在 Android 内部对各种恢复任务进行排队。

ORS 最终导致了各种有趣的应用程序的产生，比如之前提到的 [TWRP 经理](http://www.xda-developers.com/android/twrp-manager-makes-recovery-even-easier/ "TWRP Manager Makes Recovery (Even) Easier")。但是，如果你想让一个应用程序在 Android 中控制 TWRP 的几乎所有方面呢？现在与 TWRP 协调员 XDA 由资深会员 [萨梅尔迪亚卜](http://forum.xda-developers.com/member.php?u=4944297) 和公认的开发商 [直升机 88](http://forum.xda-developers.com/member.php?u=1924950) ，你可以做到这一点。

顾名思义，TWRP 协调员允许你启动基本上任何 TWRP 相关的任务，你可能想要的。这包括安装和更新 TWRP、重启以恢复、刷新 zip、创建/重命名/删除/恢复备份、擦除数据、执行工厂重置、擦除特定分区、修复权限等等。

有了这样一个强大的应用程序，你想防止未经授权的使用是正确的。幸运的是，TWRP 协调员提供了密码保护和隐藏它的能力。如果您丢失了密码或希望在应用程序被隐藏后启动它，只需拨打*#8977#进入您的电话拨号器。

自然，你需要既有根，并有 TWRP(官方或非官方)恢复安装在您的设备上。如前所述，该应用程序可以为您安装 TWRP，但这自然只适用于官方 TWRP 支持的设备。

你可以通过访问[应用线程](http://forum.xda-developers.com/showthread.php?t=2721474)开始。