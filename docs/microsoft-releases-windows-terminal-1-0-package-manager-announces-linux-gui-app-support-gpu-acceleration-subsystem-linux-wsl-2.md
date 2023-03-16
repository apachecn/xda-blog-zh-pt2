# 微软宣布终端 1.0，Windows 包管理器，和更多的变化

> 原文：<https://www.xda-developers.com/microsoft-releases-windows-terminal-1-0-package-manager-announces-linux-gui-app-support-gpu-acceleration-subsystem-linux-wsl-2/>

微软每年为软件工程师和网络开发者举办一次会议。该活动名为 Build，或//build/虽然微软每年都会在地面上举办一场活动，就像过去几年在 T2 举办的活动一样，但是因为新冠肺炎，Build 2020 只在网上发布。值此之际，微软[宣布了大量新功能](https://blogs.windows.com/windowsdeveloper/2020/05/19/developing-for-all-1-billion-windows-10-devices-and-beyond/)，如 Windows 终端 1.0、Windows 软件包管理器、Windows Linux 2 子系统，所有这些都将以某种形式对许多开发者有用。

## Windows 终端 1.0

在去年的 Build 2019 开发者大会期间，微软曾宣布 Windows 终端。这正是它听起来的样子——微软的一个新的终端应用。

该应用程序的一些亮点包括 GPU 加速的文本渲染，主题化支持，标签，撕裂式窗口，快捷方式，完整的 Unicode 支持，等等。Windows 终端的最终目标是成为 PowerShell 和 Command Prompt 等其他命令行应用程序的良好替代品。

Windows Terminal 是在 Build 2019 发布的预览版，现在，在 Build 2020，该应用已经以 [Windows Terminal 1.0](https://devblogs.microsoft.com/commandline/windows-terminal-1-0/) 的形式升级为完整版本。

Windows 终端 1.0 可以从[微软商店](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701)或者 [GitHub](https://github.com/microsoft/terminal/releases) 下载。该应用将从 2020 年 7 月开始每月更新一次。但是，如果你想在它们进入稳定分支之前尝试最新的功能，你可以在[微软商店](https://aka.ms/terminal-preview)和 [GitHub](https://github.com/microsoft/terminal/releases) 上查看预览频道。

微软文档中提到的 Windows 终端 1.0 的主要特性:

*   支持各种命令行应用程序的多个配置文件
*   定制的配色方案和配置
*   自定义键绑定
*   Unicode 和 UTF 8 字符支持
*   GPU 加速文本渲染
*   背景图像支持
*   支持命令行参数

* * *

## Microsoft Windows 包管理器

如果您熟悉 GNU/Linux 发行版，您很可能熟悉命令行包管理器。简单地说，软件包管理器管理在你的计算机上安装、配置和卸载软件包(或应用程序)的过程。命令行包管理器从命令行执行所有这些任务。微软从未正式提供命令行软件包管理器，但现在随着 Windows 软件包管理器的出现，这种情况正在发生变化。

Windows 有一些受欢迎的第三方命令行软件包管理器，如[Chocolatey](https://chocolatey.org/)——但这些都是非官方的，不是来自微软自己。与 Windows Store 等应用商店不同，包管理器支持从多个来源安装应用，这使得设置不同的开发环境变得容易，摩擦点更少。

Windows 包管理器[现在在预览表单](https://github.com/microsoft/winget-cli)中可用。更令人兴奋的是，它是开源的。

Windows 包管理器提供了以下功能，在前面加上 *winget* 命令:

*   **安装** -安装给定的应用程序
*   **显示** -显示应用程序的信息
*   **来源** -管理应用程序的来源
*   **搜索** -查找并显示应用的基本信息
*   **散列** -散列安装程序文件的助手
*   **验证** -验证清单文件
*   **-帮助** -提供命令行帮助
*   **-信息** -提供附加数据，有助于故障排除
*   **-版本** -提供客户端的版本

解释一下，如果您使用“ *winget install* ”，您将看到所有与 Windows 包管理器交互的命令行选项。例如，如果您键入“ *winget 安装终端*”，您将安装新的 Windows 终端软件。Windows 包管理器预先配置为指向微软社区库，您可以使用“ *winget search* ”搜索可用的包，并使用“ *winget show* ”显示信息。您还可以使用“ *winget source* ”添加第三方存储库。

命令行客户端在预装在 Windows 上的 App Installer 包中分发。然而，客户端将不会在预览期间普遍可用，所以你必须安装一个 [Windows 10 Insider](https://insider.windows.com/) build 或[注册预览飞行环](http://aka.ms/winget-InsiderProgram)以接收自动更新。此外，如果你不介意放弃自动更新，你也可以[手动安装它](https://github.com/microsoft/winget-cli/releases)在任何 Windows 10 版本上，因为秋季创造者更新(1709)。当 Windows 包管理器达到 1.0 版时，它将与桌面应用安装程序一起提供。

* * *

## Linux 2 / WSL 2 的 Windows 子系统

在 Build 2019 上，微软宣布了 Windows Subsystem for Linux 2，它搭载了完整的 Linux 内核，允许你运行 Linux 命令和应用程序。例如，你甚至可以在 Windows 上使用 WSL 编译 LineageOS 。

现在，[微软宣布了对 WSL](https://devblogs.microsoft.com/commandline/the-windows-subsystem-for-linux-build-2020-summary/) 的多项重大改变:

*   增加了对图形处理单元(GPU)计算工作流的支持，使 Linux 工具能够利用 GPU 为许多开发场景实现硬件加速，例如并行计算和训练机器学习(ML)和人工智能(AI)模型。
*   对 Linux 图形用户界面(GUI)应用程序的支持将使您能够打开一个 WSL 实例并直接运行 Linux GUI 应用程序，而不需要第三方 X 服务器。这将有助于您在 Linux 环境(如集成开发环境(IDE))中运行您喜爱的应用程序。
*   WSL 将很快通过运行“WSL . exe–install”命令来支持简化的安装体验，这将使在 Windows 上开始使用 Linux 应用程序比以往任何时候都更容易。

随着这些即将到来的对 WSL 2 的改变，用户不再需要运行 X 服务器来使用带有 GUI 的 Linux 应用程序。Linux 应用现在也可以在 Windows 上无缝运行了。正如米沙尔指出的，这可能只是 Linux 桌面的“[年](https://www.reddit.com/r/linux/comments/3038d4/when_was_the_first_year_of_the_linux_desktop/)”最终成为现实的转折点，具有讽刺意味的是，是微软带来了这一切。

* * *

对于微软 Build 2020 上宣布的功能，您有什么想法？请在下面的评论中告诉我们！