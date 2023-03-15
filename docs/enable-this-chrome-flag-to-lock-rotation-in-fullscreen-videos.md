# 启用此 Chrome 标志以锁定全屏视频中的旋转

> 原文：<https://www.xda-developers.com/enable-this-chrome-flag-to-lock-rotation-in-fullscreen-videos/>

# 启用此 Chrome 标志以锁定全屏视频中的旋转

启用此 Chrome 标志来锁定浏览器中播放的任何全屏视频的旋转(方向锁定)。有 Dev 和 Canary 两种款式。

在 XDA，当我们不报道我们认为当天重要的新闻或发表深入分析文章时，我们喜欢用有趣的项目、谣言和提示来填补空白。就在昨天，[我发布了一个提示](https://www.xda-developers.com/psa-moving-chromes-address-bar-to-the-bottom-no-longer-causes-visual-bug/)，提醒用户一个有用的 Chrome 标志已经过改进。今天为大家带来另一个有用的 Chrome 标志:**在播放全屏视频时锁定屏幕方向**。

> #### **全屏播放视频时锁定屏幕方向。**
> 
> #### 当视频全屏播放时，Android 会锁定设备的屏幕方向以匹配视频方向。只在手机上。

该标志在 Android 版谷歌 Chrome 浏览器的 Dev 和 Canary 频道中可用，每当您全屏播放视频时，它会锁定设备的屏幕方向，以匹配视频的方向。这在你躺在床上看视频时会很有用，你可能会不小心翻了视频(可能会发生在我们很多人身上)。以下是展示国旗运行前后的视频:

如您所见，一旦启用，视频会根据视频最突出的方向自动设置适当的旋转。此外，当我物理旋转我的设备时，我被阻止更改视频的旋转(尽管在视频中你看不到我翻转手机)。你不再需要摸索改变你的快速设置或使用 Tasker 自动改变某些应用程序中的旋转锁。现在，谷歌 Chrome 将为你处理这个问题——当然，前提是你观看的是全屏视频。

要启用此标志，只需将以下 URL 粘贴到地址栏中。请记住，这一功能被认为是实验性的，它完全有可能不会成为 Chrome 的稳定版本。不过，我在启用这个标志时没有遇到任何重大问题，所以我乐观地认为它最终会推广到所有的 Chrome 频道。

```
chrome://flags/#video-fullscreen-orientation-lock
```

享受轻松的视频观看体验！