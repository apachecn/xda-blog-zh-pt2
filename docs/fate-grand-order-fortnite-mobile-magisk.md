# 使用 Magisk 在根设备上玩命运/大订单和堡垒之夜移动

> 原文：<https://www.xda-developers.com/fate-grand-order-fortnite-mobile-magisk/>

# Magisk 已更新，支持 Fate/Grand Order 和堡垒之夜移动

Magisk 已在金丝雀频道更新，支持命运/大订单和堡垒之夜移动。现在你可以在根设备上玩这两个游戏了！

植根于你的 Android 智能手机或平板电脑可以带来许多好处，例如让你在 Android Pie 上安装[自定义主题，用](https://www.xda-developers.com/custom-themes-android-p-root-substratum/) [A.R.I.S.E](https://forum.xda-developers.com/android/software/r-s-e-sound-systems-auditory-research-t3379709) 调节你的音频输出，通过更好地控制 wakelocks 来控制你的电池寿命，等等。但是不利的一面是，你将不得不处理有反根检测的应用程序。幸运的是，有 Magisk，由 XDA 公认的开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 开发，它允许你欺骗使用安全网认证 API 的应用程序，使其认为你的设备不是根设备。然而，一些游戏，如 Fate/Grand Order 和堡垒之夜移动，仍然能够检测到你的设备是否是根设备。现在，最新版本的 Magisk 可以让你玩命运/大订单和堡垒之夜手机，甚至在你的 Android 设备上！

Fate/Grand Order 是一款根据 Type-Moon 的视觉小说系列改编的手机 RPG。堡垒之夜手机是 Epic Games 公司的一款广受欢迎的免费游戏。这两款游戏都使用 SafetyNet 认证 API 来验证运行它们的设备的完整性，但它们也实现了额外的检查来检测 root 访问。然而，多亏了 topjohnwu 的辛勤工作，加那利海峡 Magisk 的最新版本绕过了这些检查。topjohnwu 告诉了我们他为让这些游戏运行所做的修复，但我们将在本文中跳过这些细节。(Magisk 是[开源的](https://github.com/topjohnwu/Magisk)，所以你可以很容易地验证 topjohnwu 所做的所有幕后工作。)

[**堡垒之夜移动安卓下载**](https://www.epicgames.com/fortnite/android)

警告:Magisk 金丝雀建筑不适合胆小的人。它们只面向专业用户和开发人员！金丝雀频道类似于谷歌 Chrome 金丝雀:出血边缘建立在最新的来源。它可能不稳定，所以不要急于安装它！一旦所有的 bug 都解决了，与 Fate/Grand Order 和堡垒之夜移动合作的 Magisk 版本将会发布到测试版。

## 在根设备上玩命运/大订单和堡垒之夜移动

如果你已经阅读了上面的警告，并且*仍然*想要在你的根 Android 设备上玩这些游戏，你需要按照这些说明加入 Magisk Canary 频道，然后在 Magisk Hide 中隐藏该应用程序。

1.  打开 Magisk 管理器并转到设置。
2.  查找“更新频道”并将其更改为“自定义”
3.  将以下 URL 粘贴到框中:`https://raw.githubusercontent.com/topjohnwu/magisk_files/master/canary_builds/canary.json`
4.  重启管理器应用程序并安装最新的 Magisk Canary 版本。
5.  重新启动后，再次打开管理器应用程序，进入 Magisk 隐藏菜单。
6.  根据您想玩的游戏，在列表中选择命运/大订单或堡垒之夜移动。
7.  开始游戏。

享受在你的安卓设备上玩命运/大订单和/或堡垒之夜手机的乐趣吧！如果你喜欢 topjohnwu 为社区所做的工作，可以考虑在 Patreon 或通过 PayPal 支持他。