# Android Q 的多重恢复功能可以让两个应用同时运行而不会暂停

> 原文：<https://www.xda-developers.com/android-q-splitscreen-multitasking-multi-resume/>

甚至在[安卓牛轧糖的多窗口功能](https://www.xda-developers.com/everything-devs-need-to-know-about-multiwindow-in-android-n-code-examples/)发布之前，[安卓上的多窗口就以不同的形式](http://www.xda-developers.com/multi-window-is-underrated-and-every-android-should-have-it-by-now/)出现了。但后来谷歌给了 Android 一个可预测的统一的多窗口支持实现，有三种不同的多窗口模式:分屏、自由形式和画中画(适用于 Android Oreo 中的手机)。

然而，过去引入的分屏功能仍然受到一个严重的限制。虽然你可以*在分屏视图中打开*两个应用程序，并更好地利用你不断增长的屏幕空间，但你不能*同时运行*两个应用程序。当两个应用程序以分屏方式打开时，每次只有一个应用程序保留为活跃应用程序，而另一个应用程序暂停。用户需要通过与他们想要激活的应用程序进行交互来手动交换应用程序状态，因为现有的 Android 没有提供保持两个应用程序都激活的方法。

虽然谷歌确实就如何支持多窗口提供了某些[建议，以提供实际有用的体验，但大量应用程序没有根据这些建议处理暂停状态，导致视频暂停或停止或即时消息不更新等问题。](https://developer.android.com/guide/topics/ui/multi-window)

这一切都将改变。由于 [Android 最近增加了对可折叠智能手机](https://www.xda-developers.com/smartphone-foldable-display-android/)的支持，谷歌[推出了一项名为“多重简历”](https://android-developers.googleblog.com/2018/11/get-your-app-ready-for-foldable-phones.html)的新功能，该功能将在 Android Q 中强制执行

## 多重简历

多重恢复功能现在可以让多个应用程序同时打开，*实际上同时在运行*。谷歌现在允许制造商在多窗口时保持所有应用程序恢复/活动。三星已经在他们的设备上实现了这一点，其“[多星](https://www.xda-developers.com/samsung-good-lock-multistar/)”模块处于良好锁定状态，但现在原生支持正在向所有 Android 设备提供。

由于 Android Pie 已经推出，OEM 和应用程序都必须选择加入，以便在现有的 Android Pie 设备上测试该功能。这意味着 OEM 必须推出一个更新，以包括特定智能手机上的多简历支持，应用程序开发人员也需要在他们的清单中包括一个特殊的标签，以启用他们特定应用程序的功能。

``meta-data android:name="android.allow_multiple_resumed_activities" android:value="true"``

 `如果两个标准都满足(对于每个应用程序)，所有热门活动将在 Android Pie 设备上继续进行。

* * *

谷歌希望在下一个版本的 Android 中让多简历支持强制行为，也就是 Android Q。虽然这一功能肯定会在可折叠设备上得到大量使用，但我们这一代配备高显示屏的设备也将受益于这些多任务处理的改进。`