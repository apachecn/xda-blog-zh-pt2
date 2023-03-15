# 用这个 Magisk 模块修复 Razer Phone 2 的相机取景器和 EIS

> 原文：<https://www.xda-developers.com/fix-the-razer-phone-2s-camera-viewfinder-and-eis-with-this-magisk-module/>

# 用这个 Magisk 模块修复 Razer Phone 2 的相机取景器和 EIS

XDA 青年成员 Usyless 创建了一套 Magisk 模块，可用于修复 Razer Phone 2 上的相机取景器故障和 EIS。

Razer Phone 2 ( [review](https://www.xda-developers.com/razer-phone-2-review-testing-the-battery-life-and-performance-of-the-gaming-powerhouse/) )提供了一些坚实的规范，即使以今天的标准来看。这款手机采用了主频为 2.8GHz 的高通骁龙 845 芯片组，配备了高通快充 4.0+和无线 Qi 充电支持的 4,000mAh 电池，以及超现实的 120Hz IGZO LCD 1440p 显示屏。然而，原始设备制造商很难让 Razer Phone 2 保持最新，并修复长期存在的漏洞，可能是因为他们的智能手机业务目前在 T2 陷入了一点混乱。

**[【Razer phone 2 xd a 论坛】](https://forum.xda-developers.com/razer-phone-2)**

谈到 bug，据报道，手机的 [Android Pie 更新在普通相机的取景器中引入了明显的颜色模糊和模糊。显然，这个问题也影响了 Instagram 等第三方应用程序录制视频和拍照。为了在伤口上撒盐，相机的电子图像稳定(EIS)功能只暴露在有限的应用程序中，进一步限制在 30fps。](https://www.xda-developers.com/razer-phone-2-android-pie-update/)

不出所料，XDA 社区前来救援。XDA 的初级成员 Usyless 已经编译了一个 Magisk 模块，该模块用 Razer Phone 2 的 Android Oreo 固件的旧版本系统地替换了 stock OS 上的相机库，以修复上述取景器故障。下面你可以看到两个使用 Snapchat 录制视频的例子——第一个使用未修改的操作系统，第二个使用 Magisk 模块。

modder 还提供了一个补充的 Magisk 模块，可以在 1080p 60fps 视频录制上解锁 EIS。与第一个 mod 不同，第二个模块与股票相机应用程序不兼容。您必须安装一个支持 60fps 的合适的 Google Camera 端口，以利用 EIS 的真正潜力。请注意，EIS mod 打破了后置摄像头的 4K 60fps 记录和前置摄像头的 1080p 60fps 记录。

**[Razer Phone 2 取景器和 EIS Fix Magisk 模块— XDA 下载讨论线程](https://forum.xda-developers.com/razer-phone-2/themes/fix-razer-phone-2-viewfinder-eis-fix-t4129773/)**