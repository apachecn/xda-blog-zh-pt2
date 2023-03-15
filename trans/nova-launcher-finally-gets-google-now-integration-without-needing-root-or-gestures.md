# Nova Launcher 最终无需 Root 或手势即可集成 Google Now

> 原文：<https://www.xda-developers.com/nova-launcher-finally-gets-google-now-integration-without-needing-root-or-gestures/>

终于来了！Nova Launcher 最终获得了 Google Now 集成，允许用户只需向左滑动即可访问 Google Now，就像他们在 [Google Now Launcher](https://play.google.com/store/apps/details?id=com.google.android.launcher&hl=en) 上一样。您也不需要 root 或付费应用程序来启用此功能。

当谷歌增加了一个 API，允许设备制造商将 Google Now 窗格包含在他们的启动器中时，谷歌也对哪些应用程序可以使用该 API 设置了一些限制。只有系统应用程序被授予使用 Google Now 窗格的权限。或者，如果 Google 应用程序本身是可调试的，您可以在启动器上启用 Google Now 窗格，尽管这是一个不切实际的解决方法。

因此，要在启动器中启用 Google Now 窗格，您需要 root 才能将启动器移动到/system 分区。这被认为是一个太大的麻烦，因为需要 root 用户来使用你最喜欢的启动器和一些额外的功能对用户来说要求太高了。尽管对我们 XDA 的开发者和我们的读者来说，找到设备的根源很容易，但对绝大多数 Android 用户来说仍然是未知的，所以这是一个不切实际的解决方案。

启用 Google Now 窗格的另一个解决方法是利用 Nova 的手势支持来设置打开 Google 应用程序的手势。但这种解决方法首先需要 Nova Launcher Prime(一款付费应用程序)来支持手势。

令人欣慰的是，谷歌应用程序为授予使用 Google Now 窗格的权限而进行的检查略有变化。谷歌应用不再检查应用本身是否可调试，而是现在检查客户端应用是否可调试。可调试的应用程序有自己的缺点，比如不能在 Play Store 上发布，所以必须想出一个变通办法来启用 Google Now 窗格。

Nova Launcher 通过一个名为“Nova Google Companion”的配套应用程序实现了变通方法。这个配套应用程序满足了谷歌应用程序对客户端可调试性的需求，并将主要的 Nova Launcher 应用程序从这样的需求中解放出来。然而，这一伙伴不能发布到 Play Store 上，但由于 Android 允许轻松的侧装，因此存在一些问题。

### 下载和安装

如果你想在 Nova Launcher 上启用 Google Now 窗格，你必须从 APKMirror 等来源下载并安装 [Nova Google Companion app](http://www.apkmirror.com/apk/teslacoil-software/nova-google-companion/nova-google-companion-1-0-release/nova-google-companion-1-0-android-apk-download/) 。你还需要一个兼容版本的 Nova Launcher 来检测同伴，这个功能可以从 [Nova Launcher 5.3-beta1](http://www.apkmirror.com/apk/teslacoil-software/nova-launcher/nova-launcher-5-3-beta1-release/nova-launcher-5-3-beta1-android-apk-download/) 开始使用。这种变通方法将在所有运行 Android 6.0 Marshmallow 或更高版本的 Android 设备上工作。你甚至不需要 Nova Launcher Prime 来使用它，尽管许多人会推荐 Prime 值得开发者为 Nova Launcher 付出努力。

你试过新的配套应用程序来启用 Google Now 窗格吗？您希望看到其他发布者采用这种解决方法吗？请在下面的评论中告诉我们！

[**来源:AndroidPolice**](http://www.androidpolice.com/2017/06/14/exclusive-nova-launcher-finally-gets-google-now-integration-apk-download/)