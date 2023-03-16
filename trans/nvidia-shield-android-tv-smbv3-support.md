# NVIDIA SHIELD Android TV 将很快获得 SMBv3 支持

> 原文：<https://www.xda-developers.com/nvidia-shield-android-tv-smbv3-support/>

如今，我们的生活中充斥着越来越多的设备，对这些设备进行交互的需求也在不断增长。几十年来，人们一直使用服务器消息块(SMB)进行计算机联网，自其问世以来，已经经历了多次升级。大多数人使用它在计算机之间共享文件，但它已经发展成为一种通过无线进行打印机访问和串行端口访问的协议。那些拥有 NVIDIA Shield TV 的人会很高兴听到 SMBv3 即将到来，因为开发人员目前正在内部测试它。

SMB 最初是由 IBM 的 Barry Feigenbaum 设计的，其目标是将 DOS INT 21h 本地文件访问转变为网络文件系统。早在 1990 年，SMB 协议就与它的 LAN Manager 产品(3Com)合并了，该公司一直在为他们的 Windows 产品增加额外的功能。尽管 SMB 的最初版本不安全，但它被 SMB 2.0(或 SMB 2)取代，并于 2006 年包含在 Windows Vista 中。这次升级通过将命令/子命令的数量减少到 19 个，减少了 v1 的“喋喋不休”。

这次对 SMB2 的更新还增加了对符号链接的支持，文件属性的缓存，用 HMAC·SHA-256 散列算法改进的消息签名，等等。不过还是那句话，协议继续演进到 2.1、3.0、3.0.2，最近在 Windows 10 和 Windows Server 2016 中引入了 SMB v3.1.1。每次新的更新主要侧重于增加额外的安全性，但 SMBv3 还增加了 SMB 直接协议、SMB 多通道和 SMB 透明故障切换。

在 NVIDIA 论坛上周发布的一个新论坛帖子中，一名版主正式宣布，NVIDIA Shield TV 将在即将到来的更新中推出第 3 版。截至目前，该公司正在内部测试该功能，但它将在下一个预览版中向公众推出。NVIDIA 正在寻找那些使用下一个预览版来跨 Windows 和 Linux 测试该功能的人，并希望有人拥有多个服务器来安装(并使用各种类型的帐户，来宾，域，std 用户等)。).

那些最终在 Shield TV 的预览版中测试这一功能的人应该意识到其中的缺陷和副作用。所以，如果你是第一批测试新功能的人，请注意这一点。

* * *

[**来源:英伟达**](https://forums.geforce.com/default/topic/1073714/shield-tv/smb-v3-coming-soon/)