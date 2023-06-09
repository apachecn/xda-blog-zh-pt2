# [MAGISK]如何在您的 Android 设备上启用 PS4 远程游戏，并使用 DualShock 4 +玩游戏提示和意见

> 原文：<https://www.xda-developers.com/how-to-enable-ps4-remote-play-on-any-android-and-play-dualshock-4-tips-opinion/>

如果你足够幸运，既有 PlayStation 4 游戏机，又有索尼 Xperia 智能手机或平板电脑，那么你可能会知道一项为你提供的服务: [Remote Play](https://play.google.com/store/apps/details?id=com.playstation.remoteplay&hl=en) ，这是一款应用程序，让你可以通过你的游戏机在智能手机上玩 PS4 游戏。

现在，智能手机上的远程游戏有点像是一种情景功能——它非常受你的控制台和智能手机上的互联网连接速度的限制，如果没有游戏夹将你的手机和控制器固定在一起，设置起来会很麻烦。考虑到它“需要”WiFi(虽然它可能会被欺骗)，你也可能会在家里玩它。但它仍然很有用，因为它让你可以继续玩视频游戏，即使有人在囤积电视，或者如果你想在不同的房间或在厕所里玩游戏。更重要的是，你仍然可以通过使用 Nougat 的多窗口来回复文本等，而不会中断你的游戏。或者，您可以在游戏中显示浮动视频，进行多任务处理——机会是无限的。

虽然这项服务可以在 Mac 和 Windows 上使用，但遗憾的是，在 Play Store 上搜索时，Android 应用程序只能在索尼设备上使用。此外，即使你拿到了 APK，它也不能在你的非索尼智能手机上运行。最后，虽然 DualShock 4 可以被 Android(蓝牙)本机识别，但如果你甚至可以在你的设备上运行远程播放，驱动程序和兼容性问题可能会使它过时！不过，XDA 的论坛用户提出了一些解决这个问题的实用方法。具体来说，[我会参考 XDA 资深会员](https://forum.xda-developers.com/apps/magisk/module-ps-remote-play-enabler-t3575876) [leolawliet](https://forum.xda-developers.com/member.php?u=4206297) 的一个简短指南(非常感谢！)我将添加一些更详细的内容，加上一些提示和对体验的简短回顾。如果你有 Magisk (root)或者愿意刷新 Magisk，看看这个指南，让你的 PS4 游戏在你的智能手机上运行！

* * *

1.  首先，你要确保通过自定义恢复 (TWRP)来刷新 Magisk，从而启用 Magisk。你可以在这个线程上找到[必需的文件和安装说明。不管你是否想要或需要这个 mod，Magisk 都是很好的选择，因为它是最好的无系统根解决方案之一。](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)
2.  一旦你设置好 Magisk，进入侧边菜单的“下载”标签，然后**搜索 Seyaru** 的“索尼框架”模块(v1)。这将安装必要的基础来使用远程播放，就像你有一个索尼 Android 设备。下载完成后，它会要求安装和启用模块，这需要重新启动。您可以现在重新启动，也可以按照本指南继续操作，因为稍后也需要重新启动。
3.  现在你已经有了索尼的框架，**你需要检查你的 build.prop 以使你的设备兼容远程播放版本 2.0.0** 。索尼通过提示用户在建立连接之前更新应用程序，使以前的版本([，在我们的](https://forum.xda-developers.com/android/apps-games/ps4-remote-play-android-thread-t3068225)论坛上广泛提供，预先修改)过时。幸运的是，正如 XDA 资深成员 [leolawliet](https://forum.xda-developers.com/member.php?u=4206297) 所发现的[，您可以通过 build.prop 编辑来解决这个问题:只需添加(或者替换，如果您有一个具有不同值的类似行)这一行`ro.build.tags=release-keys`。或者，您可以安装由 leolawliet 提供的 Magisk 模块，以便将它添加到您的 build.prop 中。另外，据报道，最近的 Magisk 更新已经使它不需要任何更改。无论哪种方式，正如这里列出的，如果一开始就不适合你，你可以用几种方法来解决这个问题。无论您采取哪种方法，都要确保启用框架模块，并且 build.prop 更改已经存在，然后重新启动您的设备。](https://forum.xda-developers.com/apps/magisk/module-ps-remote-play-enabler-t3575876)
4.  [在 Play Store 中搜索“远程播放”](https://play.google.com/store/apps/details?id=com.playstation.remoteplay&hl=en) -您应该会看到该应用程序，尽管您可能无法安装它(结果因我而异)。如果是这种情况，您需要通过 APK 下载器网站或浏览器扩展下载 APK(检查 MD5 总和以验证 APK 的完整性)。一旦你安装了远程播放，**再次进入 Magisk，在“设置”下启用“Magisk 隐藏”。**之后，侧面板会出现一个新菜单。进入菜单，然后搜索你的 PlayStation 应用程序，然后“隐藏它们”。这样，在启动远程播放时，您将不会得到 root 访问提示。
5.  这就是棘手的地方。根据你的 ROM，你可能根本无法通过 DualShock 4 发送任何输入，或者可以将它用作游戏手柄，但不能用作远程游戏控制器(就像我在 LineageOS 上的情况)。幸运的是，有一个(公认的尴尬)通用的解决方法:这将使**你的 DualShock 4 保持与 PlayStation 4** 的连接，并能够在你的屏幕投射到你的设备时操作它。当然，唯一的限制是，你将被限制在蓝牙范围内。我发现范围不是太大的问题，尽管墙壁会碍事，当距离控制台两三个房间和墙壁时，麦克风输入和输出会开始断断续续(尽管输入延迟不会随着距离的变化而明显变化)。希望您根本不需要这种变通方法。

    1.  **创建第二个 PSN 帐户** -它不需要订阅，只需要在你的 PS4 上
    2.  确保在你的 PS4 上配置了远程播放功能，并且在那个账户上配置了远程播放功能
    3.  **通过远程游戏**连接到这个新的虚拟帐户，而你的主 PS4 帐户在前台

    This will make it so that
6.  ***尽情享受！***

* * *

## 技巧和窍门+我的看法

一旦一切就绪，连接到 PS4 进行流媒体播放就像启动应用程序并按下控制器上的 PlayStation 按钮以确保连接一样简单。您可以以标准或高帧速率(30 或 60)进行传输，分辨率选项包括 480p、540p、720p 和 1080p。我个人发现 720p 在我的使用案例中表现出色，1080p 在某些游戏或场景中也非常好。在线用户报告还指出，在高帧率模式下玩 30FPS 的游戏可以减少输入延迟。如果你在玩一个简单的独立游戏，比如“雨的风险”，你可以期待流畅和稳定的游戏，没有输入延迟和帧丢失。我还可以毫无问题地玩《黑暗之魂 3》甚至《战地 1》(除了后者的帧率低于标准，因为我当时的帧率是 30FPS)。我确实有 100mbps 的下载和 20mbps 的上传连接，但在监控我的互联网时，我从未发现 PS4 和手机占用太多流量，甚至在优先考虑这两种设备时也没有(在这种情况下，你应该优先考虑 PlayStation 4)。

我还使用游戏夹将我的控制器连接到我的 DualShock 4 上——这种设置有点笨重，因为它比标准的操纵杆设置重得多，尽管在正确的角度下，额外的重量是非常容易管理的(当然，这取决于你的设备)。即使在 1080p 下，图形保真度也不如普通 PS4 清晰，但观看距离有助于隐藏一些瑕疵。如果你有一个 AMOLED 显示屏，你将能够体验到你以前从未体验过的游戏中的黑暗区域(假设你没有一台出色的 OLED 电视)，这是我在 Bloodborne 等游戏中真正欣赏的东西。不过，最终，你要在图形质量和输入延迟之间找到正确的平衡——在稳定的互联网连接下，你应该能够在 720p 时有不明显的延迟，但我个人会调整分辨率，使游戏尽可能响应迅速。即使是 5.5 英寸显示器上的 540p 看起来也不算太差，但如果不是因为流媒体游戏引入的轻微压缩和伪像，720p 的每英寸像素将比任天堂 Switch 更多。

我最喜欢的一些用例包括和我的女朋友在厨房里闲逛时玩游戏，在我的办公室快速休息时，或者在上厕所时(因为为什么不呢？).当我的女朋友在看我们主要的电视节目时，我也会这样做。我也很感激我可以简单地**保持多任务菜单，并立即启动 splitscreen 来使用另一个应用程序，同时监控游戏**。这在加载屏幕期间，或者在等待大厅准备就绪时特别有用——如果你*让*应用*没有*多窗口活动，你将不得不重新启动远程游戏，但是游戏将继续在后台做它的事情(你的 PS4)。例如，你可以一边浏览 reddit，一边等待同事加入你的会话，或者在即时消息应用上快速回复一条短信。最后，虽然玩游戏时在多窗口上观看视频是不切实际的，但 Twitch 等应用程序提供的视频覆盖将以任何方式*而不是*中断远程游戏，允许你继续玩视频游戏，例如，在观看其他人玩视频游戏时。

* * *

我们希望你会发现这个指南很有用——再次感谢索尼框架模块和 XDA 资深成员 leolawliet 的变通方法和简短指南。环城见！