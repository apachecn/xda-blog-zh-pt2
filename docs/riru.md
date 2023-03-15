# 什么是 Riru，你能在你的 Android 设备上用它做什么？

> 原文：<https://www.xda-developers.com/riru/>

在 Magisk 成为现实之前，是 [Xposed Framework](https://www.xda-developers.com/best-xposed-modules/) 极大地塑造了与设备无关的 Android 建模方法。我们可以在运行时使用 Xposed 和一个专门构建的模块来替换任何类中的任何方法，而不必反编译应用程序、修改代码、重新编译并将修改后的文件推回到我们的设备中。该框架本质上是对`/system/bin/app_process`的修改，以在启动时加载额外的 JAR 文件，这允许开发人员挂钩到 [Zygote 进程](https://developer.android.com/topic/performance/memory-overview)，并可以在其上下文中操作。

由于 Magisk 提供了基于覆盖的修改机制(通常被称为“无系统”)，理论上可以创建一个 Magisk 模块来修改 Zygote 进程，而无需物理修改`app_process`可执行文件。这就是 Riru 的用武之地。

## Riru 是什么？

Riru 由两名名为[立夏](https://github.com/RikkaW)和[御锦城 08](https://github.com/yujincheng08) 的开发人员创建，是一个特制的 [Magisk 模块](https://www.xda-developers.com/best-magisk-modules/)，它提供 Xposed 式的功能，而不需要安装老式的 Xposed 框架。它注入到 Zygote 中，以便允许其他模块在应用程序或系统服务器中运行它们的代码。

## Riru 是如何工作的？

Riru 的最初实现依赖于一个名为`libmemtrack`的特殊系统库的替换。然而，这种方法后来被放弃了，取而代之的是一种被称为“本机桥”(`ro.dalvik.vm.native.bridge`)的系统属性。通过利用该属性，开发人员可以动态加载和卸载他们选择的共享库，这最终会导致注入到 Zygote 流程中。

## 如何下载安装 Riru？

如前所述，Riru 作为 Magisk 模块提供。由于 Magisk 应用程序不再附带内置的模块浏览器，您需要直接从其 GitHub 存储库中下载 Riru。

**[下载日如](https://github.com/RikkaApps/Riru/releases/latest)**

下载发布 ZIP 文件后，您可以使用 Magisk 应用程序安装它。

1.  如果你是在 PC 或 Mac 上下载，那么将你的 Android 设备连接到它，并将下载的 ZIP 文件复制到目标设备的内存中。
2.  打开手机上的 Magisk 应用程序，使用底部导航菜单切换到*模块*选项卡。
3.  点击名为*从存储器*安装的按钮。
4.  浏览并选择您先前下载的模块 ZIP。
5.  Magisk 现在将安装该模块，并提示您重新启动。

如果一切正常，重启后你可以看到 Riru 列在 Magisk 应用程序的*模块*标签下。

## 我能拿 Riru 怎么办？

Riru 本身只是一个让其他模块与合子进程挂钩的入口。因此，您需要通过 Magisk 应用程序安装 Riru 兼容的模块，就像任何其他 Magisk 模块一样。但是，有些模块可能与最新的 Riru 版本不兼容。因此，您必须在安装之前验证模块的 Riru 版本依赖性。

成功安装后，Riru 模块将在 Magisk 应用程序中与 Magisk 模块并列。然后，您可以打开特定于模块的配置前端来修改其参数。对于没有接口的模块，你可以简单地继续使用你的修改过的 Android 实例，Riru 会在后台处理一切。

请记住，由于特定的 SELinux 规则实现，一些库存和定制 rom 与 Riru 开箱即用[不兼容。](https://github.com/RikkaApps/Riru/wiki/Explanation-about-incorrect-SELinux-rules-from-third-party-ROMs-cause-Riru-not-working)

## Riru 和 Zygisk 有什么区别？

在较新版本的 Magisk 上，由于 Zygisk 的存在，您可能会遇到 Riru 在安装后被禁用的情况。

然而，这种冲突背后的原因很简单。Zygisk(如 Zygote 中的 Magisk)是 Riru 的精神继承者。这是无系统界面的演变，XDA 高级认可的开发人员 [topjohnwu](https://forum.xda-developers.com/m/topjohnwu.4470081/) (即 Magisk 的创造者)和其他几个开发人员已经工作了一段时间。由于 Riru 和 Zygisk 都以 Android Zygote 进程为目标，所以这两者在默认配置下不能同时存在。但是，您可以从 Magisk 的设置中禁用 Zygisk，重新启动设备，然后启用 Riru。

事实上，Riru 的维护者不久前就停止了这个项目的开发。他们建议模块开发者将来转用 Zygisk。然而，Zygisk 仍处于萌芽阶段，有很大的改进空间，因此迁移需要时间。同时，您可以继续使用 Riru 及其模块。