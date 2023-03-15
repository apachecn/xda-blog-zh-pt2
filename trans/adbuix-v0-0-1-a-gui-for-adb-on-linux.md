# adbuix v 0 . 0 . 1——用于 Linux 上 ADB 的 GUI

> 原文：<https://www.xda-developers.com/adbuix-v0-0-1-a-gui-for-adb-on-linux/>

Adbuix 是 Linux 操作系统上 Android 调试桥(ADB)的图形用户界面(GUI)。

由 XDA 论坛成员 [KodieG](http://forum.xda-developers.com/member.php?u=2056933) 开发，当使用 ADB 修改 Android 设备上的文件时，它消除了记忆命令或键入目录路径的工作。

Adbuix 消除了在终端键入命令的需要；例如，要将应用程序从计算机桌面复制到设备，请单击要复制的文件，单击要复制的文件夹，然后单击复制按钮。

> 最初由 **KodieG** 发布
> 
> **已知 bug**
> 
> *   点击“重启服务器和刷新”按钮在设备菜单不起作用，并导致程序崩溃。
> *   点击主屏幕上的“检查更新”不起作用，并导致程序崩溃。(但是，您可以在这里下载更新 bash 脚本并使用它来检查更新:[http://kodieg.com/dl/adbuixupdate.sh](http://kodieg.com/dl/adbuixupdate.sh))
> *   当使用模拟器而不是实际设备的程序时，在文件管理器中，文件夹有文件图标而不是文件夹，但一切都按预期工作。
> *   点击主屏幕上的帮助按钮将提示您访问“Adbuix 帮助页面”,但只会带您到 kodieg.com，因为帮助页面尚未制作。
> *   在安装过程中创建的桌面快捷方式称为“Adbuix.gambas ”,并带有“gambas”图标，而它本应称为 Adbuix 并带有 Adbuix 图标。
> *   当从桌面快捷方式运行 Adbuix 时，它声称您使用的是 Adbuix 版本 0.0.0，但实际上它是 0.0.1。你可以直接删除桌面快捷方式。

一旦 Linux 版本完成，KodieG 表示将会开发 Windows 版本，也许还有 OSX 版本。

Adbuix 仍处于早期测试阶段，KodieG 警告说它可能不稳定，但这是为 ADB 建立和运行 GUI 的良好开端。

要了解更多信息，并支持 KodieG，请查看[应用程序线程](http://forum.xda-developers.com/showthread.php?t=641385)。