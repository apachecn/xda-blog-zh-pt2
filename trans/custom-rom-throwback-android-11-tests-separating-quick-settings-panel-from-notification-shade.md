# Android 11 测试了快速设置面板和通知阴影的分离

> 原文：<https://www.xda-developers.com/custom-rom-throwback-android-11-tests-separating-quick-settings-panel-from-notification-shade/>

Android 11 的第一批版本于几小时前发布，以开发者预览版 1 的形式向我们展示。这个新版本的 Android 带来了许多新的[隐私和安全方面的变化](https://www.xda-developers.com/android-11-developer-preview-privacy-security-features-changes/)，[几个面向开发者的更新](https://www.xda-developers.com/android-11-developer-preview-new-development-features/)，以及[一大堆谷歌](https://www.xda-developers.com/android-11-developer-preview-changes/)发布的[公告中没有的变化](https://developer.android.com/preview/)。当我们在寻找最新版本的 Android 中更多新的、未宣布的变化时，我们偶然发现了一些让我们惊讶的东西...但也不尽然。在 Android 11 中，谷歌正在测试快速设置面板与通知阴影的分离——这一功能过去存在于几个旧的定制 rom 中。

正如 Mishaal 在他运行 Android 11 开发者预览版 1 的谷歌 Pixel 2 Xl 上演示的那样，Android 11 正在测试一项功能，该功能将快速设置下拉列表与通知面板下拉列表分开，允许你根据你从状态栏的哪一侧下拉来快速跳转到哪一侧。在视频中，你可以在状态栏上发现一条白线，指示分离点——从这条线的左侧向下滑动将下拉通知阴影，而从这条线的右侧向下滑动将下拉快速设置面板。如果您的目的是访问快速设置面板，这将通过消除当前访问它们所需的双击来简化您的体验。

从视频中可以明显看出，这一功能仍处于开发阶段。通知没有正确地与通知阴影的顶部对齐，并且快速设置面板在通知通常出现的地方有一条奇怪的线。因此，默认情况下，此功能不可用于切换，需要手动激活。

关于这个 UI 测试的一个理论是，谷歌可以在快速设置面板和通知阴影上与其他 UI 测试一起进行测试，例如在快速设置面板中集成音乐控件，而不是在通知面板中集成音乐控件。它还可以绑定到通知阴影中的[专用对话视图，再加上前面提到的音乐控件变化，可以被视为一种消除通知阴影并改善整体体验的尝试。](https://www.xda-developers.com/android-11-developer-preview-new-development-features/)

如果你在姜饼和冰淇淋三明治的时代见过定制的 ROM 场景，你会意识到这并不是一个新功能。我个人记得在基于 Android 2.3.4 姜饼的基于 Touchwiz 的定制 rom 以及基于 Android 4.0 冰激凌三明治的大量修改的 CyanogenMod 版本上使用过这个功能。看起来谷歌现在已经从定制 rom 中获得了这个 UI 测试的灵感，尽管在这个阶段，还不能保证这个功能会在 Android 11 的最终版本中实现。

**[安卓 11 XDA 新闻](https://www.xda-developers.com/tag/android-11/)**