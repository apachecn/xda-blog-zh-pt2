# 从最新的谷歌相机应用程序拍摄的照片中提取深度图并创建 3D 视差图像

> 原文：<https://www.xda-developers.com/extract-depth-map-and-create-3d-parallax-images-from-pics-taken-with-the-latest-google-camera-app/>

上周晚些时候，谷歌发布了对谷歌相机应用程序的[大规模更新，](http://www.xda-developers.com/android/apk-google-launches-chrome-remote-desktop-for-mobile-google-camera-appears-in-play-store-for-all-devices/ "[APK] Google Launches Chrome Remote Desktop for Mobile, Google Camera Appears in Play Store for All Devices")允许用户使用任何相机传感器体验类似 DSLR 的散景和类似 Lytro 的重新对焦功能。这之所以成为可能，是因为除了图像数据之外，主相机传感器也用于捕捉深度数据。最终结果与 [HTC 最近推出的双摄像头系统](http://www.xda-developers.com/android/htc-releases-dual-lens-sdk-for-the-htc-one-m8-2014/ "HTC Releases Dual Lens SDK for the HTC One M8 (2014)")非常相似。但谷歌的解决方案不是像 Duo Camera 那样使用两个镜头(或像 Lytro 那样使用一系列微镜头)，而是让用户在拍照后慢慢向上移动相机。这种视差效果随后被用于内插深度数据。

从提供的浏览器应用程序中查看这些新的有深度的图像很好，但肯定不如在屏幕明显更大的电脑上查看这些相同的图像方便。幸运的是，GitHub 用户 [panrafal](https://github.com/panrafal) 创建了开源 webapp Depthy。由 panrafal 的朋友 XDA 论坛成员 [th7org](http://forum.xda-developers.com/member.php?u=2841759) 发布到论坛上，Depthy 允许你从新的谷歌相机应用程序的图像中提取深度数据。一旦完成，你就可以生成自己的视差图像，通过 WebGL 的魔力，你可以稍微调整你的视角。此外，所有这些都是通过 webapp 在本地完成的，甚至可以在兼容 WebGL 的移动浏览器上完成，如 Chrome 的最新版本。

要开始生成自己的视差图像或提取深度图，请前往 [webapp 线程](http://forum.xda-developers.com/showthread.php?t=2726553)并给 Depthy 一个机会。如果你希望将这种深度图和视差图像创建功能整合到原生 Android 或 PC 应用程序中，请前往[项目的 GitHub](https://github.com/panrafal/depthy) 查看代码。