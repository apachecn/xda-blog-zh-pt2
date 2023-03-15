# termux——Android 的终极 Linux 终端仿真器[XDA 聚焦]

> 原文：<https://www.xda-developers.com/termux-the-ultimate-linux-terminal-emulator-for-android-xda-spotlight/>

你曾经想要一个完整的 Linux 终端环境在你的安卓手机上吗？不仅仅是一个包含基本命令的终端模拟器，而是一个全面的 Linux 命令行环境，包含您已经习惯的所有实用程序和软件包？如果是，那么 [Termux](https://termux.com/) 就是答案。

[Termux](https://play.google.com/store/apps/details?id=com.termux) 是一款功能强大的终端仿真软件，类似于现在流行的[终端仿真器](https://play.google.com/store/apps/details?id=jackpal.androidterm) app，但是还包含了一个[广泛的 Linux 包集合](https://github.com/termux/termux-packages)。Termux 的包管理系统很像 Debians 高级包工具(APT ),你可以用命令 *apt* 搜索、安装和卸载。Termux 只安装一些开箱即用的基本软件包，以减少 Play Store 上 APK 的大小，但允许你安装任何你想要的额外软件包。虽然谷歌 Play 商店上有几个替代 Termux 的方案，但没有一个能提供像 Termux 那么多的套餐。

 <picture>![](img/83d0710f7dfc6c421461bcca4e125b49.png)</picture> 

Left to Right: Apt, FFmpeg, Vim

**推荐阅读:** [了解如何在你的 Android 设备上安装完整的 GNU/Linux 环境。](https://www.xda-developers.com/guide-installing-and-running-a-gnulinux-environment-on-any-android-device/)

* * *

## termux——Android 的 Linux 终端仿真器

Termux 软件包是使用 Ubuntu 16.10 构建的，因此这意味着开发人员可以从他们的机器上编译任何现有的软件，然后将其添加到软件包管理器中，供任何人下载。这是一个非常简单和优雅的解决方案，否则可能是一个复杂和困难的问题。一个令人惊奇的副作用是，一旦软件被编译，你就有了软件的完整版本，而不是不完整的移植版本的桌面 Linux 包。

例如，我在 Mac 上使用命令行，因为我喜欢 90%的时间把手放在键盘上。因此，我使用键盘快捷键和终端应用程序来完成大部分工作。我更喜欢使用 Vim，因为它是一个很棒的文本编辑器，有包括微软在内的几乎所有插件。网！我有各种日常使用的插件，我已经在 Termux 中安装了 Vim，并取得了巨大的成功。我尝试的一切都和我预期的一样有效。我最喜欢的插件之一是 CtrlP，它是一个强大的文件查找工具，在 Termux 上的 Vim 中运行得非常好。

Termux 默认为您提供一个 bash 终端，但是如果您和我一样，喜欢 Zsh 的高级特性，也可以使用 FISH shell。多种不同的外壳类型当然是受欢迎的。

任何在 Android 上使用过终端模拟器应用程序的人都知道，当你需要输入特殊的键来控制终端(如 CTRL 或 ESC)时会有多痛苦。这些键不会显示在 android 设备上使用的标准触摸键盘上([除了黑客键盘](https://play.google.com/store/apps/details?id=org.pocketworkstation.pckeyboard))。不过，Termux 开发商 Fredrik Fornwall 对此有一个非常新颖的解决方案。他将 CTRL 绑定到音量减小键，将 ESC 等其他特殊键绑定到音量增大键。因此，通过按下音量增大+触摸键盘“L ”,您可以输入终端命令 CTRL+“L”来清除终端窗口。例如，通过按下音量增大+‘E’键来发送 ESC 键。你可以在[开发者网站](https://termux.com/touch-keyboard.html)上查看 Termux 中所有可用的密钥。

我还在 Termux 中使用 SSH 来连接我的个人 VPS 服务器。虽然存在其他 Android 应用程序，如[juice shh](https://play.google.com/store/apps/details?id=com.sonelli.juicessh&hl=en)和 [ConnectBot](https://play.google.com/store/apps/details?id=org.connectbot&hl=en) ，但在我看来，在适当的终端环境中通过 OpenSSH 建立适当的 SSH 连接更好。Termux 允许您创建多个会话，这样我就可以在一个会话上连接我的服务器，在另一个会话上连接我的本地环境。

如果您喜欢在终端中开发，Termux 也能满足您的需求。我用 Termux 的包管理器在我的手机上安装了 python，并且编写了与我在远程服务器上完全一样的 python 代码。

什么稍微重一点的东西，比如用 NodeJS 开发？Termux 也支持 NodeJS，它还支持流行的栈，比如 Express。我能够安装一个完整的 NodeJS/Express/Bootstrap 环境，并在我的设备上托管一个简单的网站。

我也能够安装和使用 Ruby，但是我在最初安装 Rails 时确实遇到了问题。幸运的是，我能够在谷歌+社区的帮助下让 Rails 在我的设备上运行，这个社区非常活跃，如果你陷入困境，它是一个很好的帮助来源。说白了，我对 Termux 及其包管理系统印象深刻。它提供了一个惊人的包清单，这是不断增长；到目前为止，我没有错过任何我每天使用的包裹。然而，我确实注意到流行的屏幕终端多路复用器是不可用的，但是替代的(在我看来更好)TMUX 是可用的。

我测试所有这些的设备也不是旗舰手机。我用的是我的小米 Max，配有 4gb 内存和骁龙 650 SoC，还有一个苹果蓝牙键盘。我使用这款手机的主要原因是因为小米 Mi Max 有 6.44 英寸的屏幕，给了我一个不错的工作空间。有了上面显示的设置，我可以在旅途中舒适地做一些严肃的工作。

关于 Termux 最令人惊奇的事情是它是完全免费的，没有 T2 的应用内购买和广告。尽管如此，您可以购买一些费用低廉的附加组件，以支持开发人员并改进 Termux 已经令人印象深刻的功能。迄今为止的插件包括:

*   [Termux:任务](https://play.google.com/store/apps/details?id=com.termux.tasker) -将 Termux 与 Tasker 集成
*   Termux:API -允许 Termux 与现有的 Android APIs 集成(比如在终端上阅读你的短信)
*   [Termux:Widget](https://play.google.com/store/apps/details?id=com.termux.widget) -从主屏幕执行 Termux 脚本
*   [Termux:造型](https://play.google.com/store/apps/details?id=com.termux.styling) -定制 Termux 的外观
*   [Termux:Float](https://play.google.com/store/apps/details?id=com.termux.window) -允许一个浮动的 Termux 窗口

Termux 现在是我所有 Android 设备上的永久安装；它允许我在本地设备上拥有一个全功能的终端和开发环境。我花了很多时间在远程服务器上开发，但是有时你会遇到无法连接到服务器的情况。最近，我去了趟新西兰，来回飞了 11 个小时。如果我当时安装了 Termux，我的飞行可能会变成总共 22 小时的编码会话。

* * *

[**在 Play Store** 上下载 Termux](https://play.google.com/store/apps/details?id=com.termux)

[**可用的 Termux 包列表(或自己构建)**](https://github.com/termux/termux-packages)

[**查看 Termux Google+社区**](https://plus.google.com/communities/101692629528551299417)