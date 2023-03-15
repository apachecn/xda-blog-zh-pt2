# 轻松使用 Deodex Lollipop 系统应用

> 原文：<https://www.xda-developers.com/deodex-lollipop-system-apps-with-ease/>

Android 5.0 已经公开发布了一个多月了，虽然棒棒糖(T2)在市场渗透率方面没有太大的进展，但是这个操作系统在高级用户和开发者群体中已经有了很大的发展。我们已经看到了各种设备的大量端口，无论新旧，而且随着时间的推移，这种情况只会继续下去。

虽然 Lollipop 的大部分基础架构与以前的版本相同，但大部分已经改变。众所周知，很长一段时间以来， [Android 5.0 最终废除了 Dalvik，代之以 ART](http://www.xda-developers.com/android/breaking-next-major-version-of-android-to-finally-remove-dalvik-and-set-art-as-default/ "BREAKING: Next Major Version of Android to Finally Remove Dalvik and Set ART as Default!") 。虽然这在性能和电池寿命节省方面是一个了不起的举动，但它对某些类别的用户也有一些副作用。除了(目前)与 Xposed Framework 不兼容之外，Lollipop 转向 ART 还意味着解密系统应用程序必须以不同的方式进行。幸运的是，XDA 资深会员 [Tech N You](http://forum.xda-developers.com/member.php?u=5941042) 创建了一个快速指南，带你完成使用 Oat2dex 转换器解密棒棒糖应用程序和罐子的过程。

> 正如我们所知，在 Android 5.0 Lollipop 框架、app、priv-app 文件夹中我们有*。apk 文件和*。jar 文件，然后当您查看名为*的子文件夹时。odex 文件，他们有一个特定的文件夹，为艺术运行时，以压缩成两种模式。
> 
> * odex.art.xz ->将艺术模式转换为原生文件。
> 
> * .odex.xz -> 7zip *。解压文件时会出现 odex。
> 
> * .odex.xz 解压文件压缩，使用*。odex 文件。
> 
> 除非手臂被压缩成文件夹*。odex
> 
> 因此，为了对文件进行 deodex，我们需要这个 deodex 工具和您的 apk 以及*.odex.xz。

如果您一直在寻找一种简单的方法，只需通过[Lollipop deo dex guide for Windows thread](http://forum.xda-developers.com/android/software-hacking/guide-android-l-5-0-lollipop-deodex-t2967242)开始。