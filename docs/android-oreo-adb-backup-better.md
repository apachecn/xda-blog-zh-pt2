# Android Oreo 获得显著的 ADB 备份增强

> 原文：<https://www.xda-developers.com/android-oreo-adb-backup-better/>

取决于你问谁，你可能会听说 [Android Debug Bridge](https://www.xda-developers.com/set-up-adb-and-fastboot-on-linux-mac-os-x-and-chrome-os-with-a-single-command/) 的备份功能是天赐之物。这项功能是在冰淇淋三明治中推出的，它允许您在不使用 root 或其他应用程序的情况下，只需使用 adb 即可对您的设备进行完整备份。然而，这个工具确实有一些限制，这给了其他应用程序如钛备份的优势。Android Oreo 旨在修复其中一些缺陷，以使其成为更好、更可靠的工具。因此，新的 Android 版本在 adb 备份和 adb 恢复方面获得了一些急需的增强功能。

* * *

**备份超时增加**

在 Android Oreo 之前，共享存储(/sdcard 内容)备份使用 5 分钟的超时，而恢复使用 1 分钟的超时。这意味着，如果 sdcard 上有任何大文件，例如长视频，备份/恢复总是会超时。更短的恢复超时意味着甚至一些更小的文件，如 zip 或大图像，也无法恢复。幸运的是，最新的 Android 版本不再是这种情况。

[从 DP2](https://android.googlesource.com/platform/frameworks/base/+/3b03673d23784fb30d5fdf11ed4fa6e1619bef0f) 开始，备份超时和恢复超时分别从 5 分钟和 1 分钟增加到 60 分钟。这 12 倍的备份增加应该给你足够的时间直接备份任何文件存储在你的手机上。此外，大规模恢复增加现在应该给你的能力，恢复你的手机上的一切。您可以使用以下方法测试此功能

```
 adb backup -shared && adb restore backup.ab 
```

用你的奥利奥手机。这将对您手机的共享存储进行完整的备份/恢复。

* * *

**增加对键/值包的支持**

[键/值备份](https://developer.android.com/guide/topics/data/keyvaluebackup.html)是 Android 2.2 Froyo 中引入的一个简洁的小功能。它们以前被称为备份 API，是开发人员通过上传到 Android 备份服务将应用数据备份到云的一种方式。但是以前，有键/值备份代理的应用程序会被 fullbackup 命令跳过。然而，对于 Android 奥利奥来说，这不再是真的了。

[从 DP1](https://android.googlesource.com/platform/frameworks/base/+/b59a4b85ade3f1f408def6a0dd3dbb146225bdd7) 开始，通过向 adb 备份命令添加-includekeyvalue 标志，所有支持键/值备份的包都将被添加到结果备份中。同样，如果备份包含键/值数据，它也将被还原。此功能为将来添加带有键/值备份代理的包的 CTS 测试做准备。您可以使用以下命令对此进行测试

```
 adb backup -includekeyvalue -all && adb restore backup.ab 
```

在你的设备上。

这两个功能应该允许 adb 备份在 Android Oreo 设备上更加可靠，并且是根备份应用程序的一个体面的替代方案。