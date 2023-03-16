# 谷歌将让文件管理器开发者提交一个表格，以在 Android 11 中获得广泛的文件存储访问

> 原文：<https://www.xda-developers.com/google-file-manager-devs-submit-form-broad-file-storage-access-android-11/>

今年早些时候发布的 Android 10 beta 2 [显示谷歌计划限制应用程序访问手机内部存储的方式。出于这个目的，Google 引入了一种叫做作用域存储的东西。然而，由于几个开发者的强烈反对，公司](https://www.xda-developers.com/android-q-beta-2-everything-new/)[不得不取消](https://www.xda-developers.com/google-gives-developers-more-time-android-q-scoped-storage/)的实施。该公司允许尚未针对 Android 10 的应用程序像以前一样工作，并在 2020 年 11 月 1 日之前给开发者时间更新他们的应用程序以针对 Android 10。

默认情况下，已经针对 Android 10 的应用程序只能看到其应用程序特定目录中的文件。为了访问其他应用程序创建的文件，如照片、图像、视频和音频，这些应用程序仍然需要请求 READ_EXTERNAL_STORAGE 权限，但现在获得此权限不再能够访问整个/data/media 分区。相反，他们只能在 MediaStore API 提供的明确定义的位置看到文件。虽然这种实现适用于需要访问媒体文件的应用程序，但它不适用于文件管理器应用程序。

文件管理器需要对外部存储的广泛访问才能工作，如果他们的目标是 Android 10，获得广泛文件访问的唯一方法是使用存储访问框架(SAF) API。尽管 SAF 自 Android 5.0 Lollipop 以来就已经存在，但开发人员倾向于不使用它，因为它有一个困难且缺乏文档记录的 API，用户体验差，性能差，可靠性差。现在，谷歌的目标是通过 Android 11 解决这些问题。

根据谷歌的 Roxanna Aliabadi、Zimuzo Ezeozue 和 Yacine Rezgui 最近发表的题为“为范围存储做准备”的演讲，谷歌正计划授予“特定用例的特殊应用访问权”。作为谈话的一部分，他们提到，这种“特殊应用程序访问权限”只授予那些证明“明确需要”完全访问共享存储的应用程序，向谷歌“提交声明表”，而不访问“外部应用程序目录”。

这意味着文件管理器将不得不请求谷歌许可来访问外部存储，就像应用程序请求短信/通话记录许可必须请求谷歌一样。因此，可能会有任意执行的问题，就像我们过去看到的 Google Play 的决定一样。最后，另一个潜在的问题是，文件管理器将不再能够访问外部应用程序目录。所以，游戏用 mods 之类的东西就再也不行了。

* * *

**来源:[YouTube](https://youtu.be/UnJ3amzJM94?t=543)**

**Via:[Reddit](https://www.reddit.com/r/androiddev/comments/dr9p98/according_to_google_storage_permission_can_be/)**