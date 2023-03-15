# Skyline 是一个正在开发的任天堂 Switch 模拟器，实际上可以工作

> 原文：<https://www.xda-developers.com/skyline-is-an-in-development-nintendo-switch-emulator-that-actually-works/>

你可以用 Android 智能手机做很多事情，你可以为现代和复古系统获得的模拟器数量令人难以置信。从古老的系统如 NES 到[任天堂 3DS](https://www.xda-developers.com/official-citra-for-android-released/) ，你都可以在手机上舒适地玩。模仿较新的系统，如任天堂 Switch，有点困难。然而，继[概念上的任天堂 Switch 模拟器](https://www.xda-developers.com/mononx-nintendo-switch-emulator-android/)发布，然后[一个需要特定游戏手柄才能使用的可疑模拟器](https://www.xda-developers.com/shady-nintendo-switch-emulator-android/)之后，Skyline 是第一个真正有效的任天堂 Switch 模拟器，你已经可以测试它了。

回顾一下，Skyline 已经开发了一年多了，直到最近才有一些游戏可以玩。正如一位开发人员告诉我的，Skyline 是专为*和* Android 设备打造的，并且完全遵循这一理念——同时利用社区项目来帮助其开发。例如，Ryujinx 由于其准确性而在整个项目中被用作参考，Skyline 中使用的着色器编译器是 yuzu 的一个分支。Ryujinx 和 yuzu 背后的团队都为 Skyline 的开发提供了帮助，Skyline 团队也获得了 yuzu 的许可豁免。

目前，开发者倾向于专注于一次运行一个游戏。第一个是*索尼克狂热*，第二个是*塞莱斯特*，现在正在进行的第三个是*超级马里奥奥德赛*。这是因为当一个游戏运行得近乎完美时，顺便提一下，其他游戏也会开始运行。

## 天际线应用

Skyline 应用程序本身非常简单，尽管它拥有你需要的所有功能。您可以设置主题、布局、性能统计、更改日志保存方式、用户名、语言等等。还有支持多个控制器的支持，这样你就可以和朋友一起玩多人游戏了。所有你需要的是确保你有你的生产密钥和标题密钥以及你的游戏，你可以通过转储你的任天堂 Switch 上的锁匙 RCM 得到这些。

## 游戏兼容性是命中或错过

目前，Skyline 还没有达到完全可玩的状态——事实上，远非如此。许多游戏都无法运行，兼容性列表中可玩的部分也很少。也就是说，我们测试了*超级马里奥奥德赛*和*塞莱斯特*，给你一个预期的概念，至少可以说，这是相当令人印象深刻的。我们也尝试过玩*动物穿越:新视野*但是没有运行。请注意，虽然以下录音的音频不同步，但播放时音频没有不同步。

### 塞莱斯特

Celeste 是一款有趣的平台游戏，可以在很多平台上使用，但不能在 Android 上使用。它在我的[一加 10](https://xda-developers.com/oneplus-10) Pro 和[高通骁龙 8 代 1](https://www.xda-developers.com/qualcomm-snapdragon-8-gen-1) 上的运行速度在 40 到 60 FPS 之间，这使得它可以完美地播放。这很有趣，尽管触摸控制有点危险。这是因为游戏需要非常精确的输入，与模拟器本身无关。

### 超级马里奥奥德赛

*超级马里奥奥德赛*是 Skyline 团队努力的最新焦点游戏。目前，它可以显示菜单，但我的一加 10 Pro 无法加载世界本身。3D 游戏比 2D 游戏更难模拟，所以你可能需要一段时间才能看到这款游戏在设备上正常运行。

## 下载并安装 Skyline

如果你想试试 Skyline，一定要[加入团队的 Discord](https://discord.com/invite/XnbXNQM) 看看最新的 apk 可以下载，并且在服务器上讨论之前先阅读规则。你需要一个 GitHub 账户，然后输入。rl ftx1”将为您提供一个链接，为您的设备下载最新的 APK。否则，你可以按照团队的构建说明，从 GitHub 上的[源代码中自己构建应用。](https://github.com/skyline-emu/skyline/tree/ftx1)