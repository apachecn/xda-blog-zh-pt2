# 谷歌的增量 FS 让你在完全下载前玩大型游戏

> 原文：<https://www.xda-developers.com/google-incremental-file-system-android-big-games/>

根据市场研究公司 [*Newzoo*](https://newzoo.com/insights/articles/newzoo-adjusts-global-games-forecast-to-148-8-billion-slower-growth-in-console-spending-starts-sooner-than-expected/) 的数据，移动游戏是一个巨大的市场，其总收入占 2019 年全球游戏市场的近一半。Play Store 每周都有大量新游戏可供尝试，如果您的游戏时间有限，这可能会很难跟上。谷歌正在为未来版本的 Android 开发新的文件系统，可能是 2021 年的 [Android 12](https://www.xda-developers.com/android-12/) ，这将使尝试新游戏更加容易。该文件系统被称为增量文件系统，它被设计为允许在应用程序的二进制文件和资源文件仍在下载的同时执行应用程序。

2019 年 5 月初，谷歌[提交了补丁](https://lwn.net/Articles/787606/)，将对增量文件系统的支持合并到 Linux 内核中。[根据 Google 提交的文档](https://lore.kernel.org/linux-fsdevel/20190502040331.81196-1-ezemtsov@google.com/T/#Z2e.:..:20190502040331.81196-2-ezemtsov::40google.com:0Documentation:filesystems:incrementalfs.rst)，Incremental FS 是一个“特殊用途的 Linux 虚拟文件系统，它允许在程序的二进制文件和资源文件仍在通过网络、USB 等被缓慢下载时执行程序。”这个特性的目的是“允许在二进制文件和资源完全下载到 Android 设备之前运行大型 Android 应用程序。”现在，如果你想玩一个 5GB 大小的 Android 游戏，你必须等到整个下载完成后才能启动游戏。谷歌表示，增量 FS 可以“无摩擦地等待(暂时)丢失的数据”，这意味着当它继续下载越来越多的完整游戏时，你可以启动游戏。在我们假设的 5GB Android 游戏中，假设游戏的 intro 大小为 200MB，偏移量为 1GB。使用增量文件系统，可以下载游戏的第一个 MB 的数据，当它被执行时，该过程可以调用 1GB 偏移量的第一个 MB 的数据来下载，从而允许开始介绍。然后，剩下的 200MB 介绍数据可以被下载，这将有望比介绍播放得更快，然后游戏的主菜单可以被加载。当需要加载下一组数据时，可能会有一个小的执行冻结。该菜单位于 150MB 的偏移量，但这将允许用户更快地进入游戏，而不是等待整个下载完成。

在向 Linux 内核提交补丁之后，Google 与多个 Linux 内核维护者就 FS 的实现和目的进行了讨论。一些人批评 Google 创建了一个定制的内核文件系统，而不是扩展现有的 FUSE，或者用户空间中的文件系统。谷歌称[基于 FUSE 的文件系统为其目标场景增加了显著的性能开销](https://www.xda-developers.com/diving-into-sdcardfs-how-googles-fuse-replacement-will-reduce-io-overhead/)，增加了功耗，以至于手机消耗能量的速度超过了通过电线充电的速度。这是有问题的，因为一个谷歌人说“项目的目标是允许从开发环境到 Android(手机)的即时应用部署。”基于这个评论，我们认为 Google 只是打算用这个特性来帮助开发者测试他们手机游戏的增量版本。然而，在对最初的 Linux 内核补丁进行最后一次评论几个月后，情况可能仍然如此，谷歌[开始将与增量文件系统相关的](https://android-review.googlesource.com/q/incremental)提交合并到安卓开源项目(AOSP)。这些提交给 Android 和 Android 的 Linux 内核的许多部分带来了巨大的变化，所以我们认为谷歌可能正计划使用增量文件系统来改善总体用户体验。也许谷歌想让用户开始玩大型安卓游戏，而不必完全下载——本质上是作为原生的[即时应用](https://www.xda-developers.com/tag/instant-apps/)的替代品，不需要开发者做任何额外的工作，因为实现是在内核中。

目前，谷歌正在 Pixel 4 XL (coral)上测试该功能[，他们还](https://android-review.googlesource.com/c/platform/system/sepolicy/+/1234498)[构建了一个内核模块](https://android-review.googlesource.com/c/kernel/common/+/1222873)，用于通用内核映像(GKI)。在一些评论中，谷歌解释说，具有这一功能的 Android 设备将有一个新的/data/incremental 目录，其中包含设备上每个应用程序的子目录。子目录将包含 apk、本地库和 OBB 文件。在这些子目录中，将挂载增量文件系统，并且每个子目录都将被绑定挂载到原始安装目录，即。/data/app/。谷歌 Play 商店[将能够检查安装在增量 FS 上的应用程序的文件签名](https://android-review.googlesource.com/c/platform/system/sepolicy/+/1234499)，这将可能阻止具有与当前安装的应用程序不同的签名的增量应用程序的执行。

鉴于这项功能的工作仍在进行中，Android 11 主要功能变化的内部截止日期可能很快就会到来，如果尚未过去，我们怀疑设备不会在 2021 年 Android 12 之前开始支持增量文件系统。我们将继续跟踪这项功能的发展，当然，如果我们对它的工作原理有了更多的了解，我们会及时更新。

* * *

感谢 XDA 知名开发商 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 和 [luca020400](https://forum.xda-developers.com/member.php?u=5778309) 的投入！