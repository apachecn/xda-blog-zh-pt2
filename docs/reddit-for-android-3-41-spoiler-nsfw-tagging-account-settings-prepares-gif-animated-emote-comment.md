# Android 3.41 的 Reddit 增加了剧透和 NSFW 标签，帐户设置，并准备添加 GIF 和动画表情评论支持

> 原文：<https://www.xda-developers.com/reddit-for-android-3-41-spoiler-nsfw-tagging-account-settings-prepares-gif-animated-emote-comment/>

甚至在阅读本文的第一句之前，你们中的一些人可能已经开始向下滚动到评论部分，告诉我们关于你认为更好的第三方 Reddit 客户端。这是一个古老的争论，总是引发互联网上的唇枪舌剑，但对大多数人来说，官方的 Reddit 移动应用程序做得很好。Android 和 iOS 移动应用程序的官方 Reddit 可能不会提供最佳的 Reddit 体验，但他们确实倾向于率先添加聊天支持等主要新功能。在一个更近的例子中，最新的 Android 测试版暗示将在评论中添加对嵌入式 gif 和动画表情的支持，但它也带来了一些新的生活质量功能。

这是最新测试版的官方变更日志:

*   剧透和 NSFW(不安全工作)标签现在可以在创建或编辑帖子时设置。这可以在键盘上方的“更多”(三个垂直点)按钮下找到
*   在“设置”屏幕中添加了一个新的“帐户设置”页面
*   小错误修复和性能改进

从左至右，以下三个截图显示了最新更新中的新功能。首先，在创建或编辑帖子时，你可以点击左下角的 3 点菜单，显示按钮，将帖子标记为 NSFW(不安全工作)和/或包含剧透。接下来，在设置中有一个新的帐户设置部分；在这里，你可以像在移动或桌面网站一样管理你的 [Reddit 个人资料的设置](https://www.reddit.com/prefs/)。最后，我们发现了一个新的通知开关，在你的 Reddit“蛋糕日”发生时提醒你。你创建 Reddit 账户的周年纪念日。每当您发表评论时，您的个人资料名称旁边都会出现一个蛋糕。出于某种原因，人们似乎很关心这个。)

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

Android v3.41 测试版 Reddit 中的新字符串还显示，该移动应用程序将很快支持在评论中嵌入 GIFS，在评论中使用动画表情符号，以及用颜色和最多 3 个徽章来设计您的用户名。这些功能将专为在 [/r/FortniteBR subreddit](https://new.reddit.com/web/special-membership/FortNiteBR) 上发表评论的 [Reddit Premium](https://www.reddit.com/premium) 订户提供。Reddit 管理员已经为浏览“新”Reddit 界面的桌面用户提供了这些功能，但他们一直在努力[将这些功能也带到手机上](https://www.reddit.com/r/FortNiteBR/comments/d06ej6/introducing_reddit_emotes_only_in_rfortnitebr/)。

```
 <string name="membership_crown_image_url">file:///android_asset/membership_paywall_crown.gif</string>
<string name="membership_demo_description_badges">Style your username with a badge and color</string>
<string name="membership_emotes_slide_description">Get access to premium animated emotes</string>
<string name="membership_emotes_slide_image_url">https://meta.redditmedia.com/public/all/mobile_assets/android/membership_tab_emotes.png</string>
<string name="membership_gifs_slide_description">Add GIFs to your comments</string>
<string name="membership_gifs_slide_image_url">https://meta.redditmedia.com/public/all/mobile_assets/android/membership_tab_gifs.png</string>
<string name="paywall_embed_gif_directly_in_your_comments">"Embed GIFs directly in your comments"</string>
<string name="paywall_get_up_to_3_badges">Get up to 3 badges</string>
<string name="paywall_loyalty_badges_subtitle">Show how long you’ve been supporting the subreddit.</string>
<string name="paywall_special_members_only">%1$s Only</string>
<string name="paywall_use_animated_emojis_in_comments">"Use animated emojis in comments"</string>
<string name="paywall_what_do_you_get">What do you get?</string> 
```

你可以从下面的谷歌 Play 商店下载最新稳定版的 Reddit for Android 应用程序。然而，3.41 版本目前还没有对公众开放。