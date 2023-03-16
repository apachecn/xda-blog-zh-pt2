# OpenAuto 将一个树莓 Pi 变成了一个 Android 自动头单元[视频]

> 原文：<https://www.xda-developers.com/openauto-raspberry-pi-android-auto-head-unit/>

Android Auto 为您的驾驶体验增添了无尽的便利。多年来，人们一直将吸盘智能手机支架贴在仪表盘上，以便快速浏览谷歌地图等应用程序。有了 Android Auto，这不再是必要的，但有一个缺点是，它需要一个兼容的信息娱乐系统。不过，如果你的汽车没有必备的硬件，还有另一种方法:OpenAuto，它可以让你创建自己的 Android 汽车主机，带有显示器、Raspberry Pi 和 8GB(或更大)的 microSD 卡。

OpenAuto 由 XDA 资深会员 [f1x](https://forum.xda-developers.com/member.php?u=7621504) 于本月早些时候发布，是一款开源的 Android Auto head unit 模拟器。该项目基于 aasdk 库和 Qt 库，还利用了 Boost 库、CMake、来自 RaspberryPi 3 固件的 Broadcom ilclient 和 OpenMAX IL API。对于那些对技术细节感兴趣的人，请务必查看这里的 [GitHub 页面](https://github.com/f1xpl/openauto)和[设置说明](https://github.com/f1xpl/openauto/wiki/Build-instructions)。

狂热爱好者和开发人员都对树莓派垂涎三尺。一些人用它来进行视频游戏仿真，另一些人用它来自动或手动控制机器人。它甚至非常适合将内容流式传输到电视机。毫无疑问，它是 OpenAuto 的首选平台。

想知道它能做什么，看看上面的视频。不过，请注意，该项目目前处于测试阶段。它目前支持 Linux、Raspberry Pi 3 和 Windows，并计划在未来添加更多功能和平台。

以下是当前版本的功能列表:

*   480p、720p 和 1080p，每秒 30 或 60 帧
*   RaspberryPi 3 硬件加速支持解码视频流(视频流高达 1080p@60)
*   所有音频通道(媒体、系统和语音)的音频回放
*   语音命令的音频输入
*   触摸屏和按钮输入
*   蓝牙
*   设备热插拔后自动启动
*   用户友好的设置

* * *

[**在我们的安卓汽车论坛**](https://forum.xda-developers.com/android-auto/android-auto-general/release-openauto-source-androidautotm-t3748563) 查看 OpenAuto