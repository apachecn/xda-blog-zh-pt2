# 加速 ROM 或内核构建过程

> 原文：<https://www.xda-developers.com/speed-up-the-rom-or-kernel-build-process/>

创建内核、ROM 或任何其他开发项目都需要知识和工具。虽然这些知识可以从书本和其他资源中获得，但是工具必须从头开始创建。不是所有的，因为在 XDA 有很多有趣的项目与社区分享。

当你在构建一个 ROM 时，你需要执行一些命令来启动构建过程。手动输入行需要时间，并且很有可能会出现输入错误，不得不重复这个过程。XDA 论坛的主持人和公认的开发者 laufersteppenwolf 决定分享他的解决方案，展示一套脚本，让你加快几乎每个项目的准备过程。

提供的脚本旨在为 [LG Optimus 4X HD](http://forum.xda-developers.com/optimus-4x-hd) 构建一个基于 CyanogenMod 的 ROM、内核和 anykernel(一个不用接触内存磁盘的 zImage 替代品)。但是，可以很容易地修改它，为您的目标设备构建您选择的 ROM。这些脚本适用于每一个 Linux 发行版，并有适当的文档，可以通过添加“-h”标志来执行。

如果您是内核或 ROM 开发人员，或者只是想了解如何自动化构建过程，请查看[原始线程](http://forum.xda-developers.com/showthread.php?t=2722461)中提供的脚本。