# [更新:链接被移除]索尼的 3D Creator 软件被移植到 Android 6.0 以上的设备上

> 原文：<https://www.xda-developers.com/sonys-3d-creator-software-android/>

# [更新:链接被移除]索尼的 3D Creator 软件被移植到 Android 6.0 以上的设备上

XDA 资深会员 IgorEisberg 刚刚发布了索尼 3D Creator 应用程序的一个端口，该应用程序内置于 Xperia XZ1 和 XZ1 紧凑型设备中。

**2017 年 9 月 8 日更新:应索尼要求移除下载链接**

* * *

索尼通常会为 IFA 准备一些智能手机发布会，这正是上周发生的事情。该公司在柏林的发布会上正式宣布了 Xperia XZ1 和 Xperia XZ1 紧凑型车。这些是我们在过去报道过谣言[的](https://www.xda-developers.com/sony-xperia-xz1-compact-leak/)[设备，但是一个新的特性是它们附带的 3D Creator 应用程序。一旦我们了解了它，我们查看了登录页面，然后](https://www.xda-developers.com/renders-and-uk-pricing-leaked-for-sonys-upcoming-xperia-xz1-flagship/)[花时间深入研究了它带来的特性](https://www.xda-developers.com/sony-equips-xperia-xz1-3d-scanning/)。

索尼将他们的 3D Creator 应用程序描述为“移动创造力的突破”，这无疑在活动中引发了很多兴趣。在发布会上，该公司吹嘘他们最新的运动眼相机，所以一些人开始怀疑这种 3D 捕捉软件是否依赖于某种类型的硬件。然而，事实似乎并非完全如此，因为 XDA 资深会员 IgorEisberg 刚刚发布了该应用程序的一个端口。

该应用程序取自 Xperia XZ1 上使用的库存固件，其清单已随应用程序重新签名一起编辑。这样做是为了让它能在任何至少运行 Android Marshmallow 并支持 Camera2 API 的设备上运行。您将能够判断您的设备是否不支持 Camera2 API，因为该应用程序在加载相机时会挂起。不过你要知道，有些设备(比如小米 Mi 5)可以通过在 build.prop 文件中设置 persist.camera.HAL3.enabled=1 来启用 Camera2 API。

该端口就像广告宣传的那样工作，能够为 AR 和 3D 打印目的创建 3D 模型。该应用程序还支持动态壁纸功能，适用于您刚刚进行了数字扫描的对象。如果你愿意，你甚至可以点击应用程序设置中的“软件版本”选项来启用开发者模式。

* * *

[**在我们的应用和游戏论坛**](https://forum.xda-developers.com/android/apps-games/app-sony-3d-creator-t3669576) 查看这个端口