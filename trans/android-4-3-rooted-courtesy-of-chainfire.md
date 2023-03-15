# Android 4.3 源自 Chainfire

> 原文：<https://www.xda-developers.com/android-4-3-rooted-courtesy-of-chainfire/>

最近发布的谷歌版 Galaxy S4 自发布以来一直令人兴奋不已。很多人没有预料到的是果冻豆 4.3 的泄露。尽管只包含一些可能会影响普通最终用户的微小变化，但我们仍然可能会发现一些差异。

最近泄露的基于 Android 4.3 的三星固件(JWR66N)被发现在最初的 TouchWiz 加载的[骁龙驱动的 Galaxy S4](http://forum.xda-developers.com/forumdisplay.php?f=2162) 上工作得相当好。然而，它直到今天才可根化，因此对于那些离不开根应用程序的人来说，它不是一个可行的选择。Cue XDA 精英公认的开发者 [Chainfire](http://forum.xda-developers.com/member.php?u=631273) 和他的改装版 [SuperSU](http://forum.xda-developers.com/showthread.php?t=1538053) ，专门适配 4.3 使用。

 **这个漏洞是由 Chainfire 在 Google+的一篇文章中公开的，它准确地解释了为什么需要一个修改过的 SuperSU。用 Chainfires 自己的话来说，这和普通版 SuperSU 的主要区别在于:

> 对于这个根，SuperSU 以守护模式运行(新特性)，并在引导期间启动。
> 
> 守护进程处理所有的 su 请求，虽然这应该大部分工作正常，但一些应用程序可能希望它们的 su 会话运行在进程树上的同一个分支上，作为启动会话的应用程序。

这些变化是因为三星还是仅仅因为 Android 4.3 还有待观察。但不用说，一旦我们看到更多基于 4.3 的固件，我们就会有答案了。还有一些你想知道的其他区别，尤其是那些使用基于 CWM 的恢复的人，所以我强烈推荐你完整地阅读这篇文章。

如果你的 S4 正在运行 4.3 版本的漏洞，这可能是你已经期待了几天的事情了。flashable zip 文件本身可以从 [Google+ post](https://plus.google.com/+Chainfire/posts/WqS2E9kkN1L) 下载，任何相关问题都应该使用当前的 [SuperSU 线程](http://forum.xda-developers.com/showthread.php?t=1538053)。**