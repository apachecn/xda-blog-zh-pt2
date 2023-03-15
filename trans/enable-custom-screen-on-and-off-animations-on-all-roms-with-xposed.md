# 在所有带有 Xposed 的 rom 上启用自定义屏幕开关动画

> 原文：<https://www.xda-developers.com/enable-custom-screen-on-and-off-animations-on-all-roms-with-xposed/>

# 在所有带有 Xposed 的 rom 上启用自定义屏幕开关动画

使用 Xposed 框架在任何 Android 4.0+ ROM 中轻松启用和自定义屏幕打开和关闭动画！

关闭动画屏幕

自 2.3 版姜饼以来，CRT 屏幕关闭动画一直伴随着 Android。从那以后，它不时地被调整，但是大部分都是一样的。不幸的是，对于那些希望修改这个特性或者将它整合到缺少这个特性的 rom 中的粉丝来说，这样做总是需要修改系统文件。

现在，通过 Xposed 框架的魔力，您无需进行永久修改就可以做到这一点——假设您已经安装了 Xposed。这个被公开的模块，被恰当地称为 ScreenOffAnimation，来自 XDA 公认的开发者 [zst123](http://forum.xda-developers.com/member.php?u=5402474) 。

正如你从它的名字中所料，*screen of animation*允许你在不支持该特性的设备上设置屏幕关闭动画。这些动画可以大量定制，包括改变速度和动画风格。如果你不介意打开设备时的延迟，你也可以定义一个屏幕动画。此外，您还可以启用动画随机化，这样当您打开或关闭屏幕时就不会感到无聊。

//www . YouTube . com/embed/3 rptd 11 cjlc

如果你运行的是 Android 4.0 或更高版本，并且你一直在寻找添加或定制你的屏幕打开和关闭动画，那就去试试[模块线程](http://forum.xda-developers.com/xposed/modules/mod-screenoffanimation-v1-1-1-custom-t2762332)吧。