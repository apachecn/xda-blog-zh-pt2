# 使用 Android 代理库检测应用程序中的代理设置

> 原文：<https://www.xda-developers.com/detect-proxy-settings-in-your-app-with-android-proxy-library/>

多年来，将 Android 设备连接到代理服务器的过程发生了巨大的变化。最初仅支持全局配置，现在可以基于每个接入点设置配置。此外，OpenVPN 等应用程序可以在运行冰激凌三明治及更高版本的设备上全球运行。

那么，如果您正在构建一个应用程序，并且希望了解用户的代理配置，该怎么做呢？到目前为止，这将是一项相当困难的任务。幸运的是，XDA 论坛成员 [lechuckcaptain](http://forum.xda-developers.com/member.php?u=3389519) 已经经历了这些麻烦，所以你不必再经历了。他创建了一个库来为您完成这项工作，无论用户的 Android 版本支持从 1.x 到 4.x。该库从确定当前代理配置开始，但现在已经发展到确定代理状态和其他相关信息。

前往[库线程](http://forum.xda-developers.com/showthread.php?t=2413129)并访问[lecchuckcaptain 的 Github](https://github.com/shouldit/android-proxy-library) 开始吧。