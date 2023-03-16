# Android Pie 中支持的设备默认启用蓝牙带内铃声，但不能停用

> 原文：<https://www.xda-developers.com/android-pie-bluetooth-in-band-ringtones-default/>

# Android Pie 中支持的设备默认启用蓝牙带内铃声，但不能停用

如果你有一个蓝牙设备，并希望通过它听到你的铃声，你会很高兴地知道该功能是在 Android Pie 上支持的设备上。

在 Android 8.0 Oreo 正式发布之前，我们了解到[谷歌终于要增加一个许多人都要求的功能](https://www.xda-developers.com/bluetooth-in-band-ringtone-android-o/):蓝牙带内铃声支持。这实际上是蓝牙免提模式(HFP)的一个功能，它的全部目的是让你的手机向连接的蓝牙设备发送自定义铃声。一旦启用，当你有电话打进来的时候，你不再需要听到你的蓝牙设备发出的默认噪音。这是很多人喜欢的东西，他们很高兴看到 Android 有一个给用户偏好的开关。在 Android Pie 中，蓝牙带内铃声现在在所有支持的设备上默认启用，并且用户不能再在开发者选项中关闭[。](https://android.googlesource.com/platform/packages/apps/Settings/+/f4f68c41179cedf22300ca07be06e116fd649980)

自从 Android Pie 推出以来，我们已经谈论了许多 Google 为他们的移动操作系统添加的新功能。许多这些新功能都受到了热烈欢迎，这可能也是其他一些变化没有被注意到的原因。在 Android 8.0 Oreo 中，蓝牙设备的新带内铃声功能被隐藏在隐藏的开发者选项菜单中。然而，当谷歌最终发布 Android 8.1 Oreo 时，该功能被默认启用，并且切换按钮[被从“启用带内振铃”重命名为“禁用带内振铃”。](https://android.googlesource.com/platform/packages/apps/Settings/+/1eca8141bf7cf8bf1839420ed99abd4e615e0fad)

这似乎是两全其美的事情。如果你想在 Android 8.1 Oreo 中通过连接的蓝牙设备播放你的铃声，那么你不必进入隐藏菜单来启用它。但是如果你不是这个功能的粉丝，那么至少你可以进入并关闭这个功能，这样打进来的电话就会播放你的蓝牙设备发出的默认噪音。很明显，谷歌认为这项功能已经为所有用户准备好了，这就是为什么他们在所有支持的设备上默认开启了这项功能。一些用户[抱怨](https://productforums.google.com/forum/#!msg/phone-by-google/f6kYMj_oJzA/jklgdGJ5CgAJ)这一变化(通过 [*PiunikaWeb*](http://piunikaweb.com/2018/09/03/android-9-pie-takes-away-key-feature-introduced-by-google-in-oreo/) )，因为他们不想让他们的铃声通过他们的蓝牙设备播放。

除非你有 root 权限，否则无法在 Android Pie 中关闭这个功能。在 AOSP 中，配置值默认为 [false，但通过受支持设备上的框架覆盖设置为 true。扭转这种情况的唯一方法是推送一个自定义框架覆盖，将该值再次设置为 false。然而，这样做需要 root 用户，因为](https://android.googlesource.com/platform/frameworks/base/+/master/core/res/res/values/config.xml#1693)[谷歌在 Android Pie 上禁止使用没有 root 用户的自定义覆盖图](https://www.xda-developers.com/android-p-blocks-custom-overlays-substratum-themes/)。