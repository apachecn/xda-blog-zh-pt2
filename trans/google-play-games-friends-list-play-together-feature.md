# Google Play Games 暗示将为新的“一起玩”功能添加好友列表

> 原文：<https://www.xda-developers.com/google-play-games-friends-list-play-together-feature/>

Google Play Games 可能不是该公司最受欢迎的应用程序之一，但谷歌重视让应用程序保持最新的新功能。这是该公司最早推出的获得黑暗主题的应用之一，谷歌去年甚至推出了一个 T2 的重大设计革新。今年 2 月早些时候，APK 对该应用的拆除揭示了一个即将到来的功能，即[通知用户谷歌选择的本周游戏](https://www.xda-developers.com/google-play-games-notify-game-week/)。现在，最新版本 Google Play Games (v2020.03.16839)的拆解发现了一些目前正在测试中的更值得注意的功能。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

### 朋友列表

一个易于访问的好友列表是你在几乎所有游戏平台上都可以找到的功能。它帮助您与平台上的朋友联系，检查他们何时在线，并轻松发送邀请一起玩游戏。遗憾的是，Google Play Games 目前没有好友列表。然而，这种情况可能很快就会改变。在该应用程序的最新拆除中发现的代码字符串显示，该公司正在内部测试该应用程序的朋友列表。

```
 <string name="games__profile__accept_invitation">Accept</string>
<string name="games__profile__achievements_loading_spinny_content_description">Loading more achievements into achievements tab.</string>
<string name="games__profile__add_friend">Accept invite</string>
<string name="games__profile__add_name">Add a name</string>
<string name="games__profile__cancel_invitation">Cancel invite</string>
<string name="games__profile__create_invite_url_menu_item">Create invite link</string>
<string name="games__profile__create_invite_url_network_error">"You're offline. Check your connection or try again later."</string>
<string name="games__playtogether__friend_requests_collapsed">Collapsed</string>
<string name="games__playtogether__friend_requests_expanded">Expanded</string>
<string name="games__profile__friend_status">Friends</string>
<string name="games__profile__friends_chip_content_description">You are friends with %1$s. Remove friend.</string>
<string name="games__profile__game_over">Remove this friend?</string>
<string name="games__profile__game_over_prompt">&lt;b> %1$s (%2$s) &lt;/b> will no longer be in your list of friends</string>
<string name="games__profile__game_over_prompt_without_nickname">&lt;b> %1$s &lt;/b> will no longer be in your list of friends</string>
<string name="games__profile__ignore_invitation">Ignore</string>
<string name="games__profile__pending_chip_content_description">Friend invitation is pending.</string>
<string name="games__profile__pending_status">Pending</string>
<string name="games__profile__remove_friend">Remove</string>
<string name="games__profile__remove_friend_menu_item">Remove friend</string>
<string name="games__profile__report_abuse_dialog_button">Submit</string>
<string name="games__profile__report_abuse_dialog_gamer_tag_option">Gamer ID: %1$s</string>
<string name="games__profile__report_abuse_dialog_nickname_option">Name: %1$s</string>
<string name="games__profile__report_abuse_dialog_title">Select the name to report</string>
<string name="games__profile__report_abuse_gamer_tag_submitted_message">"Thanks. We'll look into it."</string>
<string name="games__profile__report_abuse_menu_item">Report inappropriate name</string>
<string name="games__profile__report_abuse_nickname_submitted_message">Thanks for letting us know</string>
<string name="games__profile__send_invitation">Send invite</string>
<string name="games__profile__send_invitation_dialog_button_text_without_name">Send</string>
<string name="games__profile__send_invitation_dialog_gamer_tag_only_button_text">No, include gamer ID only</string>
<string name="games__profile__send_invitation_dialog_header">Include your name in the invite?</string>
<string name="games__profile__send_invitation_dialog_header_for_friend_suggestions">Send friend invite</string>
<string name="games__profile__send_invitation_dialog_prompt">Friend invites contain your gamer ID (%1$s). Including your name (%2$s) might help %3$s recognize you.</string>
<string name="games__profile__send_invitation_dialog_prompt_for_friend_suggestions">When you invite a suggested friend, your gamer ID (%1$s) and your name (%2$s) appear in the invite</string>
<string name="games__profile__send_invitation_dialog_real_name_button_text">Yes, include name</string>
<string name="games__profile__send_invite_button_content_description">Invite %1$s to be friends.</string>
<string name="games__profile__tab_achievements">Achievements</string>
<string name="games__profile__tab_friends">Friends</string>
<string name="games__profile__tab_unknown_count">- -</string>
<string name="games__search__friends_history_header">History</string>
<string name="games__search__friends_invitation_header">Get a link to invite your friends</string>
<string name="games__settings__automatic_friends_list_access_denied_item_label">"Games you play can't automatically access your friends list"</string>
<string name="games__settings__automatic_friends_list_access_granted_item_label">Games you play can automatically access your friends list</string> 
```

正如预期的那样，该功能将允许您使用您的玩家 ID 在应用程序中向您的朋友发送邀请，并且如果您的朋友不知道您的玩家 ID，您可以选择将您的名字添加到邀请中。接受邀请会将您的朋友添加到您的朋友列表中，您还可以选择将他们从您的列表中删除。如果你发现玩家 ID 令人不快，你还可以选择举报用户。此外，如果您的朋友没有在他们的设备上安装该应用程序，您还可以选择生成邀请链接，您可以共享该链接以将任何人添加到您的朋友列表中。此外，您还可以选择与您玩的游戏共享您的朋友列表，以便您更轻松地玩游戏，但是，默认情况下，游戏不会访问您的朋友列表。

### 一起玩

这就把我们带到了朋友列表中即将到来的“一起玩”功能。根据代码，可以访问你的好友列表的游戏会让你很容易地看到所有玩那个游戏的朋友，并和他们一起玩。您的朋友还可以选择与游戏共享他们的朋友列表，以便与更多的人一起玩。

```
 <string name="games__playtogether__friends_list_visibility_description">Games with access to your friends list let you see and play with friends easily. Games’ use of this data is subject to their &lt;a href=https:
<string name="games__playtogether__friends_list_visibility_no_description">Games will ask you for permission</string>
<string name="games__playtogether__friends_list_visibility_no_label">No</string>
<string name="games__playtogether__friends_list_visibility_title">Can games you play automatically access your friends list? (Includes gamer IDs, not emails)</string>
<string name="games__playtogether__friends_list_visibility_yes_description">Games that you play can automatically access your friends list</string>
<string name="games__playtogether__friends_list_visibility_yes_label">Yes</string>
<string name="games__playtogether__non_google_error">Sorry, you can only invite Googlers to dogfood this feature</string>
<string name="games__playtogether__privacy_settings_saved_success_message">"All set. You're ready to add some friends."</string>
<string name="games__playtogether__receive_friend_invites">Receive friend invites</string>
<string name="games__consent__dialog_content_subtitle">See and play with friends in this game. Access includes gamer IDs, not emails. The game’s use of this data is subject to their &lt;a href=https:
<string name="games__consent__dialog_content_title">%1$s wants to access your friends list</string>
<string name="games__open_invitation__clipboard_title">Play Games friend invitation link</string>
<string name="games__open_invitation__copy_toast">Link copied</string>
<string name="games__open_invitation__dialog_copy_icon_content_description">Copy friend invitation link</string>
<string name="games__open_invitation__dialog_share_button">Send link</string>
<string name="games__open_invitation__dialog_title">Invite more friends</string>
<string name="games__open_link_profile_toast_message">Viewing as %1$s</string> 
```

如前所述，默认情况下，游戏无法访问你的好友列表，每当该功能发布时，游戏都会请求你的许可。出于隐私意识，游戏对您好友列表数据的使用将受到 Google Play Games 好友隐私政策的约束。有趣的是，该代码还提到，目前该功能只允许用户“只邀请谷歌员工参与该功能。”这证实了该功能目前正在内部测试。

### 隐私设置

除了分享您的朋友列表，一起玩功能还可以让您分享您的游戏活动，以便您的朋友可以看到您一直在玩什么游戏。可见性选项将为您提供三个选项，允许您保持游戏活动的私密性，对朋友可见，或者对所有人可见。如果你停止玩某个游戏，你还可以选择拒绝该游戏进入你的好友列表。

```
 <string name="games__popup__connecting">Connecting to Play Games</string>
<string name="games__privacy__checkup_dialog_continue">Continue</string>
<string name="games__privacy__checkup_dialog_footer_text">You can change these settings in Play Games</string>
<string name="games__privacy__checkup_dialog_next">Next</string>
<string name="games__privacy__checkup_dialog_not_now">Not now</string>
<string name="games__privacy__checkup_dialog_save">Save</string>
<string name="games__privacy__checkup_dialog_saving_spinny_content_description">Saving your settings</string>
<string name="games__privacy__checkup_dialog_title">Friends and your privacy</string>
<string name="games__privacy__game_activity_description">"Select who can see your games, rankings, and achievements. If you select “Only you,” we'll hide everything except your gamer ID."</string>
<string name="games__privacy__game_activity_everyone_description">Others on Play Games can see your activity</string>
<string name="games__privacy__game_activity_everyone_description_current_setting">Others on Play Games can see your activity. &lt;b>This is your current setting.&lt;/b></string>
<string name="games__privacy__game_activity_everyone_label">Everyone</string>
<string name="games__privacy__game_activity_friends_description">Only friends you add can see your activity</string>
<string name="games__privacy__game_activity_friends_description_current_setting">Only friends you add can see your activity. &lt;b>This is your current setting.&lt;/b></string>
<string name="games__privacy__game_activity_friends_label">Friends</string>
<string name="games__privacy__game_activity_private_description">"Other gamers (including your friends) can't see your activity"</string>
<string name="games__privacy__game_activity_private_description_current_setting">"Other gamers (including your friends) can't see your activity. &lt;b>This is your current setting.&lt;/b>"</string>
<string name="games__privacy__game_activity_private_label">Only you</string>
<string name="games__privacy__game_activity_title">Who can see your game activity on your profile?</string>
<string name="games__privacy__play_together_intro_page_message">"See what they're playing, compete on leaderboards, and more"</string>
<string name="games__privacy__play_together_intro_page_title">Now you can add your friends in Play Games</string>
<string name="games__settings__friends_visibility_dialog_subtitle">Select who can see your achievements, leaderboards, and games played</string>
<string name="games__settings__friends_visibility_dialog_title">Game activity</string>
<string name="games__settings__friends_visibility_label_everyone">Everyone can see your game activity</string>
<string name="games__settings__friends_visibility_label_only_friends">Only friends can see your game activity</string>
<string name="games__settings__friends_visibility_label_private">Only you can see your game activity</string>
<string name="games__settings__friends_visibility_selection_everyone">Everyone</string>
<string name="games__settings__friends_visibility_selection_friends_only">Friends only</string>
<string name="games__settings__friends_visibility_selection_private">Only you</string>
<string name="games__settings__game_friends_list_access_currently_denied">"%1$s can't access your friends list"</string>
<string name="games__settings__game_friends_list_access_currently_granted">%1$s can access your friends list</string>
<string name="games__settings__game_friends_list_access_denied">%1$s can no longer access your friends list</string>
<string name="games__settings__game_friends_list_access_granted">%1$s can now access your friends list</string> 
```

如果您选择与朋友分享您的游戏活动，他们将能够看到他们的成就、排行榜和玩的游戏。但是，在他们更改可见性设置并使他们的活动对朋友列表中的人或所有人可见之前，你将无法访问他们的游戏活动。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*