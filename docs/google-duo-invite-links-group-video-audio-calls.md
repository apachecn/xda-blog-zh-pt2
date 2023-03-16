# Google Duo 正在为群组视频和音频通话开发邀请链接

> 原文：<https://www.xda-developers.com/google-duo-invite-links-group-video-audio-calls/>

说到通信服务，谷歌的历史记录相当糟糕。众所周知，该公司因为[终止了几个消息服务](https://www.xda-developers.com/google-announces-allo-duo-google-home-and-more-at-io-2016/)而支持新的应用程序，反过来，[也最终终止了](https://www.xda-developers.com/google-allo-shutting-down/)。然而，其视频通话应用程序——Google Duo——迄今为止被证明是一个例外。自 2016 年在[发布以来，Duo 一直受到谷歌的关注，该公司一直在频繁地为该应用程序添加新功能。群组视频通话就是去年 7 月加入该应用的一项功能。](https://www.xda-developers.com/google-announces-allo-duo-google-home-and-more-at-io-2016/)

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

在推出时，Google Duo 上的群组视频通话功能最多只支持每组 4 个用户。然而，该公司在推出后不久就将小组人数限制增加到了 8 人。今年 3 月早些时候，谷歌[进一步提高了群组限制](https://www.xda-developers.com/google-duo-group-video-calling-live/),谷歌双人组用户现在每个群组视频通话最多可以有 12 个人。虽然更大的群组规模绝对是一个受欢迎的新功能，但该应用仍然需要您手动邀请联系人加入您的群组通话，这可能会有点麻烦。为了使这一过程更容易，谷歌现在正在为群组视频和音频通话开发邀请链接。

谷歌 Duo 85 的解体揭示了一系列指向即将推出的功能的代码，该功能将允许用户共享他们的群组视频通话的邀请链接，就像其他视频通话应用程序一样。拥有群组通话链接的用户可以点击它，立即打开 Google Duo 并加入群组通话。

```
 <string name="precall_edu_invite_link_text">Share this group link for friends to join</string>
<string name="precall_edu_start_call_text_with_link">" Share this group link for friends to join. When you tap "<b>Start,</b>" group members will get a notification to join the call. "</string>
<string name="share_link">Share</string>
<string name="share_link_dialog_body">Share this link to add friends to this group. %s</string>
<string name="share_link_dialog_header">Share link to group</string>
<string name="share_link_in_call_text">Add contacts, or share a link for friends to join</string> 
```

但是，在加入通话之前，Duo 会警告用户查看群组通话的成员列表。该代码进一步透露，如果用户在群组中没有任何已知的联系人，或者群组呼叫中有被阻止的联系人，该应用程序也会警告用户。

```
 <string name="precall_join_group_blocked_contact_warning_text">This group includes a contact you have blocked on Duo</string>
<string name="precall_join_group_no_contact_warning_text">"Use caution, you don't have any known contacts in this group"</string>
<string name="precall_join_group_welcome_text">Welcome to the group! Take a look at the members before you join.</string> 
```

虽然该功能目前在该应用程序的最新稳定版本中不可用，但多产的逆向工程师简·满春·王(Jane Wilson Wong)已经成功推出了网络用户界面，当网络用户试图通过邀请链接加入群组视频或音频通话时，就会显示该界面。

到目前为止，我们还没有关于该功能发布时间表的信息。我们将在 Google Duo 的群组邀请链接上线后立即更新这篇文章。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*