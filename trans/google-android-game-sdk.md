# 谷歌准备为开发者推出一款安卓游戏 SDK

> 原文：<https://www.xda-developers.com/google-android-game-sdk/>

**更新 1 (12/5/19 @美国东部时间下午 4:30):**谷歌已经在一篇博文中正式公布了游戏 SDK。更多细节见下文。原条款保持如下。

去年年底，谷歌在 AOSP 创造了一棵名为“gamesdk”的新树在过去的一年里，谷歌的工程师们已经慢慢地向这棵树添加了代码，本周，他们似乎正在为首次公开发布做准备。“Android 游戏 SDK”的最初版本将专注于帮助移动游戏开发者改善他们的 Android 游戏中的帧速度。游戏 SDK 的 1.0.0 版本包括 Android 帧调步库，作为一个静态库，供移动游戏开发者集成到他们的引擎中。

值得注意的是，Unity 已经将 Android Frame pace 整合到了它的游戏引擎中。作为背景，今年 5 月，Unity [宣布了其游戏引擎的](https://blogs.unity3d.com/2019/05/09/unity-2019-2-beta-is-now-available/)版本 2019.2 beta。该版本在“Android 设置”部分包含了一个名为“优化帧速度”的新设置。Unity 表示，他们与谷歌的 Android 游戏和图形团队合作开发了这项功能，以“通过减少帧分布的差异来[提供]一致的帧速率。”[根据 Unity Technologies 移动平台高级技术产品经理 JC Cimetiere 的说法，这种新的优化帧调步设置“通过同步游戏提交帧的时间和显示硬件消耗帧的时间来防止帧队列的增加。”启用该选项后，“帧在队列中花费的时间更少，从而减少了输入延迟”，并使玩家的输入事件更快地反映在屏幕上。](https://forum.unity.com/threads/whats-the-optimized-frame-pacing-feature.636847/#post-4291420)

 <picture>![](img/2711c81f18f46ec0bc2efba49fae6729.png)</picture> 

Optimized Frame Pacing in Unity's Player Settings for Android. Source: Unity Technologies.

谷歌[在谷歌 I/O 2019 上简要介绍了](https://youtu.be/RY7wXC_b0R8?t=291)新的安卓帧调步 API，他们[也在安卓开发者网站上发布了关于它的页面](https://developer.android.com/games/optimize/frame-pacing)。该网页描述了如何根据您的游戏渲染引擎使用 OpenGL ES 还是 Vulkan API，使用单独的指令集将 Android 帧调整集成到您自己的项目中。提供了两个示例项目——[bouncy ball](https://android.googlesource.com/platform/frameworks/opt/gamesdk/+/refs/heads/master/samples/bouncyball)和[Cube](https://android.googlesource.com/platform/frameworks/opt/gamesdk/+/refs/heads/master/third_party/cube/)——分别演示了如何使用 Android 帧调整库在使用 OpenGL ES 或 Vulkan 的游戏中实现正确的帧调整。

尽管谷歌[发布了](https://android.googlesource.com/platform/frameworks/opt/gamesdk/+/refs/heads/master/RELEASE_NOTES)Android 游戏 SDK 1 . 0 . 0 版本的发行说明，但该公司尚未发布公告。发行说明中提到的公共游戏 SDK 页面也还没有上线，所以我们期待很快看到一个公告。

**安卓游戏 SDK 1 . 0 . 0 版本发布说明**

*   这个 Android 游戏 SDK 的初始版本以 Android 帧调步库为特色。
*   特征
    *   显示缓冲区同步。
    *   自动刷新率模式和流水线支持。
    *   帧呈现统计信息的集合。
    *   根据 Swappy 所需的 Android、OpenGL 和 Vulkan 特性，在运行时优雅地选择行为。
    *   图书馆的静态和动态链接。
    *   支持多种刷新率的设备。

欲了解更多信息，请参阅 https://developer.android.com/games/sdk/.

*感谢 XDA 公认的开发者 luca020400 的提示！*

## 更新 1:游戏 SDK 博文

在 Android 开发者博客上，谷歌[正式宣布了](https://android-developers.googleblog.com/2019/12/android-game-sdk.html)Android 游戏 SDK，这是一套程序库，手机游戏开发者可以用来增强他们的游戏。正如预期的那样，第一版侧重于帮助游戏开发者提高帧速度。谷歌表示，帧调整库已集成到 Unity SDK 及更高版本中，但访问游戏引擎源代码的开发人员可以通过访问[页面](https://developer.android.com/games/sdk/)了解如何将该库集成到他们的 OpenGL 或 Vulkan 渲染器中。