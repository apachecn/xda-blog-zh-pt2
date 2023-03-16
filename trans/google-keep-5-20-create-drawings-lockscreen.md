# 谷歌 Keep 5.20 准备让你从锁屏中创建绘图

> 原文：<https://www.xda-developers.com/google-keep-5-20-create-drawings-lockscreen/>

谷歌跨平台笔记服务 Google Keep 的新版本今天在谷歌 Play 商店发布。我在我的 Pixel 4 上下载了 5.20.081.01.40 版本，在将资源与之前的版本进行比较后，我发现了一个即将推出的功能的提示。在面向 Android 的 Keep 应用程序的未来版本中，您可以在设备锁定时创建新的绘画。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

三个新字符串非常清楚地暗示了这一特性:

```
 <string name="lockscreen_drawing_finished">Done</string>
<string name="lockscreen_drawing_not_available">This feature is not available.</string>
<string name="lockscreen_drawing_overlay">Create Keep drawings while your device is locked</string> 
```

还有两个新活动的布局:`com.google.android.apps.keep.ui.activities.SecureDrawingActivity`和`com.google.android.apps.keep.ui.activities.SecureDrawingLauncherActivity`。启动前一个活动只需打开已经可以通过打开 Google Keep 应用程序访问的绘图活动。启动后一个活动会显示一个对话框，说明“此功能不可用”，它与上面显示的字符串之一相匹配。简单地看了一下这两个活动的代码后，这个特性似乎还没有完全实现。然而，根据“lockscreen_drawing_overlay”字符串判断，Keep 应用程序可能会在锁屏顶部显示一个浮动的覆盖图标，当点击该图标时，会启动安全绘图活动，该活动会将用户与主应用程序的其余部分隔离开来。然而，在该特性得到更充分的开发之前，我们不会确切地知道它是如何工作的。

在 Chrome 操作系统上，可以从锁屏中记笔记，但在 Android 上是不可能的。有趣的是，当 Android 过去支持锁屏小工具时，Google Keep 过去支持从 Android 锁屏记录笔记。有趣的是，当锁屏小工具成为过去时，看到谷歌开发这个功能，[覆盖 API 将很快被否决](https://www.xda-developers.com/android-q-system-alert-window-deprecate-bubbles/)。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*