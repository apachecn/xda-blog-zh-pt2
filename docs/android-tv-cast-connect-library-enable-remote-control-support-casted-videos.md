# Android TV 的 Cast Connect 库支持对视频进行远程控制

> 原文：<https://www.xda-developers.com/android-tv-cast-connect-library-enable-remote-control-support-casted-videos/>

# Android TV 的新 Cast Connect 库将支持对视频的远程控制

谷歌新的 Cast Connect 库将允许 Android 电视应用程序的开发人员在应用程序中处理 Cast 会话，而不是在 HTML5 播放器中。

由于 Cast Connect 的引入，在不久的将来，将视频内容传输到您的 Android 电视设备有望变得更加自然。正如 Twitter 用户 [Android TV Guide](https://mobile.twitter.com/androidtv_rumor/status/1290921775459639296) 所指出的，这项新功能的好处是可以使用遥控器来播放视频。

谷歌的开发者页面解释了新的 Cast Connect 库是如何工作的。它建立在 Google Cast 基础设施之上，Android TV 设备充当 Cast 接收器。集成该库后，Android TV 应用程序可以接收 Cast 消息并广播媒体状态，就像它们是实际的 Google Cast 设备一样。谷歌表示，除了加载媒体和播放控制，Cast Connect 库还具有媒体元数据、自定义消息、重复/无序播放和发送者加入/离开事件。这里有一个来自 Google 的视频，旨在帮助开发者理解如何集成这个库:

本质上，从你的手机到你的 Android 电视的内容将由一个支持的应用程序处理，而不是在 HTML5 播放器中打开。因此，您将能够使用现有的遥控器而不是手机来控制内容。这让选角体验感觉更加完整，对用户来说也更好，因为专用的 Android TV 应用程序可能比通用的 HTML5 播放器支持更多的功能和编解码器。如果没有检测到受支持的应用程序，或者在转换时用户配置文件不匹配，那么转换连接库将使用 HTML5 播放器作为后备来启动会话。

截至目前，开发者必须在他们的 Android 电视应用程序中添加 Cast Connect 支持，新功能才能发挥作用。谷歌还指出，目前 Cast Connect 还不完全支持助手功能，这意味着你无法通过语音控制播放的内容。