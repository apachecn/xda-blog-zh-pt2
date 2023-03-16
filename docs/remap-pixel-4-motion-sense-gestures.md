# Pixel 4 的运动感应手势现在可以重新映射[Root]

> 原文：<https://www.xda-developers.com/remap-pixel-4-motion-sense-gestures/>

谷歌的 Pixel 4 是第一款采用 Soli 雷达进行手势检测的智能手机。尽管谷歌早期的 Soli 演示展示了极其精确的手势检测，但我们在 Pixel 4 中得到的东西没有达到最初的宣传效果。目前，你可以向左/向右滑动来跳过曲目，向任何方向滑动来静音来电/定时器/闹钟，或者伸手唤醒手机。更糟糕的是，跳过音轨手势[只适用于 23 个媒体应用](https://www.xda-developers.com/google-pixel-4-motion-sense-list-countries-supported-apps/)。幸运的是，正如[的区域限制](https://www.xda-developers.com/enable-pixel-4-motion-sense-gestures/)一样，XDA 社区想出了一个改善运动感觉的解决方案。

目前，只有内置的 Motion Sense 应用程序和两款演示游戏 Pokemon Wave Hello 和 heading South 能够与手势配合工作。上周，谷歌告诉安卓警察 T3，该公司没有立即向第三方开发者开放运动感应 API 的计划。然而，这并没有阻止 XDA 资深成员[阿什格雷](https://forum.xda-developers.com/member.php?u=4180335)。他们修改了内置的 Motion Sense Bridge 应用程序，该应用程序允许 Pokemon 使用运动感应手势向南方挥手问好，并在检测到到达、存在、滑动或轻击手势时发送隐含的广播意图。安装这个修改过的 Bridge 应用程序[需要 root 访问权限](https://www.xda-developers.com/google-pixel-4-root-magisk/)，因为开发者必须禁用谷歌的签名保护。

ashergray 还创建了一个名为“OsloBridger”的配套应用程序，可以让你控制发送哪些广播意图，甚至可以让你调整所有支持的手势的灵敏度、距离和粒度。该应用程序创建了一个前台服务，因此即使屏幕关闭，手势事件也会被广播。

开发者打算将这个模块与自动化应用程序一起使用，如 [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm) 。在 Tasker 中，您可以通过创建一个具有“Intent Received”事件上下文的新配置文件来对运动感应手势事件做出反应。在“操作”字段中，输入您在 OsloBridger 中启用的意图操作。以下是支持的 4 种意图:

*   Reach 手势 Intent:com . jcar letto . oslobridger . reach _ Gesture
*   存在手势意图:com . jcar letto . oslobridger . presence _ Gesture
*   滑动手势意图:com . jcar letto . oslobridger . swipe _ Gesture
*   轻击手势意图:com . jcar letto . oslobridger . flick _ Gesture

在实际任务中，任何额外的意图都存储在具有相应名称的局部变量中。例如，当接收到 FLICK_GESTURE 意图时，可以通过%direction 局部变量在 Tasker 中访问“方向”意图 extra。在这种特殊情况下,%direction 变量分别为东、西、北或南保存 1、5、3 或 7。如果你打算使用这个模式重新映射任何手势，那么我建议你在设置>系统>动作感应中禁用原始手势，这样就不会有任何干扰。

有了这个 mod，你基本上可以用 Pixel 4 的运动感应手势做任何你想做的事情。您可以为任何媒体应用程序启用跳过音轨手势。您可以启用增加或降低音量的笔势。这取决于你。

如果你有任何问题或想留下反馈，请访问我们论坛上的 [OsloBridger Magisk 模块](https://forum.xda-developers.com/pixel-4-xl/themes/magisk-motion-sense-soli-oslo-mod-t3993877)主题。你可以从开发者的 GitHub 页面[这里](https://github.com/jcarletto27/magisk_module_motionsense_mod)下载 Magisk 模块。开发者 GitHub 上的自述文件还解释了 OsloBridger 应用程序中的每个参数和选项。

[**像素 4 论坛**](https://forum.xda-developers.com/pixel-4)| |[|**像素 4 论坛**](https://forum.xda-developers.com/pixel-4-xl)