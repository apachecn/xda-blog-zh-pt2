# Android O 的画中画模式现在就可以启用，下面是方法

> 原文：<https://www.xda-developers.com/enable-android-o-picture-in-picture-mode/>

*特色图片:Android 电视上的画中画模式*

画中画模式(PiP)是某些电视接收机的一项功能，允许设备在一个嵌入窗口中显示一个节目，而另一个节目正在运行。从 Android 7.0 牛轧糖开始，这一功能进入了 Android 电视设备，但谷歌[最近宣布，这一功能将进入运行 Android O 的 Android 手机。有了 Android O，更新应用程序以支持 PiP 模式的开发人员现在也可以指定纵横比以及与窗口的自定义交互，如切换播放/暂停。](https://www.xda-developers.com/google-announces-android-o-developer-preview-1-available-for-supported-devices/)

Android O 开发者预览版设备上的用户可以尝试修改后的通知和其他调整，但迄今为止还不能在他们的设备上尝试画中画模式。然而，现在实际上可以在任何运行 Android O **的设备上**启用画中画**！**

正如你在上面的视频中看到的，我们打开 YouTube，导航到一个视频。视频暂停，然后我们按下导航键，折叠 YouTube 应用程序，并在所有其他活动(如 Google Play Music 和 Pixel Launcher)顶部的嵌入窗口中显示视频。窗口也可以在用户界面上移动。

然后，我们按下窗口，将 YouTube 应用程序恢复到我们打开的视频，然后我们开始播放。按下按钮启动画中画模式现在可以在视频仍在播放时最小化 YouTube 应用程序**！**目前，YouTube 应用程序似乎有点问题，因为视频在播放时不会占据整个窗口，但我们认为手机的 PiP 模式可能最适合在听音频的同时做其他事情，因为与 Android 电视设备相比，智能手机的屏幕相对较小。此外，这个错误可能会在 Android O 的后续版本或 YouTube 应用程序的更新中得到修复，但我们必须拭目以待。

* * *

## 如何启用画中画模式

好吧，好吧，我们知道你来这里的真正目的。我如何自己实现这一点？其实挺简单的。你需要发送某个键来触发 Android 手机上的画中画模式。该按键事件被称为“**键码 _ 窗口**”，它被 Android 电视设备遥控器用来切换画中画模式。幸运的是，它也适用于 Android O 系统的手机！

为了从导航栏按钮上的点击发送该键，您需要使用 SystemUI Tuner 中的[隐藏导航栏调谐器](https://www.xda-developers.com/android-o-preview-brings-nav-bar-customization-under-system-ui-tuner/)。添加一个导航按钮，选择按钮类型为“键码”，并查找**键码#171** 。一旦你这样做了，你的导航栏现在会有一个按钮，当在一个支持的应用程序中按下时，会切换 PiP。

你可能已经在想:*这难道不意味着我必须把这个键永久地放在我的导航栏上才能使用画中画模式吗？*不真实！请继续关注 XDA 门户网站，因为我们接下来将向您展示**如何只在某些应用程序中显示这个键！**

感谢 Eli Irvin 发现了这一点！