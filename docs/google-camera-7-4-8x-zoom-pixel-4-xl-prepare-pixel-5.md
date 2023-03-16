# 谷歌相机 7.4 增加了分辨率切换，并准备像素 5 支持

> 原文：<https://www.xda-developers.com/google-camera-7-4-8x-zoom-pixel-4-xl-prepare-pixel-5/>

几个月前，我们在预发布的 Pixel 4a 设备上发现了谷歌相机应用程序的泄露版本[7.4 版](https://www.xda-developers.com/google-camera-7-4-leak-4k-60fps-video-recording/)。今天，Pixel camera 应用程序的 7.4 版本面向谷歌 Play 商店的用户推出，它带来了一些明显的变化。

**更新(美国东部时间 6/5/2020 @ 11:47am):**来自 *AndroidPolice* 的 Per Rita Khoury，似乎 8 倍变焦对于 Pixel 4 系列来说其实并不新鲜——你只需要将视频质量设置为 1080p30 就可以使用它。社区中的许多人(包括我们自己)不知道 8 倍变焦的视频录制是可能的，所以这里有一个提示，它是可用的。

**像素 4 和像素 4 XL 上的视频 8 倍变焦**

首先，升级到谷歌摄像头 7.4 将使 Pixel 4 和 Pixel 4 XL 的用户能够以 8 倍的变焦水平录制视频。以前，您只能以最大 6 倍的变焦水平进行录制。由于谷歌的 Super Res Zoom 算法，Pixel 4 已经可以以高达 8 倍的变焦水平拍摄照片，而质量损失最小，尽管这款手机只有大约 2 倍的长焦摄像头。

为了以 8 倍变焦进行录制，您不能使用 1080p 视频分辨率模式下可用的“自动”或“60fps”帧速率选项。

 <picture>![8X zoom with Google Camera 7.4 on Pixel 4](img/1c4d972ca8e05e689258811c63e7af65.png)</picture> 

Credits to Telegram user @AAmedeus for the screenshot!

然而，在最新发布的谷歌相机上，4k60 [或 4k24](https://www.xda-developers.com/google-camera-7-3-do-not-disturb-setting-24-fps-video-pixel-4a-code-name/) 的视频录制仍然不可用。

**视频分辨率快速切换**

谷歌是否让用户更清楚他们将在谷歌相机 7.4 中以什么样的分辨率录制视频？当你在视频标签中点击下拉菜单时，你会看到新的“全高清(1080p)”和“4K(超高分辨率)”选项。在 7.3 版本中，下拉菜单仅显示“闪光”和“帧数/秒”选项，而 4K 分辨率录制的切换仅在完整设置菜单中可用。

最后，在清单中，添加了新的行，暗示即将支持[像素 4a](https://www.xda-developers.com/google-pixel-4a-camera-review-leak/) 和[像素 5](https://www.xda-developers.com/google-pixel-5-snapdragon-765/) 。Pixel 4a 将使用谷歌相机的“2020 年年中”配置，而 Pixel 5 将使用“2020”配置。

```
 <uses-library android:name="com.google.android.camera.experimental2020" android:required="false"/>
<uses-library android:name="com.google.android.camera.experimental2020_midyear" android:required="false"/> 
```

我们将进一步挖掘这个版本的谷歌相机应用程序，看看我们是否能发现任何新的相机功能的细节。7.4 版本现已在谷歌 Play 商店向用户推出，请访问下面的链接查看更新。