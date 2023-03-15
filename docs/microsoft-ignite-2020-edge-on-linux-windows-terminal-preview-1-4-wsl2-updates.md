# 微软 Ignite 2020:Linux 上的 Edge、Windows 终端预览版 1.4、WSL2 更新等等

> 原文：<https://www.xda-developers.com/microsoft-ignite-2020-edge-on-linux-windows-terminal-preview-1-4-wsl2-updates/>

在一年一度的 Ignite 开发者大会上，微软宣布了一系列以开发者为中心的变化，这些变化将出现在 Windows 10 中。根据该公司最近分享的博客帖子，这些变化旨在简化平台上的应用开发，并为开发者提供更好的工具，以保持专注和高效。以下是正在进行的 Ignite 2020 大会上一些最值得关注的公告:

## Linux 上的优势

微软新的基于 Chromium 的 [Edge](https://xda-developers.com/tag/microsoft-edge) 浏览器已经可以在几个平台上使用，包括 Windows 10、Windows 7、Windows 8、macOS、iOS 和 Android。现在，该公司宣布了微软 Edge for Linux 的预览版，将于下个月向用户推出。Linux 用户很快就可以从[内部网站](https://www.microsoftedgeinsider.com/en-us/download?form=MO12H9&OCID=MO12H9)或本地包管理器下载微软 Edge Dev 频道。

除了 Edge for Linux，微软还宣布了浏览器的一些重要变化，预计将为企业提供更安全的浏览体验。你可以在新的[网络体验博客](https://aka.ms/EdgeIgnite2020)的 Ignite 版本中了解更多关于这些变化的信息。

## Windows 终端预览版 1.4

今年 5 月初，微软[发布了 Windows Terminal 1.0](https://www.xda-developers.com/microsoft-releases-windows-terminal-1-0-package-manager-announces-linux-gui-app-support-gpu-acceleration-subsystem-linux-wsl-2/)——一款新的终端应用，提供了 GPU 加速的文本渲染、主题化支持、标签、分离式窗口、快捷方式、完整的 Unicode 支持等功能。该公司现已宣布发布 Windows 终端预览版 1.4，这将带来更多的功能组合。

 <picture>![Microsoft Windows Terminal Preview 1.4 Hyperlink support](img/9e6ff3cda5c3e584b2b7597de51bf437.png)</picture> 

Hyperlink support

根据 Windows 命令行博客上最近的一篇文章，Windows 终端预览 1.4 包括对嵌入式超链接和呈现闪烁图形呈现属性的支持，以帮助开发人员在文本缓冲区内包括闪烁显示。

 <picture>![Microsoft](img/dfb40691cb2c5b65930700b9bd955871.png)</picture> 

Blink support

最重要的是，Windows 10 现在将允许用户从开始菜单或任务栏启动带有特定配置文件的 Windows 终端预览。更新还包括一些错误修复，你可以通过下面的链接查看公告。

## WSL 2 更新

微软还宣布了针对 Linux (WSL) 2 的 Windows 子系统的几个更新。首先，该公司再次证实，Windows 10 版本 1903 和 1909 现在可以支持 WSL 2 发行版。得益于此，运行旧版本 Windows 10 的人现在将能够体验更快的文件系统性能，100%的系统调用兼容性，并且他们将能够使用基于 WSL 2 的引擎的 Docker Desktop。

此外，WSL 正在获得 Linux GUI 应用程序支持，这将在未来几个月内提供给 Windows 内部人员。有了这个特性，WSL 将支持几种不同类型的应用程序，包括完全在 Linux 环境下运行的 ide。如果你有兴趣了解更多关于这一变化背后的架构，你可以在 XDC 2020 大会上查看 [X11 和韦兰谈话](https://youtu.be/b2mnbyRgXkY?t=7975)。

在 BUILD 2020 上，微软宣布他们将添加一个新命令，允许用户完全安装名为 *wsl - install* 的 WSL。该功能的早期版本已经提供给 Windows 内部人员，在接下来的几周内， *- install* 参数将获得安装 WSL 发行版的能力。实际上，这将让用户只需一个命令就可以在他们的系统上完全安装 WSL 以及所选的发行版。

## Windows 包管理器预览

在今年 5 月早些时候的 BUILD 2020 上，微软还宣布了一个新的命令行包管理器，称为 Windows 包管理器。该公司现在已经宣布了几个新功能，将很快在 Windows 包管理器中推出。其中包括一个新的功能切换，PowerShell 自动完成，以及从微软商店安装应用程序的能力。

 <picture>![](img/f09353beda9c69b2422579dd39abaff8.png)</picture> 

PowerShell autocomplete

该公司还公布了一份即将在未来几个月发布的变化清单。这些功能包括列表支持，帮助您查看使用软件包管理器安装的所有应用程序，使用一个命令升级所有安装的应用程序的能力，卸载在软件包管理器之外安装的应用程序的能力，以及将软件包从一个系统导入/导出到另一个系统。

除了上面提到的变化，微软还宣布了一项名为 Project Reunion 的新计划。该计划旨在为开发者提供一个统一的应用平台，让他们专注于自己的应用，并利用新的或现有的代码。要了解更多关于 Project Reunion 的信息，请访问下面链接的 Windows 开发人员博客。

* * *

**来源: [Windows 开发者博客](https://blogs.windows.com/windowsdeveloper/2020/09/22/kevin-gallo-microsoft-ignite-2020/)，Windows 命令行博客( [1](https://devblogs.microsoft.com/commandline/whats-new-in-the-windows-subsystem-for-linux-september-2020/) ， [2](https://devblogs.microsoft.com/commandline/windows-terminal-preview-1-4-release/) ， [3](https://devblogs.microsoft.com/commandline/windows-package-manager-preview-v0-2-2521/) )**