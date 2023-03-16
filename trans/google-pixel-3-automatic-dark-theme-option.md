# 谷歌 Pixel 3 有一个基于时间的自动深色主题功能

> 原文：<https://www.xda-developers.com/google-pixel-3-automatic-dark-theme-option/>

今年新的谷歌 Pixel 智能手机带来了大量的[新相机功能](https://www.xda-developers.com/google-pixel-3-google-pixel-3-xl-specs-features-pricing-availability/)，如 Top Shot、Super Res Zoom、主体跟踪自动对焦、Photobooth、谷歌镜头建议等。谷歌 Pixel 3 在其 Android Pie build 中也有新功能，如驾驶模式、翻转到 Shhh、自适应颜色模式、谷歌双工和来电显示。然而，并不是每个新的软件功能都有自己的标题。软件体验中有大量的[小附加物](https://www.xda-developers.com/google-pixel-3-google-pixel-3-xl-minor-features/)，我们必须自己去寻找。其中一个功能是对很多读者喜欢的东西的更新:自动黑暗主题选项。是的，Android 8.1 Oreo 已经有了一个基于你当前壁纸触发的黑暗模式，但 Pixel 3 更新后的 Pie build 上的新功能会根据一天中的时间或是否启用了节电模式来自动打开黑暗主题。

提醒一下，谷歌 Pixel 3 上的[手动启用](https://www.xda-developers.com/google-pixel-launcher-manual-dark-theme/)黑暗主题目前是这样做的:

*   将**快速设置**面板的背景变暗
*   将**音量**面板的背景变暗
*   将 **Pixel Launcher 的应用抽屉**的背景变暗
*   将 **Google Discover** (原 Google Feed)的背景变暗

这不是一个全系统的主题，不像你会在即将到来的三星 Galaxy S9 或三星 Galaxy Note 9 的[三星 Experience 10](https://www.xda-developers.com/samsung-experience-10-night-theme-galaxy-s9/) 中发现的那样，但这是一个很好的触摸。这里有一些展示谷歌 Pixel 3 黑暗主题的截图。

你可以通过设置->显示并选择“设备主题”来启用黑暗主题您可以将其设置为根据当前壁纸自动更改或手动打开/关闭。这就是它目前在任何接近库存的 Android Pie 上的工作方式，比如说在 Google Pixel 或 Google Pixel 2 上。但在谷歌 Pixel 3 上运行的 Android Pie build 上，你也可以使用“设置夜间模式”开发者选项，根据一天中的时间或手动打开/关闭黑暗主题。当我根据一天中的时间启用自动黑暗主题并手动更改我的设备的时间时，黑暗主题在下午 6:55 打开，在早上 7:30 关闭。不过，我不确定时间是不是基于地点。

早期 Pixel 设备的当前版本的 Android Pie 不允许您通过这个开发者选项来控制黑暗主题。Pixel 3 能够做到这一点要感谢[这个 commit](https://android.googlesource.com/platform/frameworks/base/+/a5c846c3fa74d680eddca6b994b7cf8449d301ef%5E%21/#F0) ，它还提到了黑暗主题可以通过打开电池节省器来启用(我们可以在 Pixel 3 上确认这一点。)我们不认为这项功能将仅限于 Pixel 3，并将在其他 Pixel 设备的未来更新中推出，但我们不能肯定。

最后，通过这个开发者选项激活黑暗主题似乎不能在 Google Discover 或 Pixel Launcher 中启用黑暗背景。我们不确定为什么会这样，但如果你想更好地控制 Android Pie 中的黑暗主题，我们建议你使用 Tasker。你甚至可以根据夜间灯光状态来切换[黑暗主题。当我完成谷歌 Pixel 3 XL 评测的第二部分时，我会密切关注我发现的更多隐藏功能。你可以在这里阅读我的评论](https://www.xda-developers.com/enable-android-p-dark-theme-night-light/)[的第一部分](https://www.xda-developers.com/google-pixel-3-xl-camera-software-design-pixel-stand/)。