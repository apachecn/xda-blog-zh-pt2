# Google Photos 4.46 准备在内存中显示照片作品，并为高级照片编辑功能添加了更多提示

> 原文：<https://www.xda-developers.com/google-photos-4-46-prepares-photo-creations-memories/>

Google Photos v4.45 [于上个月末推出](https://www.xda-developers.com/google-photos-445-tests-ordering-photo-prints-memories-view-hints-premium-editing-features-one-subscribers/)，该应用的拆除显示，Google 正在测试一项新功能，该功能将允许用户在 Memories 视图中订购照片打印。拆除还透露，该公司正在为谷歌一号的订户开发一些高级编辑功能。现在，谷歌已经开始推出谷歌照片 4.46 版，最新的 APK 的拆解揭示了更多暗示高级编辑功能的代码字符串，以及在回忆视图中显示照片创作的新功能。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

### 回忆视图中的创作

谷歌[早在去年 11 月就在谷歌照片中引入了回忆视图](https://www.xda-developers.com/google-photos-memories-same-day-prints-walmart-cvs-canvas-prints/),以帮助用户重新发现旧照片。在最近一次拆除中发现的代码串显示，谷歌现在还允许用户选择是否想在 Memories 视图中查看作品。对于不知情的人来说，创作是应用程序使用你的图像自动生成的照片。其中包括拼贴画、彩色流行照片、风格化照片等等。以下代码字符串表明，Google 现在可以让用户决定他们是否希望在 Memories 视图中看到这些作品，并让他们选择显示哪种类型的作品。

```
 <string name="photos_memories_settings_creation_animations_title">Animations</string>
<string name="photos_memories_settings_creation_collages_title">Collages</string>
<string name="photos_memories_settings_creation_color_pops_title">Color pops</string>
<string name="photos_memories_settings_creation_stylized_title">Stylized photos</string>
<string name="photos_memories_settings_creation_types_summary">Select the types of creations to be shown in your memories.</string>
<string name="photos_memories_settings_creation_types_title">Advanced</string> 
```

### 高级照片编辑功能

在之前的拆解中，我们发现了一个字符串，表明谷歌正在测试该应用程序中为 Google One 订户保留的新编辑功能。我们现在发现了谷歌照片 4.46 中优质编辑功能的更多证据，这表明照片应用程序希望在照片编辑器工具上“追加销售”你。使用“追加销售”的其他字符串都与让用户购买更多 Google One 存储有关。

```
 <string name="photos_photoeditor_upsell_disclaimer">disclaimer</string>
<string name="photos_photoeditor_upsell_primary_button" />
<string name="photos_photoeditor_upsell_title">title</string> 
```

* * *

除了这些即将推出的功能，我们还在最新的更新中发现了照片应用程序的新用户界面。新的用户界面已经对一些用户开放，正如你在附件的截图中看到的，回忆视图现在在应用程序的顶部有了一个更突出的位置。在记忆视图设置中，你现在可以选择隐藏特定的人和宠物。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*