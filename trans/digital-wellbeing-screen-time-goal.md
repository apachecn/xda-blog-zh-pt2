# 数字健康让你设定屏幕时间目标

> 原文：<https://www.xda-developers.com/digital-wellbeing-screen-time-goal/>

今天早些时候，数字健康应用 1.0.263733828.beta 版在谷歌 Play 商店发布。该应用程序提供了一套健康工具，帮助你减少使用智能手机的频率，最新的更新带来了一个“专注模式”开关，让你暂停令人分心的应用程序，以便你可以完成更多的工作。现在，谷歌似乎正准备在数字福利中增加一项新功能，让你设定一个“屏幕时间目标”。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

* * *

### 屏幕时间目标

根据字符串，这一功能将让你设定一个目标，你想花多长时间在你的手机上。如果你设定了一个目标，比如说，每天按时看 4 个小时的屏幕，那么你会发现你完成或低于这个目标的频率。每周，你甚至会收到一封通知，告知你完成目标的情况。

```
 <string name="remove_goal_button_text">Remove goal</string>
<string name="remove_goal_dialog_cancel_button_text">Cancel</string>
<string name="remove_goal_dialog_remove_button_text">Delete</string>
<string name="remove_goal_dialog_title">Delete this goal?</string>
<string name="screen_time_goal_above_average">%1$s more than your average</string>
<string name="screen_time_goal_below_average">%1$s less than your average</string>
<string name="screen_time_goal_details">"This goal should be the amount of time you'd like to spend on your phone each day."</string>
<string name="screen_time_goal_equal_to_average">your average daily screen time</string>
<string name="screen_time_goal_heading">Set your daily screen time goal</string>
<string name="screen_time_goal_status_goal_exceeded">%1$s over your goal</string>
<string name="screen_time_goal_status_goal_not_reached">%1$s under your goal</string>
<string name="screen_time_goal_status_goal_reached">You hit your goal today</string>
<string name="screen_time_goal_summary_notification_checkbox">Get weekly screen time notifications</string> 
```

华为的数字健康服务(Digital Wellbeing)被称为数字平衡(Digital Balance)，[提供了类似的功能](https://www.xda-developers.com/emui-9-review-features-apps-huawei-honor-android-pie/)，但一旦你达到极限，数字平衡实际上会阻止你使用手机。另一方面，谷歌似乎只是在鼓励你少用手机。

### 从数字福利的历史中删除网站

早期的 Digital Wellbeing 测试版增加了与谷歌 Chrome 的集成，让你可以看到你最常访问的网站，还可以为它们设置应用定时器。如果你启用了集成，你在 Chrome 中访问的任何网站(匿名模式下访问的网站除外)都会被健康登录，如果你想从列表中删除某个网站，你必须在 Chrome 的隐私设置中完全禁用集成。最新的更新表明，你可以从 Wellbeing 的仪表板中删除单个网站，尽管这样做不会将该网站从 Chrome 的历史中删除。

```
 <string name="remove_past_visits_description">"Your past visits to this site will be removed from Digital Wellbeing. Chrome history won't be cleared."</string>
<string name="remove_past_visits_dialog_title">Remove past visits to this site?</string>
<string name="remove_past_visits_positive_button_label">Remove</string> 
```

* * *

如果你想获得带有对焦模式的最新测试版更新[，你可以从谷歌 Play 商店下载该应用。如果你使用 Android Q，你也可以使用](https://www.xda-developers.com/focus-mode-digital-wellbeing/)[新的 Chrome 集成](https://www.xda-developers.com/android-q-google-chrome-digital-wellbeing/)，只要你不在稳定频道，因为该功能还没有在那里实现。自从上次更新以来，Family Link 集成也可以在[使用，以防你错过那个新闻。](https://www.xda-developers.com/digital-wellbeing-integration-family-link-parental-controls/)

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*