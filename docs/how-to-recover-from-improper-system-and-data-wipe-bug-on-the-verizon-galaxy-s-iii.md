# 如何从威瑞森 Galaxy S III 的不当系统和数据擦除错误中恢复

> 原文：<https://www.xda-developers.com/how-to-recover-from-improper-system-and-data-wipe-bug-on-the-verizon-galaxy-s-iii/>

现在[引导程序终于为](http://www.xda-developers.com/android/verizon-samsung-galaxy-s-iii-unlocked/)[威瑞森三星 Galaxy S III](http://forum.xda-developers.com/forumdisplay.php?f=1708) 解锁了，开发者现在可以专注于其他事情了。也就是说，rom、内核、mod，以及对 bug 的修复。困扰威瑞森 Galaxy S III 用户的一个错误是擦除错误，它会导致权限设置不当的一些问题。

XDA 公认的开发者 PureMotive 为那些不幸遇到这个 bug 的人写了一份指南。正如 PureMotive 解释的那样:

> 有时，当你刷新 ROM (TouchWiz 或 AOSP)时，存在/system 和/data 分区不能正确擦除的风险，从而导致它们被格式化为 R/O 权限而不是 R/W。这使得手机无法启动，因为没有数据可以写入。即使是典型的 ODIN 闪回股票或扎根股票也不能解决这个问题。使用 CWM 来刷新另一个 ROM 会产生同样的无法引导的结果。此外，库存恢复将不起作用，并且无法执行工厂重置。听起来很沮丧？确实是。

这大概概括了这个问题。谢天谢地，还有一个解决方案。用户被指示获取一些文件，然后使用 Odin 让手机再次工作。有趣的部分发生在奥丁闪光期间。通常，用户被告知除了自动重启和 f .重置时间外，不要勾选任何 Odin 框。这一次，有点不一样。在闪存过程的最后阶段，用户必须勾选*并在闪存最终文件之前擦除所有*框。从那里，这是一个简单的重新启动股票恢复一些工厂重置善良和手机应该是固定的。正如 PureMotive 所说:

> 恭喜你，你刚刚省下了 600 美元和一个打到威瑞森的电话。

要获得完整的指令和文件下载链接，请前往[原始线程](http://forum.xda-developers.com/showthread.php?t=1840030)。