# Tasker 的最新测试版使得在 Android 8.0+上从 iOS 获得“按住音量键静音”手势成为可能

> 原文：<https://www.xda-developers.com/tasker-long-press-volume-button-gesture-mute-ios-android/>

# Tasker 的最新测试版使得在 Android 8.0+上从 iOS 获得“按住音量键静音”手势成为可能

Tasker 的最新测试版现在可以让你将音量键上的长按动作重新映射到任何任务，从而可以在 Android 上模仿 iOS 的静音手势。

尽管我们大多数人对 Android 感到舒适和满意，但 iOS 可以做到一些 Android 不能开箱即用的小技巧。这些 iOS 功能之一是能够按住音量降低按钮来静音设备。当你按下任何一个音量按钮时，Stock Android 都可以将来电静音，但你不能在不看设备的情况下简单地将设备静音，除非你的手机有额外的专用硬件，如一加设备上的提醒滑块。

谷歌在 Android 8.0 Oreo 中添加了[功能，让应用程序能够听到长按音量键的声音](https://www.xda-developers.com/android-oreo-volume-key-long-press/)，但没有致力于实现一个面向用户的解决方案来利用这一功能。最后，大约两年后，[下一首曲目应用程序实现了 API](https://www.xda-developers.com/skip-music-tracks-android-volume-keys-no-root/) ，允许用户长按音量键跳过曲目。这个被遗忘的 API 的重新发现促使 Tasker dev joaomgcd[在 Tasker (beta)](https://www.reddit.com/r/tasker/comments/bckqka/dev_tasker_570beta14_handle_volume_key_long/) 中加入了同样的东西，打开了一个充满可能性的世界。

Tasker 的最新测试版现在允许你重新映射音量按钮上的长按动作。使用这个，你可以非常容易地模仿 iOS“按住音量静音”手势功能。因为这是 Tasker，这只是你能做的事情之一。音量按钮很容易通过物理触摸来识别，因此您可以非常有效地使用它们来触发您想要完成的任务，而无需太多的操作或太多的思考。长按动作即使在屏幕关闭的情况下也能工作，所以你甚至不需要从口袋里掏出手机。

请注意，在配置事件之前，您需要通过 ADB 命令授予 Tasker 权限，如这里的所详述的[。](https://tasker.joaoapps.com/userguide/en/help/ah_volume_long_press_grant.html)

Tasker Beta 更新的完整变更日志如下:

*   增加了音量长按事件，允许你处理它，即使当屏幕关闭
*   添加了通知通道信息操作，该操作返回 Tasker 或正在运行的 kid 应用程序的给定通知通道的所有信息
*   在输出变量的操作中处理某些情况下的崩溃
*   如果 API > = 26，则添加在儿童应用中安装软件包的权限
*   在 Api < Oreo 的通知操作中不显示通知类别的浏览图标
*   Android 9 设备的固定显示尺寸动作
*   修复了当局部变量中包含文本时，Javascriptlet 操作无法运行的问题
*   修正了某些情况下场景自动调整大小的问题

你可以点击此链接加入测试版[。](https://play.google.com/apps/testing/net.dinglisch.android.taskerm)

* * *

[来源:tasker subredditT3](https://www.reddit.com/r/tasker/comments/bckqka/dev_tasker_570beta14_handle_volume_key_long/)