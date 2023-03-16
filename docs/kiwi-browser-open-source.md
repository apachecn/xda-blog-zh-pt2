# Android 版奇异果浏览器现已完全开源，包括扩展

> 原文：<https://www.xda-developers.com/kiwi-browser-open-source/>

基于 Blink 引擎的开源 Chromium 项目是许多网络浏览器的基础。最受欢迎的是谷歌 Chrome，还有微软 Edge、Vivaldi、Brave 等等。大多数基于 Chromium 的网络浏览器都提供了一些谷歌 Chrome 中没有的附加功能，但也有一些从根本上改变了用户体验。XDA 资深会员 arnaud42 的奇异果浏览器就是这样一款网络浏览器，在该浏览器两周年之际，开发者已经完全开源了该网络浏览器及其所有功能。

早在 2018 年，arnaud42 发布了他基于 Chromium 的网络浏览器的第一个版本。当我们几个月后第一次报道这个项目时，我们对它当时提供的功能集印象深刻，这与浏览器今天提供的功能相比相形见绌。它具有内置内容拦截器、黑暗模式、背景视频播放、放大器 skipper 等功能。随着每一次更新，浏览器[变得越来越好，但真正让它闪光的是这样一个事实:它是第一个基于 Chromium 的 Android 浏览器，](https://www.xda-developers.com/tag/kiwi-browser/)[支持 Chrome 扩展](https://www.xda-developers.com/kiwi-browser-google-chrome-extensions-android/)。

事实证明，维护这样一个雄心勃勃的项目对于孤独的开发人员来说是一个挑战。谷歌 Play 商店上最新版本的 Kiwi 浏览器基于 Chromium 版本 77.0.3865.92，远远落后于谷歌正在计划的即将发布的 Chromium 版本 83。为了不浪费这个项目，arnaud42 决定在 GitHub 上发布 Kiwi 浏览器的源代码。他说“所有的东西都被发布了，包括扩展代码”并且“没有任何附加条件”(浏览器是根据 BSD 第 3 条款授权的[)。)他鼓励其他基于 Chromium 的网络浏览器的开发者将 Kiwi 的代码集成到他们的项目中。他表示，在过去的几周里，他与其他浏览器开发人员合作，帮助他们集成 Kiwi 的一些功能，因此我们可能很快就会听到 Android 上其他 web 浏览器的一些好消息。](https://github.com/kiwibrowser/src/blob/master/LICENSE)

Arnaud42 将继续在项目的 GitHub 上审查代码提交，如果你有兴趣为项目做贡献的话。代码是用 Java 和 C++编写的，所有依赖项都已经包含在库中，以帮助那些在设置 Chromium 构建系统时遇到困难的开发人员。

**[GitHub 上奇异果浏览器源代码](https://github.com/kiwibrowser/src)| |[XDA 论坛线程](https://forum.xda-developers.com/android/apps-games/app-kiwi-browser-chromium-adblock-caf-t3797252)**

奇异果浏览器是一段时间以来我们在论坛上看到的最令人印象深刻的项目之一。开发者 arnaud42 也是 XDA 的朋友，所以我们要感谢他在过去两年里为这个项目所做的工作。我们希望其他基于 Chromium 的浏览器能很快融入 Kiwi 的一些特性，因为我真的很怀念在手机上使用扩展的能力！

[appbox xda com . kiwi browser . browser]