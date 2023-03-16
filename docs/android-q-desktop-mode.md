# Android Q 的桌面模式是真实的，这里是你的第一眼

> 原文：<https://www.xda-developers.com/android-q-desktop-mode/>

当我在 1 月第一次泄露 Android Q back [时，有一个功能我真的很想炫耀，但遗憾的是因为它没有完全实现:实验桌面模式。我们在开发者选项中发现了一个“在辅助显示器上强制实验桌面模式”的设置虽然我们可以切换设置，但我们尝试的任何方法都不能让这种“桌面模式”出现在任何地方。既然](https://www.xda-developers.com/android-q-dark-theme-desktop-mode-permission-revamp/)[第一个 Android Q beta](https://www.xda-developers.com/android-q-dp1-google-pixel-2-google-pixel-3/) 已经面向所有谷歌 Pixel 智能手机和 Android Studio 模拟器发布，就有可能试用了。

Twitter 用户@ [Shad0wKn1ght93](https://twitter.com/Shad0wKn1ght93) 注意到 AOSP 启动器有一个新组件，当启动时，会带来一个新的 Android 桌面界面。我注意到在 Q 的框架中提到了这个 launcher 组件，但是在泄露的版本中附带的 AOSP Launcher 当时没有这个组件。现在，它可以手动启动组件了。如果你有 Android Studio 模拟器，你所要做的就是根据你下载的 Q 镜像运行下面的 ADB 命令:

*   **非 GMS:** `adb shell am start -n "com.android.launcher3/com.android.launcher3.SecondaryDisplayLauncher"`
*   **GMS:**

一旦启动，下面是使用 AOSP 启动器的非 GMS 版本的桌面界面。

你可以在桌面上添加应用快捷方式，在[自由多窗口](https://www.xda-developers.com/android-nougats-freeform-window-mode-what-it-is-and-how-developers-can-utilize-it/)中启动，这是 Android 7.0 牛轧糖首次推出的功能。您也可以为桌面设置自定义壁纸。状态栏和导航栏看起来没有变化，但是您现在有了更多的工作空间。

可以通过在运行测试版的 Google Pixel、Pixel 2 或 Pixel 3 上进入开发者选项并启用“强制桌面模式”开发者选项来启用这种桌面模式，然后使用上面的“GMS”命令在 Pixel Launcher 中启动活动。不过，在将手机屏幕转换或连接到任何外部显示器之前，您需要更改 Pixel 的 DPI。

谷歌像素发射器，AOSP 发射器和其他 OEM 发射器可能不是唯一的在新的桌面模式下工作的发射器。启动器应用程序的开发人员可以添加一个意向接收器来过滤启动第二个家庭启动器的呼叫，如这里的[所述](https://developer.android.com/reference/android/content/Intent#CATEGORY_SECONDARY_HOME)。一旦被调用，第三方启动器的辅助启动器组件可能是桌面模式中显示的内容。

随着我们获得更多细节，本文将会更新。请回来查看新桌面模式的更多信息！

* * *

更新 1 2019 年 3 月 14 日@下午 51PM CT:添加了 GMS Android Studio 构建的命令。

*更新 2019 年 3 月 14 日@下午 56PM CT:添加了关于您可以在 Pixel 手机上使用此桌面模式的信息，方法是启动活动，更改 DPI，然后投射您的手机屏幕。还加了第四张截图。*

*更新 2019 年 3 月 14 日上午 10 点 16 分 CT:增加了第三方发射器的信息。*