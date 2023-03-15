# Windows 10 中的 WSL 2 现在支持挂载像 EXT4 这样的 Linux 文件系统

> 原文：<https://www.xda-developers.com/wsl-2-windows-10-supports-mounting-linux-filesystems-ext4/>

继去年在微软构建期间宣布 Windows Subsystem for Linux 2(WSL 2)[之后，微软](https://www.xda-developers.com/microsoft-announces-windows-terminal/)[在今年早些时候通过 Windows 10 2020 年 5 月更新(v. 2004)向用户推出了](https://www.xda-developers.com/microsoft-windows-10-may-2020-update-wsl-2-revamped-cortana-assistant-your-phone-calls-arm-devices/)该功能。此次更新为稳定的 Windows 10 分支引入了完整的 Linux 内核，该公司还通过 Windows Update 使 WSL 2 [可更新。上个月末，微软宣布 WSL 2 支持被](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004/)[回移植到 Windows 10 v1903 和 v1909](https://www.xda-developers.com/wsl-2-support-backported-windows-10-v1903-v1909/) 。现在，该公司宣布了该功能的更新。

**[如何使用 WSL 2 在 Windows 10 上构建 lineage OS](https://www.xda-developers.com/how-to-build-lineageos-on-windows-10-using-wsl-2/)**

根据[最近在 Windows 命令行博客上的帖子](https://devblogs.microsoft.com/commandline/access-linux-filesystems-in-windows-and-wsl-2/)，从 Windows Insider 预览版 20211 开始，WSL 2 将提供一个新功能: `wsl --mount` 。帖子称这个*“新参数允许在 WSL2 中连接和安装一个物理磁盘，“*”这将使用户能够访问 Windows 本身不支持的文件系统，如 ext4。实际上，新参数将允许用户从 Windows 访问他们的 Linux 文件，即使他们使用不同的磁盘双重启动 Windows 和 Linux。

如果您的设备上已经安装了 Windows Insider preview build 20211，您将能够通过使用管理员权限打开 PowerShell 窗口并运行: `wsl -- mount <DiskPath>` 来挂载磁盘。要在 Windows 中列出所有可用的磁盘，可以运行: `wmic diskdrive list brief` 。最后，要从 WSL 2 中卸载和分离磁盘，可以运行: `wsl --unmount <DiskPath>` 。请注意，您只能将物理磁盘挂载到 WSL 2，此时，不可能挂载单个分区。

成功装载磁盘后，您将能够通过 Windows 资源管理器访问该磁盘。为此，您需要导航到“\wsl$”，然后导航到已装载的文件夹。同样值得注意的是，默认情况下， `wsl --mount` 命令试图将磁盘挂载为 ext4。如果你想指定一个不同的文件系统，或者对于更高级的场景，你可以从微软的文档中找到[来学习如何做。](https://docs.microsoft.com/en-us/windows/wsl/wsl2-mount-disk)