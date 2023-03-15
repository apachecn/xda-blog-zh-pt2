# 拆卸:谷歌二人组可能很快就会获得会议的同伴模式

> 原文：<https://www.xda-developers.com/google-duo-preps-meet-companion-mode/>

去年 6 月，谷歌为 Google Meet 预演了一个新的第二屏幕体验，名为伴侣模式。谷歌随后在 9 月份分享了更多关于该模式的细节，透露参与者可以使用他们的笔记本电脑或智能家居设备作为视频通话的第二个屏幕。今年 1 月早些时候，该功能终于开始向用户推出，支持谷歌 Nest Hub Max，谷歌现在准备将伴侣模式引入其另一款视频通话应用 Google Duo。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

最新版本的谷歌 Android Duo 应用程序(版本 162 . 0 . 434856097 . Duo . Android _ 20220306.14 _ p2 . s)的拆解显示了指向即将推出的功能的新字符串。这些字符串表明，视频通话应用程序可能会在未来的更新中获得陪伴模式。请查看下面的部分，查看与同伴模式相关的所有新字符串。

```
 string name="companion_indicator_text">Companion mode</string>
<string name="conf_companion_badge_education">The Companion mode badge means people are using Companion mode. You can see them in the people list.</string>
<string name="conf_companion_content_description">Companion</string>
<string name="conf_companion_participant_joined_notification">{NUMBER_OF_OTHER_PARTICIPANTS, plural, =0 {{PARTICIPANT_NAME} is using Companion mode} =1 {{PARTICIPANT_NAME} and {NUMBER_OF_OTHER_PARTICIPANTS} more are using Companion mode} other {{PARTICIPANT_NAME} and {NUMBER_OF_OTHER_PARTICIPANTS} more are using Companion mode} }</string>
<string name="conf_companion_participant_left_notification">{NUMBER_OF_OTHER_PARTICIPANTS, plural, =0 {{PARTICIPANT_NAME} stopped using Companion mode} =1 {{PARTICIPANT_NAME} and {NUMBER_OF_OTHER_PARTICIPANTS} more stopped using Companion mode} other {{PARTICIPANT_NAME} and {NUMBER_OF_OTHER_PARTICIPANTS} more stopped using Companion mode} }</string>
<string name="conf_companion_usage_got_it">Got it</string>
<string name="conf_companion_user_display_name">{DISPLAY_NAME} (Companion)</string>
<string name="conf_find_companion_users">"To find who's using Companion mode, go to the people list"</string>
<string name="conf_people_using_companion">People are using Companion mode</string>
<string name="host_and_companion_indicator_text">Meeting host • Companion mode</string> 
```

如果你不熟悉谷歌会议的同伴模式，这里有一个快速复习。Google Meet 中的同伴模式允许您使用第二个设备加入会议，以获得更好的多任务处理体验。使用陪伴模式，您可以在一台设备上加入音频和视频会议，如 Google Nest Hub Max，并使用您的主要设备进行其他会议功能，如聊天、提问、投票、屏幕共享等。

值得注意的是，陪伴模式并不是 Google Duo 即将推出的唯一 Google Meet 功能。在最近的一次拆解中，我们发现一些字符串表明，谷歌也在努力将 Meet 的分会场引入谷歌二人组，以及广播和记录会议的能力。