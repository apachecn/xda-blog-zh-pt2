# Android Q 增加了对智能停留式“屏幕关注”功能的支持

> 原文：<https://www.xda-developers.com/android-q-smart-stay-screen-attention/>

# Android Q 增加了对智能停留式“屏幕关注”功能的支持

谷歌正在为 Android Q 添加一个类似三星智能停留的功能，它被称为屏幕注意力。它可以让你的手机在你使用的时候保持清醒。

在谷歌 I/O 2019 期间发布 [Android Q beta 3](https://www.xda-developers.com/android-q-beta-3-released/) 后不久， *[AndroidPolice](https://www.androidpolice.com/2019/05/09/adaptive-sleep-on-android-q-beta-3-aims-to-keep-your-phone-awake-while-youre-looking-at-it)* 发现了一个名为“适应性睡眠”的隐藏设置该团队在活动中与谷歌员工交谈，并确认“适应性睡眠”是希望实现保持清醒行为的原始设备制造商的占位符设置。在今天早些时候推出的 Android Q beta 4 中，这个功能不再是一个占位符，因为它有自己的图形、视频和一个新名字:屏幕注意力。

根据屏幕注意力的字符串，它在内部仍被称为自适应睡眠，该功能将防止您在观看屏幕时关闭屏幕。该功能使用您的前置摄像头来查看您是否在看屏幕。这类似于三星在 Galaxy 智能手机上已经存在多年的智能停留功能。

```
 <string name="adaptive_sleep_description">Prevents your screen from turning off if you’re looking at it.</string>
<string name="adaptive_sleep_privacy">Screen attention uses the front camera to see if someone is looking at the screen. It works on device, and images are never stored or sent to Google.</string>
<string name="adaptive_sleep_summary_off">Off</string>
<string name="adaptive_sleep_summary_on">On / Screen won’t turn off if you’re looking at it</string>
<string name="adaptive_sleep_title">Screen attention</string> 
```

下面的视频将在设置>显示>屏幕注意中的功能描述中向用户显示。

根据该准则，启用屏幕注意只有两个要求:

1.  布尔框架值 config _ adaptive _ sleep _ available 必须设置为 true。
2.  调用应用程序必须拥有权限 android.permission.CAMERA。

大多数 Android 设备都很容易满足这些要求，所以我不知道为什么谷歌 Pixel 智能手机还不能使用该功能。谷歌可能会将该功能保留到 Pixel 4 上首次亮相，之后该公司将在其他 Pixel 设备上启用该功能。无论如何，我们会密切关注这个和其他我们发现的特性，让你知道它们何时上线。