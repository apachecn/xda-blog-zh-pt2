# 谷歌测试版测试“发现”,作为谷歌订阅的更名

> 原文：<https://www.xda-developers.com/google-feed-rebrand-discover/>

去年，谷歌放弃了 Now 品牌，[引入了 Feed](https://www.xda-developers.com/google-improves-the-feed-experience-of-the-google-app/) 。Google Feed 可以让你快速获取算法认为你会感兴趣的当地天气和新闻。Feed [并非在每个国家都可用](https://www.xda-developers.com/enable-google-feed-any-country/)，尽管谷歌最近[宣布计划](https://www.xda-developers.com/google-for-india-event-announcements/)为更多地区提供支持。Feed 也失去了许多让 Now 如此受欢迎的功能，尽管[新的视觉快照 UI](https://www.xda-developers.com/google-assistant-google-now-cards/) 带回了 Google Now 的一些漂亮功能。虽然我们不知道谷歌在 Feed 中有什么新功能，但我们知道谷歌目前正在测试其品牌重塑。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

## 认识一下“发现”——新的 Google Feed？

首先由 XDA 公认的开发者 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) ( [强大的奎因应用](https://kieronquinn.co.uk/)的基隆·奎因)发现，也得到我们的证实，谷歌可能会将 Feed 更名为“发现”当我们打开最新版本的谷歌应用程序时，对“Feed”的引用被 Discover 所取代。此外，还有一个我们从未见过的新标志。

我们用 PNF 软件提供的 [JEB 反编译器反编译了 app，发现了相关的字符串。](https://www.pnfsoftware.com/?aid=xdadev)

```
 <string name="access_discover_promo">Check out Discover</string> 
```

我们还搜索了出现在“Check out Discover”下面的字符串，发现它是现有 Google Now/Google Feed 字符串的一部分。谷歌可能正在测试更名，看看如果 Feed 被称为 Discover，是否会有更多用户使用它。

```
 <string name="access_now_promo">Check out your feed</string>
<string name="access_now_promo_content_description">Access your Google Feed</string>
<string name="access_now_promo_detail">Tap to see updates and stories based on your interests</string> 
```

尽管我们设法手动激活了这一功能，但我们的 Telegram 组中至少有一名用户看到了新的徽标以及之前发现的“热门应用”部分，尽管他们的设备缺少图标标签。

*感谢我们电报组的@atulAn！*