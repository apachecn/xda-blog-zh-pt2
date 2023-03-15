# 轻松更改您的 Android SELinux 模式

> 原文：<https://www.xda-developers.com/easily-change-your-android-selinux-mode/>

除了 Android 4.4 KitKat 中添加的各种面向用户的功能外，谷歌还通过一系列关键变化(T3)显著增强了该平台的整体安全性(T2)。其中，一个关键的变化与 SELinux 有关，这是之前在 Android 4.3 中引入的。然而，Android 4.4 将 SELinux 的状态从许可模式转变为强制模式。

引用我们的安全专家 Pulser_G2 的话:

> **强制模式下的 SELinux**
> 
> 在 Android 4.4 中，SELinux 已经从许可模式(简单地记录失败)转变为强制模式。在 Android 4.3 中引入的 SELinux 是一个内置于 Linux 内核中的强制访问控制系统，目的是帮助实施现有的访问控制权限(*即*权限)，并试图防止权限提升攻击(*即*一个试图在您的设备上获得 root 访问权限的应用)。

虽然这在很大程度上对普通人来说是一件好事，但这种安全性增强也存在一些问题。例如，它破坏了一些支持 root 的应用程序，比如之前讨论过的终极动态导航条。

为了让用户能够轻松地在 SELinux 模式之间切换，XDA 资深会员 [MrBIMC](http://forum.xda-developers.com/member.php?u=4467676) 开发了名副其实的 SELinuxModeChanger 应用。应用程序(显然)需要 root 访问权限。一旦给定，该应用程序允许你切换 SELinux 状态，只需点击一下。一旦你做出选择，一个脚本将在启动时执行，将模式更改为你选择的模式。

自然，这款应用只能在安装了 SELinux 的设备上运行。换句话说，这只适用于运行 Android 4.3 Jelly Bean 或 4.4 KitKat 的设备。然而，值得注意的是，这还不适用于三星 KNOX 设备。然而，这是目前正在努力。

如果你想轻松地改变 SELinux 模式，并且你没有运行支持 KNOX 的 ROM，那就使用[应用程序线程](http://forum.xda-developers.com/showthread.php?t=2524485)试试这个应用程序。