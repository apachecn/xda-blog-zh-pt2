# 在你的 Android 9 Pie 或 Android 10 设备上创建一个自定义的强调颜色

> 原文：<https://www.xda-developers.com/custom-accent-color-creator-rooted-android-9-pie/>

# 在你的 Android 9 Pie 或 Android 10 设备上创建一个自定义的强调颜色

Accent Color Creator 允许 rooted Android 9 Pie 及以上版本的用户创建自定义的 Accent Color，并将其作为 magisk 模块无系统地注入。请继续阅读！

Android 10 引入了自己的内置主题选项，允许感兴趣的用户在小范围内定制自己的设备。虽然 Pixel 用户可以通过 [Pixel 主题应用](https://www.xda-developers.com/google-pixel-themes-customize-android-10/)更容易地访问主题化解决方案，但其他 AOSP 的 Android 10 用户可以通过设置菜单中的开发者选项访问一些主题化功能。这些基本的主题化功能包括选择预定义的强调色，但是选项很少。如果您希望扩展默认提供的强调颜色选项，[强调颜色创建者](https://forum.xda-developers.com/android/apps-games/app-magisk-module-qacc-custom-accent-t4011747)允许根用户定义他们自己的自定义强调颜色。

XDA 资深会员 [Akilesh_15](https://forum.xda-developers.com/member.php?u=7908443) 的强调色创建器让您创建自己的自定义强调色。在 Android 10 中，谷歌创建了多个运行时资源覆盖(rro)，替换(“覆盖”)了 Android 框架的一些资源值。因此，每种强调色都有自己的 RRO APK，用来自 RRO APK 的资源替换 Android 框架的资源。强调色创建器通过构建新的 RRO APKs 来工作，其中用户能够定义自定义强调色。然后，这个 APK 被打包到 Magisk 模块中，以便进行无系统安装。

该应用程序具有以下特点:

*   你可以从你的壁纸、应用程序预设中选择颜色，或者设置你自己的自定义颜色。
*   可以创建多种重音。
*   启用/禁用重音。
*   向左滑动以移除创建的重音。

开发者指出，该应用需要 Android 9 及更高版本，但它也可能在 Android 8 Oreo 上工作——尽管这未经测试。该应用程序及其功能也没有在 OxygenOS、OneUI、MIUI 等 OEM 皮肤上进行测试，但它应该可以在 AOSP 的定制 rom 上工作，前提是他们还没有实现定制的颜色选择器。请注意，卸载应用程序不会恢复自定义强调颜色-您必须使用 TWRP 或 adb shell 和 root 删除应用程序创建的模块，该模块位于 */data/adb/modules/* 。这个应用也是[开源的](https://forum.xda-developers.com/android/apps-games/app-magisk-module-qacc-custom-accent-t4011747)。

**[强调色彩创作者- XDA 讨论线程](https://forum.xda-developers.com/android/apps-games/app-magisk-module-qacc-custom-accent-t4011747)**