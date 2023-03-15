# 指南:在任何 Android 设备上安装和运行 GNU/Linux 环境

> 原文：<https://www.xda-developers.com/guide-installing-and-running-a-gnulinux-environment-on-any-android-device/>

正如你们很多人可能都知道的那样，Android 操作系统是由底层的 Linux 内核支持的。尽管事实上 Android 和 GNU/Linux 都由相同的内核驱动，但这两个操作系统有很大的不同，并且运行完全不同类型的程序。

然而，有时 Android 上可用的应用程序可能会感觉有点有限或乏味，尤其是与桌面应用程序相比。幸运的是，你可以在**任何安卓设备**、**根或非根**上安装并运行 **GNU/Linux 环境**。*(以下说明假设非根设备。)*

对于那些使用 Android 平板电脑或其他具有大屏幕(或可以插入更大屏幕)的 Android 设备的高级用户来说，运行桌面 Linux 软件的能力可以大大提高 Android 设备的生产力潜力。

* * *

## 在 Android 上设置 GNU/Linux

要在你的 Android 设备上建立 GNU/Linux 环境，你只需要从 Google Play 商店安装两个应用程序: **GNURoot Debian** 和 **XServer XSDL。**完成之后，您只需要运行少量的 Linux 命令就可以完成安装。

GNURoot Debian 提供了一个运行在 Android 应用程序沙箱范围内的 Debian Linux 环境。它通过利用一个名为 *proot* 的软件来实现这一点，这是 Linux 的 *chroot* 功能的用户空间重新实现，用于在主机环境中运行来宾 Linux 环境。 *Chroot* 通常需要 root 权限才能运行，但是通过使用 *proot* 您可以实现类似的功能，而不需要 root 权限。

GNURoot 带有一个内置的终端仿真器，用于访问它的 Debian Linux 环境。这对于运行命令行软件来说已经足够了，但是，运行图形软件还需要一个 X 服务器。X Window 系统被设计成具有独立的客户机和服务器组件，以便提供更大的灵活性(一个更快、更强大的 UNIX 主机可以充当运行在功能更弱、更简单的终端上的 X 服务器实例的客户机)。

在这种情况下，我们将使用一个单独的应用程序， **XServer XSDL** ，GNURoot 应用程序将作为客户端连接到该应用程序。XServer XSDL 是一个完整的 XServer 实现，由 SDL 支持，具有许多可配置的选项，如显示分辨率、字体大小、不同类型的鼠标指针行为等等。

* * *

## 逐步指南

1.从 Play Store 安装 [GNURoot Debian](https://play.google.com/store/apps/details?id=com.gnuroot.debian) 和 [XServer XSDL](https://play.google.com/store/apps/details?id=x.org.server) 。

2.运行 **GNURoot Debian** 。Debian Linux 环境会自行解包和初始化，这需要几分钟时间。最终，您将看到一个“根”外壳。不要被这个误导了——这实际上是一个仍然在 Android 应用程序沙箱范围内运行的假 root 帐户。

3.运行`apt-get update`和`apt-get upgrade`以确保您的系统上有最新的可用软件包。Apt-get 是 Debian 的软件包管理系统，你可以用它在你的 Debian Linux 环境中安装软件。

4.一旦你是最新的，是时候安装一个图形环境了。我推荐安装 **LXDE** ，因为它简单轻便。(记住，你是在后台运行 Debian，Android 操作系统的所有开销都在后台，所以最好尽可能地节省资源。)您可以选择`apt-get install lxde`安装桌面环境和全套工具，或者`apt-get install lxde-core`只安装桌面环境本身。

5.现在我们已经安装了 LXDE，让我们再安装一些东西来完成我们的 Linux 设置。

**XTerm**–这提供了在图形环境中对终端的访问

**新立得包管理器**——apt-get 的图形化前端

**pulse audio**–提供播放音频的驱动程序

运行`apt-get install xterm synaptic pulseaudio`来安装这些实用程序。

6.最后，让我们启动并运行图形环境。启动 **XServer XSDL** 并让它下载附加字体。最终你会看到一个蓝屏，上面有一些白色的文字——这意味着 X 服务器正在运行，等待客户端连接。切换回 GNURoot 并运行以下两个命令:

```
 export DISPLAY=:0 PULSE_SERVER=tcp:127.0.0.1:4712
startlxde & 
```

然后，切换到 XServer XSDL，观看 LXDE 桌面出现在您的屏幕上。

我建议将以上两个命令放入一个 shell 脚本中，这样，如果您关闭会话或者需要重启设备，就可以轻松地重启 LXDE。

* * *

## 安装 Linux 应用程序

恭喜你。你已经成功地让 Debian Linux 在你的 Android 设备上运行，但是没有应用程序运行 Linux 有什么好处呢？幸运的是，您已经有了一个庞大的 Linux 应用程序库，只等着下载。我们将使用我们之前安装的 Synaptic 包管理器来访问这个库。

点击左下角的“开始”按钮，点击运行，然后输入`synaptic`。新立得软件包管理器将被加载。从这里，只需按下顶部的搜索按钮，然后键入您想要安装的应用程序的名称。一旦你找到一个应用程序，右击它并选择“标记为安装”。标记完软件包后，单击顶部的应用按钮开始安装。卸载软件包遵循相同的过程，只是右键单击并选择“标记为删除”。

当然，由于这不是一个真正的 Linux 安装，而是一个运行在 Android 之上并受其约束的 Linux 环境，所以需要注意一些限制。一些应用程序将拒绝运行或崩溃，通常是由于一些通常暴露在 GNU/Linux 系统上的资源被 Android 隐藏起来。此外，如果一个常规的 Android 应用程序不能做一些事情，那么通常在 Android 中运行的 Linux 应用程序也不能，所以你将无法执行诸如硬盘分区之类的任务。最后，需要硬件加速的游戏将无法运行。然而，大多数标准的日常应用程序运行良好。一些例子包括 Firefox、LibreOffice、GIMP、Eclipse 和像 PySol 这样的简单游戏。

* * *

我希望这篇教程对你有用。虽然我个人在我的谷歌 Pixel C 上执行了这些步骤，但你可以在大多数 Android 设备上这样做。当然，最好是在能够访问键盘和鼠标外围设备的平板设备上。如果你已经在你的 Android 设备上运行了 GNU/Linux 发行版，请在下面告诉我们你用它做什么！