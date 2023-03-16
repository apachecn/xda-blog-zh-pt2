# 谷歌日历 6.0.56 继续致力于谷歌任务与重复任务和同步的整合

> 原文：<https://www.xda-developers.com/google-calendar-6-0-56-continues-work-google-tasks-integration-recurring-tasks-syncing/>

# 谷歌日历 6.0.56 继续致力于谷歌任务与重复任务和同步的整合

谷歌日历(v6.0.56)最新更新的拆解揭示了突出即将到来的谷歌任务集成的代码串。

自从 Google 为 Google Tasks 发布了一个独立的应用程序[以来，许多用户都要求在 Google Calendar 中无缝集成任务。据报道，该公司在过去的几个月里一直致力于整合工作，谷歌日历最新更新的拆除进一步表明，整合工作正在顺利进行。](https://www.xda-developers.com/google-tasks-app-android/)

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

谷歌日历版本 6.0.56 中发现的代码字符串清楚地突出了即将到来的功能。一旦上线，谷歌任务集成将允许用户直接在谷歌日历应用内创建任务，而无需下载独立的任务应用。代码提到了一个新的任务按钮，提示创建重复任务，保存重复任务，任务描述，任务取消消息，以及对同步的支持等。尽管任务集成还没有上线，但它似乎越来越接近发布了。

以下是日历应用程序 6.0.56 版本中添加的所有与任务相关的新字符串:

```
 <string name="accessibility_speeddial_task">Task button</string>
<string name="collapse_task_sheet">Collapse task sheet</string
<string name="creating_repeating_task">Creating repeating task…</string>
<string name="creating_repeating_task_no_connection">"No connection. The repeating task will be created when you're online."</string>
<string name="edit_scope_selection_title_task">Save recurring task</string>
<string name="error_no_task_account">No accounts that support tasks found on the device.</string>
<string name="error_repeating_task_start_time_in_past">Start time of a repeating task cannot be in the past.</string>
<string name="expand_task_sheet">Expand task sheet</string
<string name="task">Task</string>
<string name="task_creation_cancellation_message">Discard this task?</string>
<string name="task_description_hint">Add details</string>
<string name="task_edit_cancellation_message">Discard changes to this task?</string>
<string name="task_no_title_placeholder">(Task — no title)</string>
<string name="task_notification_channel">Task notifications</string>
<string name="tasks_sync_adapter">Tasks in Calendar</string> 
```

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*