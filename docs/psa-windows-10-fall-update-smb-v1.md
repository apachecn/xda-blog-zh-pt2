# PSA: Windows 10 秋季更新禁用 SMB v1，破坏许多 Android 文件管理器应用程序

> 原文：<https://www.xda-developers.com/psa-windows-10-fall-update-smb-v1/>

# PSA: Windows 10 秋季更新禁用 SMB v1，破坏许多 Android 文件管理器应用程序

SMB v1 是近年来众多安全噩梦的原因，所以微软终于在 Windows 10 的最新更新中杀死了它。

共享消息块(SMB)是一种允许通过无线方式进行文件传输访问、打印机访问和串行端口访问的协议。它是 Windows 独有的，因此该协议的另一个名字是“微软 Windows 网络”。然而，中小企业极易受到攻击，它是 2014 年索尼影业(Sony Pictures)黑客攻击的原因，也是几个月前 WannaCry 恶意软件的原因。实时攻击跟踪显示，SMB 仍然是攻击客户端的主要方法之一，因此随着 Windows 10 秋季更新，SMB v1 已被禁用。这并不意味着该协议完全消失，而是被 SMB v2 取代。唯一的问题是，许多应用程序不能再使用类似的协议将文件无线传输到 Windows 电脑。没有一个像 SMB 一样轻松。在此之前，微软已经发布了如何在 Windows 中禁用 SMB v1 的指南。

然而，正如我们仅在几个月前提到的，有一个文件浏览器实际上支持 SMB v2。FX 文件浏览器[在 8 月份](https://www.xda-developers.com/fx-file-explorer-6-0/)进行了更新，加入了新的用户界面，更重要的是，SMB v2 支持。SMB v1 和 SMB v2 之间没有太大的区别，主要都是安全修补。这一变化可能会对许多积极使用该功能的人造成不利影响，但随着 FX File Explorer 已经支持新协议和强制切换，其他应用程序开发者可能也会效仿。

WannaCry 之类的勒索软件也通过 SMB v1 传播，因为网络上的所有 Windows 机器都默认支持来自同一网络的 SMB v1 连接。这意味着恶意软件可以轻松快速地传播，因此堵住漏洞并删除 SMB v1 无疑是正确的举措。如上所述，如果您积极使用它，那么在删除它时应该会有一些初始问题，但是会有替代方案，并且很快应用程序就会支持新的协议。

* * *

[**来源:微软支持**](https://support.microsoft.com/en-us/help/4034314/smbv1-is-not-installed-windows-10-and-windows-server-version-1709)