# 微软正在 Windows 11 家庭版中禁用并移除 SMB1 支持

> 原文：<https://www.xda-developers.com/microsoft-disable-smb1-windows-11-home-remove-future/>

微软宣布，从 Windows 11 的下一个主要版本开始， [Windows 11](https://www.xda-developers.com/windows-11/) Home 将不再默认提供 SMB1(服务器消息块版本 1)协议。这是摆脱长期被否决的协议的下一个重要步骤，一些用户仍然坚持使用该协议。此外，在未来，SMB1 二进制文件将被完全删除。

SMB1 是一种旧的网络协议，允许 PC 连接到某些网络设备，如硬盘驱动器和其他设备。该协议已经在 2007 年被 SMB 2 取代，并且在 2014 年被公开否决，所以微软想摆脱它是很自然的。

这个过程可以追溯到 2017 年，当时微软开始发售 Windows 10 和 Windows Server，没有开箱安装 SMB1 服务器服务。此外，大多数 Windows 版本也不再默认安装 SMB1 客户端服务。例外的是 Windows 10 的家庭版和专业版，直到一年后，Windows 10 Pro 也默认禁用了客户端服务。

尽管如此，Windows 10 家庭版及其后的 Windows 11 家庭版仍然启用了 SMB1 客户端服务。微软表示，它不得不等待一段时间才能禁用它，因为它知道这将是一些消费者的问题，他们不明白为什么他们的旧网络设备不再工作。

然而，它终于发生了，Windows 11 的下一个主要更新将于 2022 年下半年推出，将不再在家庭版中默认启用 SMB1 客户端服务。不过这只适用于全新安装——从当前版本的 Windows 升级的机器的设置不会改变，所以你不必担心系统崩溃。此外，您仍然可以通过控制面板手动启用 SMB1 支持。

不过，情况不会永远如此。微软今天还宣布，它将在未来的版本中从所有 Windows 11 和 Windows Server 版本中删除 SMB1 的二进制文件。这意味着您将不再能够简单地在您的机器上启用 SMB1 协议。为了适应跟不上变化的用户，微软表示将发布一个带外不支持的包，为真正需要的用户启用 SMB1。

我们不知道具体什么时候会发生，甚至今年晚些时候的更新也没有确定的日期。Windows 11 的首次发布发生在 10 月 5 日，所以我们预计下一次重大更新将在一年后到来，但这仍有待观察。

* * *

来源:[微软](https://techcommunity.microsoft.com/t5/storage-at-microsoft/smb1-now-disabled-by-default-for-windows-11-home-insiders-builds/ba-p/3289473)