# 稳定的 Linux 应用程序支持有望在 Chrome OS 版本 69 中推出

> 原文：<https://www.xda-developers.com/stable-linux-apps-chrome-os-69/>

Chromebooks 上运行 Linux 应用程序的能力将在 Chrome OS 版本 69 的稳定和测试频道上提供，但这并不意味着 Crostini 项目开发的结束。一个[最近提交](https://chromium.googlesource.com/chromium/src.git/+/2dd076606271402aa23c4562a721996f79b0776c)确认测试版和稳定版频道的时间表更新。版本已经从 68 版推迟到 69 版，预计在九月中旬(稳定版)登陆[。在此之前，Linux 应用程序只能在开发者或金丝雀频道上为 Chromebooks 提供。](https://www.chromium.org/developers/calendar)

虽然这给大联盟带来了期待已久的 Linux 应用程序功能，但预计在 69 年后的几个月里会有功能更新和精简。

## 发布时会发生什么

release 69 的稳定发布将带来大量的错误修复和功能改进，但 Chrome 上 Crostini 体验的三个最大变化(在我们看来)是:

**Files app 和 Linux 集成-** 这是一项关键功能，将[使 Chrome OS 上的 Linux 体验无缝衔接](https://www.xda-developers.com/chromebook-files-app-redesign-android-linux-apps/)。除了使管理文件变得更容易，文件应用程序集成的改进将意味着那些大量使用 Linux 环境的人的工作流程更加顺畅。例如，你可以在 Chromebook 上轻松地将你在 Android Studio 中编写的应用程序加载到你的本地 Android 环境中。

**USB 接入** -想要将 USB 外设连接到您的 Linux 容器吗？也许你更喜欢 Linux 环境下的 ADB，而不是通过开发者模式启用它的[。Chrome OS 开发者正在努力实现 USB 访问，你可以通过在 Chromium bugtracker](https://www.xda-developers.com/adb-fastboot-chromebook-chrome-os/) 中关注[这个问题来跟踪。](https://bugs.chromium.org/p/chromium/issues/detail?id=831850)

**音频和声音支持** - Linux 应用程序用户目前被剥夺了这种感官体验。没有这个关键的功能，任何版本都不能被称为稳定的。这个问题的目标是在 69 版中解决，但是你可以[跟踪开发者的进度](https://bugs.chromium.org/p/chromium/issues/detail?id=851185)。

## 等待什么

Crostini 项目的 Chromium bugtracker 中有几十个 bug，从小型到大型都有。我们挑选了三个备受期待的特性，我们*不期望它们能在稳定版发布前准备好。*

**GPU 加速** -图形和 GPU 工作负载的硬件加速将对游戏、软件开发和视频播放等一系列应用非常有用。这是一个复杂的问题，对于 Chrome OS 在其设备家族中的众多架构和内核版本来说，可能会进展缓慢。你可以[在 bugtracker 上跟踪这个特殊的问题](https://bugs.chromium.org/p/chromium/issues/detail?id=837073)。

**云同步和备份** -开发环境支持对您拥有的虚拟机进行自动快照和备份是有意义的。想象一下，在一个企业环境中，你可以登录到任何一台 Chrome 设备，从谷歌硬盘上下载你的虚拟机。Chrome 开发者[意识到了这个潜在的](https://chromium.googlesource.com/chromiumos/docs/+/master/containers_and_vms.md#Are-my-VMs_containers_data-synced_backed-up)，但是还没有发现任何需要追踪的错误。

**支持 FUSE 文件系统**——开发者已经认识到了原生 FUSE 支持的[优势，但是还没有任何进展。支持 FUSE 将允许用户以一种用户友好的方式挂载和操作远程和本地文件系统，这将是开发人员社区的一大福音。](https://bugs.chromium.org/p/chromium/issues/detail?id=841787)[这里是](https://bugs.chromium.org/p/chromium/issues/detail?id=841787)。