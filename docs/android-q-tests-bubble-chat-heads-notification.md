# Android Q 测试类似 Facebook Messenger 的聊天头的通知

> 原文：<https://www.xda-developers.com/android-q-tests-bubble-chat-heads-notification/>

谷歌 Pixel 设备 Android Q 的发布仅仅过去了几天，我们已经发现了一系列 T2 的新特性和功能。其中包括一个[全系统黑暗主题](https://www.xda-developers.com/android-q-toggle-dark-theme/)、[双 SIM 双待支持 Pixel 3](https://www.xda-developers.com/android-q-dual-sim-dual-standby-support-pixel-3/) 、一个[桌面模式](https://www.xda-developers.com/android-q-desktop-mode/)、 [TLS 1.3 支持](https://www.xda-developers.com/android-q-tls-1-3-support/)、[可定制导航手势](https://www.xda-developers.com/android-q-navigation-gesture-controls/)、[锁屏定制](https://www.xda-developers.com/android-q-lock-screen-clock-customization/)，以及[更多](https://www.xda-developers.com/android-q-new-features/)。现在，您可以将类似 Facebook Messenger 的聊天标题通知添加到这个不断增长的列表中。

谷歌正在测试这些紧凑的气泡聊天头，作为呈现所有通知的一种方式。以前，开发者必须在每个应用程序的基础上添加聊天头支持，就像 Facebook Messenger 所做的那样；但是现在，您可以通过 ADB 命令在整个系统中启用聊天头。

这一堆通知可以在屏幕上移动，新闻通知的右上角有一个蓝点。展开时，气泡在屏幕顶部水平排列。然后，您可以看到应用程序名称、打开通知的按钮以及打开通知通道设置的快捷方式。您可以像处理常规通知一样与通知进行交互；所有类型的系统和应用程序警报都可以在这种气泡聊天头格式中呈现。通知在阴影和气泡中共存，从任何一个地方删除它也会从另一个地方删除它。

要在支持的设备上启用 Android Q Beta 1 上的这些聊天头，请输入以下 ADB 命令:

```
 adb shell settings put secure experiment_enable_bubbles 1
adb shell settings put secure experiment_autobubble_all 1 
```

要删除它们并恢复原状，请输入以下内容:

```
 adb shell settings delete secure experiment_enable_bubbles
adb shell settings delete secure experiment_autobubble_all 
```

目前还不知道谷歌是否计划将此作为 Android Q 上所有设备的默认设置，希望对于那些不想打扰通知的人来说，有一种选择或方法可以禁用它。

* * *

[**故事 Via: 9to5Google**](https://9to5google.com/2019/03/16/android-q-chat-head-bubble-notifications/)