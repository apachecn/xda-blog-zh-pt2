# Android Pie 设备不需要支持相机 HAL3

> 原文：<https://www.xda-developers.com/android-pie-camera-hal3/>

Android Pie 的升级带来了许多伟大的新功能，如重新设计的最近应用概述、手势控制、[自适应电池](https://www.xda-developers.com/android-p-beta-features/)、应用操作、自适应亮度，以及更多的变化。随着 Android 的每次重大更新，谷歌也用新的测试、章节和措辞变化来更新兼容性定义文档(CDD)和兼容性测试套件(CTS)，以确保通过[认证的 Android](https://www.xda-developers.com/check-phone-tablet-certified-android-before-buying/) 设备的用户获得高质量的体验。未能通过 CTS 的设备不允许预加载 Google Play 应用和服务。我们密切关注 CDD 和 CTS 的变化，因为它们经常揭示关于最新 Android 版本的有趣的新细节。

例如，CTS 的[图像测试套件](https://source.android.com/compatibility/cts/camera-hal#its_tests)部分的网页在 Android 9 Pie 发布后进行了更新，声明所有运行 Android Pie 的设备都需要 Camera HAL3 支持(不包括 [Android Pie Go 版](https://www.xda-developers.com/android-pie-go-edition-saves-500mb-space-verified-boot-security/))。

> #### 注意:所有运行 Android 9 或更高版本的设备都需要摄像头 for Android Go 设备除外)。

你们都应该关心 HAL3 支持的原因是，它对于完整的 Camera2 API 支持是必要的——正如你可能知道的，这对于在你的智能手机上工作的[谷歌相机端口](https://www.xda-developers.com/google-camera-port-hub/)是必要的。如果您的设备只支持 HAL1，那么 Camera2 API 只能在“传统”模式下工作。一些用户将他们的手机根添加到 build.prop 中，以声明他们的设备支持 HAL3，这反过来使 Google Camera 端口开始工作:

```
 persist.vendor.camera.HAL3.enabled=1 
```

小米 A1、小米 A2、华硕 ZenFone Max Pro M1 以及许多其他廉价和中档智能手机等设备需要这一小小的改变，以便谷歌相机端口可以工作。因此，Android Pie 设备需要 HAL3 支持的想法是令人兴奋的，但不幸的是，尽管其页面上这么说，这实际上并不是一个要求。

该要求未在 CDD 列出，谷歌发言人证实，HAL3 支持**仍然只是对制造商的建议**。谷歌发言人证实，该公司将更新网页，以纠正这一信息。因此，推出支持 HAL3 的红米 Note 7[开箱即用](https://www.xda-developers.com/redmi-note-7-camera2-api-google-camera/)并不是因为小米被要求这样做以满足 Android Pie 兼容性要求。最后，我们应该注意到，启用 HAL3 支持并不意味着所有 Camera2 API 功能都可用，因为公司仍然可以修改功能，如原始拍摄支持、ISO 级别、曝光时间等。