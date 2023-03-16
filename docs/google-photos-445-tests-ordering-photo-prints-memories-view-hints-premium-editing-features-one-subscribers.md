# Google Photos 4.45 测试在 Memories 视图中订购照片打印，为 Google One 订户提示高级编辑功能，等等

> 原文：<https://www.xda-developers.com/google-photos-445-tests-ordering-photo-prints-memories-view-hints-premium-editing-features-one-subscribers/>

Google Photos 可以说是最近最好的谷歌应用之一，它以一种体验和有形的形式展示了机器学习可以为最终用户做什么。通过允许用户免费备份他们所有的照片，谷歌激励了一大群 Android 用户使用这项服务。然后，它应用机器学习魔法智能地组织这些照片，不仅基于位置和时间，还基于照片中的人。像[回忆](https://www.xda-developers.com/google-photos-memories-same-day-prints-walmart-cvs-canvas-prints/)这样的功能通过向你展示你过去最美好的时光，让你踏上怀旧之旅。某些地理位置的用户还可以[订购当天照片](https://www.xda-developers.com/google-photos-memories-same-day-prints-walmart-cvs-canvas-prints/)，赋予这些时刻更多的持久性和可见性。在最新版本的谷歌照片中，谷歌正在努力使订购这些照片更容易，并扩大记忆功能的范围。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

在谷歌照片 4.45 版本中，已经在谷歌 Play 商店上推出了新的记忆功能。启用时，它会将菜单和共享按钮移到屏幕底部。它还在菜单中添加了新的选项，例如“订购照片打印”和“订购画布打印”，此外还有“设置”用于记忆和“查看今天的所有照片”。

应用程序中有更多功能可供探索，因为这些新字符串为记忆提供了新的设置:

```
 <string name="photos_memories_settings_previous_years_type_description">Photos from this week in previous years</string>
<string name="photos_memories_settings_previous_years_type_title">Previous years</string>
<string name="photos_memories_settings_recent_highlight_type_description">Photos from recent weeks</string>
<string name="photos_memories_settings_recent_highlight_type_title">Recent highlights</string>
<string name="photos_memories_settings_types_settings">Types of memories</string>
<string name="photos_memories_settings_types_summary">Select the types of memories you want to see. The memories carousel above the photo grid only appears when at least one memory type is selected.</string>
<string name="photos_memories_settings_types_title">Memory types</string> 
```

这些字符串表明，用户将能够选择在记忆中显示哪些时刻，范围从“过去的几年”到“最近的亮点”。

我们还发现了一个字符串，表明一些即将到来的编辑功能可能会作为高级功能保留给 Google One 的订户:

```
 <string name="photos_photoeditor_adjustments_premium_feature_badge">Google one feature</string> 
```

目前还不知道这是指什么编辑功能。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*