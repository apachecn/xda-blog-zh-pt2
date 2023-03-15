# PSA: Android 7.1 圆形图标支持由 OEM 决定

> 原文：<https://www.xda-developers.com/psa-android-7-1-circular-icon-support-is-determined-by-the-oem/>

自 Android 开始大规模流行以来，设计一致性一直是谷歌的主要障碍之一。最初，谷歌的理念是让原始设备制造商完全控制他们的设计理念。起初，这种开放程度诱使原始设备制造商投入大量资源制造 Android 智能手机和平板电脑。

然而，各种各样的 OEM 皮肤与严格控制的苹果 iPhone 体验形成了鲜明的对比。从 Android Lollipop 开始，谷歌进行了重大的设计变革(由当时的首席 Android 设计师马蒂亚斯·杜阿尔特(Matias Duarte)领导的材料设计 UX)，并希望应用程序开发人员和原始设备制造商也能效仿。虽然摩托罗拉和索尼等一些原始设备制造商满足于跟随谷歌的脚步，但三星和华为等其他原始设备制造商仍在炫耀一种在很大程度上非物质化的设计语言。

谷歌并没有放弃在各种 Android 设备上实施一致的设计，他们最新的努力之一是在 Android 7.1 牛轧糖中加入了[圆形图标支持。圆形图标旨在解决图标大小不一致的问题，但这种方法有一系列问题，我会让 Android Police 的设计师](http://www.xda-developers.com/android-7-1-developer-preview-is-now-available-for-the-nexus-5x6p-and-the-pixel-c/)[利亚姆·斯普拉德林描述](http://www.androidpolice.com/2016/09/27/opinion-early-thoughts-googles-round-icons-consistency-sake/)。Android 7.1 几乎没有进入 Nexus 设备，OEM 厂商开始推出 Nougat 还需要相当长的时间，所以还不清楚圆形图标支持对设计一致性会产生什么影响。但是*清楚的是，圆形图标可能会在它们有机会茁壮成长之前死去:因为**谷歌到目前为止完全由原始设备制造商决定他们是否希望他们的用户看到圆形图标。***

* * *

**圆形图标支持由框架决定**

几乎谷歌像素的每一个功能都被各种博客提前泄露了。甚至圆形图标支持也被大量暗示，因为[泄露的 Pixel Launcher](http://www.androidpolice.com/2016/09/20/pixel-launcher-sneak-peek-part-1-googles-new-circular-launcher-icons-apk-teardown/) 表示支持圆形图标，其他谷歌应用程序正在慢慢更新，在 APK 中嵌入圆形图标资产。然而，当时博客们做了一个**错误的假设**:圆形图标支持将被绑定到启动器上。然而，很难责怪他们，因为即使是谷歌在 T4 的官方声明也没有任何细节。

幸运的是，资深 Android 开发者 Commonsware 深入研究了更多关于 Android 7.1 牛轧糖中如何实现圆形图标支持的细节。不是应用程序开发人员通过 PackageManager 暴露他们的圆形图标(允许启动器决定是否显示圆形图标)，**系统框架决定是否向启动器返回常规图标或圆形图标。**

> #### 当启动器请求一个应用图标时，框架返回`android:icon`或`android:roundIcon`，这取决于设备构建配置。

这实际上意味着 OEM 可以决定是否在你的设备上显示圆形图标。如果三星、华为、LG 或任何其他 OEM 决定放弃圆形图标，那么**无论你安装什么第三方启动器，你的设备都不会看到任何圆形图标资产**。为谷歌的设计一致性推一把。

Commonsware 还发现，该框架决定是否为任何请求应用程序图标的进程返回圆形或常规图标。换句话说，开发者需要小心，他们的圆形图标不仅在特定的设备/启动器配置中看起来很棒，而且在任何需要的地方看起来都很棒。

圆形应用程序图标是一个很好的视觉变化，但很明显，他们的实现存在问题。十有八九，我们可能会看到，只有一些设备，如谷歌像素和*也许*一些摩托罗拉手机将实现圆形图标支持，而其他原始设备制造商将选择继续使用常规图标。如果这种情况发生，那么 Pixel 所有者可能会发现自己有一堆来自应用程序开发人员的非圆形应用程序，这些开发人员懒得更新他们的图标资产，以适应仅支持圆形图标的少数设备。在这种情况下，关于圆形图标一致性的争论就没有意义了。

[**感谢 Commonsware 发现这一点！**](https://commonsware.com/blog/2016/10/20/random-musings-7p1-developer-preview-1.html)