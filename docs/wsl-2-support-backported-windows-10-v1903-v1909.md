# Windows 10 v1903 和 v1909 支持 WSL 2

> 原文：<https://www.xda-developers.com/wsl-2-support-backported-windows-10-v1903-v1909/>

微软在去年的微软构建期间首次宣布了用于 Linux 2/WSL 2 的 Windows 子系统，今年早些时候随着 Windows 10 2020 年 5 月更新(2004 版)推出了稳定版[。此次更新为稳定的 Windows 10 分支引入了完整的 Linux 内核，该公司还通过 Windows Update](https://www.xda-developers.com/microsoft-windows-10-may-2020-update-wsl-2-revamped-cortana-assistant-your-phone-calls-arm-devices/) 使 WSL 2 [可更新，这意味着用户不再需要依赖命令行选项来更新内核。现在，微软正在为旧版本的 Windows 10 带来 WSL 2 支持。](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004/)

根据最近在 *Windows 命令行*博客上的一篇文章，WSL 2 支持正在通过更新进入 Windows 10 版本 1903 和 1909。然而，backport 将只适用于 x64 系统，运行 ARM64 版本的用户需要更新到 Windows 10 version 2004 才能访问 WSL 2。

如果你是运行 Windows 10 版本 1903 或 1909 的众多用户之一，你可以前往 Windows 设置中的更新与安全部分，然后点击检查更新，看看你是否收到了更新。正如博客文章所解释的，你可以通过验证当前 Windows 10 版本的次要版本号来检查你是否收到了回传。

要做到这一点，你需要右击开始菜单，点击“运行”，输入“winver”，然后按回车键。在下一页，您将能够检查您的操作系统内部版本号。如果您的次要内部版本号(出现在“.”后面的数字)在操作系统内部版本号中)是 1049 或更高(在 Windows 内部版本号 18362 或 18363 上)，那么您已经收到了反向端口，因此也收到了 WSL 2 支持。

在你确认你已经收到了回传之后，你就可以按照[这篇文章](https://docs.microsoft.com/en-us/windows/wsl/install-win10)中给出的说明来安装 WSL，或者简单的[更新来使用 WSL 2](https://docs.microsoft.com/en-us/windows/wsl/install-win10#update-to-wsl-2) 。有了 WSL 2 的支持，你将能够在你的 Windows 10 上编译[linegeos](https://www.xda-developers.com/tag/lineageos/)定制的 rom。如果你有兴趣尝试一下，你可以按照[这个指南](https://www.xda-developers.com/how-to-build-lineageos-on-windows-10-using-wsl-2/)开始。

* * *

**来源: [Windows 命令行](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/)**

*感谢 XDA 资深会员 [Some_Random_Username](https://forum.xda-developers.com/member.php?u=8234677) 的提示！*