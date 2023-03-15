# Android Oreo 为开发者增加了闪屏 API

> 原文：<https://www.xda-developers.com/android-oreo-splash-screen-api/>

# Android Oreo 增加了一个闪屏 API，这样开发者就可以轻松构建应用加载屏幕

谷歌刚刚通过制作官方闪屏 API，让开发者在最新的 Android Oreo 版本中更容易地构建应用加载屏幕！

大多数开发者对闪屏有不同的看法。一些人主张使用它来隐藏后台的应用程序加载，然后无缝地过渡到它。另一方面，有些人认为闪屏对用户和开发者来说都是浪费时间。谷歌在这个问题上的立场是混合的，之前没有推广闪屏的使用，但后来开始在许多应用程序中使用闪屏。通过 Android Oreo，谷歌希望让开发人员创建一个简单的闪屏变得更加容易。

谷歌在 Android 8.0 中引入了“闪屏 API”。这个 API 允许开发人员轻松地将可绘制资源设置为应用程序加载屏幕。你也可以在你的应用程序中的重要活动之间设置一个闪屏。在 Android Oreo 之前，有许多不同的方法来构建闪屏，最常见的是创建一个 drawable、一个自定义主题和一个 SplashActivity。谷歌希望通过让开发者利用这个新的 API 来简化和简化这个过程。

这一变化目前还没有记录在 Android 开发者网站上。该承诺于 4 月 13 日添加到 AOSP，正好在第一次和第二次 Android O 开发者预览版正式发布之间。因此，为了学习如何使用它，您需要参考 [AOSP 提交](https://android.googlesource.com/platform/frameworks/base/+/7d0d10275213f23e2bd200d22822a3b700157688%5E%21/)，并检查从那时起所做的更改。我们确实希望这个 API 的官方 Google 文档最终能够上传，以便让事情变得更简单。

这个[不是](https://www.xda-developers.com/android-oreo-virtual-reality-developer/)唯一的[变化，因为谷歌已经引入了许多新的、有用的 API 和开发者特性。我们已经做了大量的挖掘工作来寻找这些变化，但是要看到更多，你需要亲自去挖掘](https://www.xda-developers.com/virtual-sd-card-android-oreo/) [Android 开源项目](https://www.xda-developers.com/android-oreo-source-code/)！