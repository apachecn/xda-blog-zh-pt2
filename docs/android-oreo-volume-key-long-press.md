# 安卓奥利奥系统应用可以设置音量键长按监听器

> 原文：<https://www.xda-developers.com/android-oreo-volume-key-long-press/>

# 安卓奥利奥系统应用可以设置音量键长按监听器

由于 Android Oreo 实现了新的权限，系统应用程序现在可以设置监听器来检测音量键的长按。

为我们设备上的各种硬件和软件按钮添加额外的功能是 Android 爱好者已经做了一段时间的事情。大多数人都知道诸如来自 XDA 的[按钮映射器](https://play.google.com/store/apps/details?id=flar2.homebutton)这样的应用程序，公认的开发者 [flar2](https://forum.xda-developers.com/member.php?u=4684315) ，当 Galaxy S8 发布时，我们甚至谈到了[其他的 remapper 解决方案。虽然这些解决方案以某种方式处理这些动作，但谷歌似乎在 Android Oreo 中实现了一个长按音量键的监听器。这意味着，未来的应用程序可能能够对长时间按下音量键做出反应，即使在屏幕关闭的情况下，这可以用来从定制的 rom 中带来一个经常被请求的功能——用音量键控制音乐曲目。](https://www.xda-developers.com/3-applications-bypass-bixby-restriction/)

我们确实想提一下，这个功能实际上并没有在我们现在可用的面向用户的版本中启用。不过，对它的支持是存在的，正如我们发现的提交所证明的那样，这意味着 OEM 可以为您的特定设备启用它。如上所述，传统的重新映射应用程序通过检测是否发送了按键事件来工作(长时间按下，这些应用程序测量按键按下和按键向上事件之间的时间，而双击它们测量按键按下之间的时间)，但这些按键事件仅在屏幕打开时发送。此外，它们通常还需要使用可访问性服务，这会增加性能负担。

您的典型按钮重映射解决方案可以被认为是一种工作区，用于打开或关闭手电筒、打开应用程序、下拉通知面板等等。然而，谷歌在 Android Oreo 中实现的功能更进了一步，让系统应用程序自己设置这些音量按钮长按监听器。一旦平台检测到音量按钮被按住了几秒钟，这可以允许用户触发应用程序本身中的某些东西。

谷歌在 Android Oreo 中包含了对这种支持的方式，这将只适用于开箱即用的“特权”(又名预装系统)应用程序。OEM 只需要允许特权应用程序拥有`android.permission.SET_VOLUME_KEY_LONG_PRESS_LISTENER` [权限](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r4/core/res/AndroidManifest.xml#2794)就可以设置监听器。然而，我们已经能够使用 ADB 命令授予类似的权限，因此我们这些知情人士也可以为第三方应用程序手动设置此权限。