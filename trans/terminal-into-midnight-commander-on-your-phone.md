# 终端进入午夜指挥官的电话

> 原文：<https://www.xda-developers.com/terminal-into-midnight-commander-on-your-phone/>

还记得[诺顿指挥官](http://en.wikipedia.org/wiki/Norton_Commander)和它开源的二表哥[午夜指挥官](http://en.wikipedia.org/wiki/Midnight_commander)吗？我们当然知道——显然，XDA 认可的开发商[维廉](http://forum.xda-developers.com/member.php?u=3918311)也知道。开发者没有简单地回忆过去，甚至没有创建一个基于触摸的文件管理器，而是将原来的应用程序移植到 Android 上。

Midnight Commander for Android 可以通过终端模拟器直接在您的设备上执行，但通过 SSH 运行时会提供更好的体验。要设置 SSH 访问，只需在你的设备上安装[droidshd](http://forum.xda-developers.com/showthread.php?t=976187)，在你的电脑上安装 [PuTTY](http://www.chiark.greenend.org.uk/~sgtatham/putty/) 。

你还不能轻易卸载午夜指挥官。虽然您可以删除 APK，但这只会删除卸载程序，而不是应用程序本身。也就是说，你没有理由需要卸载这个应用程序！

> **特性**
> 
> a)功能键起作用(F3 -查看，F5 -复制，F8 -删除，F10 -退出等...)
> 
> b)非常稳定，不会崩溃。
> 
> c)比前一个版本更容易安装(前一个版本需要一个额外的 apt-get 克隆，名为 ipkg 等)。下面将详细介绍这一点。
> 
> d)捆绑了 xterm (terminfo)和主要语言的语法突出显示。
> 
> e)我保留了包装脚本 4.6.2，但对其进行了更新，以便功能键能够工作。

为了重温过去的文件管理，你需要一个安装了 [BusyBox](http://forum.xda-developers.com/showthread.php?t=1102124) 的根设备。一旦你满足了要求，继续到[原始线程](http://forum.xda-developers.com/showthread.php?t=1243699)下载午夜指挥官安装程序。