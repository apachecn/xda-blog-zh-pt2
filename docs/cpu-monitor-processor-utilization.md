# CPU Monitor 会跟踪每个应用的处理器利用率

> 原文：<https://www.xda-developers.com/cpu-monitor-processor-utilization/>

# CPU Monitor 会跟踪每个应用的处理器利用率

CPU Monitor 可以让您跟踪每个应用程序/每个进程的 CPU 利用率，这样您就可以发现 Android 设备何时出现了问题。

由于我们都是超级用户，我们通常喜欢调整和监视我们的移动设备的过程。由于各种原因，这是有用的。例如，通过适当的设备状态监控，您可以找出为什么您的设备有时会过热，为什么您的电池会“神秘地”消失，或者许多其他潜在的问题。虽然找出大多数问题的根源需要更复杂的工具，如 logcat 或 wakelock 检测器，但许多发热和无响应系统的问题可以通过查看每个进程的 CPU 利用率来确定。

XDA 论坛成员 [cygnus.uvdb](http://forum.xda-developers.com/member.php?u=5365467) 提供了一个很棒的 CPU 监视器应用程序，它显示了在你的设备上运行的每个进程的列表，以及它的 CPU 利用率。Linux 和 Mac 用户会很快熟悉这个概念，因为它本质上与运行 *top* 命令查看实时统计数据是一样的。这些数据会被收集并显示在通知区域和应用程序的界面上。您还可以在可查看的流程中进行搜索，以及在应用程序中开始和暂停收集。最后，该应用程序相对较轻，在后台监控模式下消耗的 CPU 工作不到 1%，在正常操作下消耗 4-10%——但这显然会因设备而异。

如果你一直在寻找一个简单的 CPU 统计应用程序，让你总是用一个通知托盘图标来监视整体 CPU 利用率，那就去试试 [CPU Monitor 应用程序线程](http://forum.xda-developers.com/android/apps-games/app-cpu-monitor-cygnus-software-t2847333)吧！