# 三星 Galaxy Note 9 的三星 DeX Linux 操作系统

> 原文：<https://www.xda-developers.com/hands-on-linux-on-samsung-dex-samsung-galaxy-note-9/>

当[三星 DeX 第一次与三星 Galaxy S8 一起推出](https://www.xda-developers.com/a-look-at-galaxy-s8-and-s8-software/)时，我质疑它的有用性。近 20 个月和 3 款旗舰 Galaxy 发布之后，一些人仍然质疑 DeX 的功能性。为了让 DeX 对专业人士和开发人员更有用，三星在 2017 年 SDC 大会上宣布了 DeX 上的[Linux](https://www.xda-developers.com/samsung-announces-linux-on-galaxy-for-dex/)，以改善访问新应用的桌面体验。现在，基于 DeX 的 Linux 终于在三星 Galaxy Note 9 和三星 Galaxy Tab S4 上进入了测试版,我必须试用一下，看看它是如何工作的。DeX 上的 Linux 是在手机上运行的合法桌面体验。

鉴于之前一些公司试图将 GNU/Linux 发行版引入移动设备的失败经历，Linux on DeX 是一个大胆的想法。在 Android 设备上运行为 ARM 编译的 GNU/Linux 发行版并不新鲜，但这是第一次做得很好。在 DeX 上运行 Linux 的底层 GNU/Linux 发行版是由 Canonical(维护 Ubuntu 的公司)和 Samsung 联合开发的经过修改的 Ubuntu 16.04 LTS。Ubuntu 必须修改以适应 Android 的安全政策。

自从第一个测试版发布以来，我就在 DeX 上使用 Linux(我甚至用它写了这篇文章)，我对该产品的第一印象是，它肯定受到运行它的硬件的限制。这显然比在大多数 x86 PCs 上运行 GNU/Linux 发行版要慢，但比运行普通的 DeX 模式还要慢。我测试的设备是 6GB 内存的三星 Galaxy Note 9，配有高通骁龙 845 和 Adreno 630。同时运行 Android 和 Ubuntu 会将设备推向极限。我们不指望它是完美的，但它应该运行，哦，男孩，它肯定运行。

如果你还没有得到消息，不要在 DeX 上为游戏或社交媒体安装 Linux。你安装的软件包必须为 ARM64(三星 Galaxy Note 9 和三星 Galaxy Tab S4 上的架构)编译，所以如果不为自己编译，你可以尝试的东西会非常有限。像《我的世界》、Discord 和谷歌 Chrome 这样的应用无法安装，这总结了一个“普通用户”在 DeX 上试用 Linux 的经历。它不是台式电脑或笔记本电脑的替代品。

另一方面，三星向开发者宣传 Linux on DeX。开发人员是可能在 DeX 上最大限度地使用 Linux 的一群用户。它带有 IntelliJ 和 Geany 用于编码。Android Studio 甚至运行在 DeX 上的 Linux 上。你可以直接从 Galaxy Note 9 或 Galaxy Tab S4 上编码、构建、安装和测试 Android 应用程序。我能够在 IntelliJ 中打开一个 Android 应用程序，并编译和安装它。我甚至有可能直接在我的 Galaxy Note 9 上开始为 OnePlus 6 编译 LineageOS 16。尽管正如开发人员 [me2151](https://forum.xda-developers.com/member.php?u=4591212) 所指出的，复制回购可能需要近 6 个小时，构建操作系统大约需要 10 个多小时。到那个时候，我的 Galaxy Note 9 电池早就没电了。RAM 也有问题:从源代码编译 Android 8.0 至少需要 8GB RAM。由于 DeX 上的 Linux，未来的三星手机可能实际上可以用作完全开发机器，但不是现在的手机。

### 基于 DeX 的 Linux 与普通 DeX

当我在 DeX 上测试 Linux 时，我也开始更频繁地使用常规的 DeX 模式。结果我开始喜欢常规的 Dex，而不是 DeX 上的新 Linux。这是因为应用程序和软件支持临时用户。在常规的 DeX 模式下，你可以访问大量的 Android 应用和游戏，而 DeX 上的 Linux 实际上只适用于一些开发工作。我使用了一款名为 Parsec 的应用程序，将游戏从我的台式机传输到我的笔记本电脑和手机上。我能够将堡垒之夜从我的个人电脑传输到三星 DeX，但这在 DeX 上的 Linux 上还无法实现。

尽管如此，DeX 还远未取代传统的笔记本电脑或台式机。商业专业人士和一些学生可能会发现 DeX 很有用，一些开发人员可能会发现新的 Linux on DeX 很有用。然而，常规的 DeX 和 DeX 上的 Linux 都太受它们运行的硬件的限制。在值得你考虑之前，我们需要更多的内存和对 DeX 上的 Linux 中的 ARM 设备更好的支持。至于常规的 DeX，它仍然不时地有它的用处，所以我不认为我会完全放弃它。

[**银河 Note 9 XDA 论坛**](https://forum.xda-developers.com/galaxy-note-9)