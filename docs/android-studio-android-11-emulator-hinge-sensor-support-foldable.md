# Android 11 模拟器支持可折叠设备的铰链传感器

> 原文：<https://www.xda-developers.com/android-studio-android-11-emulator-hinge-sensor-support-foldable/>

谷歌 Android Studio IDE 中的 Android 模拟器正在进行重大更新，改善了对可折叠设备的支持(通过 [*AndroidPolice*](https://www.androidpolice.com/2020/08/24/android-studio-emulator-updated-with-enhanced-support-for-foldables/) )。然而，该功能需要尚未发布的 Android 11 系统映像和 AVD 配置。

在去年的谷歌 I/O 上，谷歌[更新了 Android 模拟器](https://www.xda-developers.com/android-studio-3-5-changelog/)，以包括对创建虚拟可折叠设备的支持。早在 4 月份，该公司就有可能创建一个支持自由形式多窗口模式的 Android 虚拟设备(AVD)。除了 6 月份发布的 Android 11 测试版，谷歌还推出了一个更新版本的 Android 模拟器，该模拟器将扩展对模拟器中可折叠内容的支持，集成了[铰链传感器 API](https://developer.android.com/reference/android/hardware/Sensor#STRING_TYPE_HINGE_ANGLE) 和 Jetpack 窗口管理器功能。现在，Android Emulator 版本 30.0.26 增加了对虚拟铰链传感器和 3D 视图的支持，前提是你将 foldable 配置为在新的 Android 11 系统映像下运行。

根据[发布说明](https://developer.android.com/studio/releases/emulator#foldables_support_with_virtual_hinge_sensor_and_3d_view)，当开发者在未来的 Android 11 系统映像之上配置虚拟可折叠设备时，铰链传感器是默认启用的。配置完成后，模拟器会向游客发送铰链角度传感器更新和姿势变化。当开发者按下工具栏的折叠或展开按钮时，现有的可折叠设备更新铰链传感器角度和姿态。

更新后的 Android Emulator 更新还引入了从 x86_64 到 arm64 主机的交叉编译、对 virtio-gpu 主机一致性 blob 资源的支持、Windows 上的 USB passthrough、隐藏当前 AVD 的设备框架的能力、对计量支持的切换以及几个错误修复。

虽然可折叠设备尚未成为主流，但有早期迹象表明，它们可能是智能手机设计的下一次演变。三星凭借其 Z Fold 系列产品正在追求可折叠设备的世界。微软最近推出了名为 [Surface Duo](https://forum.xda-developers.com/surface-duo) 的双屏安卓设备。与此同时，谷歌在过去的一直在[开发可折叠像素设备的原型，尽管没有迹象表明这些项目打算发展成为消费产品。然而，随着改进的开发工具的到位，开发人员将有机会创建利用这些独特外形的应用程序。](https://www.xda-developers.com/google-prototype-foldable-pixel-smartphone/)