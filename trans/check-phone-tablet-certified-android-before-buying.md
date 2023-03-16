# 如何在购买前检查手机或平板电脑是否经过 Android 认证

> 原文：<https://www.xda-developers.com/check-phone-tablet-certified-android-before-buying/>

所以你想买一部安卓智能手机或者平板电脑。有这么多的设备在那里，它可以是一个真正的头痛试图决定买什么。如果你负担得起，你可以花数百美元购买旗舰设备，如三星 Galaxy S9 T1、T2 华为 P20 Pro T3 或 T4 索尼 Xperia XZ2 Premium T5。你也可以选择中端设备，如[小米红米 Note 5 Pro](https://www.xda-developers.com/xiaomi-redmi-note-5-redmi-note-5-pro-hands-on/) 、 [Honor 9 Lite](https://www.xda-developers.com/honor-9-lite-western-europe/) 或[摩托罗拉 Moto X4](https://www.xda-developers.com/motorola-moto-x4-android-one-project-fi/) 。像[诺基亚 1](https://www.xda-developers.com/nokia-8-sirocco-nokia-7-plus-nokia-6-nokia-1-8110-reloaded/) 或[中兴 Tempo Go](https://www.xda-developers.com/zte-announces-blade-v9-blade-v9-vita-tempo-go/) 这样的廉价手机也是选择。尽管规格、功能和定价大相径庭，但所有这些设备都有一些共同点:它们由主要的 Android OEMs 厂商制造，并且是经过认证的 Android 设备，因此它们可以支持谷歌 Play 商店。

如果你想省钱，并为自己、亲戚或朋友购买/推荐一部智能手机或平板电脑，那么你可能会寻找一部不太知名的制造商生产的安卓智能手机或平板电脑。网上零售商充斥着这类设备，其中许多来自你从未听说过的中国品牌。购买这些设备中的一个没有错，但你必须小心你买的东西，因为它们可能不是谷歌认证的 Android 设备。这一点很重要，因为没有这一认证，设备可能无法与[谷歌 Play 商店](https://www.xda-developers.com/tag/play-store/)或任何其他谷歌应用程序正常工作，如 [Gmail](https://www.xda-developers.com/tag/gmail/) 、[谷歌地图](https://www.xda-developers.com/tag/google-maps/)、[谷歌照片](https://www.xda-developers.com/tag/google-photos/)、[谷歌播放音乐](https://www.xda-developers.com/tag/google-play-music/)等等。

在 Android 的大部分历史中，任何没有预装谷歌 Play 商店和其他谷歌应用的设备都可以简单地从外部资源下载应用。一种流行的方法是启动设备并刷新一个 [Google Apps](https://www.xda-developers.com/open-gapps-now-supports-android-8-1-oreo-arm-arm64/) 包(缩写为“GApps”)。有时候，当你可以直接下载并安装应用程序时，你甚至不需要这样做，就像在[许多亚马逊 Fire 设备](https://forum.xda-developers.com/amazon-fire/general/how-to-install-google-play-store-fire-t3486603)上一样。某些 OEM 厂商，如魅族，甚至预装了一个应用程序，指导你在购买设备后安装 Play Store 和其他谷歌应用程序。

这些伎俩已经运作了很长时间，以至于谷歌似乎并不关心自己的[谷歌移动服务](https://www.android.com/gms/) (GMS)项目，如果制造商想要预装所有重要的谷歌应用和服务，就必须注册该项目。作为 GMS 认证流程的一部分，设备必须遵循特定 Android 版本的[兼容性定义文件](https://source.android.com/compatibility/cdd) (CDD)中列出的要求，通过[兼容性测试套件](https://source.android.com/compatibility/cts/) (CTS)。这一点很重要，因为 Android 操作系统的开源性质:由于任何制造商都可以将 Android 安装到智能手机或平板电脑上，谷歌确保 Android 设备某种程度一致性的唯一方法是让制造商注册 GMS，以便他们可以预装 Play Store、Gmail、地图等。

为了执行 GMS 的规定，谷歌最近[开始阻止任何未经 GMS 认证的 Android 设备](https://www.xda-developers.com/google-blocks-gapps-uncertified-devices-custom-rom-whitelist/)访问 GApps。这可以通过[手动注册一个白名单](https://www.xda-developers.com/how-to-fix-device-not-certified-by-google-error/)来规避，虽然这对于一个精通技术的 Android 爱好者来说并不难做到，但我不会建议朋友或亲戚这么做。相反，在购买之前，我想知道这个设备是否是[认证的安卓](https://www.android.com/certified/) *。*

去年年初，谷歌 Play 商店开始在设置页面显示设备的认证状态。这是最常推荐的检查认证 Android 状态的方法，但显然需要你已经拥有该设备，并且已经能够访问 Play Store。从本质上说，如果你在购买新设备，这是一个无用的方法来检查认证。

 <picture>![GApps Play Store Uncertified](img/605daa0831f5286c379a47055821a04f.png)</picture> 

Message in Settings page of the Google Play Store if device is uncertified.

但是有一个鲜为人知的由谷歌维护的网页，上面有一个允许访问谷歌 Play 商店的所有认证安卓设备的列表。我们谈论的是“ **Google Play 支持的设备**”页面，该页面没有链接到谷歌认证的 Android 或谷歌移动服务页面的任何地方。事实上，它甚至没有链接到告诉你“未经认证的 Android 设备”是什么意思的页面上！以下是如何访问该页面以查看您的设备是否在列表中。

* * *

## 如何检查手机或平板电脑是否通过安卓认证

1.  点击进入[该网页。](https://support.google.com/googleplay/answer/1727131?hl=en)
2.  在“支持设备的完整列表”下，点击“**PDF 格式查看**”或“**CSV 格式查看**”
3.  这将下载经认证可访问 Play Store 的全部**大型设备列表**。
4.  在您最喜欢的文档阅读器中打开 PDF 文件或 CSV 文件(后者可以导入任何电子表格应用程序，如 Microsoft Excel、Google Sheets、LibreOffice Calc 等。)
5.  通过按 Ctrl+F (Windows、Linux、Chrome OS)或 Command+F (MacOS)并输入设备的市场名称或代号(如果您知道的话)来找到您的设备。
6.  如果您的设备在列表中，那么它是一个认证的 Android 设备，应该可以使用 Play Store！请注意，此列表将包含您拥有的设备的所有变体，因此您的特定设备变体可能没有列出。请务必比较并查看“型号”栏，以确保您的特定变体受到支持！

这个列表由谷歌不断更新，非常全面。新设备发布后可能需要几天时间才会出现在这里，但一般来说，在设备上市销售时，您应该能够找到您的设备。如果它不在这个列表中，那么这意味着你的设备将属于“未经认证的设备”类别，如果你想访问 Gmail 或 Google Play Music 等谷歌应用和服务，你需要[遵循本教程](https://www.xda-developers.com/how-to-fix-device-not-certified-by-google-error/)。