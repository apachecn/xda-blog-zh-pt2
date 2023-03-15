# 用于监控性能的“Systrace”Android Studio 工具将内置于 Android P

> 原文：<https://www.xda-developers.com/systrace-android-studio-tool-coming-to-android-p/>

# 用于监控性能的“Systrace”Android Studio 工具将内置于 Android P

Android 开源项目 Gerrit 中的新承诺表明，Android Studio 中内置的 Android 内核性能工具 systrace 可能会进入 Android P。

除非你是应用程序开发人员，否则你可能从来没有听说过 **systrace** 。它是“系统追踪”的缩写，是谷歌集成开发环境 [Android Studio](https://www.xda-developers.com/google-quick-boot-android-studio/) 中内置的一项功能。systrace 的目标是让开发人员能够收集和检查在给定设备上运行的所有系统级进程的计时信息，这对可视化系统资源使用非常有帮助。现在，有证据表明它正走向 Android P。

Android 开源项目 Gerrit 中的一项承诺表明，谷歌正在将 systrace 构建成 Android 的下一个主要版本。[正如我们在这里看到的](https://android-review.googlesource.com/q/project:platform/packages/apps/Traceur)，它将被添加为一个应用程序，出现在隐藏的开发者选项设置菜单中。经常使用它的开发人员会很高兴听到它也会以快速设置磁贴的形式出现。

systrace 生成的报告提供了给定时间段内 Android 设备系统进程的总体情况。它实际上并不收集关于应用程序进程中代码执行的信息 Android Studio 中还有其他工具(如 CPU profiler 或“生成跟踪日志”工具)可以显示应用程序正在执行哪些方法以及它使用了多少 CPU 资源。尽管如此，它在开发过程中仍然非常有用，因为它从 Android 内核收集数据，如 CPU 调度程序、磁盘活动和应用程序线程，并将其组合成一个方便的 HTML 报告。

开发人员可以利用它来查看工具运行时哪些资源正在被使用。Systrace 将检查捕获的跟踪信息，并突出显示它观察到的任何问题，包括(但不限于)显示运动或动画时的 UI jank。它甚至会提供如何解决问题的建议。

有一件事是肯定的:假设这个新的应用程序能够进入 Android P 的用户版本，它将是 bug 测试的福音。