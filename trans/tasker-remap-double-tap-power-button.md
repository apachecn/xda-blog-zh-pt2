# 最新的 Tasker 5.7.0 Beta 6 可让您将双击电源按钮手势重新映射到任何您想要的位置

> 原文：<https://www.xda-developers.com/tasker-remap-double-tap-power-button/>

Tasker 是 Android 爱好者社区可用的最通用的工具之一，允许用户配置和设置他们的设备来做他们想要它做的事情。尽管价格昂贵，但自动化工具因其在过去几年中所开辟的所有可能性而广受赞誉。

Tasker 最近的巧妙解决方案包括将三星的 Bixby 按钮重新映射到其他虚拟助手。三星长期以来一直禁止创造性地使用 Bixby 按钮，迫使用户坚持使用三星的虚拟助手，而不管它对他们的效用。随着[三星 Galaxy S10](https://www.xda-developers.com/samsung-galaxy-s10-s10-and-s10e-launch-with-the-snapdragon-855-ultrasonic-in-display-fingerprint-scanners-reverse-wireless-charging-and-a-whole-lot-more/) 的发布，三星终于重新考虑了允许用户在特定条件下重新映射 Bixby 按钮的决定。您只能从可用的两个动作(单按和双按)中重新映射一个动作，另一个默认为 Bixby。另外，如前所述，你[不能重新映射按钮来启动其他虚拟助手](https://www.xda-developers.com/samsung-remap-bixby-button-google-assistant/)。

人们可以通过[使用 Tasker 导出一个启动语音助手的任务作为应用](https://www.xda-developers.com/samsung-remap-bixby-button-google-assistant/)来解决后一个限制，然后设置 Bixby 来启动导出的应用。Tasker 开发者 joaomgcd 通过[引入一个配套的二级应用](https://www.xda-developers.com/tasker-beta-remap-bixby-button/)扩展了这一过程，允许用户轻松地将 Bixby 按钮重新映射到他们想要的任何 Tasker 操作。

现在，[最新的 Tasker 5.7.0-beta.6](https://www.reddit.com/r/tasker/comments/axnuod/dev_tasker_570beta6_remap_doubletap_power_and/) 通过允许用户重新映射电源按钮上的双击动作，扩展了这个辅助应用的功能。

Tasker 通过将辅助应用程序声明为相机实现了电源按钮重新映射，因此允许双击动作触发它。然后，您可以在触发时设置进一步的任务，允许您轻松地重新映射按钮以打开任何其他应用程序或执行任何其他操作。

最新测试版的完整变更日志如下:

*   让辅助应用程序充当摄像头，这样双击电源按钮就可以触发它。
*   如果 Tasker 设置中尚未使用，请在打开时解释第二个应用程序。
*   将 Tasker 二级图标改为灰度
*   修正了有时第二个应用程序会打开 Tasker 而不是触发配置文件的错误
*   增加了隐藏或显示二级应用的选项
*   修正了有时无法获得拦截通知的通知文本的错误
*   修正了%屏幕变量事件和状态不起作用
*   修复如果显示快速平铺，快速平铺不会从任务更新的问题
*   在为配置文件运行任务之前保存%PACTIVE，使其在触发的配置文件中立即可用

[注册 Tasker Beta](https://joaoapps.com/beta-testing/) 试用这些即将推出的功能。要利用这一新的辅助应用程序操作，您的设备必须支持双击电源按钮来启动相机操作。并非所有设备都有这种手势——华为 Mate 20 X、Honor View20 和其他 EMUI 设备当然没有——所以在尝试重新映射之前，请检查确保你的设备支持该手势。

* * *