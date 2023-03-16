# 在 LG G7 和 LG V30 上启用所有锁屏天气效果[Root]

> 原文：<https://www.xda-developers.com/enable-all-lockscreen-weather-effects-lg-g7-lg-v30/>

# 在 LG G7 和 LG V30 上启用所有锁屏天气效果[Root]

XDA 资深成员 pittvandewitt 找到了一种不同的方法来启用 LG G7 和 LG V30 上的所有锁屏天气效果。

LG 手机有一个独特的功能，可以在智能手机的锁屏上显示天气效果。大多数原始设备制造商只会在时间或日期旁边使用一个小图标，但 LG 更进一步，实际上为你选择的任何锁屏图像添加了完整的视觉效果。多年来，已经有了让你为他们的设备添加更多天气效果的 mods(通过修改他们的 LGKeyguardEffect.apk)，但 XDA 的高级成员 [pittvandewitt](https://forum.xda-developers.com/member.php?u=4539728) 在 LG G7 ThinQ 和 LG V30 上找到了一种不同的方式。

[**LG G7 XDA 论坛**](https://forum.xda-developers.com/lg-g7-thinq)

通过反编译应用程序，他们发现它实际上是从 build.prop 文件中读取一个布尔值。如果这个值以这种方式设置，那么它将解锁设备的所有锁屏天气效果。所以不用修改 APK 文件，你可以简单地添加“ro.build.brand_dsny=true”到 build.prop 并重启你的 G7 或 V30。完成后，开发者提醒你仍然需要进入设置应用程序，并在锁屏&安全部分启用该功能。

开发人员甚至为那些不想修改 build.prop 文件的人在 OP 上附加了一个 Magisk 模块。

[**LG V30 XDA 论坛**](https://forum.xda-developers.com/lg-v30)

[**在我们的 LG G7 论坛**](https://forum.xda-developers.com/lg-g7-thinq/themes/mod-enable-weather-effects-t3884674) 查看这个 mod