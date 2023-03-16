# 未来的 Android 版本将提供手动 Google Drive 备份支持

> 原文：<https://www.xda-developers.com/android-pie-manual-google-drive-backup/>

# 未来的 Android 版本将提供手动 Google Drive 备份支持

在 Android 9 Pie 的未来版本中，手动应用数据、通话记录、设备设置和短信备份到 Google Drive 将成为可能。

据 Android 开发团队的一名记者在 [Google Issue Tracker](https://issuetracker.google.com/issues/112233564) 上称，未来的 Android 版本将允许用户手动将应用程序数据备份到 Google Drive。这包括备份您的应用程序数据、通话记录、设备设置和短信。目前，在特定条件下，如时间、电源状态等，您的备份会自动转到 Google Drive，用户不可能通过正常方式进行干预。令人欣慰的是，在未来的 Android 版本中，用户将能够自己触发备份，这样你就可以在知道你的数据安全存储在云中的情况下更换手机。

然而，事实并非如此，您根本无法手动触发备份*。该功能确实存在，但你需要通过在 Android 智能手机上启用 USB 调试来在你的计算机上设置 ADB。然后，您可以在计算机上使用以下命令，将所有数据手动备份到 Google Drive 上。*

```
 adb shell bmgr backupnow  
```

虽然你可以在谷歌 Pixel 2 XL 这样的 Android Pie 设备上通过进入**设置** - > **系统** - > **备份&重置**来打开和关闭自动备份，但唯一真正手动触发备份的方法是通过上面的 ADB 命令。

 <picture>![Google Pixel 2 XL Android Pie backup](img/f4daf5b75aca18866fc75c004344f122.png)</picture> 

Settings --> System --> Backup settings on the Google Pixel 2 XL running Android 9 Pie

一旦谷歌将这一功能添加到 Android 中，你就不必再依赖一个晦涩的 ADB 命令了。对于普通消费者来说，它不会是最有用的功能，但肯定会被一些人使用。幸运的是，通过内置的 Android 备份管理器备份的应用程序不会用完 Google Drive 的存储配额。WhatsApp 等特定应用程序的备份在备份时确实会占用你的存储空间，[不过对于非常流行的消息客户端](https://www.xda-developers.com/whatsapp-backup-google-drive-storage-quota/)来说，这种情况将会改变。我们将密切关注这项功能的上线，我们希望它有可能在 Android Pie 的下一个版本中推出。*