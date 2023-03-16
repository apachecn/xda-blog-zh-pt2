# Android Q beta 5 阻止了第三方启动器上的手势导航

> 原文：<https://www.xda-developers.com/android-q-beta-5-third-party-launcher-gesture-navigation/>

谷歌首次在 Android 9 Pie 中引入手势导航，即现在众所周知的双按钮导航。在 Android Q beta 2 中，谷歌修改了手势，使其更加流畅，占用空间更少。可以说更像 iPhone，Android Q 的新手势比 Android Pie 的手势有了实质性的改进，但仍有改进余地。在即将到来的 Q beta 5 版本中，谷歌证实他们将改变导航抽屉的[手势行为，但](https://www.xda-developers.com/android-q-beta-5-gesture-behavior-navigation-drawers/)[早期泄露的](https://www.xda-developers.com/android-q-beta-5-google-assistant-gesture-animation/)也显示将有新的助手手势提示和动画以及背部灵敏度选项。

现在，我们有了更多关于 Android Q beta 5 将如何改变手势导航的信息。泄露新助手手势变化的同一位 Redditor 也证实了第三方启动器现在与手势导航不兼容。考虑到对第三方启动器的手势支持一直有点不稳定，这并不奇怪。从 Android 9 Pie 开始，最近的应用程序组件被集成到默认的系统启动器中。Android Q 的新手势栏使得最近的应用程序概览中的应用程序之间的切换非常流畅，但这导致了自 Q beta 3 以来第三方启动器支持更加繁琐。似乎谷歌已经决定，当默认启动器改为第三方应用程序时，只阻止用户启用手势导航。

上面的截图由/u/Charizarlslie 发布，展示了当你试图改变启用手势导航的默认启动器时会发生什么。当默认启动器被改变时，导航样式被强制回到 3 按钮导航，并且手势导航选项变得不可访问。我们检查了 Q beta 5 的 SystemUI APK，并确认 NavigationModeController 类增加了一个方法，当默认启动器切换到非系统应用程序时，可以禁用手势控制。

有趣的是，通过发出以下 ADB 命令，当第三方启动器被设为默认时，可以强制启用手势控制:

```
 adb shell cmd overlay enable com.android.internal.systemui.navbar.gestural 
```

这是因为 3 个手势选项都是由覆盖切换的，所以谷歌可能没有预见到用户手动启用覆盖。

* * *

*T* *感谢 PNF 软件公司为我们提供使用许可[杰布反编译器](https://www.pnfsoftware.com/?aid=xdadev)，这是一款用于 Android 应用的专业级逆向工程工具。*