# AOSP 7.1.2 的艺术子模块为牛轧糖自定义 rom 增加了曝光功能

> 原文：<https://www.xda-developers.com/art-submodule-for-aosp-7-1-2-adds-xposed-functionality-to-custom-roms/>

Xposed Framework 是最受欢迎的 Android 修改之一，因为它允许用户安装将特定功能添加到当前固件的模块。这需要大量的工作，这也是为什么在 Android 的一个新的主要更新发布后，XDA 资深公认开发者需要这么长时间来开发。

社区一直在呼吁一个更新，增加了 Android 7.0 牛轧糖的兼容性，现在看起来有一个方法。

现在，这不是传统的 Xposed 框架安装，它需要在自定义恢复中刷新，并且可以添加到各种设备中。相反，已经为 AOSP 7.1.2 创建了一个独特的艺术子模块，**支持开箱即用的自定义 ROM 的 Xposed 框架功能**。这种方法有其优点和缺点，因为它不能安装在当前的 ROM 上，用户或维护人员需要通过采用这些更改来编译支持 Xposed 的 ROM。

官方 Xposed 框架的一大部分工作是通过修改安装它的 ROM 的一部分来使它正确地安装在所有设备上(如果您还记得，这是唯一需要 root 的步骤)。简而言之，这种非官方方法通过在构建 ROM 时进行所需的更改来消除所有这些问题，这是通过将修改后的子模块添加到定制 ROM 的构建过程中来实现的。类似于[底层如何在没有根](https://www.xda-developers.com/substratum-to-work-on-custom-roms-without-root-soon/)的定制 ROM 上使用，这将向定制 ROM 本身添加暴露的功能。也就是说，你需要你当前的定制 ROM 维护者通过在 AOSP 源代码树中添加/放置 ART 子模块来增加对这个方法的支持，然后从头开始构建整个 ROM。

然后，定制 ROM 维护人员需要用修改后的框架替换原来的框架/base/cmds/app_process [，创建一个预构建的模块，将 XposedBridge.jar 复制到 system/framework，然后更新 build/target/product/base.mk 以包含 libxposed_art 和 XposedBridge。因此，虽然这种方法不会让*所有人*满意，因为它不能直接安装到你当前的 ROM 上，但它确实在过去可能的基础上增加了一些好处。早期的报告表明，各种模块也可以兼容。](https://github.com/abforce/xposed_app_process)

我们只需要看看定制的 ROM 维护者是否会将这种支持添加到他们当前的版本中。对于那些正在寻找更详细解释的人，请务必[阅读 GitHub 上的 readme.md。总的来说，这可能是 Nougat 用户体验和使用 Xposed 的一个很好的变通方法，允许新手机访问一系列模块。](https://github.com/abforce/xposed_art_n/blob/master/README.md)

* * *

[**来源:GitHub**](https://github.com/abforce/xposed_art_n)