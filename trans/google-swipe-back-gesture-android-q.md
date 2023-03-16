# 谷歌可能正在测试 Android Q 中新的侧扫手势

> 原文：<https://www.xda-developers.com/google-swipe-back-gesture-android-q/>

**更新 1(美国东部时间 2019 年 4 月 22 日晚上 8 点 28 分)**:评论中的用户 Pablo 通过使用[之前我们使用的一个技巧](https://www.xda-developers.com/android-q-navigation-gesture-controls/)成功地让背部手势工作。更多细节在最后的更新部分。原文如下。

Android Q 带来了大量面向用户的新功能，如[浮动气泡通知](https://www.xda-developers.com/android-q-beta-2-notification-bubbles/)、[全系统黑暗主题](https://www.xda-developers.com/android-q-toggle-dark-theme/)、[桌面模式](https://www.xda-developers.com/android-q-desktop-mode/)、[新隐私控制](https://www.xda-developers.com/android-q-privacy-permission-controls/)等等。谷歌还解决了用户对 Android Pie 手势控制的许多投诉。我们已经看到[多次](https://www.xda-developers.com/android-q-gestures-back-button/) [调整](https://www.xda-developers.com/android-q-iphone-navigation-gestures/)到[方式](https://www.xda-developers.com/android-q-beta-2-iphone-x-gesture-bar/)手势工作，其中一个变化甚至进入了[第二个 Android Q beta](https://www.xda-developers.com/android-q-beta-2-everything-new/) 版本。虽然我们不知道谷歌最终发布会采用哪种手势实现，但我们已经发现了谷歌的另一个手势实验。这一次，我们发现了一个似乎是向后滑动的手势。

## 向后滑动手势

华为的 EMUI 和小米的 MIUI 中的手势控制放弃了后退按钮，转而支持滑动手势，即从左侧或右侧滑动以返回。我个人不喜欢这种手势，因为它干扰了许多遵循材料设计准则的 Android 应用程序的导航抽屉。尽管如此，看起来谷歌至少正在试验这种形式的手势控制，正如 XDA 资深成员[帕冯布](https://forum.xda-developers.com/member.php?u=6018897)首先发现的那样。他录制了以下视频，展示了来自 [Android Studio 的模拟器](https://www.xda-developers.com/android-studio-3-4-stable-android-q-emulator-r8-proguard/)的 Android Q 系统图像中的新手势。如您所见，该手势目前没有功能，但从侧面出现的箭头表明，一旦代码完全实现，它将执行后退操作。

我们证实了这一新手势存在于谷歌 Pixel 2 XL 上的 Android Q beta 2 中。启用它需要几个简单的 ADB 命令:

```
 adb shell settings put global prototype_enabled 1
adb shell settings put global quickstepcontroller_edge_width_sensitivity 48
adb reboot 
```

同样，请注意，即使您可以看到动画，手势目前也不起作用。此外，手势的灵敏度，换句话说，离允许开始手势的边有多远，可能取决于屏幕分辨率和密度。出于演示的目的，我们在这里只是强制使用一个数字。

最后，视频显示了潜在的向后滑动手势以及我们之前发现的[新 iPhone X 风格手势栏](https://www.xda-developers.com/android-q-beta-2-iphone-x-gesture-bar/)。iPhone X 手势栏在当前形式下缺少向后推送手势，因此新的手势栏可能会与这种新的从侧面向后推送手势配对。我们正在接近今年的[谷歌 I/O](https://www.xda-developers.com/google-io-2019-may-7-9/) ，在那里我们可能会了解更多关于 Android Q 的新手势。

## 导航栏颜色变化

paphonb 发现的另一个调整涉及手势栏着色方式的微妙变化。根据 paphonb 的说法，这一调整使手势栏“根据其背后的实际内容而不是应用程序所说的内容变暗。”他录制了下面的视频来展示这种变化，这种变化在主屏幕页面和应用程序抽屉之间的转换过程中表现得最好。

启用它需要发送以下 ADB 命令:

```
 adb shell settings put global navbar_color_adapt_enable 1 
```

自从我们在一月份第一次接触到 Android Q 泄漏版本以来，我们就知道这些 ADB 命令，但当时这两个功能都没有实现，所以我们无法让他们确切地发现他们做了什么。现在，他们至少部分工作在第二个 Android Q 测试版中，我们可以再次展示谷歌已经在引擎盖下进行的实验。如果我们在 Google I/O 之前发现任何类似的变化，我们会让您知道。

* * *

## 更新 1:如何让向后滑动手势工作

如果您还输入了以下 ADB 命令，则向后推送手势有效:

```
 adb shell settings put global quickstepcontroller_gesture_match_map 172233 
```

关于如何工作的更多细节可以在[这里](https://www.xda-developers.com/android-q-navigation-gesture-controls/)找到。