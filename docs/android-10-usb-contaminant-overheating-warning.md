# Android 10 增加了 USB 端口污染和过热的警告

> 原文：<https://www.xda-developers.com/android-10-usb-contaminant-overheating-warning/>

# 当你的手机 USB 接口被污染或过热时，Android 10 会发出警告

Android 10 增加了一个警告，当你的 USB 端口被碎片或水污染，或者端口过热时，它会告诉你。

昨天，谷歌[为其所有四代 Pixel 智能手机发布了稳定的 Android 10 更新。不久之后，Essential](https://www.xda-developers.com/google-releases-stable-android-10-for-pixel-smartphones/) [发布了 Essential 手机的](https://www.xda-developers.com/oneplus-7-7-pro-android-10-oxygenos-open-beta-1/)稳定更新，一加[发布了一加 7 和一加 7 Pro 的](https://www.xda-developers.com/oneplus-7-7-pro-android-10-oxygenos-open-beta-1/)测试版，小米[发布了红米 K20 Pro 的](https://www.xda-developers.com/redmi-k20-pro-android-10-miui-update/)稳定测试版。然而，对我们来说更重要的是，谷歌开始向 AOSP 上传 Android 10 源代码，开始为新的 Android 操作系统开发定制 ROM。当我们在 AOSP 和谷歌的公开页面上寻找新的 Android 版本时，我们发现了两个新功能:USB 端口污染和过热检测。

第一个功能将禁用手机上的 USB 端口，如果它检测到液体或碎片。Android 系统将发布通知，告知用户 USB 端口已被禁用。一旦 USB 端口没有任何液体或污染物，Android 系统将通知用户现在可以安全地插入附件。然而，用户也可以选择在清除端口中的任何液体或污染物后，手动重新启用 USB 访问。由于这是 Android 10 的[广告功能，我们假设它会出现在所有 Android 认证设备上。](https://www.android.com/android-10/)

使用 ADB 的 dumpsys usb 命令，我模拟了 usb 端口污染，以显示此通知(如左图所示)和对话框(如右图所示)。)

Android 10 增加的第二个 USB 相关功能旨在建议用户在端口过热时从手机上拔下电缆。一旦 USB Type-C 端口达到预定义的温度阈值，Android 系统[将向用户](https://android.googlesource.com/platform/frameworks/base/+/ce02ed3a460d22f28090676d8296e7015c7028eb%5E%21)显示一个警报对话框，告诉他们“拔掉充电器”并“小心电缆可能会变热。”该对话框将一直显示，直到用户按下确定按钮或显示“注意步骤”的按钮来降低温度。根据该准则，Android 认为设备处于“危急状态”的温度是 60°C，而 Android 认为设备处于紧急状态的温度是 65°C。Android 已经有一个“皮肤”温度过高的警告，但现在该操作系统还可以帮助保护设备的 USB-C 端口免受短路或过热的影响。这个特性是可选的，由 OEM 在 SystemUI 的 config.xml 中设置一个标志来控制。