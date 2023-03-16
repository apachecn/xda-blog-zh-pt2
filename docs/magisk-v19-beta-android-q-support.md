# Magisk v19 beta 带来了无图像 Magisk、Android Q 支持等等

> 原文：<https://www.xda-developers.com/magisk-v19-beta-android-q-support/>

Magisk 可能是最近一段时间发布的最伟大的 Android 相关 mod 之一。目前，它是最广泛使用的根解决方案，但它也是一个无系统的接口，允许 Magisk 模块实现的无数可能性。Magisk 的无系统特性也允许它安装在来自不同制造商的大量不同设备上。但是也有例外，[因为更新的设备](https://www.xda-developers.com/exynos-samsung-galaxy-s10-rooted-magisk/)以及更新的软件可以改变事物的工作方式，从而破解 Magisk。这些怪癖通常会很快得到解决，Magisk 的最新测试版就是证明。

Magisk v19.0 作为主要版本的规范，为确保每个人在使用 Magisk 时都有相同的稳定体验，对底层工作方式进行了一系列重大更改和改进。v19 中最大的改进可能是无图像 Magisk。以前，所有模块都存储在 EXT4 映像中，该映像在引导时循环挂载。虽然这种方法在大多数设备上运行良好，但这可能会导致在某些设备上安装模块的问题，特别是一些使用 F2FS 的设备。模块现在直接安装在/data 分区中，确保了每个人的兼容性。

其他改进包括 MagiskHide 的重新设计方法(现在基于 zygote ptrace-ing)，在 Google Pixel 和 Pixel 2 上对 Android Q 的完全支持(Pixel 3 设备尚不支持，因为 Magisk 目前不支持 Android Q 引入的逻辑分区)，原生 64 位支持等等。如果你想了解 v19 的全部细节，现在就把它下载到你的设备上，但是请记住，它是一个测试版，因此，它可能会有一些错误——考虑到它是如何给整个界面带来重大变化的，如果你不希望事情发生变化，等待可能是更明智的。或者，你可以[在这里](https://github.com/topjohnwu/magisk_files/blob/6378e4404ceb89979d367bcc4687d673aa02c927/notes.md)查看完整的 [变更日志。](https://github.com/topjohnwu/magisk_files/blob/6378e4404ceb89979d367bcc4687d673aa02c927/notes.md)

[**立即查看 Magisk v19！**](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)