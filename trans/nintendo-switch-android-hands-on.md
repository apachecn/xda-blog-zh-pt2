# 我们已经在任天堂 Switch 上安装了安卓系统:下面是它的功能

> 原文：<https://www.xda-developers.com/nintendo-switch-android-hands-on/>

如果你最近一直关注任天堂 Switch 的发展，你会注意到现在有很多很酷的事情正在发生。从 L4T (Linux 4 Tegra) Ubuntu 的发布到 emuMMC 的发布，这是拥有一台( [hackable](https://www.xda-developers.com/nvidia-tegra-x1-google-pixel-c-nvidia-shield/) )任天堂 Switch 的最好时机。现在，埃利亚斯已经超越了他自己，因为你很快就可以把你的任天堂 Switch 变成一个成熟的 Android 平板电脑——完全支持 dock 和 Joycon。在公开发布之前，我们有机会在任天堂 Switch 上测试 Android，看看它能做什么。

**[任天堂 Switch XDA 论坛](https://forum.xda-developers.com/nintendo-switch)**

注意:这个版本的 Android 还没有公开发布，因为安装过程需要简化。它完全是无系统的，并且在 SD 卡上运行，所以任天堂的服务被禁止的可能性很小甚至没有。你需要一个可开发的开关，你可以在这里阅读更多关于[的信息。](https://nh-server.github.io/switch-guide/faq/#what-firmware-versions-are-currently-hackable)

## 任天堂 Switch 上的 Android 是如何工作的

任天堂 Switch 从来就不是用来运行安卓系统的。这是一款便携式游戏主机，配有 6.2 英寸 720p 显示屏，由 Tegra X1 芯片组(也可以在 NVIDIA SHIELD Android TV 中找到)驱动，4GB lpddr 4 RAM 和 4，310 mAh 电池。它运行的游戏有*《塞尔达传说:野性的呼吸》*、*《超级马里奥奥德赛》*和*《马里奥赛车 8:豪华版》*。这些规格造就了一台相当强大的掌上游戏机，但想象一下具有这些规格的 Android 平板电脑吧？这就是我们现在所拥有的[多亏了规章制度和开发伙伴](https://www.xda-developers.com/developer-turn-nintendo-switch-into-android-tablet/)，虽然它当然还不完美*和*，但它已经非常强大了。

交换机最吸引人的一个方面是它是一个混合控制台。当你把它放在 Switch dock 中，并从侧面拆下控制器时，它就变成了一个成熟的控制台，通过 HDMI 输出 1080p，CPU 和 GPU 时钟频率更高。完成后，只需重新连接控制器，将交换机从坞站中取出，并在任何地方使用它。NVIDIA SHIELD 平板电脑也采用了类似的想法，这是一款 Android 游戏平板电脑，可以以高达 8K 的分辨率输出到电视上。Android 在 Switch 上的工作方式与它曾经在 NVIDIA SHIELD 平板电脑上的工作方式相同。对接你的开关，它会通过 HDMI 输出显示，你可以在更大的屏幕上继续正常使用。Switch dock 还有 3 个 USB 端口，您可以将键盘、鼠标和其他外围设备插入其中。目前，USB 大容量存储安装不工作。

除此之外，任天堂 Switch 上的 Android 就像平板电脑一样工作。

 <picture>![](img/2d17e0bd082f3d1f5cb9b7626836eb18.png)</picture> 

Android for the Nintendo Switch is currently based on the LineageOS 15.1 (Android 8.1 Oreo) build for the 2015 NVIDIA SHIELD Android TV (foster).

通常情况下，人们购买 Android 平板电脑的首要原因是媒体消费。更大、更好的屏幕非常适合观看视频和玩游戏，这就是 Switch 的用武之地。它完全支持 Google Play 商店上的所有应用，所以你可以看网飞、YouTube、听音乐...几乎所有你期望从安卓平板电脑上得到的东西。当然，有一些小问题需要解决，但不会太严重。可以把这看作是 Android 智能手机 LineageOS 的第一次构建:它还远未完成或完善。

 <picture>![Netflix Nintendo Switch](img/f92c1333650ad545c808b2659b041974.png)</picture> 

Netflix on the Nintendo Switch running Android. You can't watch Netflix videos in HD as the Switch is not [Widevine L1 certified](https://www.xda-developers.com/android-netflix-hd-amazon-prime-video-hd-drm/). I tested viewing Breaking Bad and Love, Death & Robots.

如果你是一个媒体狂热者，喜欢离线存储文件，那么我有好消息要告诉你。用于任天堂 Switch 的安卓系统可以拥有和你放在上面的 SD 卡一样多的存储空间。这是因为安装的一部分涉及到在启动之前将/data 分区扩展到您想要的大小，所以我扩展了它以填充我的 64GB micro SD 卡的剩余部分。这意味着您不会受限于交换机上的 32GB eMMC 存储，更重要的是，您不会修改设备本身的任何内容。

## 游戏性能

正如您对 Tegra X1 的期望，游戏轻而易举。这里和那里都有一些小问题，尽管我认为这是由于目前缺乏优化造成的。例如，我测试了 PUBG Mobile，虽然 Joycons 不工作，但游戏在平衡的图形上运行良好。我用了 balanced，因为游戏不会让我走得更高，告诉我这些选项将“很快”出现在我的设备上

然而，Joycons 是另一回事，因为它们目前还没有像你预期的那样无缝地工作。它们需要通过蓝牙连接，让它们物理连接到您的交换机上，仍然可以在无线模式下使用它们。没有像我们在一加 7 Pro 上遇到的奇怪的输入延迟问题。从技术上讲，你可以用它们来导航整个系统 UI。然而，并非所有东西都支持 Joycons。我在试用 Dolphin Emulator 和 Steam Link 时遇到了问题，尽管看起来它们在以前的版本中运行得很好。因此，我相信他们会在发布时再次工作。

有一个模拟器，我得到了完美的工作:DraStic。DraStic 是谷歌 Play 商店上最好的任天堂 DS 模拟器之一，它在 Switch 上运行完美。这是一个巨大的成就，因为还没有其他的 DS 模拟器能在这上面完美的工作。我可以通过 DraStic 用我分离的游戏手柄和我的对接开关玩*口袋妖怪黑*，这是一次愉快的经历。

对于模仿其他游戏主机，我推荐使用 RetroArch。我通过它玩了口袋妖怪绿叶游戏，它与一个配对的 Joycon 一起工作，尽管我在配对第二个时也有问题。除此之外，它工作良好，运行完美。玩*口袋妖怪*也不需要两台游戏机的功能。SNES 模拟很棒，我通过 Snes9x 玩了一些*到过去*的链接。

目前，我只能想象，随着时间的推移，整个系统中存在的性能问题将会得到解决。与 SHIELD TV 相比，Switch 上的 Tegra X1 的时钟不足，但 Switch 8.0 的更新使游戏开发者能够在加载屏幕时提高时钟速度，Android 版本也将在发布时利用这一点(最新的私有版本中添加了时钟控制)。任天堂 Switch 已经成长为一款出色的安卓游戏设备，在这方面它的前景是光明的。我还被告知，几乎所有东西都是功能性的，因为它们都是从 NVIDIA SHIELD Android TV 移植过来的。应该全力支持 SoC 及其所有功能。

## 什么不起作用

遗憾的是，将任天堂 Switch 用作安卓平板电脑有很多缺点。例如，Switch 不支持 GPS，也没有麦克风，甚至没有摄像头。这意味着没有口袋妖怪 Go，没有与 T2 和谷歌的语音和视频通话，也没有 Snapchat 这样的应用。您可以将蓝牙耳机用于音频，尽管它使用基本的 A2DP 来连接。这里没有使用 LDAC 或任何其他更先进的蓝牙编解码器。Joycons 还不能与所有的应用程序兼容，至于它们能与什么兼容，不能与什么兼容，这看起来非常不一致。RetroArch 发现左侧 Joycon D-Pad 上的所有四个按钮具有相同的功能，但它们显然不具有相同的功能。你也不能使用每个 Joycon 的导轨上的 L 和 R 按钮，如果只使用一个的话会有问题。你也还不能截图。

## 你问了，我们测试了

我们在 XDA 开发者的 Twitter 账户上发帖，询问我们的读者他们想在任天堂 Switch 的 Android 上测试什么。我们收到了很多测试不同游戏和应用的请求，你可以在上面读到。我们还被问及 Spotify(可以用)和堡垒之夜(不能用)。

也邀请了 Flappy Bird。我测试过了。[起作用了](https://twitter.com/AdamConwayIE/status/1142081077047123968)。YouTube、Spotify 和 Twitch 也都可以。

## 它什么时候发行？

章程和其他参与任天堂 Switch 开发的人正在准备发布。会有一个简单的安装程序来设置你的 SD 卡，目前是通过赫卡忒启动的。没有预期的 ETA，虽然你应该检查我们的任天堂 Switch 论坛，并留意交换机上的 Android 线程！

**[任天堂 Switch XDA 论坛](https://forum.xda-developers.com/nintendo-switch)**