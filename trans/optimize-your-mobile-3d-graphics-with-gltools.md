# 使用 GLTools 优化您的移动 3D 图形

> 原文：<https://www.xda-developers.com/optimize-your-mobile-3d-graphics-with-gltools/>

你可能还记得几年前，我们[快速浏览了一下 Chainfire3D](http://www.xda-developers.com/android/take-control-of-all-aspects-of-your-devices-3d-rendering-subsystem-with-chainfire3d/ "Take Control of All Aspects of Your Device’s 3D Rendering Subsystem with Chainfire3D!") 。对于那些不记得的人，Chainfire3D 允许用户调整 3D 渲染路径的各个方面，如纹理大小和质量。由于其插件系统，该应用程序还允许用户加载其他设备的游戏。

不幸的是，由于 Android 3.0 及以上版本中使用的渲染路径发生了巨大变化，Chainfire3D 无法再在现代设备上使用。幸运的是，有一个选项带来了 Chainfire3D 的大部分功能，以及一些新的技巧。

由 XDA 论坛成员 [n0n3m4](http://forum.xda-developers.com/member.php?u=4246628) (并由公认的贡献者 [Hammer_Of_The_Gods](http://forum.xda-developers.com/member.php?u=2920816) 发布到论坛)开发的 GLTools 允许用户在每个应用程序和系统范围的基础上控制他们的 3D 渲染管道的许多方面。该应用程序允许用户更改任何应用程序的渲染分辨率、位深度、纹理压缩等。它还允许您动态优化着色器，并启用抗锯齿以提高质量。

使用 GLTools，您甚至可以伪造各种报告的 GL 标志，如 *GL_VENDOR* ，以便玩不是为您的设备设计的游戏。但与使用 Chainfire3D 的插件不同，这款应用实际上没有添加任何额外的专有扩展。相反，它只能更改报告的硬件功能。也就是说，有许多游戏会任意限制哪些设备可以访问哪些功能，因此这种能力肯定可以派上用场。

如果你想在你的 Android 设备上调整 3D 渲染管道，那就去[应用线程](http://forum.xda-developers.com/showthread.php?t=2615514)试试 GLTools 吧！