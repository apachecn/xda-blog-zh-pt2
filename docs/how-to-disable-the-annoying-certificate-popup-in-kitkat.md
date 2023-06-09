# 如何禁用 KitKat 中烦人的证书弹出窗口

> 原文：<https://www.xda-developers.com/how-to-disable-the-annoying-certificate-popup-in-kitkat/>

我妈妈总是告诉我安全很重要。她是对的。安全很重要，因为现在，设备可能被黑客攻击、网络钓鱼或以多种方式诈骗。这就是保护措施如此重要的原因，尤其是在公共场所。安全证书被发明并广泛用于防止小偷窃取我们的数据。

XDA 论坛成员 [forceu](http://forum.xda-developers.com/member.php?u=2683146) 似乎也很关心安全问题，因为他写了一个安装自定义安全证书的指南，以便在连接到 KitKat 中的某些网络时绕过“您的网络可能被监控”的消息。这种弹出窗口可能很烦人，它迫使你忽略实际上很重要的消息。

Forceu 随后发现可以将证书推送到*/system/etc/security/cacerts/*文件夹，设备会将其解释为可信证书。因此，对于你选择的特定网站来说，这个小烦恼将被永久禁用。证书文件必须以 PEM 格式保存，并按照指南中的建议进行编辑。该设备必须是根设备，以允许将文件复制到*/系统*分区。完成此过程后，可以从可信证书列表中自由启用或禁用新创建的证书。

请访问[导丝](http://forum.xda-developers.com/showthread.php?t=2533550)了解更多信息。