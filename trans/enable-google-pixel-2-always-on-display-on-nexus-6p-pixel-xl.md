# 在没有 Root 用户的 Nexus 6P、Pixel 和 Pixel XL 上启用 Google Pixel 2 的始终显示

> 原文：<https://www.xda-developers.com/enable-google-pixel-2-always-on-display-on-nexus-6p-pixel-xl/>

谷歌 Pixel 2 和 Pixel 2 XL 是谷歌 Pixel 智能手机系列的最新智能手机，虽然硬件主要是对上一代 Pixel 手机的渐进式改进，但软件有几个非常漂亮的新功能。这款手机的[肖像模式功能](https://www.xda-developers.com/google-pixel-2-tech-emulate-bokeh/)中使用了新的摄像头技术，名为[的永远听音乐识别功能现在正在播放](https://www.xda-developers.com/how-google-pixel-2-now-playing-works/)，以及永远显示功能。不幸的是，这些功能都不会出现在谷歌以前的智能手机上，至少官方不会。我们之前展示了可以通过自定义 ROM 启用 Pixel 2 的 Always on Display [，但是我们最近发现可以在没有 root 的 Nexus 6P、Pixel 和 Pixel XL 上启用 Always on Display**。**](https://www.xda-developers.com/enable-google-pixel-2-always-on-ambient-display/)

*图片来源:XDA 少年成员[炎 03](https://forum.xda-developers.com/member.php?u=7322252)*

* * *

## 得益于 Android 8.1 和 Substratum，现在可以启用“始终显示”

之前，我们曾报道过，在任何老款谷歌手机上都无法启用“永远显示”功能。这是因为 Google 硬编码了这个函数，使得 Always on Display 总是返回 false。Android 8.0 Oreo 的源代码下降就是这种情况，但随着 [Android 8.1 Oreo 开发者预览版 1](https://www.xda-developers.com/android-8-1-oreo-developer-preview-features/) 的发布，情况不再如此。

如上面的屏幕截图所示，负责确定是否启用始终显示的函数先前只返回“false”然而，在最新的[AmbientDisplayConfiguration](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r4/core/java/com/android/internal/hardware/AmbientDisplayConfiguration.java#82)代码中，它现在会检查一个名为“[config _ dozealysondisplayavailable](https://android.googlesource.com/platform/frameworks/base/+/oreo-dr3-release/core/res/res/values/config.xml#1832)的布尔配置值，该值由谷歌设置为在 Pixel 2 和 Pixel 2 XL 上为真，但在他们制造的其他手机上为假。

更具体地说，Google 使用安装在/vendor/overlay 中的一个名为 framework-RES _ auto _ generated _ rro 的框架覆盖来指定该配置的值。由于这个框架覆盖是基于 OverlayManagerService (OMS)的，我们可以创建自己的框架覆盖来**强制 config _ dozeAlwaysOnDisplayAvailable 在 Nexus 6P、Pixel 和 Pixel XL 上返回“true”**。

这是可能的，因为索尼构建的主题框架 OMS 从 Android Oreo 开始被原生集成。得益于此，我们可以使用内置的命令来管理和安装我们自己的主题— [，而不需要 root](https://www.xda-developers.com/android-oreo-rootless-system-theme/) 。在这样做的过程中，开发者发现了如何让流行的[底层主题管理器](https://www.xda-developers.com/andromeda-substratum-custom-themes-oreo/)在 Android Oreo 设备上运行。因此，为了让显示器始终工作，**我们将使用 Substratum 主题管理器及其 Andromeda 插件**，以便在 Nexus 6P、Pixel 和 Pixel XL 上安装我们的特殊框架覆盖。

最后，还有一个我想解决的困惑点——即，我们正在使用通常所说的“主题引擎”来实现一个隐藏的特性。虽然 Substratum 通常用于安装主题，但称这些主题为“资源覆盖”更准确这是因为这些“主题”指定了替换其目标应用程序的原始资源的值。通常资源覆盖只是替换原始应用程序中的颜色值，但它们也可以针对应用程序资源中的整数、字符串或布尔值。一些现有的底层覆盖使用这个[来定制锁定屏幕，最近的应用程序屏幕，和快速设置](https://www.xda-developers.com/minimal-lock-screen-rounded-recent-app-more-quick-setting-columns-android-oreo/)例如。

无论如何，希望你对我们将要做的事情有更好的理解。按照下面的教程，从 Pixel 2 到第一代谷歌 Pixel 手机以及 Nexus 6P，都可以实现始终显示。

* * *

## 如何在 Nexus 6P、Pixel 和 Pixel XL 上启用 Google Pixel 2 的始终显示功能

**要求**:

*   Nexus 6P，谷歌 Pixel，或者谷歌 Pixel XL。Nexus 5X 可以工作，但不建议使用，因为它没有有机发光二极管屏幕。
*   Android 8.1 奥利奥开发者预览版 1。你可以在这里找到固件文件。
*   Substratum 的 Andromeda 插件的许可证(1.99 美元)。没有这个，你将无法安装我们制作的框架覆盖。至少，不容易。

### **教程**

*特别感谢 XDA 初级会员 [InFlames03](https://forum.xda-developers.com/member.php?u=7322252) 协助发现这一特性，并对其进行测试，最后提供了一个框架覆盖图供下载。看看他的新[奥利奥](https://play.google.com/store/apps/details?id=baka.sai.oreo)和[新鲜](https://play.google.com/store/apps/details?id=baka.sai.thema)主题。*

1.  设置底层和它的仙女座插件。你可以一路跟随[这篇教程](https://www.xda-developers.com/custom-themes-android-oreo-substratum/)直到你完成第 1 部分。
2.  安装安卓文件主机的 [alwaysOn-enabler APK 或谷歌 Play 商店的](https://www.androidfilehost.com/?fid=673791459329060953) [Pixel Enabler 应用](https://play.google.com/store/apps/details?id=baka.sai.pixelEnabler)。前者只是实现这一功能的基本叠加，而后者将在未来包含更多功能。
3.  打开底层，在主题列表中寻找 Sai 的“ **Always On Enabler** ”。轻敲它。
4.  点击“**选择以切换所有覆盖图**
5.  点击**浮动漆滚筒按钮**。
6.  选择**建立&启用**
7.  **重启**。
8.  打开设置->显示。展开“**高级**类别，点击“**环境显示**
9.  您应该会看到一个“**始终打开**”开关。**禁用并重新启用**。享受永远展示！

或者，您可以观看下面的视频，该视频介绍了启用始终显示所需的基本步骤。该视频是由 XDA 资深会员 eqbirvin 在他运行 Android 8.1 Oreo 的 Google Pixel XL 上拍摄的。**注意，即使视频中没有显示重启，我们仍然建议你重启。**

### 警告

Nexus 6P、Pixel 和 Pixel XL 默认情况下不提供始终显示功能，因为它们的屏幕没有像 Pixel 2 的屏幕那样正确地调整到低功耗休眠状态。因此，使用这种覆盖来实现始终显示可以被认为是一种黑客行为，因为它并非没有警告。我们已经很长一段时间没有使用它来测量功耗或其他潜在问题，但目前为止我们遇到了以下问题:

*   按下电源按钮从“始终打开”屏幕直接唤醒到锁定屏幕不起作用。你必须按两次电源按钮。
*   双击从“总是打开”屏幕直接唤醒到锁定屏幕不起作用。你必须双击两次(4 次点击)。
*   有时，在解锁阶段可能会弹出一个灰色屏幕。

如果使用指纹扫描仪从“始终显示”屏幕解锁手机，则不会出现上述任何问题。如果你确实遇到了上面列出的任何问题，一个简单的重新锁定和解锁与您的指纹可以解决这个问题。

## 结论

我们怀疑上面列出的问题与显示器不能正确地从“始终显示”状态转换到“屏幕显示”状态有关，我们正在研究潜在的修复方法。这些问题可能永远不会得到解决，或者可能会在未来的开发者预览版中得到解决。我们最大的恐惧是谷歌看到我们在做什么，并且总是显示硬编码。我们希望这不会发生，但这肯定是有可能的。现在，尽你所能享受谷歌 Pixel 2 的永远显示功能吧！