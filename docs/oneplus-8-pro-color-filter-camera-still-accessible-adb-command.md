# [更新 2:仍然适用于 DP4]一加 8 Pro 的彩色滤光片摄像头仍然可以通过 ADB 命令访问

> 原文：<https://www.xda-developers.com/oneplus-8-pro-color-filter-camera-still-accessible-adb-command/>

**更新 2 (09/04/2020 @ 05:46 AM ET):** 显然，这些命令仍然可以在 Android 11 开发者预览版 4 版本上访问。

**更新 1(****08/24/2020****@****02:25am****ET):**一加已经默默打补丁，能够真正通过 ADB 接入彩色滤镜摄像头。滚动到底部了解更多信息。下面保留了 2020 年 7 月 17 日发表的文章。

自手机推出以来，一加 8 Pro 的彩色滤光片摄像头一直陷入争议的泡沫中。首先，这种辅助滤色相机被许多人认为没有实际用途。然后，有消息称，具有 Photochrom 模式的彩色滤光片相机[能够透过薄塑料物体](https://www.xda-developers.com/oneplus-8-pro-color-filter-camera-see-through-some-plastic-objects/)和非常薄的衣服进行观察！因此，Photochrom 模式在接下来的更新中被禁用——先是在中国[的](https://www.xda-developers.com/oneplus-8-pro-color-filter-x-ray-infrared-see-through-camera-temporarily-disabled-future-update/)，然后是在全球版本的[(尽管后者是偶然的)。这款设备甚至在印度上市时开箱就禁用了](https://www.xda-developers.com/oxygenos-10-5-9-disables-oneplus-8-pro-color-filter-camera-even-global-variant/) [Photochrom 模式](https://www.xda-developers.com/oneplus-8-pro-may-go-on-sale-india-color-filter-camera-disabled-oxygenos-update/)！然后，一加最终通过 [OxygenOS 10.5.10 更新](https://www.xda-developers.com/oxygenos-10-5-10-oneplus-8-pro-fixes-photochrom-color-filter-see-through-xray-issue/)将传感器的信息分层到主传感器的图像上，解决了彩色滤光片的透明问题。但事实证明，如果你仍然真的希望使用最初设置的辅助摄像头，你实际上可以通过一个隐藏的应用程序访问彩色滤光片摄像头。

**[一加 8 XDA 论坛](https://forum.xda-developers.com/oneplus-8) ||| [一加 8 亲 XDA 论坛](https://forum.xda-developers.com/oneplus-8-pro)**

XDA 成员[皮斯克](https://forum.xda-developers.com/member.php?u=10961671) [发现，在一加 8 Pro 的最新更新中，彩色滤光片摄像头仍然可以通过工厂模式应用程序访问](https://forum.xda-developers.com/oneplus-8-pro/how-to/guide-access-color-filter-command-shell-t4134237)。不过这个 app 需要通过亚行推出。一旦应用程序启动，你可以将它锁定在手机的内存中，无需 ADB 即可访问它。这个发现最好的一点是，你不需要启动，甚至不需要解锁你的引导程序。

要使用[一加 8 Pro](https://www.geekbuying.com/item/Global-ROM-OnePlus-8-Pro-5G-Smartphone-8GB-128GB-Glacial-Green-424238.html) 上的彩色滤光摄像头，请将您的手机连接到 ADB 并运行以下命令:

```
adb shell

我从 com.oneplus.factorymode/.camera.manualtest.CameraManualTest 出发
```

这将启动工厂模式应用程序。进入应用程序后，使用右下角的相机切换器图标在不同的相机之间切换。彩色滤光摄像头位于应用程序中的第 4 位。

这款相机的整体效用仍然是个问题。x 射线/透视效果只能在非常薄的塑料上重现。一加 8 Pro 的彩色滤光片相机模式的整体效用范围非常狭窄，你更有可能只欣赏几次它的新奇感，然后就完全忘记它。

**[【向导】通过命令 shell 访问颜色-滤镜- XDA 线程](https://forum.xda-developers.com/oneplus-8-pro/how-to/guide-access-color-filter-command-shell-t4134237)**

上面的图片来自 Max Weinbach。我在我的一加 8 Pro 上尝试了同样的方法，我无法用足够薄的塑料外壳来定位我周围的任何物体。就服装而言，观察到了同样的结果。因此，利用这一点达到邪恶目的的可能性仍然非常非常有限，如果有的话。

* * *

## 更新:一加已经悄悄地修补了一加 8 Pro 的彩色滤光片摄像头，不再能够通过 ADB 命令访问

在这个过程中的某个地方，通过干预更新，一加已经悄悄地修补了通过 ADB 命令访问一加 8 Pro 的彩色滤光片摄像头的能力。您不能再运行命令来访问彩色滤光片相机。该命令不再启动 factory 应用程序，而是返回“ *Activity not started ”,因为当前 Activity 正在为用户*保留。你现在需要完全依靠一加的实现来利用这个硬件。

**来源:[/r/一加](https://www.reddit.com/r/oneplus/comments/ife3a4/looking_for_a_traditional_sticker_style_glass/)**

* * *

## 更新:仍然适用于 Android 11 开发者预览版 4

[根据 XDA 资深会员 cyberbandit1998](https://forum.xda-developers.com/showpost.php?p=83410827&postcount=139) 的说法，ADB 命令仍然可以用于一加 8 Pro 的彩色滤光片摄像头，但只能在最近发布的 [Android 11 开发者预览版 4 版本的 OxygenOS 11](https://www.xda-developers.com/download-oneplus-8-pro-receive-android-11-developer-preview-4-based-oxygenos-11-builds-september-2020-security-patches/) 上使用。然而，我们并不期望这些功能在稳定版本发布时仍然存在。