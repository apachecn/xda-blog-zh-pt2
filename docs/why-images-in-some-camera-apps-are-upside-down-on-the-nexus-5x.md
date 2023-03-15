# 为什么一些相机应用程序中的图像在 Nexus 5X 上是颠倒的

> 原文：<https://www.xda-developers.com/why-images-in-some-camera-apps-are-upside-down-on-the-nexus-5x/>

# 为什么一些相机应用程序中的图像在 Nexus 5X 上是颠倒的

Nexus 5X 上的一些相机应用程序显示颠倒，这是由于一个罕见的制造决定。下面是它是如何发生的以及如何修复的。

iFixit 拆除 Nexus 5X

谷歌 Nexus 5X 的新用户可能已经注意到了一个奇怪的问题，当他们使用一些第三方相机应用程序拍照时，图像最终会上下颠倒！

不过，这个问题并不仅限于 Nexus 5X，因为它之前也曾出现在 Nexus 6 的前置摄像头上。这个问题是什么原因造成的？是厂商问题，还是软件问题？结果是两者都有一点。

据 Android 摄像头框架的技术负责人 Eino-Ville Talvala 称，这个问题的出现是因为一些制造商[以一种不常见的方向为他们的设备安装摄像头传感器。](https://code.google.com/p/android/issues/detail?id=191210#c4)为了符合 [Android 兼容性要求](https://source.android.com/compatibility/)，制造商必须将其摄像头传感器的长边与设备的长边对齐(这意味着默认情况下，背面摄像头传感器的方向应使图像为横向)。然而，对于传感器必须面向哪个特定的景观方向没有要求。通常情况下，大多数制造商使用前视传感器，但 LG/Google 选择了后视传感器。对于大多数手机来说，空间是非常珍贵的，所以制造商们经常不得不将就他们所受到的限制。Nexus 5X 也不例外——快速看一下拆解图就会发现，由于电池的巨大尺寸，设备中几乎没有留给主板的空间。

因为这种反向横向方向很少见，所以许多第三方应用程序开发人员在处理图像时不会校正这种方向。使用旧的相机 API，开发人员可以通过调用 [setDisplayOrientation()](http://developer.android.com/reference/android/hardware/Camera.html#setDisplayOrientation(int)) 方法来检查传感器的正确 UI 方向并正确旋转图像，从而解决这个相机方向问题。然而，随着 Camera2 API 的引入，这不再是必要的，因为该 API 确保预览正确定向。不过，如果你注意到你最喜欢的应用程序错误地定向了你的图片，请给他们发一封电子邮件，要求他们更新代码来纠正这种奇怪的现象。

你遇到过这个问题吗？请在下面的评论中告诉我们(尤其是让开发者知道！)