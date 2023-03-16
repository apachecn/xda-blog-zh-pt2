# Digital Wellbeing 准备跟踪您的睡眠，让您做夜间笔记，等等

> 原文：<https://www.xda-developers.com/digital-wellbeing-sleep-tracking-night-notes/>

谷歌在 2018 年谷歌 I/O 大会上首次推出了数字福利，并推出了一些工具来帮助用户减少智能手机的使用，但该公司在过去的两年里通过引入大量新功能稳步改进了该应用。在 1.0.312292882 版本的最新测试更新中，谷歌准备推出主要的新功能，以帮助你获得更好的睡眠。

**在“管理您的数据”中新增“日常设备使用”切换功能**

谷歌推出的第一个功能已经在最新的测试版中为每个人提供了。如果你打开“数字健康”中的“设置”菜单，你会看到一个新的“管理你的数据”选项，带你进入一个带有“日常设备使用”开关的新活动此选项将让您决定 Digital Wellbeing 是否应跟踪您的设备解锁、收到的通知和应用程序使用情况。禁用此选项会关闭使用访问，因此 Digital Wellbeing 无法再跟踪您的手机使用情况。

目前，此开关是“管理您的数据”中唯一可用的开关然而，其他选项很快也会加入进来。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

**睡眠习惯追踪**

最大的新功能是睡眠习惯跟踪。我们设法推出了一项新的活动，让用户授权 Digital Wellbeing 和谷歌时钟应用程序访问日常应用程序使用情况、你预定的就寝时间内的运动和光线传感器数据以及时区历史。授予这两个应用程序访问这些数据的权限将让这两个应用程序“向你展示你的睡眠习惯的快照”

来自 APK 内部的字符串告诉我们数字福利将能够在睡眠方面提供什么样的见解。总之，数字健康可以告诉你在床上花了多长时间，在床上花了多长时间使用手机(以及你花了多长时间没有使用手机)，以及你的就寝时间开始和结束的时间。

### 数字健康睡眠洞察字符串

```
 <string name="sleep_insights_footer_wake_up">%1$s • Wake up</string>
<string name="sleep_insights_footer_wake_up_desc">Bedtime ended at %1$s on %2$s</string>
<string name="sleep_insights_header_bedtime">%1$s • Bedtime</string>
<string name="sleep_insights_header_bedtime_desc">Bedtime started at %1$s on %2$s</string>
<string name="sleep_insights_more_apps">+%1$d</string>
<string name="sleep_insights_more_apps_ellipsis">…</string>
<string name="sleep_insights_on_your_phone">On your phone</string>
<string name="sleep_insights_on_your_phone_duration">&lt;primary>%1$s&lt;/primary> • %2$s</string>
<string name="sleep_insights_title_bedtime_activity">Recent bedtime activity</string>
<string name="sleep_insights_title_screen_time">Screen time during bedtime</string>
<string name="sleep_insights_total_time_in_bed">Time in bed</string>
<string name="sleep_insights_total_time_in_bed_desc">%1$s in bed</string>
<string name="sleep_insights_total_time_on_phone">Time on phone</string>
<string name="sleep_insights_total_time_without_usage">Without your phone</string>
<string name="sleep_insights_total_time_without_usage_desc">%1$s without your phone</string>
<string name="sleep_insights_usage_group_collapse_action_desc">collapse</string>
<string name="sleep_insights_usage_group_collapsed_desc">Apps used for %1$s, from %2$s to %3$s</string>
<string name="sleep_insights_usage_group_expand_action_desc">expand</string>
<string name="sleep_insights_usage_group_expanded_desc">Expanded list of apps used for %1$s, from %2$s to %3$s</string>
<string name="sleep_insights_usage_group_row_desc">%1$s for %2$s</string>
<string name="sleep_insights_usage_group_single_app_desc">%1$s used for %2$s from %3$s to %4$s</string>
<string name="sleep_insights_usage_range">%1$s - %2$s</string>
<string name="sleep_screen_education_notification_text">Bedtime mode turns off always-on display to help you sleep better. Tap to make changes.</string>
<string name="sleep_screen_education_notification_title">Screen stays dark at bedtime</string> 
```

一旦该功能上线，“管理您的数据”中将有一个新项目来控制就寝时间传感器数据的使用:

```
 <string name="manage_data_bedtime_sensor_data_subtitle">Includes motion and light detection during your scheduled bedtime</string>
<string name="manage_data_bedtime_sensor_data_title">Bedtime sensor data</string> 
```

您还可以看到发送到时钟应用程序的数据，以及您的预定就寝时间历史记录:

```
 <string name="show_app_usage_and_sleep_api_result">Show Clock API result</string>
<string name="show_bedtimes">Show bedtime schedule history</string>
<string name="show_sleep_data">Show sleep data</string>
<string name="show_time_zones">Show time zone history</string> 
```

最后，如果您关闭睡眠习惯跟踪，所有已收集的现有数据都将被删除:

```
 <string name="turn_off_action">Turn off</string>
<string name="turn_off_sensor_data_dialog_message">Existing data will be deleted</string>
<string name="turn_off_sensor_data_dialog_title">Turn off access to sensor data?</string>
<string name="turn_off_time_zone_data_dialog_message">Existing data will be deleted</string>
<string name="turn_off_time_zone_data_dialog_title">Turn off access to time zone history?</string> 
```

**夜笔记**

与睡眠习惯跟踪一起开发的另一个主要新功能是数字健康中的“夜间笔记”。这个功能可以让你在睡觉前或者已经躺在床上，刚刚有了顿悟的时候，快速记下笔记。

```
 <string name="night_note_notification_reminder_text">"Anything on your mind? Offload your thoughts to Night Notes."</string>
<string name="night_note_notification_reminder_title">Bedtime mode starts at %s</string> 
```

一旦你醒来，Digital Wellbeing 会向你显示一个通知，询问你是否想查看你在晚上做的任何笔记。

```
 <string name="good_morning_notification_text">Tap to view your Night Notes.</string>
<string name="good_morning_notification_title">Good morning!</string> 
```

我不完全确定笔记会被写到哪里，但在 Digital wellness 的功能标志中有一个暗示，它将推出“com . Google . Android . compose . capture . capture activity”活动。这个活动不属于 Digital wellness、谷歌时钟应用程序，甚至不属于谷歌 Keep，所以它可能是谷歌为这项功能推出的新应用程序的一部分。

**横向屏幕时间使用**

接下来，一个让 Work Profile 用户满意的功能是查看工作应用程序的屏幕时间使用情况。目前，你必须在 Digital Wellbeing 中点击“切换到工作档案”，才能在工作档案中查看应用的应用使用统计数据。

```
 <string name="cross_profile_meta_data">See your screen time for work apps</string> 
```

**与其他应用程序共享数据**

最后，有迹象表明，Digital Wellbeing 将与其他应用程序共享一些数据。我们认为这可能仅限于谷歌应用程序，但谷歌有可能将一些福利数据作为 API 的一部分开放给第三方应用程序。

```
 <string name="data_sharing_with_other_apps">Other apps that use your data</string> 
```

您现在可以从谷歌 Play 商店下载最新版本的数字福利测试版应用程序。

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*