# 索尼发布了如何为 Xperia 设备构建 Android 7.1 AOSP 的说明

> 原文：<https://www.xda-developers.com/sony-publishes-instructions-on-how-to-build-android-7-1-aosp-for-xperia-devices/>

索尼是为数不多的仍坚定相信 AOSP 的原始设备制造商之一。大多数公司都懒得提供必要的固件二进制文件来让开发者将 AOSP 移植到设备上。但是，尽管一些原始设备制造商确实为开发人员提供二进制文件来制作 AOSP 版本，就像我们在 OnePlus 3 上看到的一样，索尼却更进一步，确保 AOSP 在他们所有的设备上都能正常运行。虽然索尼的开放设备计划并没有扩展到它发布的每一个设备，但是他们发布的工作使得定制 ROM 开发者的生活变得非常非常容易，社区对此非常感激。

目前，[索尼已经公布了](http://developer.sonymobile.com/open-devices/list-of-devices-and-resources/) [Xperia X Compact](http://forum.xda-developers.com/x-compact) 、 [Xperia X](http://forum.xda-developers.com/xperia-x) 、 [Xperia Z5 Premium](http://forum.xda-developers.com/z5-premium) 、 [Xperia Z5](http://forum.xda-developers.com/xperia-z5) 、 [Xperia Z5 Compact](http://forum.xda-developers.com/z5-compact) 、 [Xperia Z3+](http://forum.xda-developers.com/xperia-z4) 、 [Xperia Z4 Tablet](http://forum.xda-developers.com/z4-tablet) 、 [Xperia Z3](http://forum.xda-developers.com/z3) 、[Xperia Z5](http://forum.xda-developers.com/z3-compact) [Xperia Z1](http://forum.xda-developers.com/xperia-z1) ， [Xperia Z1 Compact](http://forum.xda-developers.com/sony-xperia-z1-compact) ， [Xperia Z Ultra](http://forum.xda-developers.com/xperia-z-ultra) ， [Xperia Z](http://forum.xda-developers.com/xperia-z) ， [Xperia ZL](http://forum.xda-developers.com/xperia-zl) ， [Xperia 平板 Z](http://forum.xda-developers.com/xperia-tablet-z) ， [Xperia E3](http://forum.xda-developers.com/xperia-e3) ， [Xperia M2](http://forum.xda-developers.com/xperia-m2) ， [Xperia T2 Ultra](http://forum.xda-developers.com/t2-ultra) ， [Xperia T3](http://forum.xda-developers.com/xperia-t3) ， [请注意，每个设备支持的 Android 版本差异很大，因为列表中的许多设备都不支持 Nougat。](http://forum.xda-developers.com/xperia-l)

索尼也是唯一一家广泛参与 Android N 开发者预览版项目的原始设备制造商。他们之前发布了一份关于如何为他们各种支持的 Xperia 设备构建 Android 7.0 AOSP 的指南，本周末他们为新发布的 Android 7.1 牛轧糖开发者预览版做了同样的事情。请记住，只有在索尼的二进制资源页面上被列为支持 Android 7.0 的设备才有资格获得 Android 7.1 的早期版本。因为这是一个早期版本，所以请记住它目前被标记为**实验版**。本指南假设您运行的是 Ubuntu，因为本指南是使用 Ubuntu 14.04 LTS 版制作的，但它在其他 Linux 发行版上的工作方式类似。

该指南首先让您准备 Java 环境，然后让您安装必要的工具来构建 Android，然后让您下载 Repo 工具并设置路径。然后，该指南引导您初始化 AOSP 树，添加来自 AOSP 上游分支的必要补丁，然后说明如何为 Android 7.1 牛轧糖构建 AOSP 映像，以便可以将它们闪存到设备上。

请务必[查看索尼 Xperia 开发者 GitHub 页面](https://github.com/sonyxperiadev)并尽你所能做出贡献。

[**来源:索尼移动开发者世界**](http://developer.sonymobile.com/open-devices/aosp-build-instructions/how-to-build-aosp-nougat-for-unlocked-xperia-devices/#build-experimental-aosp-nougat-7-1)