# RT 越狱工具允许用户在 Windows RT 上安装非微软的可执行文件

> 原文：<https://www.xda-developers.com/rt-jailbreak-tool-lets-users-install-non-microsoft-executables-on-windows-rt/>

这是 XDA 开发者，我们以某种方式喜欢我们的设备。我们喜欢它们不被锁住，扎根，并且可以随心所欲地自由处理。然而，很少有设备在这种情况下发布。因此，我们的大型社区的专门开发人员找到了一种方法来做到这一点。毕竟，事情发生了[又](http://www.xda-developers.com/android/unlock-the-verizon-samsung-galaxy-note-ii-bootloader-xda-developer-tv/)又[又](http://www.xda-developers.com/android/htc-droid-incredible-4g-lte-finally-gets-non-htcdev-bootloader-unlock/)又[又](http://www.xda-developers.com/android/dirtyracun-released-for-htc-evo-4g-lte-brings-s-off-for-hboot-1-151-19-without-downgrade/)。 [Windows RT](http://forum.xda-developers.com/forumdisplay.php?f=1286) 出来的时候也不是 100%开放。有适当的安全特性来防止用户安装未签名的*。exe* 文件。这当然意味着用户不能在微软应用商店之外安装太多。现在，有一个越狱工具可以绕过它。

XDA 论坛成员 [clrokr](http://forum.xda-developers.com/member.php?u=1935041) 首先发现了这个漏洞，XDA 资深成员 [netham45](http://forum.xda-developers.com/member.php?u=1854527) 用一个漂亮的小工具把它包了起来。它被称为 RT 越狱工具，允许用户在他们的 Windows RT 设备上签署未签名的应用程序。这是一个相当大的问题，因为大多数有趣的应用程序都是未签名的。

使用这个工具非常简单。它以 zip 文件的形式出现，必须先将其解压缩。一旦提取，用户运行*。包含 bat* 文件以打开菜单。有几个选项:用户可以只安装一次越狱，让脚本在每次登录时应用越狱，或者卸载工具。你可能注意到它说它只能安装一次。这种利用的一个警告——或者可能是一个优点——是它会在重启后消失。换句话说，如果你因为任何原因想要回去，很容易就可以删除。

这个工具还有其他一些有趣的事实。它不会让你运行 Photoshop、AutoCAD 等应用程序。您仍然只能安装 RT 应用程序。安装越狱并不会让传统 x86-64 应用突然兼容 ARM。但是，可以为 ARM 处理器编译的开源应用程序也可以工作。一个例子就是从已经在开发的桌面应用移植而来的越来越多的 ARM 兼容应用。此外，还有一些链接可以帮助人们解决 lib 问题和从源代码编译他们自己的应用程序。

也有一些问题。一些尝试这种方法的人可能会得到一个学士学位。这已经被追踪到只在登录后的前几分钟发生的事情。因此，如果您尝试它并获得 BSoD，请在下次重新启动后等待几分钟，然后重试。还建议您确保通过 Windows Update 完全更新。而且，因为它允许无符号的*。exe* 文件被安装，总有感染病毒的风险。因此，请确保您信任未签名应用程序的来源。

如果这看起来像是你想用你的 Windows RT 副本做的事情，那么检查一下 [RT 越狱工具线程](http://forum.xda-developers.com/showthread.php?t=2092158)以获得更多细节。