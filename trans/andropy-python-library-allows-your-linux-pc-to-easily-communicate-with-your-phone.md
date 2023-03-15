# AndroPy Python 库允许您的 Linux PC 轻松地与您的手机通信

> 原文：<https://www.xda-developers.com/andropy-python-library-allows-your-linux-pc-to-easily-communicate-with-your-phone/>

当你得到一个新的 Android 设备时，你无疑是极其兴奋的。很有可能，你的一个朋友告诉了你这些所谓的“rom”，根访问，等等。但是你需要从某个地方开始，这就是你在 XDA 的旅程的开始。

对你们大多数人来说，使用亚行就像泡茶一样简单。然而，一些缺乏经验的人可能很难安装一个完全工作的 ADB 和 fastboot，尤其是在 Linux 上。当你想获得你的设备的日志或者只是简单地根它的时候，Android Debug Bridge 是必须的。

受 [JDroidLib](http://www.xda-developers.com/android/a-new-android-communications-library-jdroidlib-java/) 的启发，XDA 资深会员 [zantekk](http://forum.xda-developers.com/member.php?u=2314467) 写了一个 python 等价物，让你的手机/平板电脑和 Linux PC 之间的通信更容易。这个库仍处于早期开发阶段，所以没有多少东西工作。但是，您可以在 64 位版本的 Linux 上安装 ADB 二进制文件，并重启您的设备进行引导加载和恢复。它还可以执行更改权限等操作所需的 shell 命令。唯一的要求是安装一台(64 位)Linux 机器和 [Python 3](http://www.python.org/) 。

如果你是 Android 世界的新手，或者只是在寻找一些工具来让你的生活变得更简单，请前往[开发线程](http://forum.xda-developers.com/showthread.php?t=2563475)，找到更多关于 Android 开源[项目](https://github.com/tehmk/andropy)的细节。