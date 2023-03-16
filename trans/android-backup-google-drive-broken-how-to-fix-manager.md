# Android 备份到 Google Drive 已经坏了很多次，以下是修复的方法

> 原文：<https://www.xda-developers.com/android-backup-google-drive-broken-how-to-fix-manager/>

从一个 Android 智能手机迁移到另一个 Android 智能手机的一个痛点是，在应用数据的上下文中，您不太可能进入与开始时相同的设备状态。当您在不同的 OEM 之间迁移时，这个问题会更加突出，因为特定的 OEM 解决方案通常以该生态系统为中心。谷歌试图通过利用 Google Play 服务框架和 Google Drive 为谷歌的 Android 提供内置备份管理器服务来解决这个问题。这个内置的解决方案会自动将联系人、通话记录、短信以及某些应用数据和设备设置备份到 Google Drive，但从 Android Pie 开始，你也可以[自己触发备份](https://www.xda-developers.com/android-pie-test-manual-backup-google-drive/)。然而，用户一直抱怨谷歌硬盘的备份在过去几个月里被破坏了。

据 *[AndroidPolice](https://www.androidpolice.com/2019/11/13/android-backups-to-google-drive-have-been-disabled-on-many-phones-for-months-no-proper-fix-in-sight/)* 报道，几个月来，一些用户一直在抱怨谷歌硬盘备份对他们来说已经完全崩溃了。“立即备份”按钮是灰色的，不能点击，手机停止备份数据，没有任何警告。在各种设备和其他变量中都发现了这个问题，因此您可能需要检查您的设备是否备份了数据。

可悲的是，谷歌还没有承认这个问题，这意味着没有正式的解决方案。幸运的是，您可以通过几个简单的 ADB 命令将事情掌握在自己手中并[强制备份。正如 XDA 资深会员](https://www.xda-developers.com/android-pie-test-manual-backup-google-drive/) [Dexer125](https://forum.xda-developers.com/member.php?u=8083015) 在[他的线程](https://forum.xda-developers.com/mi-8/how-to/guide-google-backup-waiting-to-backup-t3895101)中提到的，您可以使用备份管理器的 shell 命令界面强制进行备份:

```
 adb shell
bmgr run
bmgr backupnow  
```

这应该会强制在您的设备上进行备份。如果得到“*备份完成，结果:备份取消*”，则运行以下命令:

```
 bmgr backupnow appdata
bmgr backupnow  
```

这应该有希望返回一个成功的结果。完成后，重启你的设备。“立即备份”按钮现在应该是可点击的，您的数据应该在后台备份。然而，我们仍然希望谷歌承认这个问题，并推出一个解决方案。

**[修复谷歌硬盘“等待备份”bug 指南——XDA 线程](https://forum.xda-developers.com/mi-8/how-to/guide-google-backup-waiting-to-backup-t3895101)**

* * *

虽然这个问题对受其影响的用户来说肯定是一个问题，但谷歌也应该认识到一个事实，即与苹果为其设备提供的强大解决方案相比，Android 上的应用程序和设备设置备份情况非常糟糕。诚然，苹果处理的设备数量少得多，而 Android 生态系统的多样性绝对是巨大的。

应用程序数据恢复在 Android 6.0 棉花糖中被引入为“[自动备份应用程序](https://developer.android.com/guide/topics/data/autobackup.html)”。

> *自动备份应用程序*自动备份目标为 Android 6.0 (API 级别 23)或更高版本并在其上运行的应用程序中的用户数据。Android 通过将应用程序数据上传到用户的 Google Drive 来保存应用程序数据，在 Google Drive 中，应用程序数据受到用户的 Google 帐户凭证的保护。你的应用的每个用户的数据量被限制在 25MB，并且存储备份数据是免费的。你的应用程序可以定制备份过程或通过[禁用备份](https://developer.android.com/guide/topics/data/autobackup.html#EnablingAutoBackup)选择退出。

默认情况下，应用程序可以选择将多达 25MB 的([符合条件的](https://developer.android.com/guide/topics/data/autobackup.html#Files))数据备份到用户的 Google Drive 账户。但出于各种原因，许多开发者选择不将他们的应用程序数据保存到 Google Drive。

至于设备设置，Google Drive 备份包括设置中的值。系统，设置。但是由于这些设置表对于每个 OEM 来说往往是不同的，所以许多数据不能被成功地备份或恢复。

由于这些原因——应用程序开发人员选择退出，以及 OEM 实施中的差异——Android 的备份和恢复已经变得脆弱和不完整。大多数用户不太可能知道这个痛点，直到他们到达恢复他们的数据的节点，才发现他们不得不花很多时间让他们的新手机类似于旧手机的软件状态。或许谷歌是时候涉足这些领域了？