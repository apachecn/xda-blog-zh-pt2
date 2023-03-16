# ARCore 的深度 API 有助于使用单个相机创建深度图

> 原文：<https://www.xda-developers.com/google-arcore-depth-api-create-depth-maps-using-single-camera/>

[Google ARCore](https://www.xda-developers.com/tag/arcore) ，最近更名为 [Google Play Services for AR，](https://www.xda-developers.com/google-play-services-for-ar-rog-phone-ii-redmi-k20-pro-xperia-5-realme-5-galaxy-a50s-a90-tab-s6/)是谷歌试图将增强现实及其体验扩展到越来越多的设备，而不需要专门的利基硬件，这不同于以前的[项目 Tango](https://www.xda-developers.com/project-tango-dead-google-arcore/) 。谷歌现在通过新的深度 API，使 ARCore 更具沉浸感，适用于更广泛的设备。

Tango 项目下的设备，如[联想 Phab 2 Pro](https://www.xda-developers.com/first-google-tango-phone-the-lenovo-phab-2-pro-now-available-in-the-usa-for-499/) ，依赖于传感器和摄像头形式的专用硬件，使设备能够感知深度和 3D 空间。然而，对专用硬件的需求意味着需要有意识地为最佳 AR 体验构建设备，这反过来又会扰乱智能手机的用户体验。ARCore 通过消除对专用硬件的需求来翻转等式，从而为已经确定用户体验的智能手机带来最佳的 AR 体验。

ARCore 现在正在通过新的 ARCore Depth API 扩展其最佳 AR 体验的可用性。这个新的 API 改善了带有单个 RGB 摄像头的设备的沉浸感，因为它允许开发人员利用谷歌的运动深度算法来创建深度图。这种深度图是通过从不同角度拍摄多幅图像，并在用户移动手机时进行比较，估计每个像素的距离而创建的。

深度数据对于启用诸如遮挡之类的功能很有用:数字对象精确地混合在现实世界对象周围的能力。

遮挡作为一个功能，现在可以通过[场景查看器](https://developers.google.com/ar/develop/java/scene-viewer)提供给超过 2 亿个支持 ARCore 的 Android 设备，场景查看器是一个支持 AR 搜索的开发工具。

除了遮挡，3D 深度数据还支持其他可能性，如更真实的物理、路径规划、表面交互等。因此，深度 API 可以让开发人员创建可以让对象准确地在表面和纹理上反弹和飞溅的体验，以及新的交互式游戏机制，使玩家能够躲避和隐藏在现实世界的对象后面。

由于深度 API 不依赖于专门的硬件，它将在更广泛的设备上工作。但是当然，更好的硬件会改善体验。用于深度映射的其他传感器，如飞行时间(ToF)传感器，将允许开发人员释放新的功能，如动态遮挡-在移动物体后面遮挡的能力。

如果你想尝试新的深度 API，谷歌会要求你填写这里的[合作者征集表格。然后，谷歌将联系它认为最适合推进这项技术的合作者。](https://services.google.com/fb/forms/ARCoreDepthCollab/)

* * *

**来源:[谷歌开发者博客](https://developers.googleblog.com/2019/12/blending-realities-with-arcore-depth-api.html)**