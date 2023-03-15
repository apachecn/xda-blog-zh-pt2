# Steam 现在可以作为 Snap 包在 Linux 上使用

> 原文：<https://www.xda-developers.com/steam-linux-snap-package/>

在这一点上，Steam 游戏商店已经在桌面 Linux 上可用了许多年，随着 Windows 游戏的质子兼容层的加入，它已经成为 Linux 上游戏的无价工具。Ubuntu Linux 的开发者 Canonical 现在引入了一种在 Ubuntu 和其他 Linux 发行版上使用 Steam 的新方法:一个 Snap 包。

Canonical 在一篇博客文章中透露:“我们一直在努力提高 Linux 玩家的生活质量，而今天……我们很高兴地宣布，Steam snap 将提前推出访问功能！”Canonical 被列为开发人员，因此 Valve 似乎没有参与该项目。

Steam 及其游戏与操作系统的其他部分隔离开来

新的包在一次下载中包含了 Steam 及其所有的依赖项，没有 Linux 上的 Steam 有时需要的额外步骤(比如启用 32 位库或 Mesa 驱动程序)。Steam 及其游戏与操作系统的其余部分隔离，因此游戏无法看到你电脑的所有文件——类似于 Chrome OS 上的新 [Steam 容器。](https://www.xda-developers.com/chrome-os-steam-announcement/)

Snap 是 Canonical 开发的一个容器化的包系统，旨在使桌面 Linux 软件更容易安装、更新和跨不同的 Linux 发行版使用。尽管 Snap 包有一些优势，特别是对于传统包较少的桌面 Linux 系统(例如，不是基于 Ubuntu 或 Arch 的发行版)，Snap 背后的技术受到了 Linux 社区中一些人的批评。Canonical 控制着唯一的 Snap“应用商店”，而 Snap 应用通常比普通软件需要更长的时间才能打开。去年，当 Ubuntu [将默认的 Firefox 网络浏览器切换到 Snap 包](https://www.omgubuntu.co.uk/2021/09/ubuntu-makes-firefox-snap-default)时， [Linux Mint 与 Mozilla](https://www.xda-developers.com/linux-mint-firefox-deal/) 达成协议，保留非 Snap 版本。

从 Snap 商店可以获得 Steam，或者如果你已经在你的 Linux 系统上安装了 Snap，你可以在你的终端上运行“snap install steam - beta”(不带引号)。Snap 包可以在 Ubuntu、Arch、Fedora、Linux Mint、KDE Neon、Debian 和大多数其他主要的 Linux 发行版上获得。

**来源:** [Ubuntu](https://ubuntu.com//blog/level-up-linux-gaming-new-steam-snap)