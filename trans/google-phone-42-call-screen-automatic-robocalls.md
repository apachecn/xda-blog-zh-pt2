# 谷歌 Pixel 的通话屏幕可能会开始自动筛选 robocalls

> 原文：<https://www.xda-developers.com/google-phone-42-call-screen-automatic-robocalls/>

我们可以整天讨论 Pixel 智能手机的硬件质量，但我相信我们大多数人都同意，软件是 Pixel 设备真正闪光的地方。每个新的 Pixel 设备都引入了新的软件功能，在社区中广受欢迎，对于 Pixel 3 来说，其中一个新功能是呼叫屏幕。这项功能适用于所有 Pixel 设备，甚至一些摩托罗拉手机也可以使用，它通过回答一系列问题来找出你为什么被呼叫，从而帮助你免受机器人呼叫者的攻击。描述呼叫屏幕让它看起来非常“智能”，但实际上，启动它和选择响应都是用户控制的。然而，这可能会在即将到来的更新中发生变化，因为我们发现了新的自动呼叫屏幕功能的字符串。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

今天早上早些时候，谷歌手机 v42 在谷歌 Play 商店推出，更新的 APK 也可以在 APKMirror 上找到。我们下载了 APK 并解码资源来寻找新的字符串。在最新的更新中，我们发现了大量与代号为“revelio”的功能相关的字符串自 8 月初首次添加代码以来，我们一直在跟踪这项功能的开发，但当时还不清楚它是新的呼叫筛选功能还是垃圾邮件检测功能。琴弦现在清楚地表明了这一点。代号“revelio”很可能是指去除魔法伪装的*哈利波特*咒语。

**自动来电过滤**

这些第一个字符串描述自动来电过滤的设置切换。你可以自动屏蔽拒绝 robocalls，拨打电话(这是默认行为)，或者自动无声地拒绝电话。

```
 <string name="call_action_label_automatically_screen">Automatically screen. Decline robocalls.</string>
<string name="call_action_label_ring_phone">Ring phone (default)</string>
<string name="call_action_label_silently_decline">Silently decline</string> 
```

下一批字符串描述了自动呼叫筛选功能是如何工作的。演示页面上说，谷歌助手会自动替你接听未知来电；检测到的 robocalls 会在不打扰您的情况下自动拒绝，而未知号码会在几分钟后响起，并会保存通话记录。保存在联系人列表中的任何号码都不会被过滤，因此您会一直收到它们。如果助理无法自动筛选呼叫，您可以点击通知中的按钮来启动手动呼叫筛选(即当前功能。)

当助理自动为您应答呼叫时，您可以选择保存这些简短呼叫的音频。我们在 8 月初就发现了这种[的证据，但当时还不清楚该功能是否可用于手动呼叫屏幕，因为在美国一些州，用户记录呼叫可能存在法律问题。现在很明显，这个功能是为了自动呼叫筛选，这是有意义的，因为谷歌助理总是会向对方宣布它将记录呼叫。](https://www.xda-developers.com/google-tests-saving-call-screen-audio-pixel/)

### Revelio 琴弦。点击/单击以展开。

```
 <string name="revelio_callers_how_it_works_text">"To turn off automatic screening select the \"Ring phone (default)\" setting for unknown calls. Your contacts are never automatically screened. Automatic screening won't work if your phone is connected to headphones or speakers. Call Screen doesn't use data or Wi-Fi but does use carrier call minutes. %1$s"</string>
<string name="revelio_demo_audio_button_text">Hear what the caller hears</string>
<string name="revelio_demo_key">revelio_demo_key</string>
<string name="revelio_demo_page_1_description">Your Assistant automatically answers unknown calls. Detected robocalls are silently declined; other unknown calls ring a few moments later with a transcript of the call. %1$s</string>
<string name="revelio_demo_page_1_title">Robocalls are declined without interrupting you</string>
<string name="revelio_demo_page_2_description">Your Assistant never automatically screens your contacts, so you receive their calls immediately.</string>
<string name="revelio_demo_page_2_title">Calls from your contacts are never delayed</string>
<string name="revelio_demo_page_3_description">"If a call isn't automatically screened, you can tap to have your Assistant find out who's calling so you can decide to answer or decline."</string>
<string name="revelio_demo_page_3_title">You can always screen other incoming calls</string>
<string name="revelio_demo_setting_title">See how Call Screen works</string>
<string name="revelio_demo_title">How Call Screen works</string>
<string name="revelio_demo_unable_to_fetch_audio">Unable to fetch sample audio</string>
<string name="revelio_demo_unable_to_play_audio">Unable to play sample audio</string>
<string name="revelio_dialog_button_cancel_call">Cancel</string>
<string name="revelio_dialog_button_end_screen">End current call, start new call</string>
<string name="revelio_dialog_description">Your Assistant is automatically screening an unknown call. To start a new call, end the current call.</string>
<string name="revelio_dialog_header">End current call?</string>
<string name="revelio_end_call_after_voicemail">"Thanks, I'll pass along your message. Goodbye."</string>
<string name="revelio_end_call_user_missed_internal_message">The call was missed</string>
<string name="revelio_google_help_fallback_uri">https://support.google.com/phoneapp</string>
<string name="revelio_how_it_works_key">revelio_how_it_works_key</string>
<string name="revelio_intro">"Hi. This is the Google Assistant. Can I ask what you're calling about?[sonic branding]"</string>
<string name="revelio_no_response_from_caller_ui_text">No response from caller</string>
<string name="revelio_pref_title">Call Screen</string>
<string name="revelio_preference_summary_automatic_screening_off">Automatic screening off</string>
<string name="revelio_preference_summary_screening">Screening %1$s</string>
<string name="revelio_promotion_details">Turn on automatic Call Screen to let your Google Assistant screen unknown calls automatically. Detected robocalls will be declined without interrupting you.</string>
<string name="revelio_promotion_title">Try automatic screening</string>
<string name="revelio_save_audio_setting_key">revelio_save_audio_key</string>
<string name="revelio_save_audio_setting_summary">Save the audio from calls answered by your Assistant</string>
<string name="revelio_save_audio_setting_title">Save Call Screen audio</string>
<string name="revelio_setting_title">Call Screen</string>
<string name="revelio_transfer_to_voicemail">"Sorry, but I couldn't get ahold of them. If there's anything else you'd like to let them know, go ahead and do so after the tone."</string>
<string name="revelio_try_to_reach">All right, hang on while I try to reach them.</string> 
```

**为自动筛选的通话保存通话屏幕音频**

这里有更多关于保存屏幕调用音频的字符串。以前，您只能在通话屏幕中保存记录。

```
 <string name="conversation_history_dropdown_menu_full_transcript_link_text_with_audio">Transcript and audio</string>
<string name="conversation_history_dropdown_menu_full_transcript_link_text_without_audio">Transcript</string>
<string name="save_audio_error_cant_load_value">Unable to fetch current Save Call Screen audio value</string>
<string name="save_audio_error_cant_set_value">Unable to save Save Call Screen audio value</string>
<string name="low_confidence_revelio_summary_prefix">"(Audio wasn't clear) "</string> 
```

**垃圾邮件偏好**

最后，这些字符串定义了新功能的垃圾邮件首选项。谷歌手机应用程序上的垃圾邮件检测将检测更改的号码、私人或隐藏的号码、未知号码和/或与谷歌垃圾邮件数据库匹配的号码。这些首选项将允许您调整自动呼叫筛选功能对哪些类型的号码起作用。

```
 <string name="possibly_faked_numbers_action_preference_description">Callers that may be spammers using an altered number</string>
<string name="possibly_faked_numbers_action_preference_key">possibly_faked_numbers_action_preference_key</string>
<string name="possibly_faked_numbers_action_preference_title">Possibly faked numbers</string>
<string name="private_or_hidden_action_preference_description">Callers hiding their caller ID</string>
<string name="private_or_hidden_action_preference_key">private_or_hidden_action_preference_key</string>
<string name="private_or_hidden_action_preference_title">Private or hidden</string>
<string name="unknown_call_settings_category_key">unknown_call_settings_category_key</string>
<string name="unknown_call_settings_category_preference_title">Unknown Call Settings</string>
<string name="spam_action_preference_description">"Numbers that match Google's spam database"</string>
<string name="spam_action_preference_key">spam_action_preference_key</string>
<string name="spam_action_preference_title">Spam</string>
<string name="screening_unknown_caller">Screening an unknown call</string> 
```

这项自动呼叫屏幕功能尚未在运行最新谷歌手机 42 测试版应用程序的 Pixel 2 XL 或 Pixel 4 上运行。我们也不知道谷歌什么时候会宣布。[简·满春·王](https://twitter.com/wongmjane/status/1196739426732277761)今天早些时候首次激活了该功能，但我们也访问了设置，为您带来了以下截图:

你可以从下面的谷歌 Play 商店链接下载谷歌手机 v42。

* * *

*感谢 PNF 软件为我们提供了使用 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) 的许可，这是一款用于 Android 应用的专业级 rever* *se 工程工具。*

*更新 1 (11/19/19 @美国东部时间上午 11:15):添加了@wongmjane 的推文，并改写了垃圾邮件首选项部分。*

更新 2 (11/19/19 @美国东部时间上午 11:40):添加了我们自己的功能截图。