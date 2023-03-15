# 在 Google Pixel 或 Pixel 2 [Root]上设置自定义饱和度

> 原文：<https://www.xda-developers.com/custom-saturation-level-google-pixel-2/>

谷歌最新的旗舰智能手机谷歌 Pixel 2 和 Pixel 2 XL T1 在发布周引起了一些争议。一些早期的评论者抱怨显示问题，如[所谓的烧屏](https://www.xda-developers.com/google-pixel-2-xl-display-burn-issues/)和柔和的颜色。经过[的调查](https://www.xda-developers.com/google-pixel-2-xl-display-burn-issues/)，谷歌[得出结论](https://www.xda-developers.com/google-pixel-2-xl-warranty-color-mode/)烧屏只是暂时的图像残留，而柔和的颜色是因为显示器的颜色准确。尽管如此，该公司还是承认了用户的抱怨，调整了导航栏以防止图像残留，并在 11 月的安全更新中引入了新的颜色模式。不过，多亏了这次更新，我们可以利用引入的方法为我们的设备设置一个**自定义饱和度**。

随着 11 月谷歌 Pixel 2/2 XL 的安全更新，增加了三种新的颜色模式:自然、增强和饱和。根据添加这些颜色模式的[提交](https://android.googlesource.com/platform/packages/apps/Settings/+/adf6951843f36496c85843c1e57e417a7fd77229%5E%21/#F0)，自然是 sRGB，增强是 sRGB + 10%饱和度，饱和是未管理的颜色。关于 Android 上色彩管理的深入解释，我推荐你阅读谷歌的 Nick Butcher 的这篇[优秀文章](https://medium.com/google-design/android-color-management-what-developers-and-designers-need-to-know-4fdd8054557e)。

虽然这些选项足以安抚大多数用户，但有些人想要更多。一些用户，比如来自 *AndroidPolice* 的 Artem Russakovski，想知道是否有可能添加一个饱和度滑块来定制 Pixel 2 XL 显示器的外观。

不管颜色是否准确，有些用户只是喜欢修改显示设置，直到一切看起来都适合他们。在查看了引入新颜色模式的提交之后，我可以报告说，至少可以修改饱和度值。不幸的是，这个**需要 root 权限**，因为 SurfaceFlinger 中的[方法](https://android.googlesource.com/platform/frameworks/native/+/0147a17adb08a155e1d6f72e6ca5e794fc7f5cc4%5E%21/#F0) [要求调用应用程序拥有 HARDWARE_TEST 权限。](https://android.googlesource.com/platform/frameworks/native/+/fabce80b98227b897b4e708afb0b3130596d3f5f)

如果你想在你的设备上尝试一下，你需要确保你的谷歌 Pixel/Pixel XL 安装了 [Android 8.1](https://www.xda-developers.com/android-8-1-oreo-final-release-imminent/) ，或者你的谷歌 Pixel 2/2 XL 至少安装了 11 月的安全更新。至于如何让你的设备扎根，我们的论坛上有几个指南。一旦您满足了这两个要求，那么您可以尝试在“终端”中使用以下命令来调整设备的饱和度。

## 在 Google Pixel 上设置自定义饱和度

首先，在手机上下载一个终端模拟器应用程序。我们推荐谷歌 Play 商店的材料终端。

打开它，然后键入“su”授予 root 访问权限。然后，您可以输入以下命令来修改饱和度:

```
 service call SurfaceFlinger 1022 f X.X 
```

其中 X.X 是介于 0.0 和 2.0 之间的整数值。该值越高，显示越饱和。0.0 使颜色变成黑色和白色，而 2.0 将显示设置为 100%饱和度。

您也可以通过发出以下命令来切换 sRGB 色彩管理:

```
 service call SurfaceFlinger 1023 i32 0/1 
```

其中 0 设置 sRGB 色彩管理，1 禁用色彩管理。

最后，您可以设置以下两个系统属性，以便在引导时保存这些值。

```
 setprop persist.sys.sf.color_saturation X.X
setprop persist.sys.sf.native_mode 0/1 
```

如果你想更容易地改变你显示器的饱和度，你也可以使用这个由 XDA 论坛主持人[zachare 1](https://forum.xda-developers.com/member.php?u=7055541)制作的[开源](https://github.com/zacharee/Sa2ration)应用。这款应用在 XDA 实验室是免费的，所以你可以在下面下载。

[appbox xda com . xda . sa 2 定量]

如果您想要更多的显示器校准选项，如设置显示器伽玛，您可以随时使用 [KCAL](https://forum.xda-developers.com/android/software-hacking/dev-kcal-advanced-color-control-t3032080) 内核模块刷新自定义内核。