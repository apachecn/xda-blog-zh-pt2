# 如何在 Android O 中给导航栏添加自定义图标

> 原文：<https://www.xda-developers.com/how-to-add-custom-icons-to-the-navigation-bar-in-android-o/>

如果你一直在关注我们对 Android O 的报道[，那么你可能已经看到了我们的教程，关于如何修改导航栏以](https://www.xda-developers.com/tag/android-o/)[切换画中画模式](https://www.xda-developers.com/enable-android-o-picture-in-picture-mode/)，在播放音乐时启用[媒体控制键](https://www.xda-developers.com/how-to-enable-media-playback-nav-bar-controls-in-android-o-when-playing-music/)，以及今天如何添加[前进/前进按钮以快速浏览你的电子邮件](https://www.xda-developers.com/add-forward-backward-keys-to-android-o-nav-bar-quickly-read-emails/)。一个[可定制的导航条](https://www.xda-developers.com/android-o-preview-brings-nav-bar-customization-under-system-ui-tuner/)的可能用途是巨大的，我们的前三个教程仅仅触及了表面。但是，虽然我们确实有一些更有用的教程与我们的读者分享，但在我们继续下一个教程之前，有一件事我们必须知道:**如何在 Android O 中向导航栏键添加自定义图标。**

Android O 的新导航栏定制器，可通过 SystemUI Tuner 访问，允许您为导航键设置键码。(提醒:为了访问 SystemUI Tuner，您必须下拉状态栏并长按右上角的齿轮图标，直到您看到一条提示消息，告诉您 SystemUI Tuner 现在可以访问。)由于键码太多，Android O 并没有为你可以放在导航条上的每个键码提供一个图标，而是允许你从 6 个图标中选择:*圈*、*加*、*减*、*左*、*右*和*菜单*。

既然我们知道了如何通过 shell 命令手动设置键码，我们也想知道有哪些图标是可用的。我们首先发现两个导航栏键在[设置下被定义为两个系统属性。安全等级](https://developer.android.com/reference/android/provider/Settings.Secure.html)。这两个属性被命名为`sysui_nav_bar_left`和`sysui_nav_bar_right`，分别对应左侧导航条键和右侧导航条键。这些属性接受一个字符串值，可以是`clipboard`、`menu_ime`或`key([KEYCODE_KEY](https://developer.android.com/reference/android/view/KeyEvent.html):ICON_RESOURCE)`中的一个。

使用运行 Android O 开发者预览版的测试 Google Pixel 设备，我们发现默认显示的 6 个图标对应于 SystemUI 中包含的特定内容资源，由 URI 表示。

1.  `com.android.systemui/2131230944`(圆圈)
2.  `com.android.systemui/2131230848`(加)
3.  `com.android.systemui/2131231002`(减号)
4.  `com.android.systemui/2131230907`(左)
5.  `com.android.systemui/2131231004`(右)
6.  `com.android.systemui/2131230913`(菜单)

由于这些值来自 Google Pixel，因此这些图标资源在运行 Android O 开发者预览版的其他 Google 设备上可能会有所不同。但是由于图标资源是一个内容 URI，我们可以用一个文件 URI 方案来替换它，以指向存储在我们设备上的任何图标。

### 如何在 Android O 中设置自定义导航条图标

文件 URI 如下所示:

```
 file: 
```

结合我们上面设置自定义键码的知识，我们现在可以将任意图像设置为显示在导航栏中的图标。例如，如果我想将我的左导航键设置为[键码 _ DPAD _ 向下](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_DPAD_DOWN) (#20)，自定义向下箭头图标保存为 down.png，将我的右导航键设置为[键码 _ DPAD _ 向上](https://developer.android.com/reference/android/view/KeyEvent.html#KEYCODE_DPAD_UP) (#19)，自定义向上箭头图标保存为 up.png，这两个图标都存储在我的内部存储器的根目录上，我的命令如下所示:

```
 settings put secure sysui_nav_bar_left key(20:file:
settings put secure sysui_nav_bar_right key(19:file: 
```

您可以使用 ADB shell 输入这些命令，或者将`WRITE_SECURE_SETTINGS`权限授予 [SecureTask](https://play.google.com/store/apps/details?id=com.balda.securetask&hl=en) ，然后使用 Tasker 根据特定条件触发导航条更改，正如我在以前的教程中概述的那样(也将在另一个教程中展示)。

### 如何为你的导航条定制图标

当然，考虑到你的导航条的大小，你不能把你从网上下载的任何图片放在上面。图像需要合适的大小，否则它要么看起来太小，要么看起来太大。如果你还没有使用 PhotoShop 或其他图像处理软件的经验，获得合适尺寸的图像可能是一个挑战，但幸运的是，有一些网站提供了许多我们可以使用的免费图标。

你需要做的第一件事是确定你的设备的显示指标，这可能是你已经知道的，但如果你不知道，你可以[在 Material.io](https://material.io/devices/) 上查找。接下来，你需要将你的显示密度与[图标参考图表](http://iconhandbook.co.uk/reference/chart/android/)联系起来，以确定你需要什么尺寸的图标。最后，使用免费的[图标数据库](http://www.iconsdb.com/)下载你正在寻找的合适尺寸的图标。

确保您将要使用的图标保存在特定的文件夹中，如/NavIcons，并将图标命名为简单的名称，以便在命令中引用。

* * *

我们希望你觉得这个教程有用！对我个人来说，我对导航条定制器的一个主要疑虑是不能为导航键选择自定义图标，这样我就能立即知道我的导航键在做什么。但是现在我们已经知道了如何在我们自己的条件下放置我们自己的自定义键*和*自定义图标，我们可以开始真正利用我们的导航栏了。