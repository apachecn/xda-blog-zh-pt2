# PrivSet 更新了 Android Oreo 支持，使得修改 Android Framework-res 变得容易

> 原文：<https://www.xda-developers.com/privset-updated-android-oreo-modify-android-framework-res/>

# PrivSet 更新了 Android Oreo 支持，使得修改 Android Framework-res 变得容易

PrivSet 是一款允许用户在不需要 Apktool 的情况下更改 Android framework-res 值的应用程序，已经更新为支持 Android 8.0 和 Android 8.1 Oreo。

Apktool 是一种工具，允许您反编译 Android 应用程序，以便您可以进行修改，它最受欢迎的用途之一是修改 Android framework-res.apk。这款应用程序称为 Android framework，负责在您的设备上提供大部分资产、颜色、图像和配置值。例如，您可以修改 framework-res 来启用或禁用圆形图标支持。在 PrivSet 出现之前，修改 framework-res 需要一些努力。 [PrivSet](https://www.xda-developers.com/modify-android-framework-values-privset/) ，由 XDA 资深成员[莫德雷德爵士](https://forum.xda-developers.com/member.php?u=5450821)制作，是一款无需使用 Apktool 就能改变 Android 框架值的有用 root app。

它通过重定向 Android 来从它为 framework-res.apk 创建的覆盖图中提取资源值。如果你熟悉 Substratum，PrivSet 的工作方式与它基于使用 RRO(用于 Android 棉花糖和牛轧糖)和 OMS (Android 奥利奥)的覆盖图的工作方式相同。因此，根本不需要直接修改 framework-res，因为这些值是从覆盖图中读取的，而不是从原始的 framework-res.apk 中读取的。

它使用户能够更改许多与处理四向旋转的设置相关的 Android 框架值，强制所有应用程序都采用圆角，更改用户双击电源按钮时手机的操作，等等。用户必须在应用更改后重启设备。他们也可以选择重置所有更改并重新开始。需要注意的是，PrivSet 允许用户生成覆盖图，用于仅更改那些实际存在于设备的 framework-res.apk 中的框架值。它通过读取用户设备的系统属性来实现这一点。

当我们之前报道这款应用时，它并不支持 Android Oreo。现在，已经更新支持安卓 8.0 和安卓 8.1 奥利奥。值得注意的是，PrivSet 还没有 Android Oreo 的无根模式。据开发人员称，这是一项正在进行的工作，应该会在未来的更新中出现。