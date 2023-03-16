# 谷歌在 Android 11 上测试 Pixel 手机的新双击手势

> 原文：<https://www.xda-developers.com/google-pixel-android-11-double-tap-rear-gestures/>

谷歌昨天发布了第一个 Android 11 开发者预览版，我花了几个小时浏览了我的 Pixel 2 XL 的更新，以搜索我能找到的任何变化。[我们已经发现了很多](https://www.xda-developers.com/tag/android-11/)，但是和往常一样，代码中还隐藏着更多等待被发现的东西。在浏览负责谷歌 Pixel 手机上 SystemUI 组件的应用程序 SystemUI 谷歌 APK 时，我们发现了一个代号为“哥伦布”的神秘新手势系统的参考资料当激活时，新的手势将允许你双击背面——是的，手机的*背面*——来启动某些操作，如启动谷歌助手，启动默认的相机应用程序，播放/暂停媒体等等。

我们知道这项新的手势功能是针对 Pixel 手机而不是所有运行 Android 11 的设备，因为谷歌友好地坚持了他们的传统，即以“com.google”而不是“com.android”作为每个类的前缀，这是他们为包括 Active Edge 和 Motion Sense 在内的其他手势系统遵循的命名方案。与 Active Edge 和 Motion Sense 相比，这些“哥伦布”手势的有趣之处在于，它们似乎不需要任何特殊的硬件——只需要你手机的陀螺仪和加速度计。事实上，我们设法让几个新手势不仅在我们自己的 Pixel 2 XL 上工作，还在 XDA 高级成员 [cstark27](https://forum.xda-developers.com/member.php?u=2712580) 的 Pixel 4 XL 上工作，两者都运行 Android 11 开发者预览版 1。[*9 to 5 谷歌*](https://9to5google.com/2020/02/20/android-11-dp1-pixel-columbus-double-tap/) 也独立启用了一个新的“哥伦布”手势，尽管他们只展示了启动谷歌助手。

我们可以确认通过新的“哥伦布”功能可以使用以下手势:

*   解散计时器
*   发射照相机
*   启动谷歌助手
*   播放/暂停媒体
*   折叠状态栏
*   静音来电
*   贪睡闹钟
*   取消固定通知
*   执行“用户选择的操作”

为了防止这项功能过于随意地激活，谷歌还增加了“闸门”，以防止双击动作生效。目前实现的一些门包括相机可见性、充电状态、键盘守卫等等。

“Columbus”的代码引用了 SettingsGoogle 中目前不存在的名为“COLUMBUS_GESTURE_TRAINING”的类，因此我们认为 Settings 应用程序将包含在 SetupWizard 期间呈现给用户的手势训练活动。我们还认为，Android 11 中的 Pixel 设置应用程序可能会有页面来配置新的双击手势，特别是执行“用户选择的动作”。如果用户没有动作集，似乎“哥伦布”默认启动谷歌助手。由于目前在设置谷歌或任何其他系统应用程序中没有任何“哥伦布”的代码，可能会有更多关于这个功能的内容需要我们去发掘。

## Android 11 双击手势演示

这里有一个视频(由 Kieron Quinn 提供)显示了在运行 Android 11 的 Pixel 2 XL 上双击手势播放/暂停媒体:

https://gfycat.com/ifr/ScholarlyInfiniteIndianglassfish

Kieron Quinn 使用一个古老的 BBC 应用程序的原因是 KeyEvent 85，即播放/暂停媒体键的[键码，没有被我们尝试的大多数音乐应用程序的接收器接收到。对 logcat 的检查揭示了几个不允许后台执行的警告，阻止了 Google Play Music、YouTube、Amazon Prime Video、Spotify、VLC 和许多其他应用程序接收意图。](https://developer.android.com/reference/android/view/KeyEvent#KEYCODE_MEDIA_PLAY_PAUSE)

下面是我在运行 Android 11 DP1 的 Pixel 2 XL 上启动谷歌相机应用程序的视频:

https://gfycat.com/ifr/InsidiousTartFennecfox

最后，这是我启动谷歌助手的视频:

https://gfycat.com/ifr/AdventurousAgonizingFugu

虽然这个功能在旧的 Pixel 设备上运行得很好，但我们不知道谷歌是否会为所有运行 Android 11 的 Pixel 设备启用它。谷歌可能会将其作为 Pixel 4a 或 Pixel 5 的独家功能推出，然后在未来的更新中推广到其他 Pixel 设备。或者，我们可以看到未来推出的未来[像素特征下降](https://www.xda-developers.com/google-pixel-feature-drop-post-snap-portrait-mode-auto-call-screen/)。

* * *

非常感谢 Kieron Quinn，在 XDA 论坛上也被称为 Quinny899，帮助我们测试这个功能！