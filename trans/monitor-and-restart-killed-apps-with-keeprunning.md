# 用 KeepRunning 监控并重启已关闭的应用程序

> 原文：<https://www.xda-developers.com/monitor-and-restart-killed-apps-with-keeprunning/>

通常来说，Android 的[进程生命周期](http://developer.android.com/guide/components/processes-and-threads.html#Lifecycle)是一件伟大的事情。进程生命周期并不允许应用无限期运行，而是定义了当系统需要新内存来容纳更新、更重要的应用时，旧进程会发生什么。这种行为通常是一件好事，除非其中一个被关闭的应用程序恰好是您希望保持打开的应用程序。

应用程序有几种方法可以解决这个问题。例如，如果一个应用程序在通知栏中放置了一个正在进行的通知，它将留在前台，不会被自动取消。但是，如果您希望保留其他应用程序呢？

幸运的是，XDA 资深成员 [defim](http://forum.xda-developers.com/member.php?u=4501300) 正是为了这个目的创建了 KeepRunning。虽然该应用程序不会阻止您的应用程序被杀死，但 KeepRunning 会监控您的应用程序，并在用户指定的监控时间间隔内重启多达三个您选择的应用程序。这对于容易崩溃的 messenger 应用程序非常有用，否则它们可能会在未打开时错过消息。

转到[应用线程](http://forum.xda-developers.com/showthread.php?t=2456612)开始。