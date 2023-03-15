# Chainfire 为 Android 6.0 发布无系统 Root

> 原文：<https://www.xda-developers.com/chainfire-releases-root-for-android-6-0-without-modifying-system/>

如果你曾经根过一个设备，那么很有可能你听说过[](http://forum.xda-developers.com/member.php?u=631273)【链火】，XDA 资深版主，资深公认开发者。如果你没有，Chainfire 是 SuperSU、CF Auto Root、TriangleAway 和 CF.lumen 等热门作品背后的开发者，这使他成为 Android modding 社区中最有影响力的开发者之一。

 我们最近报道了 Chainfire 将 SuperSU 移交给 Code Code Mobile Technology LLC(CCMT)的决定，但指出 Chainfire 将继续使用 SuperSU，最终在两年内逐步淘汰自己。

说到做到，Chainfire 仍然参与 SuperSU，他刚刚发布了 Android 6.0 棉花糖的 [root，而没有对/system 分区](http://forum.xda-developers.com/showpost.php?p=63197935&postcount=2)进行修改。这被贴上了**实验**的标签，因为其背后的想法有一些警告，其中主要是工厂重置设备将删除 root。

> 为了在现代 Android 版本上拥有根，我们需要我们的文件是可执行的，并且我们的守护进程在引导时启动。我们通常通过修改/system、接入 init 执行的二进制文件和脚本来实现这一点。如果我们还修改了引导映像，那么我们应该能够在根本不修改系统的情况下完成所有这些工作。

那么，我们能从无系统的根中得到什么好处呢？我们联系了 Chainfire，与传统 SuperSU 相比，它的优势包括:

1.  更干净的方法和设计
2.  更容易拔出
3.  无照明/系统分区
4.  排除“sugote”之类的东西，安卓 6.0 棉花糖上不需要
5.  OTA 现在稍微容易一些，因为刷新引导映像通常比刷新整个/系统更容易。
6.  最重要的是，如果您没有正确的内核安装，这不会使您的设备变软。以前的 Android 6.0 方法需要在内核中安装 SELinux 策略补丁，否则设备将无法启动。使用这种方法，如果支持内核不存在，您将没有根，但设备将启动。

正如所料，这种新方法不能与旧的根方法协同工作，因为新方法不能清理旧的根文件。因此，您需要刷新您的股票/系统分区，以确保在开始之前有一个干净的石板。

如需下载，请前往[论坛帖子](http://forum.xda-developers.com/showpost.php?p=63197935&postcount=2)。开发人员要求讨论应该在[超级测试线程](http://forum.xda-developers.com/apps/supersu/2014-09-02-supersu-v2-05-t2868133)上进行，所以请前往那里进行一般性讨论。请记住，这是**的实验版**，很可能会有错误，所以风险自担。

更新:Reddit 用户 MajorNoodles [通知【Android Pay 可以在他的 Nexus 5 上运行。在](https://www.reddit.com/r/Android/comments/3qu3zk/chainfire_systemless_root_experiment/cwiezgg)[的 Google+帖子](https://plus.google.com/+Chainfire/posts/aJbqUZ8PEP4)上，Chainfire 确实提到 Android Pay 的运行是偶然的，而不是故意的。他预计 Android Pay 将在未来更新，以抵消这一点。