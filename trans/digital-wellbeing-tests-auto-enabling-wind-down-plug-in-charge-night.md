# 数字健康测试当你晚上插上电源时，自动启动放松

> 原文：<https://www.xda-developers.com/digital-wellbeing-tests-auto-enabling-wind-down-plug-in-charge-night/>

# 数字健康测试当你晚上插上电源时，自动启动放松

Digital Wellbeing 正在测试一项针对放松功能的日程安排选项，允许用户在夜间充电时将其设置为自动启用。

今年，我们看到电话公司重新将精力集中在确保用户不会在智能手机上花太多时间上。谷歌[将数字福利作为像素专属](https://www.xda-developers.com/digital-wellbeing-google-pixel-xl-google-pixel-2-xl/)推出，然后[将其作为所有 Android 设备的要求](https://www.xda-developers.com/google-digital-wellbeing-parental-controls-required-android/)，促使原始设备制造商将它包含在他们的 rom 中。[数字福祉](https://www.xda-developers.com/tag/digitalwellbeing/)本质上是告诉用户他们使用智能手机的时间，并提供工具来帮助他们通过计时器减少使用时间，并通过放松功能在一天结束时减少手机的注意力。现在，谷歌正在探索当手机在夜间充电时自动启用放松功能的可能性。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

Digital Wellbeing 中的[放松功能](https://www.xda-developers.com/digital-wellbeing-wind-down-days-of-the-week/)可以设置为将您的显示器变成灰度级，并启用请勿打扰模式。这些都可以设置为自动启用，无论是在设定的时间表，或遵循夜间照明时间表(日落到日出)。digital well being v 1 . 0 . 279068912 . beta 包含指示将向应用程序添加额外计划选项的字符串。

```
 <string name="power_state_item_description">If you plug-in your phone between 9pm - 8am, your phone will start Wind Down. It will end whenever you unplug.</string>
<string name="power_state_item_label">Plug-in to unplug</string>PASTE YOUR CODE HERE 
```

因此，当你晚上插上手机的时候，你就可以放松，当你拔掉手机的时候，你就可以放松了。对于那些喜欢在床边充电时在床上使用手机的人来说，这将特别方便，因为这是开始放松的最佳时间，以便达到让你脱离手机的目的。如果你确实需要手机的全部功能，你可以简单地拔掉插头，而不必担心改变任何设置或拨动任何开关。

我们设法将测试版中的设置浮出水面，给你一张截图:

我们希望这个特性能很快在稳定的发布渠道中推出。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*