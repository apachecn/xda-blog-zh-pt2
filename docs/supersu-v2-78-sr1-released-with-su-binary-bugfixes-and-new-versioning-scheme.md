# SuperSU v2.78 SR1 发布了 SU 二进制错误修复和新的版本控制方案

> 原文：<https://www.xda-developers.com/supersu-v2-78-sr1-released-with-su-binary-bugfixes-and-new-versioning-scheme/>

XDA 知名开发者 [Chainfire](http://forum.xda-developers.com/member.php?u=631273) 已经[发布了他的 SuperSU 应用](https://plus.google.com/+Chainfire/posts/8mPirmjhgqT)的更新，包括一些错误修复和一个 supolicy 的关键更新。

用这个人自己的话来解释 supolicy 的关键更新是最好的:

由于 v2.68 BETA 中引入的初始化错误，一些 SELinux 上下文(包括 shell 和不可信 _app)可能被授予 sys_module 功能。**如果**发生这种情况，**和**你的内核编译有模块加载支持(大多数现代的普通内核都禁用了这个)**和**利用漏洞获取 uid 0，这个**然后**允许完全的 SELinux 旁路和内核 pwn。

Chainfire 提到，该漏洞所需的确切组合使其被利用的机会非常小。尽管如此，这是一个漏洞，现已在此版本中修复。因此，建议通过刷新 SuperSU zip 来更新 SuperSU，因为 apk 更新在这种特定情况下是不够的。

变更日志的其余部分如下:

*   子二进制:用操纵的挂载名称空间调整 app_process 检测
*   子二进制:将合子 PID 检测调整为首选 64 位
*   子二进制:修复 LD_PRELOAD 清理中可能出现的 NPE
*   子二进制:在无系统模式下，确保路径包含/su/bin 和/su/xbin
*   政策:确保新规则的零分配
*   supolicy:修复解析允许在单个定义中使用多个源/目标的 xperm
*   ZIP/Systemless:给 su.d 60 秒来执行(从 4 秒开始)

除此之外，这个 v2.78 SR1 还为 SuperSU 使用的版本系统带来了变化。通过此次更新，SuperSU 将从 BETA 版升级到 Service Release 命名方案。下一个测试版本将使用与当前稳定版本相同的主版本号，这意味着 v2.78 SR1 将被称为 v2.79 Beta。版本号将保持不变，以降低人们试图将测试版本上传到 Google Play 以外的应用商店的效率，因为大多数非 Play 商店不接受已经存在的版本号。

你可以从这里下载 v2.78 SR1 [的 flashable zip。或者，同样的论坛主题可以在](https://download.chainfire.eu/1003/SuperSU/SR1-SuperSU-v2.78-SR1-20160915123031.zip)[这里找到](http://forum.xda-developers.com/apps/supersu/2014-09-02-supersu-v2-05-t2868133)。

* * *

Chainfire 还借此机会提到了一些即将发布的与 Code Code Mobile Technology LLC 相关的公告。我们之前讨论过他们和 SuperSU 的未来，如果你想看的话。我们将关注即将发布的公告。

你试过最新的 SuperSU 吗？请在下面的评论中告诉我们！