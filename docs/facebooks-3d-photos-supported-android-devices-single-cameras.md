# 脸书为单摄像头 Android 设备提供 3D 照片支持

> 原文：<https://www.xda-developers.com/facebooks-3d-photos-supported-android-devices-single-cameras/>

回到 2018 年脸书的 F8 开发者大会，该公司首次宣布了该平台的一项名为 3D 照片的新功能。顾名思义，这个功能可以让你在自己的[脸书新闻订阅源](https://www.xda-developers.com/facebook-testing-tabbed-news-f)中发布和查看三维照片。这些照片像任何其他照片一样出现在您的新闻订阅源中，但当您滚动经过它们、轻按它们或倾斜您的设备时，3D 照片的视角会发生变化。你也可以使用 Oculus Go 或 Oculus Rift 等虚拟现实耳机来观看 3D 照片。在推出时，脸书允许用户创建 3D 照片，前提是你在桌面上导入深度图文件，并使用双摄像头手机，如最新的三星 Galaxy 或 iPhone 设备。双摄像头要求背后的原因是脸书可以从两个摄像头捕捉的图像中创建一个深度图。然而现在，在 Android 手机上创建 3D 照片不再需要双摄像头。

根据该公司最近的一篇博客文章，脸书现在使用人工智能和机器学习来创建一张没有任何深度图数据的 3D 照片。正如 *VentureBeat* 解释的那样，该公司已经改进了其机器学习算法，这样它就可以在不需要深度数据的情况下推断图像的 3D 结构。此外，该功能现在也适用于自拍、绘画和复杂场景。

为了实现这一壮举，脸书使用数百万对 3D 图像及其深度图训练了一个卷积神经网络。一旦经过训练，这个神经网络现在被用来推断没有伴随深度图的 3D 图像应该是什么样子。这种神经网络可以在“几分之一秒”内运行在典型的移动处理器上，使其适合 3D 照片功能。谷歌也在去年年底在 AR Core 的深度 API 中启用了类似的功能，这允许平台使用单个相机创建深度地图[。](https://www.xda-developers.com/google-arcore-depth-api-create-depth-maps-using-single-camera/)

然而，即使有了新的进步，这个特性也有一些限制。根据 Engadget 关于此事的一份报告，尽管现在任何设备都可以在新闻订阅源中查看 3D 照片，但在脸书的应用程序中发布 3D 照片的能力仅限于 iPhone 7 和更新的产品，以及几款“中档或更好”的安卓手机，包括三星的 Galaxy Note 8 和 Note 9，以及除预算友好的 Pixel 3A 之外的整个 Pixel 系列。随着这一新的发展，也值得注意的是，脸书目前正在测试一个[图像编辑建议](https://www.xda-developers.com/facebook-android-tests-image-editing-suggestions-google-photos/)功能，用于你在新闻订阅上发布的照片。

* * *

**来源:[脸书艾](https://ai.facebook.com/blog/-powered-by-ai-turning-any-2d-photo-into-3d-using-convolutional-neural-nets/)**

**Via: [Engadget](https://www.engadget.com/2020/02/28/facebook-converts-3D-photos-without-portrait-mode/?guccounter=1) ，[venturebeat](https://venturebeat.com/2020/02/28/facebooks-3d-photos-feature-now-gives-any-image-simulated-depth/)**