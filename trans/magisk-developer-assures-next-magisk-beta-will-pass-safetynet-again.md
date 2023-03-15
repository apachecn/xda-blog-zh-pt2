# Magisk 开发者保证下一个 Magisk 测试版将再次通过 SafetyNet

> 原文：<https://www.xda-developers.com/magisk-developer-assures-next-magisk-beta-will-pass-safetynet-again/>

今天早些时候，开始有报道称，谷歌更新了他们的 Play 服务，导致 Magisk 等当前“安全”的根方法再次无法通过 SafetyNet 检查。这意味着带有 root 和其他修改的设备再次被 SafetyNet 检测到，随后在试图使用依赖 SafetyNet 的应用程序(如 Android Pay)时被阻止。

XDA 公认的开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 已经[在 Magisk 论坛帖子](https://forum.xda-developers.com/showpost.php?p=72665021&postcount=501)中发表评论，向用户保证他已经意识到了这些变化，并且已经完成了必要的修改，再次绕过了谷歌的安全网检查，同时仍然保留了 root 和 Magisk 模块的功能。

在随后的澄清帖子中， [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 提到安全网故障是由谷歌使他们的检测更加严格引起的，但开发者能够解决它。**目前还没有可供用户刷新和绕过新政策的版本，但我们可以期待未来有一个**。局势在[topjohnwu](https://forum.xda-developers.com/member.php?u=4470081)的控制之下，所以我们目前所能做的就是等待下一个 Magisk 测试版。

[Topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 进一步展开，可能不存在任何有效的方法来完全阻止 magiskhide 工作。因此，当谷歌推出新的安全网检查时，magiskhide 只需要一次更新就能领先一步。这之所以成为可能，是因为 Magisk 可以作为根用户运行，而 SafetyNet checks 则不能。特权优势允许 Magisk 对 SafetyNet 进程可以看到的内容进行更多的控制。

困难的是找到一个隐藏 Magisk Manager 主应用程序的好方法。几个应用程序已经开始通过包名检测 Magisk Manager 应用程序的存在，因为 Android 允许任何应用程序知道设备上安装了什么其他应用程序。这种“检查”是相当初级的，因为对于主要的应用程序开发人员来说，更改包名是一项微不足道的任务(尽管这仍然是一个有其自身缺点的决定)。简单地安装一个特定的应用程序也不能充分证明修改的存在，因此“检查”也会产生相当数量的误报。

但是因为这种类型的检查是初级的，所以对于正在为他们的应用程序寻找“免修改”设备的开发人员来说，实现它是很容易的。Magisk 可以通过简单地改变它的包名来隐藏自己，但是应用程序可以开始检查修改后的包名；如此等等，因此对任何一方都没有真正解决这个问题。

Magisk 针对这种基本检查的一个可能的解决方案是将代码注入 Android 的 PackageManager，以从已安装的应用程序列表中过滤掉 Magisk Manager。这既可以通过 Xposed(但 Xposed 本身破坏了 SafetyNet，Xposed 仅限于较老的 Android 版本)，也可以通过修改 oat/dex 文件直接修补框架的 Java 代码。

目前， [Topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 并不希望专注于绕过这些基本的检查，因为 magiskhide 的主要兴趣点是绕过谷歌的安全网检查。用户可以期待很快进行更新，允许 SafetyNet reliant 应用程序再次开始与 root 和 Magisk 模块一起工作，尽管我们要求用户不要通过在相同的模块上请求 eta 来麻烦开发者。

**对于 Google 的 SafetyNet 和 Magiskhide 之间这场猫捉老鼠的游戏，你有什么想法？请在下面的评论中告诉我们！**

[**来源:Magisk 论坛**](https://forum.xda-developers.com/apps/magisk/beta-magisk-v13-0-0980cb6-t3618589/post72666791#post72666791)