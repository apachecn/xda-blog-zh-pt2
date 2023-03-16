# 任天堂 Switch 的安卓移植终于来了

> 原文：<https://www.xda-developers.com/switchroot-lineageos-android-nintendo-switch/>

我们通常不会将任天堂 Switch 与 Android 开发联系在一起，然而，由于 XDA 高级成员[兰格汉斯](https://forum.xda-developers.com/member.php?u=576676)和 XDA 初级成员[章程](https://forum.xda-developers.com/member.php?u=9648761)的努力工作，任何可黑客攻击的任天堂 Switch(通常是 2018 年 7 月之前出售的设备)现在都可以直接从 SD 卡启动 LineageOS 15.1。几周前，我写了一篇[实践文章](https://www.xda-developers.com/nintendo-switch-android-hands-on/)，你可以从中了解我的经历。我还为 XDA YouTube 频道制作了一个视频，嵌入在下面。

https://www.youtube.com/watch?v=FINSGgFCc_o

## 任天堂 Switch 的非官方 Android 端口(LineageOS 15.1)

任天堂 Switch 上的 LineageOS 15.1 基本上拥有你对 LineageOS 的所有期望。您可以获得所有基本的 Android 功能，支持谷歌服务，甚至支持原生 Nvidia Shield 应用程序。这意味着你可以在旅途中玩半条命和传送门，如果你是测试版的一员，现在甚至可以使用 GeForce。Joycons 和 Nintendo Pro 控制器工作顺利，键盘和鼠标在对接时工作正常...几乎所有能起作用的东西都会起作用。这是一个壮观的 Android 端口，如果你有备用的 SD 卡，这是一个非常值得设置的端口。

*   LineageOS 15.1 -安卓 8.1 奥利奥
*   基于英伟达盾电视树
*   TWRP 预装
*   CPU 和 GPU 性能配置文件
*   在手持和对接模式下工作
*   支持音频
*   Joycons 通过蓝牙连接，也是手持模式

不过，那是另一回事。在任天堂 Switch 上安装 Android 可能会有点困难，因为你需要向你的 SD 卡写入一个与其大小相匹配的图像。在此过程中，该映像还会擦除其上存储的所有数据。有一些东西也不起作用，列表如下。

*   深度睡眠，所以电池寿命不是很大
*   自动旋转
*   在 dock 中屏蔽
*   未检测到充电，但控制台仍在充电
*   某些应用程序不能正确处理 joycon 输入
*   触摸屏有时会检测到触摸，即使你的手指只是浮在屏幕上

在你的任天堂 Switch 上安装安卓系统不会影响到它上面安装的主操作系统，所以你不需要担心会破坏任何东西。如果你想开始，看看下面的 switchroot LineageOS 15.1 线程！

[**任天堂 Switch**15.1](https://forum.xda-developers.com/nintendo-switch/nintendo-switch-news-guides-discussion--development/rom-switchroot-lineageos-15-1-t3951389)