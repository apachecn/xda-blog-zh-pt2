# Magisk 管理器从 Play Store 移除，开发者评论 Magisk 的未来

> 原文：<https://www.xda-developers.com/magisk-manager-removed-from-play-store-developer-responds-on-the-future-of-magisk/>

眼尖的社区成员发现，社区钟爱的项目之一 [Magisk](https://forum.xda-developers.com/apps/magisk) 在谷歌 Play 商店上不再可用。Magisk Manager 的 [Play Store URL 将会是 404，这表明该项目已经脱离了 Android 应用分发的主要和最受欢迎的来源。即使您之前下载了该应用程序，该列表也不会再显示在 Play Store 的“已安装应用程序”选项卡上。](https://play.google.com/store/apps/details?id=com.topjohnwu.magisk)

XDA 认可的开发者和 Magisk 的主要开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 在我们的论坛上阐明了这个问题:

*这是我今天早上从谷歌上得到的:*

*Magisk Manager，com.topjohnwu.magisk 因违反恶意行为政策，已被 Google Play 暂停并移除，作为政策打击。*

*所谓的“恶意行为”是什么？根据我的猜测，查看[对恶意行为](https://play.google.com/about/privacy-security/malicious-behavior/index.html)的定义，我很可能违反了以下两条政策:*

*   *引入或利用安全漏洞的应用。*
*   *从 Google Play 以外的来源下载可执行代码(如 dex 文件或本机代码)的应用程序或 SDK。*

*对于第一个策略:Magisk 绕过了谷歌严格的兼容性检查——对被篡改设备的 CTS 检查(SafetyNet 检查 CTS 状态)。CTS 是谷歌判断一家制造商是否可以将一款设备与其谷歌服务一起发运的标准，因此谷歌肯定非常认真地对待这个问题。另外，Magisk 为你的设备安装了根，修补了大量的 SELinux 策略(所有的根方法都这样)等等，这也是一个明显的安全漏洞。然而，我怀疑这是主要原因，因为许多超级用户管理应用程序也在 Play Store 上。*

*主要原因应该是另外一个。*

我列出的第二条规则可以解释为:你不能有任何“类似市场”的东西让用户在你的设备上下载和运行代码。显然，Magisk 的在线回购完全违反了这一规则。

如果是出于第二个原因，谷歌移除 Magisk 应该不会令人感到意外。谷歌不允许任何其他 Play Store 竞争对手进入 Play Store，无论其功能多么有限。这就是为什么我们在 Play Store 上的 [XDA 应用程序与我们论坛上的](https://play.google.com/store/apps/details?id=com.xda.labs.play&hl=en) [XDA 实验室应用程序](https://www.xda-developers.com/xda-labs/)不同且受限的原因之一。XDA 实验室有一个应用程序分发系统，这与谷歌 Play 商店的政策不兼容，因此 Play Store 上的 XDA 应用程序不支持该分发系统。

### 那么，Magisk Manager 现在从 Play Store 中删除后会发生什么情况呢？

[Topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 提到 [Magisk](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445/) 作为一个项目并没有被放弃，事实上，Magisk 最近已经取得了一些重大进展。开发商已经注意到他在这个阶段的选择:

*现在我有两个选择:从 Magisk Manager 中移除在线回购，在商店上重新发布一个**新的 app** (是的，一旦你的 APP 被拉下，包名和 APP 名被永久封禁)。*

另一种方法是通过 XDA 和第三方市场(就像 Xposed Installer 一样)发布应用程序。

我更喜欢第二个决定，因为我仍然可以使用相同的包名，而且我也不需要删除在线回购功能，这对于像 XDA 这样的开发社区来说是最宝贵的东西之一。我真正失去的是 Play 商店注册 lol 的 25 美元。

发展绝对是**而不是**以任何方式暂停，事实上，我最近有了显著的进步。 *还有一些 bug 没有整理出来，我需要一些用户的反馈，所以我决定 **开始一个新线程进行公测！*** *期待新线程很快上线，但我还是需要做一些小调整来应对不幸的 Play Store 情况....*

*所以结论是:是的，Magisk Manager 因违反政策被从 Play Store 中拉出来；不，这不是发展结束的标志。* *事实上，我认为 Magisk 正在经历发布以来最活跃的发展！*

尽管 Play Store 遭遇挫折，Magisk 仍在强劲发展。开发者坚持认为，Play Store 作为一种分发方式的消失并不意味着 Magisk 开发的结束。事实上，Magisk 的公测版即将推出，即将发布的 v13 版本号称是 Magisk 自发布以来最大的版本！Magisk 发生了很多变化，开发人员将寻找测试人员和用户来提供反馈和日志来解决问题。期待 Magisk 开发的更多消息。

Play Store 作为 Android 上的一个分发平台的受欢迎程度是无可争议的，失去它确实会影响到让你的应用程序对很大一部分 Android 用户可用的难易程度。然而，Magisk 并不像人们初步认为的那样受到影响。Magisk 只吸引那些需要 root 和其他定制的用户，这本身就意味着有更精明的受众。此外，您还可以加载 Magisk Manager apk，这对于希望利用 Magisk 功能的用户来说应该没什么大不了的。

### 谷歌拿走的东西，XDA 会归还

尽管如此，轻松更新的希望并没有破灭。 [Topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 已经将 [Magisk Manager 上传到了 XDA 实验室](https://labs.xda-developers.com/store/app/com.topjohnwu.magisk)，这让想要随时保持最新版本的用户很容易。

XDA 实验室是一个应用程序平台，是谷歌 Play 商店的替代品，在这样的时代，它是最合适的。你可以通过 XDA 实验室获得对 [Magisk 管理器](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445/)的更新，所以我们建议安装 XDA 实验室，以便在 Magisk 有新更新时得到通知。这也不是第一个应用程序从 Play Store 下架，但继续通过 XDA 实验室分发的例子，如 [AdAway](https://labs.xda-developers.com/store/app/org.adaway) 。

正如 topjohnwu 所提到的，Magisk 的更新即将到来。敬请期待！

[**获取 XDA 实验室**](https://labs.xda-developers.com/latest) [**通过 XDA 实验室获取 Magisk 管理器**](https://labs.xda-developers.com/store/app/com.topjohnwu.magisk) [**在我们的论坛中查看 Magisk！**](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445/)