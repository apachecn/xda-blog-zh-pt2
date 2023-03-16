# 独家:小米 Mi Max 3 配备了无线充电功能，可能还有虹膜扫描仪

> 原文：<https://www.xda-developers.com/xiaomi-mi-max-3-wireless-charging-iris-scanner/>

小米今年最受期待的智能手机可能是他们的两款旗舰手机:Mi Mix 2S 和 T2 Mi 7。两款手机都将采用来自高通的最新 SoC，[骁龙 845](https://www.xda-developers.com/qualcomm-snapdragon-845-hands-on-benchmarks-first-impressions/) ，预计将在即将到来的巴塞罗纳世界移动通信大会上或之后发布。然而，并不是每个人都喜欢购买昂贵的旗舰硬件，这就是为什么像小米这样的公司以各种价位提供许多不同的设备。小米的中档品牌之一是 Mi Max 系列，该系列以其[巨大的电池容量](https://www.xda-developers.com/xiaomi-launches-the-new-mi-max-2-in-india-for-%E2%82%B916999-265/)而闻名。我们相信小米今年将继续这一趋势，发布新的小米 Mi Max 3，我们已经独家获得了其固件文件。

* * *

## 小米 Mi Max 3 延续了这一趋势

早在 12 月，一个名为[*【CNMO】*](https://www.xda-developers.com/xiaomi-mi-max-3-rumors/)的中文博客报道称，Mi Max 3 将配备 5500 毫安时的超大电池。报道还称，该设备将采用 7 英寸 18:9 的显示屏，拥有双摄像头，并根据型号选择高通骁龙 630 或高通骁龙 660 SoC。

虽然我们无法确认任何有关显示器尺寸的信息，但我们获得的固件文件允许我们确认大多数其他信息，以及我们自己的一些新发现。

*以下信息基于 [@FunkyHuawei](https://twitter.com/FunkyHuawei) 获得的固件文件，他是 [FunkyHuawei.club](https://funkyhuawei.club/) 服务的幕后人，该服务允许用户付费[更新](https://funkyhuawei.club/models)、[解锁](https://www.reddit.com/r/FunkyHuawei/comments/7d5wsi/introducing_funkyhuawei_unbrick_flash_tool/)或[更名](https://www.reddit.com/r/FunkyHuawei/comments/7a5sab/introducing_funkyhuawei_rebrand_tool_rebrand_any/)华为和 Honor 手机。他只向 XDA 开发者提供对这些固件文件的访问。*

首先，我们将讨论最基本的规格。根据各种构建属性，我们正在寻找的设备将与[高通**骁龙 660** SoC](https://www.xda-developers.com/qualcomm-unveils-snapdragon-660-and-snapdragon-630-two-upper-mid-tier-socs/) 一起推出。可能会有 Snapdragon 630 的变体，但我们还没有看到那个。电池容量确实是**5500 mAh**，这应该会让任何对长续航设备感兴趣的人感到高兴。我们还可以确认它将有一个 **18:9** 显示屏，尽管我们不能确认显示分辨率。

然而，这款设备最有趣的是，它可能有无线充电功能。小米手机之前从未支持 Qi 无线充电，但小米[终于在去年年底加入了](https://www.androidauthority.com/xiaomis-next-flagship-might-feature-wireless-charging-802187/)无线电源联盟。小米 Mi 7 据称将成为第一款具有无线充电功能的小米设备，但我们[尚未找到任何直接证据证明这一点](https://www.xda-developers.com/xiaomi-mi-7-oled-panel-always-on-display/)。不过，小米 Mi Max 3 很可能会支持**无线充电**，因为我们在它的固件中找到了两个直接证据。

在 MIUI 键盘卫士 APK 中，我们发现了与无线充电相关的字符串。有一些字符串会告诉你充电是否已经停止，如果已经停止，是否是因为设备的位置偏离了充电器底座。

此外，我们发现了小米制作的帮助视频和图形，向用户展示了如何将他们的设备放在无线充电器上。图片中显示的手机可能不是 Mi Max 3 本人的样子，因为图片可能只是展示小米未来一系列具有无线充电功能的智能手机的通用设备。

接下来，由于一个配置文件，我们能够准确地找出设备将使用什么相机传感器。在背面，该设备将拥有索尼的 IMX363 或 S5K217+S5K5E8 三星双摄像头设置。正面会有一个孤零零的三星的 S5K4H7。然而，该设备的正面似乎可以通过另一个成像传感器来连接:虹膜扫描仪。

这里提到的前置辅助模块是 OmniVision 2281，根据其[官方页面](http://www.ovt.com/sensors/OV2281)，它“利用 PureCel 技术的 1.12 微米像素，为智能手机、平板电脑和笔记本电脑实现准确、可靠的**虹膜识别**”。该传感器似乎仍在为设备开发中，因为与它相关的行已被注释掉。我不知道该设备的最终型号是否会有虹膜扫描仪，但很明显这是在工程中。鉴于这款设备将支持无线充电，并将有一个后置指纹传感器，它有必要添加虹膜扫描，以便当手机放在桌子上时，你可以快速解锁手机。

关于软件，固件显示该设备运行的是 Android 8.1 Oreo。值得注意的是，构建属性中设置的第一个 API 级别是 25，这意味着该设备开始运行 Android 7.1 牛轧糖。这款设备可能会推出 Android 8.1，但也有可能我们正在寻找的固件是开发者 ROM，稳定版本将是旧版本的 Android。基本上，不要抱太大希望。

我们可以透露的其他次要方面是，该设备将有一个双 SIM 卡插槽，支持双 SD 卡，一个 IR blaster，用于通知的 LED 灯，由 Dirac 调谐的音频，高通的 aptX 和 aptX HD 蓝牙音频编解码器，但不幸的是没有 NFC。它还可能有双扬声器(尽管固件不是 100%清楚)，以及一个称为前置“remosic”传感器的东西。

如果我们了解更多关于小米 Max 3 的信息，我们将在 XDA 门户网站上为您提供最新消息。在那之前，请务必关注我们新的[专属标签](http://xda-developers.com/tag/exclusive)以获取更多类似的帖子！

* * *

### 更新:骁龙 636 对 660

我们注意到，Mi Max 3 可能采用骁龙 636 而不是 660，尽管固件说什么。这有两个原因:

*   骁龙 636 是一个降频 660。固件中列出的最高频率为 1.8GHz，低于 660 的最高频率 2.2GHz。
*   小米红米 Note 5 Pro 采用了骁龙 636 SoC，但在其固件文件中，它被列为骁龙 660。

最终，差异非常小，但为了准确起见，还是值得一提。