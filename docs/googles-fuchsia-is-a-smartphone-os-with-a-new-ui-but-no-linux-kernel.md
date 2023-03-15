# 谷歌的 Fuchsia 是一款智能手机操作系统，有新的用户界面，但没有 Linux 内核

> 原文：<https://www.xda-developers.com/googles-fuchsia-is-a-smartphone-os-with-a-new-ui-but-no-linux-kernel/>

按照谷歌的惯例，如果它存在，[肯定不止一个。玩笑归玩笑，谷歌似乎不仅对开发和维护 Android 和 Chrome 操作系统作为可行的主流操作系统非常感兴趣，而且他们也在考虑以](https://www.xda-developers.com/how-allo-and-duo-want-to-complicate-messaging-by-fracturing-the-market/) [Fuchsia](https://fuchsia.googlesource.com/) 的形式开发另一个操作系统。

Fuchsia 最后一次被谈论是在 2016 年 8 月，但是这个操作系统还处于雏形，刚刚成型。从那以后，谷歌一直在努力工作，尽管是小心翼翼地，赋予这个羽翼未丰的操作系统更多的内容。

Fuchsia 是谷歌的新开源操作系统，不使用 Linux 内核。相反，Fuchsia 使用谷歌开发的名为 [Magenta](https://github.com/fuchsia-mirror/magenta) 的微内核。 [Magenta 内核遵循](https://github.com/fuchsia-mirror/magenta/blob/master/LICENSE)一个麻省理工风格的许可，允许其他人对代码做任何他们想做的事情(包括修改、分发和保持所述修改的私有性)，只要原始许可在衍生产品中的某个地方可用。

Magenta 是支持 Fuchsia 操作系统的核心平台。Magenta 由一个微内核(内核中的源代码/...)以及一小组用户空间服务、驱动程序和库(来源于 system/...)是系统引导、与硬件对话、加载用户空间进程并运行它们等所必需的。Fuchsia 在此基础上构建了一个更大的操作系统。Magenta 的目标是现代手机和现代个人电脑，它们配有快速处理器、大量 ram 以及进行开放式计算的任意外设。

这与 Android Linux 内核上的 GPL v2 相比是一个明显的变化，如果修改者(通常是原始设备制造商)修改和发布代码的任何部分，他们就有义务开放源代码。根据你站在哪一边，你可以争论选择许可和背离 Linux 内核是好是坏。

操作系统的其他部分是单独许可的，通常是根据 BSD License 2.0、Apache 2.0 和 MIT 单独许可的。

[*Ars Technica* 指出](https://arstechnica.com/gadgets/2017/05/googles-fuchsia-smartphone-os-dumps-linux-has-a-wild-new-ui/)Fuchsia 上的界面和应用程序是使用谷歌的 [Flutter SDK](https://flutter.io/) 编写的，该项目能够生成可以在 Android 和 iOS 上运行的跨平台代码。Flutter 应用程序是用 Dart 编写的，Dart 是谷歌的内部 Web 开发语言，专注于移动设备上的高性能应用程序。Fuchsia 也有一个基于 Vulkan 的图形渲染，名为 [Escher](https://github.com/fuchsia-mirror/escher) ，Ars Technica 提到它似乎是为运行谷歌的阴影重材质设计 UX 而定制的。

由于 Fuchsia 的界面是用跨平台的 Flutter SDK 编写的，因此可以在 Android 设备上运行 Fuchsia 的部分功能。揭示了[如何构建犰狳](http://www.hotfixit.net/single-post/2017/05/03/How-to-build-Armadillo)，基本上是一个演示应用程序，展示 Fuchsia 的 SystemUI 是什么样子。你可以下载 Fuchsia 的源代码，将 Fuchsia 的 SystemUI 编译成 Android apk，并安装在你的设备上。如果你不想走那条路，也不想等人来编译和发布它，*Hotfix.net*很友好地提供了一个界面演示视频:

由于 SystemUI 由许多处于不同开发阶段的组件的占位符组成，到目前为止，您还不能对 SystemUI 做太多事情。Fuchsia 的主屏幕目前由一个垂直滚动的列表组成，中间有一个信息窗口，显示日期、你所在的城市和你的个人资料图片。这个小部件上面是最近的应用程序，滚动到这个小部件下面会显示类似 Google Now 的建议，这些建议目前只是占位符。点击这个小工具会在一定程度上引发对 Android 快速切换的重新想象。

Armadillo UI 还具有多任务功能，比目前在 Android 上看到的窗口管理更好。有很多方法可以排列应用程序，包括同时打开四个应用程序，甚至采用选项卡式界面。犰狳 UI 还采用了 Fuchsia 的键盘和新的黑暗主题。

* * *

显而易见，Fuchsia 作为一个操作系统仍然处于初级阶段。人们只需要看一眼 Android 就可以意识到制作一个操作系统并对其进行改进需要付出多少努力，这反过来会让你估计 Fuchsia 作为一种“大众产品”在未来有多远。

由于谷歌也对整个操作系统及其进展保持沉默，因此很难估计这个操作系统的未来，如果它真的有未来的话。Ars Technica 援引 Fuchsia 开发商 Travis Geiselbrecht 的话说:

> [Fuchsia]不是一个玩具，不是一个 20%的项目，不是一个我们不再关心的死东西的垃圾场。

虽然开发者坚持认为 Fuchsia 不仅仅是暂时的，但不幸的是，谷歌(和 Alphabet)的善变本性是众所周知的。

Ars Technica 推测，该操作系统在目前的状态下似乎很像 Android 的一个新分支，谷歌正在修复其早期和基础错误，并利用其多年来获得的大量经验来构建世界上最受欢迎的智能手机操作系统。有了 Fuchsia，Google 可以从一开始就成功地将自己从 Linux 内核和 Java 中分离出来——这在目前的 Android 中是非常非常困难的任务。

倒挂金钟的未来令人兴奋。这可能是下一件大事，你可以在它成为下一件大事之前体验它。关于如何构建 Fuchsia 的 Armadillo UI 以在 Android 上试用的说明，请跟随[*Hotfix.net*的简要指南](http://www.hotfixit.net/single-post/2017/05/03/How-to-build-Armadillo)。你也可以在 [Github](https://github.com/fuchsia-mirror) 或 [GoogleSource](https://fuchsia.googlesource.com/) 查看 Fuchsia 的源代码。

**你对 Fuchsia 和它的 Armadillo UI 有什么想法？你认为 Fuchsia、Android 和 Chrome 操作系统的未来会怎样？请在下面的评论中告诉我们你的想法！**

[**来源 1:Hotfix.net**](http://www.hotfixit.net/single-post/2017/05/03/How-to-build-Armadillo)[**来源 2: Ars Technica**](https://arstechnica.com/gadgets/2017/05/googles-fuchsia-smartphone-os-dumps-linux-has-a-wild-new-ui/)