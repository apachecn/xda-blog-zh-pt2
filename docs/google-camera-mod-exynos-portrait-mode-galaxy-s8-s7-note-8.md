# 带有肖像模式的谷歌相机端口现在可以在三星 Galaxy S7、S8 和 Note 8 (Exynos)上工作

> 原文：<https://www.xda-developers.com/google-camera-mod-exynos-portrait-mode-galaxy-s8-s7-note-8/>

[Pixel 2 的](https://www.xda-developers.com/edge-sense-plus-updated-support-google-pixel-2-active-edge/)谷歌相机的流行端口将谷歌的后处理技术带到了各种高端设备上。它经历了几次迭代，但最近发布的[支持手机上的镜头模糊、散景调整和高分辨率视频录制](https://www.xda-developers.com/pixel-2-google-camera-port-essential-phone/)模式，如 [OnePlus 3](https://www.xda-developers.com/oneplus-3-oxygenos-501-play-protect-factory-mode/) 、[三星 Galaxy S8](https://www.xda-developers.com/samsung-galaxy-note-8-deep-discharge-protection/) 和 [LG V30](https://www.xda-developers.com/lg-v30-raspberry-rose-ces-2018/) 。

本周，XDA 资深会员 [miniuser123](https://forum.xda-developers.com/member.php?u=4798833) 修复了基于 Exynos 设备的一个小问题:肖像模式。他修改后的谷歌相机应用程序为装有三星内部 Exynos 处理器的智能手机提供了人像模式——这种相机效果可以模糊你的自拍背景，并将你的脸聚焦——其中包括国际版的 [Galaxy S7](https://www.xda-developers.com/t-mobile-galaxy-note-8-s7-update/) 、S8 和 [Note 8](https://www.xda-developers.com/samsung-galaxy-note-8-deep-discharge-protection/) 。随着应用程序的安装和在**设置**菜单中的一些调整，它是无缝的——尽管比高通骁龙片上系统的设备慢一点。而且目前来看，**只对后置摄像头有效。**

下面是如何启动和运行它:一旦你安装了 [miniuser123 的谷歌相机 APK](https://drive.google.com/file/d/1zaYbOcWcpkFoIkBuDbyiizKh1hCHBELw/view) ，在设置菜单中应用这个配置:

> #### 型号:Nexus 6
> 
> #### 所有型号的肖像模式:开
> 
> #### camera.af.debug.show:关闭
> 
> #### camera.faceboxes:打开

一旦你做到了这一点，肖像模式和 HDR+在你基于 Exynos 的智能手机上应该不太容易崩溃。(注意，你的手机必须支持 Camera2 API，[，而不是所有的都支持](https://www.xda-developers.com/camera2api-magisk-module-enables/)。)

当然，肖像模式只是谷歌相机端口功能的皮毛。你还将享受同时捕捉原始照片和压缩照片的能力，零快门延迟(ZSL)，和 4K 视频录制(如果你的手机硬件支持)。

查看源代码链接中的完整说明列表。

* * *

[**来源:XDA 论坛**](https://forum.xda-developers.com/showpost.php?p=75118407&postcount=252)