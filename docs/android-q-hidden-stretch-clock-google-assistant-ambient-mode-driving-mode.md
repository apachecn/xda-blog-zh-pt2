# 谷歌助手环境模式显示隐藏的安卓 Q 钟面

> 原文：<https://www.xda-developers.com/android-q-hidden-stretch-clock-google-assistant-ambient-mode-driving-mode/>

当谷歌推出 Pixel 3 和 Pixel 3 XL ( [我们的回顾](https://www.xda-developers.com/google-pixel-3-xl-camera-software-design-pixel-stand/))时，他们还发布了一款名为 Pixel Stand 的无线充电配件。将 Pixel 3 与 Pixel 支架对接会启动一种特殊的环境显示模式，显示您的 Google 相册、来自 Google Assistant 的视觉快照以及“我的一天”助手程序的快捷方式。对于过去几个版本的谷歌应用程序，谷歌已经开发了一种新的助手环境模式，可能会取代 Pixel 3 上的 Pixel Stand UI。

谷歌应用程序 10.24 测试版最近推出，所以本周早些时候，[*9 至 5 谷歌*](https://9to5google.com/2019/07/15/assistant-ambient-mode-early/) 访问了一个开发中的版本，他们认为这是谷歌助手中的新环境模式。我们还访问了我们认为的环境模式，尽管在我们的设备上有一些明显的差异。下面的第一行截图显示了我们看到的环境界面，而第二行显示了*9 到 5* 启用了什么。在我们的截图中，没有天气，时钟总是居中，尽管它的垂直位置发生了变化。在我的 Pixel 3 XL 上，当我的手机在我的坞站上时，环境模式保持在第一个截图中显示的界面上，但每当我举起手机时，界面就会切换到第二个和第三个截图中显示的界面。这种行为在我的 Pixel 2 XL 上不起作用，所以有可能新模式不是为 2017 像素设计的。

此外，我们的版本显示了隐藏在 Android Q 中的新“拉伸”钟面[。这个钟面在 Android Q beta 1 中可以短暂访问，但在较新的测试版中不再显示在锁定屏幕上。有趣的是看到它再次出现在这里，当我们也希望看到它作为一个选项出现在](https://www.xda-developers.com/android-q-lock-screen-clock-customization/)[即将推出的像素主题应用](https://www.xda-developers.com/android-q-pixel-customization/)中。最后，我们设法得到一个弹出窗口，要求我们尝试助手的新[驾驶模式](https://www.xda-developers.com/google-assistant-driving-mode-waze/) ( [我们的动手](https://www.xda-developers.com/google-assistant-driving-mode-android-auto-redesign-video/))，尽管我们还没有设法实际启动新的驾驶模式。

顶行:XDA 的谷歌助手环境模式截图。底排:9to5 的助手环境模式截图。

谷歌也分享了我们去年发现的[用户界面的更新版本](https://www.xda-developers.com/google-assistant-google-pixel-3-pixel-stand/)。他们推测，这个界面将与上面显示的内容结合起来，形成环境模式，我们将在该功能推出时看到。第二个界面有一列助手建议，就像我们前面看到的那样，但它还添加了一个音乐小部件。

如果您使用的是最新的 Google 应用程序，您可以启动环境模式活动，并通过在提升的 shell 中发出以下两个命令来弹出驾驶模式:

```
 am start -n "com.google.android.googlequicksearchbox/com.google.android.apps.gsa.staticplugins.opa.samson.activity.OpaAmbActivity"
am broadcast -a "com.google.android.apps.gsa.staticplugins.opa.morris.notification.INTENT_ACTION_SHOW_MORRIS_AFFORDANCE" 
```

如果我们设法在发布前让驾驶模式或谷歌助手环境模式完全工作，我们会让你们都知道。