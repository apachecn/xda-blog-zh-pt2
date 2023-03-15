# Android 11 的音频输出选择器显示谷歌演播设备

> 原文：<https://www.xda-developers.com/android-11-audio-output-picker-support-showing-google-cast-devices/>

在 Android 11 中，谷歌引入了一个重新设计的媒体播放器通知，位于快速设置面板下方。除了提供对媒体播放控制的快速和持久访问，新的媒体播放器还具有一个“无缝媒体传输”按钮，当点击该按钮时，会显示一个可用设备列表，以将声音输出路由到该设备。人们最初认为这种输出选择器不会包括谷歌 Cast 设备，但事实证明事实并非如此。

正如 Twitter 用户@ [Cirilla1253](https://twitter.com/Cirilla1253) (通过 *ArsTechnica 的* Ron Amadeo)指出的，最新版本的 [MediaRouter Jetpack 库](https://developer.android.com/jetpack/androidx/releases/mediarouter)，版本 1.2.0-beta01，添加了一个新功能，描述为“支持无缝媒体传输，通过系统 UI 实现媒体传输。”这个库是 [MediaRouter](https://developer.android.com/reference/android/media/MediaRouter) 类的兼容性包装器，它“允许应用程序控制从当前设备到外部扬声器和目的设备的媒体通道和流的路由”MediaRouter 支持库是为 Android 设置 [Cast 应用程序框架](https://developers.google.com/cast/docs/android_sender) (CAF)的依赖项之一，这是带有 Cast 按钮的应用程序用来将回放路由到 Google Cast 设备的。

虽然这证实了音频输出选择器可以支持显示 Google Cast 设备，但用户可能需要一段时间才能在菜单中看到这些选项。开发者需要更新他们的应用程序，以使用最新版本的 Mediarouter Jetpack 库，从而集成到 Android 11 的“无缝媒体传输”UI 中。

Android 11 的媒体播放控制比以前更加强大。最大的变化之一是它移动到快速设置面板下的一个专用位置，使用户可以轻松访问媒体控制，而不管其他通知正在显示什么。媒体控制也可以显示在锁定屏幕上，它还具有快速访问输出选取器的功能。此外，媒体控制也可以记住多达五个以前的媒体会话，因为我们[以前解释过](https://www.xda-developers.com/android-11-media-controls/)。

你最喜欢的流媒体音乐和视频应用程序可能会更新，以支持在声音输出选择器中列出 Google Cast 设备。只是时间问题。