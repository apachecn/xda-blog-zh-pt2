# PSA:播放服务更新打破钛备份和底层。这里有一个解决办法。

> 原文：<https://www.xda-developers.com/psa-play-services-update-broke-titanium-backup-substratum-heres-a-fix/>

最近，很多用户的某些流行的根应用程序，如钛备份和底层开始遇到一些奇怪的问题。

突然，当试图恢复应用程序时，Titanium Backup 会[卡在 0%](https://forum.xda-developers.com/nexus-6p/help/tibu-stuck-0-restoring-apps-t3569959) 处，Substratum 用户注意到主题无法应用。一些用户认为问题是[与 USB 调试](https://forum.xda-developers.com/v20/how-to/solution-to-titanium-backup-stuck-0-t3569855)被启用有关，但禁用该功能也没有帮助。

各种设备上的这些应用恢复应用的所有根用户几乎在同一时间开始出现这些问题，所以很明显，问题不在于应用本身。Substratum 团队成员乔治 G 和 [XDA 认可的开发者尼古拉斯查姆](https://forum.xda-developers.com/member.php?u=3605033)推测这些强制关闭可能与最近的 Google Play 服务更新有关。沿着这条思路，他们发现了似乎至少是这个问题的临时**解决方案。**

修复非常简单直接。你所需要做的就是导航到位于**设置- >谷歌- >安全**中的“**验证应用**”部分。一旦你到达“验证应用程序”部分，**禁用功能**。然后前往开发者选项并**取消勾选“通过 USB 验证应用程序”**选项。就是这样。成功完成上述两个步骤后，您应该可以再次在您的设备上完美地运行 Substratum 和 Titanium Backup。

由于谷歌显然正在加强其服务器端“验证应用程序”功能的安全性，因此降低 Google Play 服务应用程序的等级是行不通的。但是现在我们已经为我们的根用户提供了一个修复，这对于那些用户来说应该是一个令人满意的妥协。只是要格外小心你正在安装的应用程序，因为启用这个补丁你是故意禁用谷歌的安全功能。

就对底层感兴趣的开发者而言，Nicholas Chum 在一篇 G+帖子中表示，开发者可能想看一看这个提交以了解这个问题是如何修复的。然而，如果 OMS7 无根提交已经被合并，上面链接的提交可以被忽略。

* * *

这个修复对你有用吗？请在下面的评论中告诉我们！