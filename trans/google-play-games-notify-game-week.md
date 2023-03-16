# Google Play Games 将很快通知您所选择的本周游戏

> 原文：<https://www.xda-developers.com/google-play-games-notify-game-week/>

# Google Play Games 准备通知您 Google 选择的本周游戏

对 Google Play 游戏最新更新的拆解揭示了一项新功能的代码，该功能将通知用户谷歌每周的热门游戏选择。

尽管 Google Play Games 不是该公司最受欢迎的应用程序之一，但谷歌一直在为该应用程序带来新功能，以使其与所有其他产品保持同等水平。Google Play Games 是该公司最早推出黑暗主题的应用之一，它甚至在去年接受了 T2 的重大设计革新。现在，谷歌似乎正在测试该应用的一项新功能，该功能将通知用户该公司的每周游戏选择，以促进发现。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

最新版本的 Google Play Games(v . 2020 . 01 . 15707)的拆解揭示了关于即将到来的功能的代码字符串。一旦发布，每周游戏通知功能将在应用程序设置中提供，并允许用户点击一个开关来接收谷歌每周最佳选择的通知。第一次点击设置会弹出一个对话框，显示“我们将每周突出显示一个不同的即时游戏，并在它准备好时通知您。无需安装。该对话框将包括一个“完成”按钮来启用该功能。

```
 <string name="games__gotw__game_of_the_week_notifications_disabled_label"><u>Enable Game of the week notifications in settings</u></string>
<string name="games__gotw__notification_channel_name">Game of the week</string>
<string name="games__gotw__opt_in_dialog_body">"We'll highlight a different instant game every week and notify you when it's ready. No installation needed."</string>
<string name="games__gotw__opt_in_dialog_button">Done</string>
<string name="games__gotw__opt_in_dialog_label">Get game of the week notifications</string>
<string name="games__gotw__opt_in_dialog_title">Want updates on the game of the week?</string> 
```

对于不知情的人来说，即时游戏是 Google Play 游戏中的一个独立类别，它由无需安装在设备上就可以立即玩的游戏组成。这些游戏包括《微旅行》、《迷宫与更多》和《海战》,只需点击列表旁边的“即时播放”按钮即可播放。截至目前，谷歌尚未透露该功能何时将推出该应用的稳定版本。但由于代码已经在应用程序中出现，我们预计该公司将很快披露更多信息。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*