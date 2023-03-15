# 谷歌像素 2 有一个隐藏的，但被禁用的，黑暗的主题

> 原文：<https://www.xda-developers.com/hidden-dark-theme-google-pixel-2/>

更新 11:14 CST:根据 *The Verge* ，有一个隐藏的方法可以启用这个黑暗主题(可能只有在使用 Pixel Launcher 的情况下)。我们不知道这是如何被忽视的，但是原文在下面。

你听说了吗？威瑞森昨天开放了他们的商店，现场演示新的谷歌像素 2 和谷歌像素 2 XL。当大多数人都在花时间感受这款手机时(因为这是你在这类促销活动中应该做的)，我们 XDA 一直在挖掘手机，为你带来最新的应用程序，揭示最新的功能。你可以获得我们提取的最新 [Pixel Launcher](https://www.xda-developers.com/get-google-pixel-2-pixel-launcher-bottom-search-bar/) 和 [Google Camera](https://www.xda-developers.com/download-google-camera-motion-photo/) 应用，但还有几个其他的预装应用你不容易安装。一个这样的应用实际上非常有趣，因为它是 SystemUI 的**隐藏黑暗主题。**

不幸的是，看起来这个黑暗的主题被**禁用了**，无法在 Pixel 2 中访问它(至少，在没有 ADB 的情况下，我无法测试它，直到我得到我的审查模型)。app 简单命名为“Dark”，其包名为“`com.android.systemui.theme.dark`”它存储在`/vendor/overlay/SysuiDarkTheme/SysuiDarkThemeOverlay.apk`中。

正如我们在 Android 8.0 Oreo 的完整[源代码发布后不久发现的那样，谷歌已经引入了一个用于管理主题](https://www.xda-developers.com/android-oreo-source-code/)的[命令行界面。这实际上使得 Android Oreo](https://www.xda-developers.com/android-oreo-command-line-themes/) 的[无根底层成为可能，也是目前任何运行 Android Oreo](https://www.xda-developers.com/andromeda-substratum-custom-themes-oreo/) 的人能够[在他们的设备上安装黑暗主题](https://www.xda-developers.com/install-dark-theme-android-oreo-without-root/)的最佳方式。

*安卓奥利奥黑暗主题安装了[仙女座附加软件用于底层](https://www.xda-developers.com/custom-themes-android-oreo-substratum/)*

利用我们对 OMS 的了解(覆盖管理器服务——谷歌在 Android 8.0 中添加了对索尼主题框架的全面支持),我们很快就发现这个预装的“黑暗”系统 APK 实际上是 SystemUI 的 OMS 主题。安装位置是一个线索，因为它存储在目录中，Google 指示供应商存储他们希望预安装的任何主题。

不幸的是，我们无法测试这种黑暗主题是否可以在谷歌 Pixel 2 上实际启用。这是因为我们只能在我们当地的威瑞森商店使用手机，在那里获得亚行的访问权限来运行必要的命令是不可能的。

### 更新 1 -启用它的方法

根据早期的亲身经历 [*濒临*](https://www.theverge.com/2017/10/4/16405192/new-google-pixel-2-xl-phone-photos-video-hands-on) :

> #### 它还会关注你的壁纸:如果是深色的，应用启动器和通知阴影会自动切换到深色模式来匹配。

通知阴影是由 SystemUI 控制的，所以这就解释了谷歌 Pixel 2 在哪里使用了这个黑色主题。这并不意味着我们不能利用这些发现，尽管如此，因为这种自动黑暗主题切换可能只有在你使用股票像素启动器时才有效。这意味着如果你使用 Nova Launcher(我说“可能”是因为还没有人在 Pixel 2 上测试过第三方 Launcher ),设置深色壁纸可能不起作用。)

这是我们下周收到 Pixel 2 XL 后必须彻底测试的东西。

### 更新 2 -黑暗主题的能力

看起来黑暗主题在它所能表达的主题方面是非常有限的。ArsTechnica 的 Ron Amadeo 指出，黑暗主题只适用于快速设置面板。出于好奇，我回去提取覆盖 APK，然后反编译它来验证自己:

```
 ?xml version="1.0" encoding="utf-8"?>
<resources>
<style name="qs_base" parent="@android:style/Theme.DeviceDefault">
<item name="android:colorControlNormal">?android:textColorPrimary</item>
<item name="android:colorPrimary">@android:color/primary_device_default_settings</item>
<item name="android:colorPrimaryDark">@android:color/primary_dark_device_default_settings</item>
<item name="android:colorAccent">@android:color/accent_device_default_dark</item>
<item name="android:colorBackgroundFloating">#ff000000</item>
<item name="android:colorSecondary">@android:color/secondary_device_default_settings</item>
</style>
</resources> 
```

这样做的目的是指定快速设置面板的颜色，在这种情况下，使其颜色更深。

### 更新 3 -没有骰子

我们去了威瑞森商店，试图通过设置深色壁纸来启用深色主题，就像 The Verge 提到的那样，但是我们没有成功。什么都没发生。我们不完全确定原因。

### 更新 4——它工作了——短暂地

我亲自回到威瑞森商店，确认如果你启用“阴影”类别中的一种壁纸，你可以为快速设置面板设置一个深色主题。