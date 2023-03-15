# RCTD 去除器摆脱 LG 的根检查工具

> 原文：<https://www.xda-developers.com/rctd-remover-removes-lg-root-checking-tool/>

# RCTD 去除器摆脱 LG 的根检查工具

LG 的 RCTD 会导致 LG 设备的性能问题，因为它会检查 root，但不会终止进程，从而无限期地繁殖它们。这个应用程序阻止了这一点。

 <picture>![lg g7](img/a8596726f8240d1de7bac9988edbd2ba.png)</picture> 

LG Electronics' company logo is displayed at their news conference at the Consumer Electronics Show (CES) in Las Vegas January 7, 2013\. REUTERS/Rick Wilking

最近，我们在许多 LG 设备上发现了一个扫描 root 访问的系统模块。这款名为 [RCTD](https://www.xda-developers.com/lg-root-checker-tool-slow-performance/) 的工具在运行股票软件的 LG 手机被植入系统后被激活。这导致了设备运行速度变慢(因为进程永远不会停止)，也让一些用户对此感到不安。多亏了 XDA 论坛的主持人[zachare 1](https://forum.xda-developers.com/member.php?u=7055541)，我们现在可以用在 XDA 实验室找到的一个简单的应用程序来禁用这种检查。

[app box xda com . za chare 1 . rctdremoverforlg]

这个应用程序所做的是备份你的设备上的启动映像，通过注释掉一些代码来阻止 RCTD 进程的运行，从而在你的设备上修补它，然后将它刷新到你的设备上！这阻止了 RCTD 进程的产生和减慢你的设备，所以试试吧！