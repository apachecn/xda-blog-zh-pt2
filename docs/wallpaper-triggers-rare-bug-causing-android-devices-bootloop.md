# [更新 2:修复]这张壁纸引发了一个罕见的错误，导致 Android 设备启动

> 原文：<https://www.xda-developers.com/wallpaper-triggers-rare-bug-causing-android-devices-bootloop/>

**更新 2 (08/03/2020 @美国东部时间下午 3:03):**随着 2020 年 8 月 Android 安全补丁的发布，谷歌对 Android 进行了更新，修复了这个 bug。更多细节可以在底部找到。

更新 1(美国东部时间 06/04/2020 @ 03:12AM):关于“被诅咒的壁纸”导致手机崩溃的原因，出现了新的解释，谷歌也做出了回应。滚动到底部了解更多信息。下面保留了 2020 年 6 月 1 日发表的文章。

想象一下，你正在网上搜寻很酷的壁纸，然后你看到了一幅如画的风景。它什么都有；郁郁葱葱的绿色森林，有一个小岛的原始湖泊，背景是白雪皑皑的山脉，厚厚的云层覆盖着阳光透过缝隙渗透进来。你立即下载图片，把它设置成你手机的壁纸，然后嘣！你的安卓手机卡在引导回路里了。听起来不太可能，不是吗？嗯，对这张特殊的壁纸来说是真的。

知名的[三星](https://www.xda-developers.com/tag/samsung/)泄密者 Ice Universe 最近在*推特* 上分享了这张壁纸，他声称这张壁纸“会导致你的手机死机！”尽管他们发出了警告，一些用户还是下载了壁纸，以检查它是否真的在他们的手机上做了什么，他们得到了以下结果:

据总部位于 AOSP 的定制 ROM(POSP)的首席开发者大卫·比安科(Davide Bianco)称，这种特殊的壁纸会导致一些 Android 设备崩溃，因为它使用了 RGB 色彩空间，而不是 Android 上原生支持的 sRGB 色彩空间。比安科[已经向 AOSP 提交了一个补丁](https://android-review.googlesource.com/c/platform/frameworks/base/+/1321016)，据报道该补丁修复了这个问题，补丁描述称“当用户试图将一张不是 sRGB 的图片设为壁纸时，就会出现这个问题。发生的情况是变量 y 值高于直方图界限，使 SysUI 崩溃。一种可能的解决方法是将 y 值限制为总是小于 256。除了 Bianco 之外，来自流行的 LineageOS 定制 rom 团队的两位开发人员，XDA 资深成员 [BadDaemon](https://forum.xda-developers.com/member.php?u=5662620) 和 XDA 认可的开发人员 [luca020400](https://forum.xda-developers.com/member.php?u=5778309) ，也提出了解决该问题的独特方案。你可以通过点击[这个链接](https://review.lineageos.org/c/LineageOS/android_frameworks_base/+/276907)和[这个链接](https://review.lineageos.org/c/LineageOS/android_frameworks_base/+/276909)在 LineageOS Gerrit 上查看补丁描述。

我们强烈建议在任何情况下都不要使用这张图片作为你的壁纸。如果您已经使用了它，并且您的设备卡在引导循环中，请查看下面的说明，了解如何能够恢复您的设备。

来自*9 到 5 谷歌*T3 关于此事的[报告进一步透露，该问题仅限于运行 Android 10 或更旧版本的设备，它不影响运行](https://9to5google.com/2020/05/31/android-phone-wallpaper-soft-brick-bug-video/) [Android 11](https://www.xda-developers.com/tag/android-11/) 开发者预览版的设备。这是因为在 Android 11 上，如果不支持，系统会转换色彩空间，但在 Android 10 上不会。这意味着这不是这个特定图像的问题，而可能是由使用 RGB 颜色空间的其他图像引起的。

请注意，虽然这个问题不会影响所有的 Android 设备，但我们强烈建议不要在手机上尝试壁纸。如果您尝试使用它，您可以通过完全重置或进入安全模式并更改壁纸来恢复您的设备。但是由于 Twitter 上的一些用户无法使用上述方法恢复他们的设备，所以最好不要使用确切的图片作为壁纸。如果你真的喜欢这张壁纸，就把它截图下来作为你的壁纸。

* * *

## 更新 1:新的解释，谷歌的回应

根据 XDA 资深会员 [BadDaemon](https://forum.xda-developers.com/member.php?u=5662620) 和 XDA 公认开发者 [luca020400](https://forum.xda-developers.com/member.php?u=5778309) 对 bug 原因的解释，被“诅咒”的壁纸被编码在一个特殊的颜色空间中，这个颜色空间被称为“Google/Skia/E3 cadab 7 BD 3 de 5e 3436874 D2 a9 dee 126”(这是颜色空间的全称，Skia 指的是 Google 制作的 [2D 图形库)。)相比之下，大多数其他壁纸图像是在称为“sRGB”的色彩空间中编码的。](https://skia.org/)

在 Android 版本 10 和更老的版本中，所有图像都被转换成 sRGB，除非开发者另有说明。将图像转换为 sRGB 时会出现一个罕见的错误，其中计算每个像素的“亮度”值的代码设法超过了 255 的最大限制。

使用以下公式计算亮度:

亮度= .2126f * r + .7152f * g + .0722f * b

这里“r”、“g”和“b”是红色、绿色和蓝色值，用从 0 到 255 的 8 位值表示。

这种计算的问题是，在最后求和之前，每个部分总是被四舍五入。“被诅咒的”壁纸中的一个像素，在将图像从 sRGB 转换到灰度的过程中，具有以下 RGB 值:255，255，243，当插入上面的等式时，看起来像:

r: .2126 * 255 = 54.213 => 55

g: .7152 * 255 = 182.376 => 183

b: .0722 * 255 = 18.411 => 19

亮度= r+ g + b = 257

这个值导致 SystemUI，基本上是整个 OS 崩溃，因为它超过了最大值。这是一个非常特殊的错误，因为它涉及到舍入误差和色彩空间转换误差的组合。

这个错误不会影响 Android 11，因为图像的“Skia”色彩空间在默认情况下不会转换为 sRGB。因此，这种色彩空间转换错误和舍入错误不会在 Android 11 上出现。

然而，谷歌 Android Toolkit 团队的 Romain Guy 认为，这个问题的根本原因只在于亮度的计算方式，而不是任何色彩空间转换问题。[谷歌正在进行自己的内部测试，所以我们很快就会看到他们的成果。](https://android-review.googlesource.com/c/platform/frameworks/base/+/1321017/1#message-0cca806c0e467116956512548ee16cede6758903)

*更新了此解释，以澄清“被诅咒的”壁纸中的一个像素是此特定亮度舍入计算错误的原因。我们还澄清了舍入发生在亮度计算的每个步骤中，而不是在最后。*

* * *

## 更新 2:2020 年 8 月修复补丁

8 月份的 Android 安全补丁刚刚上线，XDA 认可的开发者在 AOSP 发现了一个修复壁纸漏洞的提交。