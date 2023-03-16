# 一次用户界面更新悄悄屏蔽了三星 Galaxy S8/Galaxy Note 8 上的 Substratum/Swift 安装程序

> 原文：<https://www.xda-developers.com/one-ui-blocks-substratum-swift-installer-samsung-galaxy-s8-galaxy-note-8/>

# 一次用户界面更新悄悄屏蔽了三星 Galaxy S8/Galaxy Note 8 上的 Substratum/Swift 安装程序

三星 Galaxy S8、Galaxy S8+和 Galaxy Note 8 的 One UI beta 更新(Android 9 Pie)已经悄悄地阻止了 Substratum/Swift 安装程序主题化。

当第一个 Android P 开发者预览版首次发布时，关于最新版本[阻止自定义覆盖图](https://www.xda-developers.com/android-p-blocks-custom-overlays-substratum-themes/)(主题)被安装，爱好者之间有很多争议。热心者希望这是一个错误，但是,[通过谷歌](https://www.xda-developers.com/rootless-custom-themes-android-p/)证实这是一个安全措施。由于负责阻止自定义覆盖的代码是 AOSP 的一部分，OEM 厂商发布的 Android Pie 版本最终也应该有这些补丁。奇怪的是，三星 Galaxy S9、Galaxy S9+和 Galaxy Note 9 的 One UI (Android Pie) [beta](https://www.xda-developers.com/custom-themes-samsung-experience-10-before-android-pie-beta/) 和稳定更新没有这种限制。然而，出于某种原因，为骁龙和 Exynos 三星 Galaxy S8 和 Galaxy Note 8 构建的 beta One UI 有这个限制，阻止用户从 Substratum 或 Swift Installer 等应用程序安装自定义覆盖。

据 Swift Installer 的开发者称，Exynos 三星 Galaxy S8 和 Galaxy Note 8 最先受到这些限制。在 Swift 的官方 Telegram 组中，一名开发人员发布了一个常见问题列表，以回答用户可能对这些新变化提出的任何具体问题。

**三星派 One UI 常见问题——(18/01/19)**

问:我可以在哪个 UI 设备和固件上使用主题？

答:这个不一样。在我写这篇文章的时候:

在三星 S9、S9+和 Note 9 Stable Pie 上:你目前可以在没有 root 的情况下使用 Substratum themes 和 Swift Installer。

在三星 S8、S8+和 Note 8 Beta Pie 上:三星目前已经在这些版本中阻止了无根覆盖安装。据报道，这显然只适用于 Exynos 设备(较新的版本)，而骁龙设备(较旧的版本)似乎可以使用主题。

重要提示:请注意，所有这些在新的 Samsung Pie 版本中可能会改变，也可能不会改变，对于提到的任何设备-无论是好是坏-它都是在 Samsung 的控制之下，而不是我们的！这是显而易见的，但有必要指出。

不幸的是，这个常见问题已经过时了，因为我们也注意到骁龙三星 Galaxy S8 的官方 One UI 测试版也有这些变化。我们对此感到惊讶的原因是，骁龙 Galaxy S8 和 Galaxy Note 8 的一个 UI 的早期[泄露版本](https://www.xda-developers.com/samsung-galaxy-s8-snapdragon-install-closed-one-ui-android-pie-beta/)仍然允许安装自定义覆盖，这意味着 Swift 安装程序和底层仍然可用。为了证实这一变化，我拿着我的骁龙三星 Galaxy S8，试图安装一个已经编译好并安装在我的骁龙三星 Galaxy Note 9 上的主题。如果你试图在运行 Android 9 Pie 的 Google Pixel 3 上安装一个主题，下面的错误和你得到的错误是一样的。

我们不确定为什么这一限制只影响 Galaxy S8 和 Galaxy Note 8，特别是因为我测试的 Galaxy S8 One UI beta 的构建日期早于 Galaxy Note 9 的最新 One UI 构建日期(1 月 21 日对 1 月 31 日)。这个消息真的让三星的主题社区很扫兴。三星官方主题商店真的限制了定制主题的可能性。大多数主题仍然可以在[底层上工作，因为你已经根化了](https://www.xda-developers.com/custom-themes-android-p-root-substratum/)，但是很多用户不愿意根化他们的设备。