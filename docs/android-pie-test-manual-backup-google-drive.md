# 手动 Google Drive 备份支持现在正在 Android Pie 中测试

> 原文：<https://www.xda-developers.com/android-pie-test-manual-backup-google-drive/>

如果你没有同一个品牌的设备，升级你的 Android 智能手机可能会很烦人。这是因为，除非你有一个带有 TitaniumBackup 的根设备，否则你可能会发现自己不得不重新设置所有的应用程序，因为内置的备份解决方案不是那么强大。虽然内置的解决方案可以将联系人、通话记录和短信备份到 Google Drive 帐户，但它可以备份和恢复哪些应用程序的数据和设备设置是有限制的。如果你从谷歌 Pixel 2 升级到即将推出的谷歌 Pixel 3，内置的谷歌驱动器备份将会非常好，但备份功能缺少一个功能:手动触发备份的能力。幸运的是，谷歌[已经证实](https://www.xda-developers.com/android-pie-manual-google-drive-backup/)我们将在“未来版本”中获得手动谷歌硬盘备份，并且我们已经在最新的 Android Pie 版本中发现了正在开发的功能。

目前，您只能通过进入系统设置中的备份和重置来启用或禁用 Google Drive 备份。备份不能从“备份与重置”设置中手动启动，因为它们受到时间或电源等条件的限制。谷歌表示，将数据手动备份到 Google Drive 将在未来的 Android 版本中推出，但尚不清楚该功能是否会在 Android Q 或谷歌 Pixel 的每月更新中推出。在 XDA 知名开发商 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) 的帮助下，我们成功地在运行安卓 9 Pie 的谷歌 Pixel 2 XL 上启用了手动备份功能，并安装了[最新的 10 月安全补丁](https://www.xda-developers.com/october-android-security-patches-pixel-2-nexus/)。

虽然我们不能说这项功能何时推出，但它在最新的 Android 版本中功能齐全的事实表明，谷歌可以在未来的更新中添加它，而不会推迟 Android Q 的更新。希望在不久的将来，你可以手动触发数据备份，这样你就不必等待备份自动触发，然后再去出售你的设备。

像 WhatsApp 这样特定于应用程序的备份可能会变得非常大，但幸运的是，Google [将不再将](https://www.xda-developers.com/whatsapp-backup-google-drive-storage-quota/) WhatsApp 备份计入您的 Google Drive 存储配额。你存储在设备内部存储器上的任何照片或视频都不会备份到 Google Drive，尽管备份&重置设置页面会将你引导到 Google 相册，这样你就可以高质量地上传你的整个收藏。

## 如何通过 ADB 手动触发数据备份

如果你真的想知道如何手动触发 Android 中的 Google Drive 备份，实际上有一个 ADB shell 命令可以运行，它将启动备份过程。不过，同样的限制也适用，所以不要指望通过这种方式获得完整的数据备份。

```
 <span >adb shell bmgr backupnow </span><span >--</span><span >all</span> 
```