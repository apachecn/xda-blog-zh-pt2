# OAndBackupX 是流行的 Android 开源备份应用的一个分支

> 原文：<https://www.xda-developers.com/oandbackupx-android-backup-app/>

在 XDA，我们都是定制 rom、主题和其他各种修改的超级粉丝。我们中的一些人经常在不同的定制 rom 之间切换，因此需要使用应用程序数据备份解决方案，如 [Migrate](https://www.xda-developers.com/migrate-app-switch-custom-roms/) 或全能的 [Titanium Backup](https://www.xda-developers.com/titanium-backup-v8-1-0-adds-support-for-oreo/) 。如果这些解决方案的封闭源代码特性对您来说是一个障碍，那么 OAndBackupX 可能正适合您。

如果这个应用的名字听起来很熟悉，那很可能是，因为 OAndBackupX 是 [oandbackup](https://github.com/jensstein/oandbackup) 项目的一个分支。XDA 成员 [Machiav3lli](https://forum.xda-developers.com/member.php?u=8093836) ，又名 [Antonios Hazim](https://github.com/machiav3lli) ，决定重新使用 oandbackup 的代码库作为 oand backup 的基础。与 oandbackup(自 2019 年 3 月以来[一直未更新)相比，OAndBackupX 具有时尚、现代的用户界面，兼容较新的 Android 版本，能够处理分裂的 apk，支持应用内备份加密，以及许多其他改进。](https://f-droid.org/packages/dk.jens.backup/)

以下是 OAndBackupX 的核心功能:

*   它需要 root 用户，并允许您备份单个应用程序及其数据。
*   支持一次备份和还原一个程序，也支持批量备份和还原多个程序。
*   恢复系统应用程序应该是可能的，不需要重新启动。
*   备份可以安排在没有数量限制的单个计划，并有可能从安装的应用程序列表创建自定义列表。

请记住，开发者尚未添加对 Android 的[存储访问框架](https://www.xda-developers.com/android-q-storage-access-framework-scoped-storage/)的支持。因此，OAndBackupX 无法访问外部 SD 卡或 USB OTG 存储介质，尽管 Antonios 正在积极解决这一问题。

app 本身是开源的，源代码[托管在开发者的 GitHub profile](https://github.com/machiav3lli/oandbackupx) 上。你可以在[的 GitHub repo 的发布版块](https://github.com/machiav3lli/oandbackupx/releases/latest)、 [F-Droid](https://f-droid.org/packages/com.machiav3lli.backup/) 和 [Izzyondroid](https://apt.izzysoft.de/fdroid/index/apk/com.machiav3lli.backup) 上找到 OAndBackupX 的现成安装的 APK。查看下面链接的论坛帖子以了解更多信息。

**[OAndBackupX:安卓应用和数据备份工具——XDA 线程](https://forum.xda-developers.com/android/apps-games/app-oandbackupx-apps-data-backup-tool-t4167179)**