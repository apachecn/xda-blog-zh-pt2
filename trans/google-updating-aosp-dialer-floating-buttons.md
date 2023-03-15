# 谷歌正在更新 AOSP 拨号器，增加了浮动通话按钮等功能

> 原文：<https://www.xda-developers.com/google-updating-aosp-dialer-floating-buttons/>

# 谷歌正在更新 AOSP 拨号器，增加了浮动通话按钮等功能

自从谷歌切换到 AOSP 拨号器的公共开发模式，开源拨号器应用程序正在接受一系列重大更新。

谷歌一直在努力为谷歌拨号器应用程序添加更多的功能，但尚未决定切换开关并公开这些功能。上个月晚些时候，我们介绍了一种在应用程序中启用新的浮动气泡功能的方法，但现在看来，如果更多人愿意安装其开源版本，他们将可以使用这一功能。我们已经发现，谷歌正在更新 AOSP 拨号器应用程序的这一具体功能，并致力于保持 AOSP 拨号器最新。

这其实很有趣，因为 AOSP 拨号器(以及其他 AOSP 应用程序和功能)已经被裸露了很长一段时间。随着谷歌在核心的 Android 操作系统上增加更多功能，他们已经关闭了许多最有趣的功能的源代码，任何人都无法使用 AOSP 的普通版本。大多数人只是喜欢在他们基于 AOSP 的 rom 上运行 Gapps 包，但也有很多人喜欢开源包，尽可能避免使用谷歌服务。

不幸的是，这导致他们使用旧版本、功能不丰富的 Android 基本应用和服务。例如，AOSP 拨号器之前已经在版本 10 上停留了相当长一段时间，因为谷歌只会在他们放弃主要版本的源代码时更新 AOSP 拨号器。然而，根据我们发现的的[提交，AOSP 拨号器已经升级到第 13 版，更好的是，谷歌正在转向公共开发模式。](https://android.googlesource.com/platform/packages/apps/Dialer/+/2ca4318cc1ee57dda907ba2069bd61d162b1baef)

这意味着 AOSP 拨号器的用户不必等待主要的新 Android 版本发布来尝试新功能，定制 ROM 开发者可以更频繁地将更新整合到 AOSP 拨号器中。结果，AOSP 的拨号器接收到了我们最近讨论过的那些[浮动呼叫按钮](https://android.googlesource.com/platform/packages/apps/Dialer/+/master/java/com/android/dialershared/bubble)。