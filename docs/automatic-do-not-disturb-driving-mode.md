# 自动驾驶时请勿打扰功能为部分用户推出

> 原文：<https://www.xda-developers.com/automatic-do-not-disturb-driving-mode/>

# 自动驾驶时请勿打扰功能为部分用户推出

驾驶模式是一项新功能，它可以检测你何时驾驶，并将手机置于请勿打扰模式。它正在向一些用户推出。

类似于谷歌在将新功能推广到更多国家之前在特定市场(通常是美国)测试新功能的方式，他们在将新功能推广到更多设备之前，会在自己的硬件上测试新的软件功能。一个很好的例子是，谷歌助手起初是一个像素专属的软件功能，所以他们可以在一些人身上进行测试。一旦他们确信它准备好了，它就开始向其他设备推广。一些工程师还在 [Pixel 2 上测试了一项功能，当你正在驾驶时，它会自动启用请勿打扰模式](https://www.xda-developers.com/pixel-2-do-not-disturb-mode-driving/)，但这项功能现在已经演变成了谷歌所谓的“驾驶模式”,它现在出现在多个非 Pixel 设备上。

驾驶模式是一项新功能，我们上个月刚刚报道过，在 APK 拆卸之后，我们在 Google Play 服务应用程序的 14.3.62 版本[上做了这项工作。我们都知道开车时积极使用智能手机是很危险的。事实上，我所在的州(乔治亚州)最近通过了一项免提法律，禁止司机手持手机或用身体任何部位支撑手机。它声明耳机和听筒仅用于通信(而非娱乐)，并且只能使用语音到文本或文本到语音来发送/接收基于文本的通信。](https://www.xda-developers.com/android-pie-driving-mode-android-auto-do-not-disturb/)

智能手机正在成为美国驾驶人员的头号分心因素，谷歌一直在努力防止这些分心因素导致碰撞和死亡。他们这样做的一种方式是使用他们新的驾驶模式，该模式已被添加到 Google Play 服务应用程序中。我们在 14.3.62 版本中发现了它，但报告显示人们已经收到了启用该功能的 14.3.66 版本。启用该功能后，一旦智能手机检测到你正在驾驶，它将进入勿扰模式或自动启动一个汽车友好应用程序(如 Android Auto)。

驾驶模式使用谷歌[在 3 月](https://android-developers.googleblog.com/2018/03/activity-recognitions-new-transition.html)开放的 [ActivityTransition API](https://developers.google.com/android/reference/com/google/android/gms/location/ActivityTransition) ，这与 Pixel Ambient Services 在谷歌 Pixel 2 上使用的 API 相同。如果这个功能已经在你的设备上运行，那么你应该会在 Android 9 Pie 的连接首选项中看到这个新选项。

* * *

[**来源:jdayellow**](https://www.reddit.com/r/Android/comments/9kxg46/looks_like_i_got_a_do_not_disturb_while_driving/)