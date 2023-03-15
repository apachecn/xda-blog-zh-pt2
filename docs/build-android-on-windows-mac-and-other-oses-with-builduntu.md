# 在 Windows 和 Mac 上构建 Android。和其他操作系统

> 原文：<https://www.xda-developers.com/build-android-on-windows-mac-and-other-oses-with-builduntu/>

创建一个 Android 版本是一个有趣的，但往往是困难的过程。首先你需要使用一个类似 UNIX 的 OS 比如 Linux 或者 Mac OS，并不是每个人都每天使用所说的 OS。有一个 Ubuntu 的原生设置很好编译，但是并不是所有人都知道 Android 也可以在 Windows 上运行。

Ubuntu、Windows 和基本上所有其他操作系统都可以在使用 VirtualBox 等应用程序的虚拟机上运行。系统映像是可以共享的，XDA 资深成员 [sylentprofet](http://forum.xda-developers.com/member.php?u=2645562) 已经做到了。sylentprofet 的方法中使用的操作系统是 Ubuntu 14.04 Trusty Tahr 的测试版，不久前,[在 XDA 门户网站](http://www.xda-developers.com/android/build-android-on-test-versions-of-ubuntu-14-04-trusty-tahr/)上介绍过它。

虚拟机上的操作系统已经清除了所有不必要的应用程序，并准备好编译 Android。剩下的唯一一件事就是初始化您最喜欢的 ROM 的存储库并执行 make 命令。

可以将映像导入能够运行 VirtualBox 的所有操作系统。但是请记住，你的电脑需要更多的物理能力来运行虚拟机上的系统，所以不要忘记调整 VirtualBox 中的参数。

让 Builduntu 工作的过程在它的[原始线程](http://forum.xda-developers.com/showthread.php?t=2585828)中描述。