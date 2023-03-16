# 应用程序音量控制可让您控制应用程序的单个音量级别[Root]

> 原文：<https://www.xda-developers.com/app-volume-control-individual-volume-levels-android/>

如果你曾经试图在智能手机上同时播放几个 Android 应用程序的音频，你可能已经意识到这样做很糟糕。当 Spotify 上你最喜欢的音乐在背景中响起时，你可以随意地欣赏一款 Android 游戏，这将是一件很棒的事情。另一方面，如果你能把大部分精力放在像《使命召唤:手机》这样的游戏上，而不让你的音乐完全盖过游戏音频，那也不错。Android 的问题是，该操作系统只提供少数几个你可以控制音量的音频流，其中一个是媒体流。这个媒体流是游戏和大多数音乐应用程序输出音频的地方，所以在大多数情况下，你必须同时控制游戏和音乐的音量。幸运的是，有一个名为“应用音量控制”的手机新模式可以解决这个问题。

Android 提供了“[音频焦点](https://developer.android.com/guide/topics/media-apps/audio-focus)的概念，这是一组可以由第三方应用程序合作使用的 API，以便一次只有一个应用程序可以保持焦点。每当另一个应用程序接管音频焦点时，应用程序可以选择是否暂停或“闪避”它们的音频。因为谷歌让开发人员决定当音频焦点丢失时如何处理事情，所以当另一个应用程序接管音频焦点时，应用程序的行为有很多不一致之处。

XDA 少年成员 [Alcatraz323](https://forum.xda-developers.com/member.php?u=10682425) 想出了一个有趣的开源 mod，它不仅允许你强制多个应用程序同时播放音频(以防一个应用程序在另一个应用程序接管音频焦点时选择停止音乐)，而且还能够控制每个应用程序的音量。开发者在谷歌 Play 商店上发布了一个名为“应用音量控制”的配套应用，他们还发布了一个名为“音频总部”的 Magisk 模块来设置 mod。Magisk 模块由低级库组成，而 Android 应用程序允许您在每个应用程序的基础上定制音量行为。成功安装该模块后，用户可以通过配套应用程序创建和调整应用程序特定的音频预设。用户还可以启用应用程序的浮动窗口来轻松调节应用程序外部的音量。

据开发商称，接近库存的软件或 AOSP 衍生的定制 rom 如 LineageOS 是最适合这种模式的。小米的 MIUI 或华为的 EMUI 等重型 OEM 皮肤可能会有问题，让 mod 工作。我们在我们运行 Android 10 的根 Google Pixel 4 上安装了这个 mod，以验证它是否有效。我们能够让它识别 Spotify 何时播放，这使我们能够在玩《使命召唤:手机》时控制 Spotify 音乐的音量。不过，该应用无法识别 Google Play Music 中的音乐播放。该应用程序警告说，它可能无法识别不是通过 AudioMixer API 发送的直接音频输出会话，该 mod 与该 API 挂钩。因此，您的里程可能会有所不同。

[app](https://github.com/Alcatraz323/audiohq_md2)和[模块](https://github.com/Alcatraz323/audiohq_module)的源代码托管在 GitHub 上。您可以使用 Magisk Manager 中的搜索功能下载音频总部模块，也可以直接从资源库的 [GitHub 发布页面](https://github.com/Alcatraz323/audiohq_module/releases)获取。开发者建议不要使用 Magisk 的 Canary 版本，并建议在 Magisk 20.2 或之后的上安装 mod。虽然你可以从谷歌 Play 商店安装配套的应用程序(链接如下),但没有底层的二进制文件，应用程序本身什么也做不了。

**音频总部: [XDA 讨论线程](https://forum.xda-developers.com/android/software-hacking/app-app-volume-control-t4101893) ||| [GitHub 回购](https://github.com/Alcatraz323/audiohq_module)**

注意:该模块的默认安装选项是将 SELinux 设置为 permissive，这是非常不安全的，不建议这样做。开发人员注意到，该模块的一个新版本(尚未在 GitHub 上发布)可能会与设置为 enforcing 的 SELinux 一起工作。

[app box Google play " io . Alcatraz . audio HQ "]