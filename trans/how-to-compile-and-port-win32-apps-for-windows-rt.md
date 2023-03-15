# 如何为 Windows RT 编译和移植 Win32 应用程序

> 原文：<https://www.xda-developers.com/how-to-compile-and-port-win32-apps-for-windows-rt/>

Windows RT 用户发现最令人沮丧的事情之一是无法在他们闪亮的新设备上运行传统的桌面应用程序。尽管这已经不是什么秘密了，但是由于开发社区的存在，许多人仍然希望这不再是一个问题。

发布了允许设备运行的 [RT 越狱工具](http://www.xda-developers.com/windows_phone/rt-jailbreak-tool-lets-users-install-non-microsoft-executables-on-windows-rt/)。 exe 未经微软官方编译和签名的文件，是解决这个问题的一大进步。剩下的工作就是开始跨应用程序移植，以便在 ARM 架构上运行。XDA 资深会员 [no2chem](http://forum.xda-developers.com/member.php?u=542308) 已经整理了一份非常全面的指南，介绍如何将 Win32 应用移植到 Windows RT 上运行，这将有望激励一些人移植和共享一些应用，并帮助实现 RT 驱动设备的潜力，至少在我们看到该平台可用的应用有所增加之前是如此。

如果你以前有开发 Windows 的经验，很可能你已经拥有了大部分(如果不是全部的话)所需的工具，不应该为此而挣扎。如果你以前没有任何经验，你可能需要在尝试之前做一点阅读，尽管第二个 chems 指南确实详细地带你完成了这个过程。如果你想添加到以前移植的应用程序集合中，请查看[原始论坛主题](http://forum.xda-developers.com/showthread.php?t=2096820)以获取更多信息。