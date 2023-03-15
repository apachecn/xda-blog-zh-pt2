# Android 13 将为 DSU 带来显著的性能提升

> 原文：<https://www.xda-developers.com/android-13-dsu-new-features-performance-improvements/>

动态系统更新( [DSU](https://www.xda-developers.com/android-11-dsu-loader-gsi-locked-bootloader-developers-test-apps-stock-android/) )是 Android 中最不为人知的功能之一，允许用户在不解锁引导加载程序或刷新系统更新的情况下安装通用系统映像(GSI)。该功能首次在 Android 10 中推出，是开发者测试最新 Android 版本的最简单方法之一。而且在 Android 13 中变得更好。

正如米沙·拉赫曼所指出的，DSU 将在 Android 13 中获得几个新功能和改进，包括性能大幅提升，加权进度条，以及对 system_ext 和产品图像的支持。

AOSP·格里特的新承诺表明，谷歌正在为 DSU 带来一些重大的性能改进。由于默认共享内存的增加，通过 DSU 安装 GSI 会快得多。谷歌指出，内存的适度增加(从 8KiB 到 64KiB)将大大加快物理和虚拟设备上的动态系统安装时间。谷歌的测试显示，安装时间从物理设备上的 2 分 2 秒缩短到了 45 秒。

提交的描述如下:

> 这一 8KiB-> 64kb 的适度调整显著提升了 DSU
> 
> 安装时间:
> 
> *物理设备:2m34s -> 45s
> 
> *虚拟设备:46 秒-> 30 秒
> 
> 还可以定制共享内存的大小以进行微调。

进度条也有了一些新的改进。当 GSI 安装正在进行时，通知区域中的进度条将显示正在安装哪个分区。目前，它只显示“正在安装”此外，进度条将被加权，因为只读分区比可写分区花费的时间长得多。

> 不要显示“正在安装”，而是显示正在安装的分区和分区总数，例如:“正在安装:系统分区[2/3]”

最后，DSU 将增加对系统、系统扩展和产品图像的支持。请注意，这些功能和改进并没有出现在 [Android 13 开发者预览版](https://www.xda-developers.com/android-13-developer-preview-2/)中。它们可能会在即将到来的测试版或最终版本的 Android 13 中发布。

* * *

**来源** : AOSP [ [1](https://android-review.googlesource.com/c/platform/frameworks/base/+/2033044) ，[ [2](https://android-review.googlesource.com/c/platform/frameworks/base/+/2045078) ，[ [3](https://android-review.googlesource.com/c/platform/frameworks/base/+/2044810) ，[ [4](https://android-review.googlesource.com/c/platform/frameworks/base/+/2044809/4) ]