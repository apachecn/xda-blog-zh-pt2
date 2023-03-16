# TWRP 3.2.2-0 对 OTA 更新进行了 ADB 修复和改进

> 原文：<https://www.xda-developers.com/twrp-3-2-2-0-adb-fixes-improve-ota/>

# TWRP 3.2.2-0 对 OTA 更新进行了 ADB 修复和改进

TWRP 3.2.2-0 已经发布，它为 OTA 更新的安装带来了许多 ADB 修复和改进。看看这里！

最著名的自定义恢复项目 Team Win Recovery Project(称为 TWRP)已更新到版本 3.2.2-0。这个版本对以前的版本进行了大量的修复和改进。值得注意的修复包括对 adb 备份功能的正确支持，以及改进 OTA 更新的安装，以便在您的设备上安装它们时不需要解密。你可以在 GitHub 上阅读下面由 XDA 资深知名开发者 [Dees_Troy](https://forum.xda-developers.com/member.php?u=912474) 发布的完整变更日志。

*   adb 备份修复
*   OTA 风格的更新拉链现在会自动安装而不提示解密
*   在高通设备上处理日期/时间的细微调整
*   一些语言翻译的更新

拥有官方兼容设备的用户可能会在未来几天看到 TWRP 的更新版本，如果它还不可用的话。虽然对于那些只使用 TWRP 闪存的人来说，这不是一个重要的更新，但对每个人来说都有一些很酷的变化。OTA 能够在没有/data 的情况下安装并不是非常重要，但它肯定会加快用户在更新手机时的体验。几乎所有的在线旅行社都只接触/system 分区，所以它会在不损害用户利益的情况下加速这个过程。

adb 备份是这里较大的修复之一，也是[在 3.1.0 版本中推出](https://www.xda-developers.com/twrp-v3-1-0-is-now-rolling-out-with-support-for-adb-backup-ab-ota-zips-and-more/)的一个特性。不过，这个功能自推出以来已经出现了许多问题，由于围绕它的不同原因，[的许多问题](https://github.com/TeamWin/Team-Win-Recovery-Project/issues/877)被[在 GitHub 上公开](https://github.com/omnirom/android_bootable_recovery/issues/207)。我们可以假设这个特性现在很可能没有 bug 并且工作正常。虽然在线旅行社现在在安装方面效率更高，但漏洞修复也很重要，所以看到工作的平均分配很好。

如果你想查看 GitHub 的官方变更日志，你可以看看下面的链接。

* * *

[**来源:TWRP GitHub**](https://github.com/TeamWin/twrpme/blob/master/_posts/2018-07-01-twrp-3.2.2-0-released.markdown)