# 联发科发布 Android One 全内核源代码

> 原文：<https://www.xda-developers.com/mediatek-android-one-source/>

# 联发科为首批 Android One 设备发布完整内核源代码

联发科遵守了 GPL 许可，发布了 Android One 全线设备的全内核源码！

那些可能认为联发科永远不会发布工作内核源代码的人现在可能不得不擦擦眼睛了。这类读者最好坐下来，因为你们所有人都在享受美食。正如我们前段时间谈到的，联发科在支持开发社区方面取得了长足的进步。现在，联发科已经兑现了这一承诺，发布了第一批 Android One 设备(T3)的全部源代码。启动你的 Linux 机器，确保有很多现成的咖啡，因为这些预算友好的设备将会有一些严肃的发展。

尽管联发科尽了最大努力，但许多采用联发科芯片组的设备背后的原始设备制造商未能遵守 [GPL 规定的](https://www.gnu.org/licenses/gpl-2.0.html)内核源代码发布政策。但现在，联发科通过将 3.4.67 Linux 内核的代码推送到[谷歌的 Android repo](https://android.googlesource.com/kernel/mediatek/) 上的内核/联发科 repo 中，绕过了这个问题。这意味着计划在 Android One 设备上工作的开发人员可以克隆源代码树，添加不同的调控器，超频，欠电压，以及做任何他们需要做的事情，以在 Android One 设备上进行开发和运行。我们希望谷歌也将推动 [Micromax Canvas A1](http://forum.xda-developers.com/canvas-a1) 、 [Karbonn Sparkle V](http://forum.xda-developers.com/sparkle-v) 和 [Spice Dream Uno](http://forum.xda-developers.com/dream-uno) 的设备树，就像他们对整个 Nexus 系列所做的那样，但这还没有看到。

您可以通过输入以下命令获得内核源代码，在本地处理它，然后推送到您自己的在线 git repo，如 Github:

> git 克隆 https://android.googlesource.com/kernel/mediatek/-b 安卓-联发科-萌芽-3.4-kitkat-mr2

希望在未来几周和几个月，我们将继续看到联发科取得更多类似的进展！