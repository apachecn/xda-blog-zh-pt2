# 学会用 Unison 在 Android 和 PC 之间同步文件

> 原文：<https://www.xda-developers.com/unison-android-pc-sync/>

# 学会用 Unison 在 Android 和 PC 之间同步文件

本指南解释了如何使用 Unison 在 Android 设备和装有 Linux 的 PC 之间无缝同步您的文件。

如果你打算让你的文件在你的设备之间保持同步，Dropbox 和类似的云服务是很好的选择。像几乎所有事情一样，云同步也有利弊。然而一个主要的缺点是速度，因为你使用网络协议和传输来保持你的文件是最新的。

SSH 是云的最佳替代方案之一，它允许您管理 WI-Fi 网络中许多设备上的文件(或者几乎任何安装了 SSH 客户端的设备)。XDA 论坛成员 [Genericxx](http://forum.xda-developers.com/member.php?u=5369313) 决定分享他关于 SSH、共享和 Unison 文件同步器的知识，他写了一个指南，解释如何将你的 Android 设备与你的 PC 同步。Genericxx 专注于 Linux，bit Unison 是一个独立于平台的工具，可以在 OS X 和 Windows 上使用。

所描述的过程使用 SSH 和 SSHFS 来轻松地配对您的设备。Unison 将完成其余的同步工作，因此您只需连接您的设备并等待文件同步即可。它简单、快速，不需要任何电缆或外部设备。若要执行同步，您的设备必须是根设备。通过复制/system 分区来安装 mod 从未如此简单。在开始愉快地来回移动文件之前，请确保创建当前 ROM 的备份。

前往 [Setup 2way-sync over WiFi 使用 Unison 论坛线程](http://forum.xda-developers.com/android/general/guide-setup-2way-sync-wifi-using-unison-t2981737)了解更多信息。