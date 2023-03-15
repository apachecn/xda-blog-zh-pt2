# 增加 Android 上的短信限制

> 原文：<https://www.xda-developers.com/increase-the-sms-limit-on-android/>

如果你对 Android 操作系统强加的每小时 100 条短信的限制感到沮丧，你可以实施一个调整来解决这个问题。

在 XDA 论坛成员在这个[原始帖子](http://forum.xda-developers.com/showthread.php?t=626771)中提出问题后，XDA 成员 [matthenry87](http://forum.xda-developers.com/member.php?u=1594981) 已经设法让这个调整生效。

这项调整需要在 Android 设备上的终端应用程序中输入一些命令，或者使用 adb 从您的计算机中输入一些命令，这样您就可以将“sms_outgoing_check_max_count”值从 101 更改为一个新的限制，或者通过将“sms_outgoing_check_interval_ms”设置为 0 来完全删除该限制。

matthenry87 已经证实，第二个选项在他的 Android 设备上立即生效。

要了解更多信息，请访问 [tweak 的线程](http://forum.xda-developers.com/showthread.php?p=5519546#post5519546)。