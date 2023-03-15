# MT6752 和 MT6732 设备的非官方 Stagefright 补丁

> 原文：<https://www.xda-developers.com/unofficial-stagefright-patches-for-mt6752-mt6732-devices/>

我们之前已经讨论过[什么是](http://www.xda-developers.com/stagefright-explained-the-exploit-that-changed-android/)，也给出了[类似舞台恐惧错误的代码演示](http://www.xda-developers.com/a-demonstration-of-stagefright-like-mistakes/)。不用说，如此大规模的漏洞被认为是相当严重的事件。这一漏洞给几家制造商和谷歌敲响了警钟，他们中的大多数人都醒悟过来，赶紧保护自己的设备(和用户)。

但是，由于我们并不是生活在一个理想的世界里，有些设备可能永远也不会受到制造商的青睐。这些设备将继续运行在有漏洞的 Android 版本上，不断将用户暴露在此类漏洞的风险之下。

值得庆幸的是，对于这些设备中的一小部分，特别是那些运行在特定联发科 SOC 上的设备，帮助已经以[非官方 Stagefright 补丁](http://forum.xda-developers.com/android/development/bug-fix-stagefright-t3193219)的形式出现。由 XDA 公认的开发者和贡献者 [superdragonpt](http://forum.xda-developers.com/member.php?u=5238428) 创建的可闪存恢复文件修补了所有被研究公司 Zimperium 列为 Stagefright 相关漏洞的 CVE。

该补丁据称可在所有 MT6752 和 MT6732 设备上工作，并已确认可在许多手机上工作，包括嘉誉 S3、iOcean Rock 和 ZOPO ZP920 (MT6752 设备)以及 UMI 锤子和 Elephone P6000 (MT6732 设备)。

如果这是您第一次听说这些设备，您可以想象它们收到安全补丁更新的可能性有多大。在这种情况下，由业余爱好者开发人员自愿提供的非官方补丁和修复程序成为长期安全性和可用性的唯一手段。

更新这个补丁的先决条件是在 Android 5.1.1 上进行自定义恢复，但你应该在继续之前创建一个备份(即使没有说明，这也是一个好主意)。如果你拥有任何这些设备，或任何其他基于 MT6752 或 MT6732 的设备，前往[论坛线程进行讨论](http://forum.xda-developers.com/android/development/bug-fix-stagefright-t3193219)。

你有一台永远不会更新 Stagefright 补丁的设备吗？你采取了什么措施来保护自己？请在下面的评论中告诉我们！

阅读相关报道: