# 使用 UAPM 管理分区

> 原文：<https://www.xda-developers.com/uapm-partition-management/>

# 使用 UAPM 管理分区

该工具允许您创建 Android 分区的备份，并直接从您的设备刷新映像。

要像内核或恢复一样刷新映像，您通常需要访问您的 PC 并正确配置快速启动驱动程序。这并不太方便，尤其是当你在旅行时，并且有一个新版本的内核可以试用。XDA 论坛成员[费雷拉瓦克斯](http://forum.xda-developers.com/member.php?u=5859397)编写的工具现在可以直接在你的设备上执行分区的高级操作。该工具允许您备份当前分区，而无需进行恢复。该应用程序还可以直接从您的设备上刷新图像。要使用该应用程序，您需要找到正确的分区块号。可以执行一些命令来获得正确的块号。对于一些设备来说:`adb shell ls -al /dev/block/platform/msm_sdcc.1/by-name`这确实取决于你的设备，你可以通过阅读[这些](https://github.com/ameer1234567890/OnlineNandroid/wiki/How-To-Gather-Information-About-Partition-Layouts)简短[指南](http://androidcreations.weebly.com/how-to-get-android-mounts-and-partition-images.html)来了解更多关于这些命令的信息。您也可以查找当前手机的设备树来检查正确的 Fstab。**被警告**闪错了可以 **硬砖你的设备** 。首先备份你的分区，并与 ClockworkMod 或 TWRP 所做的备份进行比较，这是一个明智的选择。如果尺寸匹配，很有可能一切正常。该应用程序需要 root 访问权限才能正常工作。你可以通过访问[通用 Android 分区管理器](http://forum.xda-developers.com/android/apps-games/app-uapm-universal-android-partition-t2976587)应用线程来了解这个项目的更多信息。