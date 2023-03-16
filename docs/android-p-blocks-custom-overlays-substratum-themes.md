# Android P 阻止安装自定义覆盖图(底层主题)

> 原文：<https://www.xda-developers.com/android-p-blocks-custom-overlays-substratum-themes/>

**CST 3/8/18**晚上 10:05 更新:我们社区的一名成员在 Google 的官方问题跟踪器上提交了一个功能请求。这是引起 Google 注意的正确方法，我们和底层开发者谈过了，他们也会支持这个请求。请明星，但不要评论[这一页](https://issuetracker.google.com/issues/74354703)如果你支持的要求。

谷歌 Pixel、谷歌 Pixel XL、谷歌 Pixel 2 和谷歌 Pixel 2 XL 的首个 Android P 开发者预览版今天[发布](https://www.xda-developers.com/android-p-developer-preview-1-google-pixel-xl-pixel-2-xl/)。我们在这里记录了大量的[用户界面和生活质量的变化](https://www.xda-developers.com/everything-new-android-p-developer-preview/)，但有一个潜在的变化不会让你高兴:自定义覆盖不再能安装在 Android P 上。这意味着**不再有无根的底层**。**不再定制主题**。都没了。

对于那些不知道的人，Android Oreo 引入了索尼的覆盖管理器服务(OMS ),可以通过 ADB 命令控制。使用一个聪明的技巧，流行的 Substratum 主题引擎应用程序背后的开发人员能够开发一个名为 Andromeda 的插件，允许 Substratum 在不需要 root 访问的情况下应用主题。这是一个令人难以置信的成就，因为这是第一次谷歌的 Android 可以主题化，而不需要定制 ROM 或根来替换系统文件。使用仙女座，用户可以[安装一个黑暗主题](https://www.xda-developers.com/install-dark-theme-android-oreo-without-root/)，[在一些应用中改变表情符号](https://www.xda-developers.com/blob-emojis-whatsapp-telegram-android-oreo/)，[定制导航栏图标](https://www.xda-developers.com/customize-navigation-bar-icons-android-oreo/)，[锁屏，最近的应用缩略图，快速设置](https://www.xda-developers.com/minimal-lock-screen-rounded-recent-app-more-quick-setting-columns-android-oreo/)和[等等](https://www.xda-developers.com/tag/substratum-tutorials/)。

Android P 实现了我们认为将被称为 [Material Design 2](https://www.xda-developers.com/chromium-gerrit-material-design-2-colors/) 的东西，它比以往任何时候都更亮。我们确信很多人会寻找各种方式来为它的各个方面添加主题。

然而，如果您尝试在 Android P 中安装自定义覆盖，您将在 [logcat](https://www.xda-developers.com/guide-sending-a-logcat-to-help-debug-your-favorite-app/) 中看到以下消息:

```
 1239 W PackageManager: Package couldn't be installed in /data/app/com.dropbox.android.SwiftDark.Android81NexusorPixel-wb7JxFaAXaHgw7WkZFCvEQ==
03-07 21:00:13.099 1179 1239 W PackageManager: com.android.server.pm.PackageManagerException: Overlay com.dropbox.android.SwiftDark.Android81NexusorPixel must be signed with the platform certificate. 
```

这意味着**只有系统安装的覆盖图才被允许运行**。这类似于 Razer 手机上的[主题引擎的行为，现在在 Android P 上看到这种情况令人难以置信地失望](https://www.xda-developers.com/razer-phone-theme-engine-oms/)

我在自己的设备上证实了这种行为。在我把我的谷歌 Pixel 2 XL 更新到 Android P 之前，我禁用了所有底层覆盖，以确保更新顺利进行。当我更新时，我注意到我所有安装的覆盖图不再显示在“`cmd overlay list`”命令中。我与 Substratum 的主要开发人员进行了交谈，并确认其他人也面临着同样的问题。换句话说，这似乎是谷歌有意的改变。

不幸的是，拥有 root 访问权限的用户也将受到这些变化的影响。您不能简单地“强制”安装一个覆盖并期望它工作，因为平台证书不匹配仍然是一个问题。很可能需要对 framework.jar 打补丁来消除这一需求。定制的 rom 当然能够做出这种改变，但是非 ROMs 用户不能。

对于 Andromeda plug-on for Substratum 的付费用户，Substratum 团队声明 Andromeda 框架仍在工作中，因此您的钱不会白花。该团队将尝试发起请愿，希望社区能够表达他们对这一举措的强烈不满，但最终的决定取决于谷歌是否扭转这一变化。