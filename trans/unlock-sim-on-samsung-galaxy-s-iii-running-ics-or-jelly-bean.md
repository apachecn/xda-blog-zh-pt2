# 轻松解锁三星 Galaxy S III 的 SIM 卡

> 原文：<https://www.xda-developers.com/unlock-sim-on-samsung-galaxy-s-iii-running-ics-or-jelly-bean/>

锁定你的 SIM 卡通常不会引起很多问题。当然，这意味着你卡在了你当前使用的任何一个载体上，但是除此之外，它并没有真正地阻碍诸如 root，flash rom 等等。这并不是说解锁 SIM 卡没有用。那些旅行或只是想消除运营商限制的人可以从 SIM 解锁设备中受益。现在，[三星 Galaxy S III](http://forum.xda-developers.com/forumdisplay.php?f=1563) 的用户可以解锁他们的模拟市民，这样他们就可以随心所欲了。

该方法以 zip 文件的形式出现，其中包含一些必须移动到 Galaxy S III EFS 文件夹中的文件。由 XDA 公认的开发者 [zohawkish](http://forum.xda-developers.com/member.php?u=2018170) 发布，方法很容易做到。正如 zohawkish 解释的那样:

> -首先你需要在安全的地方备份你的“EFS 文件”。
> 
> -你必须在解锁的股票固件中，比如 BLG8(使用 voodoo app+libsec-RIL . so(Mike 1986 fix))
> 
> -解压缩附带的 zip“EFS . zip”
> 
> -复制文件(。nv_core.bak，。nv_core.bak.md5)添加到您的 EFS 文件中
> 
> -重启并享受吧！！！

当然，也有一些潜在的并发症。如上所述，你需要备份你的 EFS 文件以防出错。此外，如果您想要更新到未来的果冻豆版本，您必须恢复您备份的 EFS。除此之外，用户报告说，国防部工程完美。

**编者注:**OP 不再支持实际线程，因此它已被关闭。