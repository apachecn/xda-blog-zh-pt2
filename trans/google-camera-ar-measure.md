# 谷歌相机准备添加增强现实测量模式

> 原文：<https://www.xda-developers.com/google-camera-ar-measure/>

上周末，谷歌相机应用的新版本开始向谷歌像素用户推出。该应用的 6.2 版本在相机应用的设置页面中添加了一个黑暗模式，但没有添加太多其他内容。然而，我们发现字符串暗示了一种新的相机模式，称为“测量”我们认为这意味着谷歌将把他们名为“ [Measure](https://www.xda-developers.com/measure-length-arcore-app/) 的增强现实测量应用程序集成到谷歌相机中，这看起来确实如此。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

* * *

## 谷歌相机 6.2 提示测量模式

这两个新字符串表明，谷歌 Pixel 的股票相机应用程序将添加一个“测量模式”:

```
 <string name="mode_measure">Measure</string>
<string name="mode_measure_desc">Switch to Measure mode</string> 
```

XDA 资深会员 [cstark27](https://forum.xda-developers.com/member.php?u=2712580) ，一个[在谷歌相机模块](https://www.xda-developers.com/google-camera-night-sight-google-pixel-3-google-pixel-2-google-pixel/)上工作的开发者，设法让新的测量模式显示在应用程序的“更多”标签中(见上面的精选图片)。新模式的图标与谷歌的 Measure 应用程序的启动器图标相匹配，暗示新模式确实与增强现实尺寸测量应用程序相关。尝试启动该模式会导致应用程序崩溃，并显示以下 logcat 输出:

```
 04-03 08:56:16.088 29466 29466 E AndroidRuntime: android.content.ActivityNotFoundException: Unable to find explicit activity class {com.google.vr.apps.ornament.measure/com.google.vr.apps.ornament.meas
ure.MeasureMainActivity}; have you declared this activity in your AndroidManifest.xml? 
```

这次崩溃的原因是因为我们缺少一个包名为 com . google . VR . apps . corrupt . measure 的应用程序。Google Play 上目前不存在这样的应用程序，因为 Google 尚未推出它。值得注意的是，这个包名的第一部分“com . Google . VR . apps . corrupt”与 [Playground](https://www.xda-developers.com/download-playground-2-0-ar-stickers-marvel/) (以前称为 AR 贴纸)的包名相匹配。因此，我认为谷歌会重新推出 Measure 应用程序，作为 Playground 的附加软件。Playground 和谷歌相机官方只支持谷歌 Pixel 智能手机，所以不要指望在其他设备制造商的智能手机上看到新的测量模式。然而，[谷歌相机和游乐场应用的非官方端口](https://www.xda-developers.com/google-playground-ar-stickers-port-arcore-devices/)可能会让你在 [ARCore 支持的设备](https://www.xda-developers.com/huawei-p30-pro-moto-one-vision-google-arcore-supported-device/)上使用这种测量模式。

一旦新的测量模式启动，我们会通知大家。对于那些对它如何工作感到好奇的人，这里有一个来自谷歌的视频演示。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*