# Android 调试桥初学者指南

> 原文：<https://www.xda-developers.com/beginners-guide-to-the-android-debug-bridge/>

我们这里的大多数人已经非常熟悉 ADB (Android 调试桥)。见鬼，我甚至敢打赌，我们很多人都经常使用它——*ADB 推送* ing 和*拉取* ing 文件， *adb 重启* ing，运行 shell 命令，等等。然而，大多数新用户还没有这样的经历。让我们面对现实吧:对于在 GUI 出现和普及之后出生的年轻人来说，命令行界面可能相当吓人。因此，如果你是一个经验丰富的老手，对亚行了如指掌，这篇文章不适合你。但是如果你是一个新用户，想对这个伟大的工具有更多的了解，请继续阅读！

Android Debug Bridge 是 Android SDK 的一部分，它允许桌面计算机和目标设备之间的通信。那么你能用亚行做什么呢？相当多。如前所述，您可以将文件从客户端 PC 推送到设备，将设备从设备拉送到客户端 PC，您可以重新启动(到 Android、引导加载程序或恢复)，记录 logcat，获得错误报告，执行许多标准 Linux 命令，等等。

对于新用户来说，最大的问题是知道可以执行什么命令，以及记住正确的语法。幸运的是，这些命令及其语法都很容易理解。例如，看看以下命令的正确语法:

*   adb start-server:该命令启动桌面计算机上的 adb 守护程序，并允许您的计算机与您的设备进行交互。注意，这个命令不是必需的，因为执行任何其他 ADB 命令都会自动启动守护进程。
*   adb kill-server:如你所料，这会杀死 adb 守护进程。
*   adb logcat:这会生成一个 [logcat](http://www.xda-developers.com/android/learn-to-use-a-logcat-to-diagnose-and-fix-your-issues/ "Learn to Use a Logcat to Diagnose and Fix Your Issues") ，这在找出哪里出错时非常有用。您可以使用>将输出重定向到一个文本文件中。例如，您可以键入“adb logcat > logcat.txt”将您的 logcat 记录为 logcat.txt。
*   adb 错误报告:生成一个简单的错误报告。就像 logcat 一样，您可以使用“>”将它重定向到一个文本文件中
*   adb 安装<local apk="" name="">:将 APK 从你的桌面电脑直接安装到你的设备上。</local>
*   adb pull  <destination path="" and="" filename="">:拉取指定的文件，存放到指定文件夹中指定的名称。</destination>
*   adb push  <destination path="" and="" filename="">:功能与 adb pull 类似，但方向相反。</destination>

然而，以上所述并不全面。这些只是您将会遇到的一些更常见的命令。

对于那些希望学习更多知识的人，或者那些只想看到这些命令在运行中的可视化输出的人，XDA 认可的贡献者 [doctor_droid](http://forum.xda-developers.com/member.php?u=4923920) 创建了一个基本指南，涵盖了初学者需要知道的一切，以便通过 ADB 完成基本任务。

Doctor_droid 还包含了一个 Windows 用户所需的 ADB 二进制文件的直接链接，这样您就不必为了启动和运行 ADB 而下载 SDK。虽然安装过程严格适用于 Windows 用户，但本指南的其余部分同样适用于 Linux 和 Mac 用户。

如果你是一个新用户，想要学习更多关于 ADB 的知识，或者即使你是一个经验丰富的兽医，想要确保你知道所有的常用命令，请前往[指南线程](http://forum.xda-developers.com/showthread.php?t=2266638)了解更多。