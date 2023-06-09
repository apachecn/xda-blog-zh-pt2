# Digital Wellbeing 准备添加一个工作配置计划程序来自动暂停应用程序

> 原文：<https://www.xda-developers.com/digital-wellbeing-prepares-add-work-profile-scheduler-pause-apps-automatically/>

# Digital Wellbeing 准备添加一个工作配置计划程序来自动暂停应用程序

digital health 准备添加一个工作档案计划程序，允许用户在一天工作结束后暂停工作应用程序。

Digital Wellbeing 首次在谷歌 2018 年 I/O 大会上亮相，推出了一些工具来帮助用户减少智能手机的使用，该公司在过去的两年里通过引入大量有助于[数字排毒](https://www.xda-developers.com/google-adds-experimental-digital-wellbeing-apps/)的新功能[稳步改进了该应用](https://www.xda-developers.com/tag/digitalwellbeing/)。在[1 . 0 . 327635162](https://www.apkmirror.com/apk/google-inc/digital-wellbeing/digital-wellbeing-1-0-327635162-release/)版本的最新更新中，谷歌正准备引入一个工作档案调度程序，该程序会在你下班后自动暂停应用程序。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

在新冠肺炎·疫情诱发的在家工作(WFH)习惯中，最常见的抱怨之一是工作时间已经融入了个人生活。在家工作的员工现在抱怨他们一天结束就无法离开工作。随着家变成了办公室，空闲时间和工作职责已经开始大量溢出到通常留给个人生活的时间里。

谷歌现在希望通过工作档案调度程序来解决这些问题，正如最新版本的数字福利中的字符串所示。

```
 <string name="work_scheduler">Work profile schedule</string>
<string name="work_scheduler_info">Disconnect from work by scheduling work apps to turn on and off automatically</string>
<string name="work_scheduler_notification_channel_name">Work profile schedule</string>
<string name="work_scheduler_set_schedule">Set a schedule</string>
<string name="work_scheduler_subtext_no_schedule">Off</string>
<string name="work_scheduler_subtext_with_schedule_off">Off / Turns on at %1$s on %2$s</string>
<string name="work_scheduler_subtext_with_schedule_off_on_within_24h">Off / Turns on at %s</string>
<string name="work_scheduler_subtext_with_schedule_on">On / Turns off at %1$s on %2$s</string>
<string name="work_scheduler_subtext_with_schedule_on_off_within_24h">On / Turns off at %s</string>
<string name="work_scheduler_title">Work profile schedule</string>
<string name="work_session_postpone_turning_off">Wait until %s</string> 
```

这些字符串表明，该应用程序将很快允许用户“打开和关闭”应用程序，并帮助他们脱离工作。这些字符串并没有明确说明打开和关闭一个应用程序需要什么。但如果说[一加的工作生活平衡功能](https://www.xda-developers.com/oxygenos-open-beta-3-oneplus-7-pro-work-life-balance-mode-india/)对 Digital Wellbeing 中的这一功能有任何启发，那么这可能只是应用程序暂停的通知，在此期间不会向用户显示。一加的工作生活平衡功能实际上允许设置工作和生活档案(你也可以选择避免在工作时间显示来自“生活”应用程序的通知)，而数字福利显然只专注于一个方面。谷歌可以选择在未来将这一功能扩展到这两个领域。

* * *