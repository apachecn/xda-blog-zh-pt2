# 一加 8 系列上的一加相机 4.0.267 增加了视频过滤器，并准备增加一个“智能场景增强”开关

> 原文：<https://www.xda-developers.com/oneplus-camera-4-0-267-on-the-oneplus-8-series-adds-video-filters-and-prepares-to-add-a-smart-scene-enhancement-toggle/>

一加[最近推出了](https://www.xda-developers.com/oneplus-8-8-pro-oxygenos-update-camera-system-network/)一加 8 ( [评测](https://www.xda-developers.com/oneplus-8-xda-review/))和一加 8 Pro ( [评测](https://www.xda-developers.com/oneplus-8-pro-review-never-settle-on-hardware/))的重大 OxygenOS 更新。根据官方变更日志，此次更新为一加相机应用程序添加了几个新功能，包括支持视频的 H.265 HEVC 编解码器，新的自动超广角镜头功能，对点击动画的优化，以及对相机稳定性的改进。然而，changelog 没有提到的是，更新还包括一组新的“视频过滤器”，用于相机应用程序中的视频模式。

一加相机应用版本 4.0.267 最近随着 OxygenOS 10.5.8/10.5.10 更新在印度的一加 8 和一加 8 Pro 上推出。该应用程序带来了一套新的视频滤镜——生动、夜晚、复古、B&W 和美味——你可以在设备上录制视频时使用。

除了 4K 60Hz 设置之外，所有视频分辨率都支持滤镜，点击应用右上角的滤镜图标即可访问滤镜。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

```
 <string name="settings_key_is_smart_scene_enhancement_enabled">IsSmartSceneEnhancementEnabled</string>
<string name="settings_smart_scene_enhancement_description">Auto enhance image based on scene detection</string>
<string name="settings_smart_scene_enhancement_title">Smart scene enhancement</string>
<string name="settings_smart_scene_enhancement_toast">Scene enhancement icon will pop up when triggered</string> 
```

此外，一加相机应用程序的拆除显示，该公司正准备在相机设置中添加一个新的“智能场景增强”开关。虽然智能场景增强功能在当前版本的相机应用程序中已经处于活动状态，但它对用户来说是不可见的，也不能被禁用。新添加的代码字符串表明，该应用程序的未来更新将在取景器中引入一个新的指示器，向用户显示智能场景增强功能何时激活，并在应用程序设置中引入一个新的切换，让用户完全禁用该功能。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*