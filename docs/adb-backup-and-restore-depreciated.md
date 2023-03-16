# 谷歌警告称，在未来的 Android 版本中，可能会删除 ADB 备份和恢复功能

> 原文：<https://www.xda-developers.com/adb-backup-and-restore-depreciated/>

# 谷歌警告称，在未来的 Android 版本中，可能会删除 ADB 备份和恢复功能

不幸的是，ADB 备份和恢复服务似乎即将消失。AOSP 的提交标题为“向 adb 备份/恢复添加弃用警告”

这些年来，安装一部新的 Android 手机已经变得容易多了。Android Oreo 的[自动填充功能](https://www.xda-developers.com/android-os-autofill-framework-will-finally-resolve-a-long-standing-lag-issue-with-password-managers/)使得登录你的所有应用程序变得更加容易，一些应用程序甚至会保留你的所有偏好。在同一家 OEM 厂商的手机之间切换特别容易，因为大多数手机都有自己的备份和恢复工具。然而，这种体验并不完美，在不同 OEM 厂商的手机之间切换可能会很痛苦。这就是[亚行备份和恢复](https://www.xda-developers.com/android-oreo-adb-backup-better/)可以派上用场的地方。

ADB 备份和恢复是一个方便的工具，它允许你做比一些内置的备份选项更多的事情。您可以存储私人数据和已安装的应用程序，而不需要 root 用户，这取决于应用程序是否允许。不幸的是，看起来 ADB 备份和恢复可能会在未来的 Android 版本中消失。AOSP 的[提交标题为“向 adb 备份/恢复添加弃用警告”每当用户在最新的 ADB 工具版本中运行该工具时，都会显示一条警告，告诉他们该功能可能无法继续使用。](https://android-review.googlesource.com/c/platform/system/core/+/958872)

对于依赖这种非根解决方案来获得更好备份的人来说，这将是一个遗憾。如果你给手机装根的话，还有更强大的选择，比如[钛备份](https://www.xda-developers.com/titanium-backup-v8-1-0-adds-support-for-oreo/)。在这一点上，这只是一个警告，所以我们不知道该工具多久会失效。我们将继续关注这个故事，看看谷歌何时决定继续推进。

* * *

[**来源:AOSP**](https://android-review.googlesource.com/c/platform/system/core/+/958872)

*感谢 XDA 知名开发商 [luca020400](https://forum.xda-developers.com/member.php?u=5778309) 的提示！*