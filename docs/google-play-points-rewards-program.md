# Google Play Points 是一个即将推出的奖励计划，每次购买都会给你积分

> 原文：<https://www.xda-developers.com/google-play-points-rewards-program/>

# Google Play Points 是一个即将推出的奖励计划，每次购买都会给你积分

谷歌 Play 商店的最新版本暗示了一项名为“Google Play Points”的奖励计划，该计划将为您的每次购买提供积分。

谷歌提供了一些方法，你可以为他们的服务做出贡献，以获得一些额外的好处。例如，你可以成为谷歌地图的当地导游，或者参加谷歌意见奖励的调查。你可以加入的一个新项目叫做“Google Play Points”根据字符串判断，这将是一个忠诚度/奖励计划，允许您在 Google Play 中购买的所有商品被动赚取积分。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

## Google Play 积分——Play 商店的奖励计划

以下字符串是通过对从 [APKMirror](https://www.apkmirror.com/apk/google-inc/google-play-store/google-play-store-11-6-15-release/) 获得的最新版本谷歌 Play 商店 11.6.15 中的 strings.xml 执行 diff 并将其与 11.4.17 版本进行比较而获得的。字符串显示，您每次购买都会获得积分，这些积分可以兑换为应用内项目或 Google Play 点数。有一个字符串表示，你每消费 100 英镑(约 0.90 美元)就能获得 1 点积分，不过谷歌可能会将美国客户的积分提升至 1 美元。字符串中没有显示其他地区的比率。

### 谷歌 Play 商店版本 11.6.15 的 Google Play 点字符串

```
 <string name="loyalty_help_menu">Help</string>
<string name="loyalty_home_points_expiry">Exp %1$s</string>
<string name="loyalty_home_points_expiry_content_description">Points expire on %1$s</string>
<string name="loyalty_level_benefits_menu">Level Benefits</string>
<string name="loyalty_points_balance_content_description">You have %1$d points</string>
<string name="loyalty_side_nav_content_description">%1$s. %2$s</string>
<string name="loyalty_side_nav_new">New</string>
<string name="loyalty_signup_bottom_notification_bar_subtitle">Join Google Play Points</string>
<string name="loyalty_signup_bottom_notification_bar_title">Earn points on all purchases</string>
<string name="loyalty_signup_error_dialog_generic_text">Something went wrong. Try joining Play Points again.</string>
<string name="loyalty_signup_interstitial_body">Earn points on everything you buy. Use points for special in-app items or Google Play credit.</string>
<string name="loyalty_signup_interstitial_body_jp">Earn 1 point per ¥100 on everything you buy. Use points for special in-app items or Google Play credit.</string>
<string name="loyalty_signup_interstitial_secondary_button_label">Not now</string>
<string name="loyalty_signup_interstitial_title">Introducing Google Play Points</string>
<string name="loyalty_terms_of_service">Terms of Service</string>
<string name="loyalty_tiers_page_title">Levels</string>
<string name="play_points">Play Points</string>
<string name="points_history">Points History</string>
<string name="points_history_empty_view_description">This is where you can track the points you earn and use</string>
<string name="points_history_empty_view_title">Nothing here yet</string> 
```

字符串还显示，将有“水平的好处。”在最新版本的游戏商店中有几个新的图片，显示将有 5 个级别:铜，银，金，白金和钻石。不幸的是，字符串并没有告诉我们你将在每个级别得到什么好处。

我反编译了这个应用程序，查看了一下代码，但是没有发现太多额外的信息。我找到了这张图片的链接，它给出了一个从火徽:英雄等游戏中购买应用内物品的例子，以及如何将其转化为奖励(看起来像糖果粉碎的游戏内货币。)

一旦该计划上线，支持页面将在[链接](https://support.google.com/googleplay/?p=play_points_topic)处可用。如果我们了解到更多关于 Google Play 积分的信息，我们会通知大家。