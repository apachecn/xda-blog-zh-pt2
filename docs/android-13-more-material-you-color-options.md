# Android 13 可能会有更多的材质和颜色选择

> 原文：<https://www.xda-developers.com/android-13-more-material-you-color-options/>

Google 的素材你是在 [Android 12](https://xda-developers.com/android-12) 中加入的，我们看到是在 Android 12L 中[最终加入了 AOSP。现在它将被更多的原始设备制造商使用，谷歌正致力于为](https://www.xda-developers.com/monet-engine-open-sourced-android-12l/) [Android 13](https://www.xda-developers.com/android-13) 的发布改进它，它的第一个改进看起来将打包多达五种额外的颜色风格。这些新的颜色风格被称为色调 _ 点，充满活力，富有表现力，SPRITZ，彩虹和水果 _ 沙拉。

从本质上来说，谷歌创建了一个名为“莫奈”的主题引擎，可以从用户的壁纸中生成丰富的彩色调色板[。然后，这些颜色被应用到系统的各个部分，它们的值通过用户应用程序可以调用的 API 来提供，从而让应用程序决定是否也要对其 UI 重新着色。然而，正如*斯珀*所发现的，现在通过使用 adb，实际上有可能在](https://www.xda-developers.com/android-12-wallpaper-theme/) [Android 13 开发者预览版 2](https://www.xda-developers.com/android-13-developer-preview-2/) 上启用一套全新的颜色选项。下面详细介绍了这些新颜色样式的作用:

*   色调 _ 专色:默认材质你的颜色
*   充满活力:生成色调更丰富的调色板，色调稍有变化，二级色和背景色更加丰富多彩
*   表现力:生成具有多种突出色调的调色板，这些色调比鲜艳的色彩更丰富
*   SPRITZ:生成一个更低的调色板

斯珀没有分享彩虹和水果沙拉的信息。

*图片来源:斯珀*

您可以运行以下 adb 命令，在任何运行最新 Android 13 开发者预览版的设备上设置这些音调，将“STYLE”替换为上述内容之一。

```
 adb shell settings put secure theme_customization_overlay_packages '''{\"android.theme.customization.theme_style\":\"STYLE\"}''' 
```

当然，谷歌可能不会在 Android 13 的最终版本中通过面向用户的 UI 来实现这些功能。该公司也有可能在未来的版本中致力于此，这正是我们发现该公司正在为 Android 11 开发滚动截图后发生的事情。这项功能后来才在 Android 12 中推出。

尽管如此，除非谷歌锁定对它的访问，否则你还是有希望通过亚行访问它。不过，如果你不想为 adb 费心，你可以使用最新版本的 Repainter ，它将在你的 Google Pixel 上为你运行 adb 命令。

* * *

**来源:** [斯珀](https://blog.esper.io/android-13-deep-dive/#material_you_styles)