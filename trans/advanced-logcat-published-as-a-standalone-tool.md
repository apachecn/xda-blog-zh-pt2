# 作为独立工具发布的高级 Logcat 查看器

> 原文：<https://www.xda-developers.com/advanced-logcat-published-as-a-standalone-tool/>

每个 Android 用户都曾遇到过应用程序或游戏崩溃的情况。然而，找到这些崩溃的原因是另一回事。Android 提供了自己的日志系统 logcat，它使用 ADB 来获取所有必要的信息，供开发人员分析和修复问题。

安装 android-sdk 并执行标准的 adb logcat 命令很容易，但是输出可能有点难以理解。XDA 认可的开发者 [Diamondback](http://forum.xda-developers.com/member.php?u=2295247) 写了一个方便的 Windows 工具来简化使用 logcats 的过程。

该应用程序易于使用，并提供了重要的功能，如日志突出显示，动态过滤，导出到文本文件，并上传到 pastebin。它还可以通过从文本文件中导入日志来帮助您分析其他用户的日志。

高级 Logcat 查看器最初是[良性十工作室](http://www.xda-developers.com/android/virtuous-ten-studio-becomes-self-aware-decompiles-skynet/ "Virtuous Ten Studio Becomes Self-Aware, Decompiles Skynet")的一部分，这是一个功能齐全的 IDE，用于 Android 上与逆向工程相关的一切。然而，为了降低 [VTS](http://forum.xda-developers.com/showthread.php?t=1619473) 的复杂性，响尾蛇决定将 VTS 的某些部分也作为独立版本发布。据开发商称，ALV 只是这些突破性功能中的第一个，还有更多功能要开发。

如果您正在使用 Windows，并且希望在分析 Logcat 时提高您的生产率，请访问[实用程序线程](http://forum.xda-developers.com/showthread.php?t=2454610),尝试一下高级 Logcat 查看器或[良性十工作室](http://forum.xda-developers.com/showthread.php?t=1619473)。