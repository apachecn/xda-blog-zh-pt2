# Init.d 支持任何根电话

> 原文：<https://www.xda-developers.com/init-d-support-for-any-rooted-phone/>

Init.d 在 Android 开发和定制领域扮演着重要角色，它允许用户安装脚本和 mod 以便在启动时运行——从电池调整到性能调整。它本质上打开了一扇通向 mods 世界的大门，只有通过 *Init.d* 进程才有可能，而这通常只能在定制内核上实现。

XDA 资深成员 [Ryuinferno](http://forum.xda-developers.com/member.php?u=4576707) 开发了一个脚本，允许在任何根手机上使用 *Init.d* 脚本，而不依赖于自定义内核。Term-init 只是一个在终端模拟器中运行的脚本，它将自动执行安装过程，并添加一些由开发人员提供的额外功能。完成后， *Init.d* 支持将是你的！

Ryuinferno 还创建了一种替代的实现方法，即使用一个名为 zip-init 的可闪存 Zip 文件，它以通常的方式安装在恢复中。

使用 Term-init 或 Zip-init 只需要您的根电话、Busybox 和一个终端模拟器应用程序。

如果你想在你的设备上得到 *Init.d* 的支持，就去找[开发线程](http://forum.xda-developers.com/showthread.php?t=1933849)。