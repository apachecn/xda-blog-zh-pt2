# 美国电话电报公司三星 Galaxy Note 3 的引导定制恢复

> 原文：<https://www.xda-developers.com/bootstrap-custom-recovery-for-the-att-samsung-galaxy-note-3/>

定制恢复是 Android 中大多数售后市场奇迹发生的地方。使用一个，你可以备份你的 ROM，擦除你的数据，当然也可以刷新一个新的 ROM。与快速启动相比，恢复甚至可以在锁定的设备上刷新 rom。需要一些变通办法，但这是可以做到的。

三星 Galaxy Note 3 的 [AT & T 变体的所有者现在可以恢复工作了，这要感谢 XDA 公认的开发者](http://forum.xda-developers.com/note-3-att) [Hashcode](http://forum.xda-developers.com/member.php?u=4243514) ，他使用了一种引导方法来使他完全恢复工作。Hashcode 使用的方法不同于 Nexus 5 中使用的标准方法。这种类型的引导恢复保留了*/系统*分区，并在内部 eMMC 区域创建了多达 2 个“ROM 插槽”: */sdcard* 。基本上，定制 ROM 就像设备上的第二个*/系统*分区。激活第二个插槽后，基于 TWRP 的标准恢复会刷新所有必需的文件。

第二个分区的大小是可调的，但你需要记住，更多的插槽意味着更少的空间给其他 rom。恢复可以作为一个应用程序安装，不需要弄乱*/系统*分区。开发仍处于 alpha 阶段，可能会出现一些错误，但这仍然是一个很好的开始！

如果你是美国电话电报公司三星 Galaxy Note 3 用户，想尝试定制 ROM，你应该考虑前往[开发线程](http://forum.xda-developers.com/showthread.php?t=2572978)和 [Hashcode 的博客](http://blog.hash-of-codes.com/how-to-safestrap/)了解更多信息。

非常感谢 XDA 论坛成员 [dirtydroidx](http://forum.xda-developers.com/member.php?u=3456228) 的新闻提示！ ]