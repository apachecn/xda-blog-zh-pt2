# 谷歌应用 v7.20 测试版暗示了新的助手 Hotword、智能显示器的双核集成等等

> 原文：<https://www.xda-developers.com/google-app-v7-20-beta-teardown/>

谷歌应用 7.20 测试版现已向 Play Store 上注册谷歌应用测试版的用户推出，尽管谷歌尚未发布官方更新日志，但我们在 APK 进行了拆解，发现了一些与谷歌助手、谷歌双显示器对智能显示器的支持等相关的变化。我们在下面做了记录。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

* * *

## Google Duo 通过智能显示屏打电话

“Jasper”是由谷歌助手驱动的智能显示器的代号。它们是来自 LG、索尼、JBL 和联想等公司的新型智能扬声器，带有触摸屏显示器，可以播放视频，从[谷歌照片](https://www.xda-developers.com/try-google-lens-launcher-google-photos/)中调出图片等等，谷歌应用 7.20 测试版的字符串显示，它们将能够通过[谷歌二人组](https://www.xda-developers.com/google-duo-vilte-integration-pixel-nexus/)进行视频通话。有对 Knock-Knock 的内置支持和一个新的**视频通话**菜单，允许用户登录、注销或取消链接阿朵账户。

```
 <string name="assistant_device_id_jasper_duo_preference_category_title">Video calls</string>
<string name="assistant_device_id_jasper_duo_preference_category">assistantDeviceIdJasperDuoCategory</string>
<string name="jasper_duo_account_title">Duo Account</string>
<string name="jasper_duo_knock_knock_summary">See the caller's video before you pick up. And let people you call see your video while their phone rings. &lt;a href=\"https://support.google.com/duo/answer/6376115\"&gt;Learn more&lt;/a&gt;</string>
<string name="jasper_duo_knock_knock_title">Knock-knock</string>
<string name="jasper_duo_not_signed_in">Not signed in</string>
<string name="jasper_duo_signed_in">Signed in</string>
<string name="jasper_duo_unlink">Unlink</string> 
```

## 一个新的热门词汇

此次拆除也暗示了谷歌将很快启用除“OK Google”和[“嘿 Google”](https://www.xda-developers.com/hey-google-voice-command-google-assistant/)之外的第三个热词的可能性。但是，我们只能推测到这一点。

```
 <string name="hotword_enrollment_enroll_listening_talkback_assistant_device_again">Say it again</string>
<string name="hotword_enrollment_tgoogle_summary_header_title">\"%1$s\" is now available</string>
<string name="hotword_enrollment_tgoogle_summary_usage_example_first">"%1$s, what's my name?"</string>
<string name="hotword_enrollment_tgoogle_summary_usage_example_second">"%1$s, what's the traffic to work?"</string>
<string name="hotword_enrollment_tgoogle_summary_usage_example_third">%1$s, tell me about my day.</string>
<string name="hotword_enrollment_tgoogle_summary_usage_sample_end">You can also still say \"%1$s\" and \"%2$s\" to talk to your Assistant.</string>
<string name="hotword_enrollment_tgoogle_summary_usage_sample_title">Your Assistant will now respond when you say things like:</string>

<string name="user_defined_action_task_custom_query_query_summary">You can enter any Google Assistant command.</string>
<string name="user_defined_action_task_custom_query_query_title">What custom command would you like to run?</string>
<string name="user_defined_action_task_custom_query_title">Custom command</string>

```

## Smart Displays 通知和提醒

它还展示了为智能显示器提供动力的软件平台的发展，被称为“石英”。我们看到了通知、提醒徽章、提醒和回放控制的占位符(例如，**暂停**和**播放**)。

```
 <string name="quartz_badge_view_less_than_ten">%1$d</string>
<string name="quartz_badge_view_ten_or_more">9+</string>
<string name="quartz_notification_list_title">Notifications</string>
<string name="quartz_notification_type_other">Notification</string>
<string name="quartz_notification_type_reminder">Reminder</string>
<string name="quartz_photo_list_slideshow_button_pause_content_description">Pause</string>
<string name="quartz_photo_list_slideshow_button_play_content_description">Play</string> 
```

## 新订单跟踪消息

谷歌似乎也在研究更详细的订单跟踪信息。新的字符串包含标签，指示物品何时发货，预计何时送达，以及递送是否被取消或延迟。

```
 <string name="order_group_header">Orders</string>
<string name="shipped">Shipped</string>
<string name="shipped_with_estimation">Shipped, delivery expected %s</string>
<string name="expect_delivery_day">%s</string>
<string name="out_for_delivery">Out for Delivery</string>
<string name="delivered">Delivered</string>
<string name="available_pick_up">Available for Pickup</string>
<string name="delayed">Delayed</string>
<string name="cancelled">Cancelled</string>
<string name="returned">Returned</string>
<string name="action_required">Action Required</string>
<string name="more_orders">More Orders</string> 
```

## 播客管理功能

最后，我们看到播客方面的一些发展。目前，谷歌应用程序没有原生播客管理器，也不清楚谷歌何时(或是否)会推出这一功能。但是新的字符串显示了播客下载器、订阅管理器等等的开端。

```
 <string name="sign_in_message">Sign in to subscribe to podcasts and access your listening history on other devices</string>
<string name="sign_in_reject">Not now</string>
<string name="sign_in_accept">Sign in</string>
<string name="downloads">Downloads</string>
<string name="downloaded_episodes">Downloaded episodes</string>
<string name="download_setting_message">Downloaded episodes are removed after 30 days or 24 hours after completion</string>
<string name="all_downloaded_episodes">All downloaded episodes</string>
<string name="homebase_link_tool_tip_message">See your subscriptions here</string>
<string name="opt_in_message">Web &amp; App Activity is turned off. Turn it on to access your podcasts and listening history on other devices.</string>
<string name="remove_completed_episodes">Remove completed episodes</string>
<string name="remove_unfinished_episodes">Remove unfinished episodes</string> 
```

如果我们在拆解中发现更多有趣的东西，我们会更新这个帖子。

如果您正在寻找最新的谷歌应用测试版，[注册预览计划](https://play.google.com/apps/testing/com.google.android.googlequicksearchbox)并从谷歌 Play 商店更新谷歌应用。