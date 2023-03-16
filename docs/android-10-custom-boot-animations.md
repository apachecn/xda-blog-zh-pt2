# Android 10 增加了安装自定义启动动画的支持

> 原文：<https://www.xda-developers.com/android-10-custom-boot-animations/>

谷歌安卓操作系统的最新版本是安卓 10，昨天[刚刚发布](https://www.xda-developers.com/google-releases-stable-android-10-for-pixel-smartphones/)用于 Pixel 智能手机。随着正式发布，我们可以看到新的启动动画，展示了 Android 的[新的，没有甜点的品牌](https://www.xda-developers.com/android-10-android-q-brand-redesign/)(见上面的特色图片)。引导动画是 XDA 社区中最流行的自定义内容之一，但是这样做需要 root 访问权限，因为引导动画驻留在只读系统、产品或 oem 分区中。然而，这种情况在未来可能会改变。根据我们在 AOSP 发现的一份提交，谷歌已经增加了通过 APEX 模块安装定制启动动画的支持。

我们之前在[项目主线](https://www.xda-developers.com/android-q-project-mainline-security/)的背景下讨论过 APEX，这是 Android 10 最重要的功能之一。APEX 是一个[的新包类型](https://www.xda-developers.com/android-q-apex-biggest-thing-since-project-treble/)，它被设计成允许安全地更新系统库和其他系统组件，但它显然也将被用来提供定制的引导动画。在 Android 10 中，引导动画二进制文件已被修改，以支持从名为 com.android.bootanimation.apex 的 APEX 模块加载引导动画[。提交描述指出“这是支持定制引导动画的下载和安装所必需的”由于引导动画将包含在 APEX 模块中，因此可以通过 ADB 或具有适当权限的系统安装程序应用程序(如谷歌 Play 商店)进行安装，无需 root 访问权限。](https://android.googlesource.com/platform/frameworks/base/+/android10-release/cmds/bootanimation/BootAnimation.cpp#72)

不过，你将无法从互联网上安装任何自定义启动动画。如果第三方 APEX 模块未通过 Android 验证的引导验证，则该模块将被拒绝安装。这意味着只能安装来自可信来源(如 Google 或您设备的 OEM)的 APEX 模块，因此您只能使用他们提供的启动动画。这与谷歌[在 Android Pie](https://www.xda-developers.com/android-p-blocks-custom-overlays-substratum-themes/) 中对第三方覆盖图施加的限制相同。

我们不知道谷歌是否计划在 Pixel 设备上提供一系列定制的引导动画。启用该功能的提交是由索尼工程师在去年 11 月提交的，但它在今年 5 月下旬被谷歌内部合并到 AOSP。谷歌很可能增加了这个功能，只是允许原始设备制造商分发定制的引导动画，而他们自己并没有任何这样做的意图，但该公司可能会将引导动画定制添加到其即将发布的[像素主题应用](https://www.xda-developers.com/android-q-pixel-themes-google-pixel/)中。毕竟，我们最近已经看到谷歌在 Android 10 中变得更加开放，开发者选项中的[各种强调颜色、图标形状和字体](https://www.xda-developers.com/android-q-pixel-customization/)覆盖，隐藏的时钟样式，最后是全系统的黑暗主题。