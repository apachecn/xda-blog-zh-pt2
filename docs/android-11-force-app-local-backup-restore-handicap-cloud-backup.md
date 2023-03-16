# Android 11 强制应用支持本地备份，但不支持云备份

> 原文：<https://www.xda-developers.com/android-11-force-app-local-backup-restore-handicap-cloud-backup/>

对我来说，在 Android 上备份和恢复应用程序是一种可怕的体验，这一点没有争议。现在，这种说法并不普遍适用——如果你要升级到与你之前的设备来自同一个供应商的 Android 设备，那么应用程序迁移过程通常会非常无缝。问问那些试图将所有应用程序迁移到来自不同 OEM 厂商的新手机上的人——这几乎包括科技媒体中的所有人——你可能会听到不得不再次设置应用程序的抱怨。Android 11 已经悄悄地在这方面做出了重大改变，但可悲的是，谷歌还没有走得足够远。

在 Android 上备份和恢复应用程序如此痛苦的主要原因是，许多应用程序不允许备份他们的数据。Android 原生支持通过[备份管理器](https://developer.android.com/reference/android/app/backup/BackupManager)基础设施备份和恢复应用程序及其数据，在大多数 Android 设备上，这是通过 Google Play 服务处理的[，文件存储在用户个人 Google Drive 帐户的云中。最多可以备份 25MB 的](https://www.xda-developers.com/android-pie-test-manual-backup-google-drive/)[应用程序的私人数据文件](https://developer.android.com/guide/topics/data/autobackup.html#Files)，包括共享的偏好设置、数据库和保存到应用程序特定的内部和外部存储目录的文件。然而，许多开发人员通过将 [`android:allowBackup`清单属性](https://developer.android.com/guide/topics/manifest/application-element#allowbackup)设置为“假”来选择不备份他们的应用数据一些应用程序选择退出有很好的理由，特别是如果应用程序处理敏感数据并且不希望这些数据被提取，但这些应用程序不应该依赖于他们的私人数据目录不能被访问的假设，而是应该加密他们正在处理的任何敏感数据。

因此，无论你采取哪种方法来备份你的应用程序及其数据，无论是通过 ADB 、Google Drive 还是像 [Helium](https://www.xda-developers.com/must-have-app-review-helium-backup-without-root/) 这样的应用程序，都没有办法完全备份你设备上的每个应用程序。这就是为什么像 [Titanium Backup](https://www.xda-developers.com/tag/titanium-backup/) 这样的根支持备份和恢复应用已经存在了这么长时间，因为所有的非根解决方案[在数据迁移方面都不那么有效](https://www.xda-developers.com/android-backup-google-drive-broken-how-to-fix-manager/)。对于普通用户来说，当在工厂重置之后设置设备或者当切换到新设备时，这可能导致令人沮丧的体验。

## Android 11 有什么变化

然而，在 Android 11 上，[系统忽略了](https://developer.android.com/preview/behavior-changes-11#device-to-device-file-transfer)应用文件“设备到设备”迁移的`allowBackup`清单属性。这只会影响以 API 等级 30 为目标的应用程序，目前没有多少应用程序这样做，但由于 Google Play 的[改变 API 等级要求](https://www.xda-developers.com/play-store-updated-requirements-api-level-64-bit/)，明年以 Android 11 为目标的应用程序将会大幅增加。

对于高级用户来说，这意味着 ADB 备份和恢复在 Android 11 中可能会变得更加强大。ADB backup and restore 上次升级[是在 Android 8.0 Oreo](https://www.xda-developers.com/android-oreo-adb-backup-better/) 中。不幸的是，ADB 备份和恢复[已被否决](https://www.xda-developers.com/adb-backup-and-restore-depreciated/)，并可能在未来的版本中被删除(它仍在 Android 11 Beta 1 中工作)，所以谁知道你还能利用平台行为的这一变化多久。

另一方面，对于基于云的备份和恢复，系统仍将尊重`allowBackup`属性。可悲的是，这意味着普通用户无法从 Google Drive 恢复更好的备份和恢复。