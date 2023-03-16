# 谷歌要求为安卓系统提供数字福利和家长控制

> 原文：<https://www.xda-developers.com/google-digital-wellbeing-parental-controls-required-android/>

谷歌 I/O 2018 的最大主题之一是改善数字健康。随着消费者意识到他们在网上花费的时间太多，谷歌和其他科技公司推出了新的健康工具，以尽量减少我们使用智能手机和社交媒体的时间。为了帮助用户监控和控制他们的智能手机使用，谷歌创建了[数字健康](https://www.xda-developers.com/digital-wellbeing-google-pixel-xl-google-pixel-2-xl/)应用程序，用于当时最新的安卓版本 Android 9 Pie。最初，这款应用仅限于 Pixel 智能手机，但谷歌[慢慢开放了它在其他 Android 设备上的使用。现在，我们了解到谷歌要求其所有 Android 合作伙伴预装一个内置父母控制的数字福利解决方案。](https://www.xda-developers.com/tag/digitalwellbeing)

[谷歌的数字健康应用](https://play.google.com/store/apps/details?id=com.google.android.apps.wellbeing)提供了几个功能来帮助你控制智能手机的使用。首先，它的仪表盘可以让你监控你在手机上使用应用程序的时间(屏幕时间)，你打开每个应用程序的次数(打开次数)，以及你从每个应用程序收到的通知数(收到的通知数)。)仪表盘为每个选项提供了一个条形图，让您可以比较一周中每天的应用使用情况，从仪表盘中，您还可以设置应用计时器，以限制您每天对特定应用的使用。接下来，放松功能通过减少晚上使用手机的冲动来帮助你入睡；它通过在屏幕上应用灰度过滤器并在夜间启用勿扰模式来实现这一点。通过[对焦模式](https://www.xda-developers.com/focus-mode-digital-wellbeing/)，你可以暂时停止使用手机上的某些应用。最后， [Family Link integration](https://www.xda-developers.com/digital-wellbeing-integration-family-link-parental-controls/) 提供了对谷歌父母控制应用的便捷访问。

*运行 Android 10 的一加 7 Pro 上的数字福利*

在为 Pixel 智能手机有限发布几个月后，谷歌的数字福利应用程序开始适用于 HMD Global 的少数几款 Android One 智能手机。在今年的世界移动通信大会上，谷歌宣布将该应用扩展到 [Moto G7 系列](https://www.xda-developers.com/google-assistant-digital-wellbeing-google-lens-mwc/)。从那以后，我们已经看到这款应用在来自[华硕](https://www.xda-developers.com/asus-zenfone-max-pro-m1-digital-wellbeing-dark-mode-update/)、 [Realme](https://www.xda-developers.com/realme-3-pro-coloros-6-update-quick-settings-screen-on-counter-digital-wellbeing/) 、 [Razer](https://www.xda-developers.com/razer-phone-android-pie-update-plan/) 和其他公司的手机上推出。[小米的 MIUI](https://www.xda-developers.com/miui-10-beta-digital-wellbeing/) 和[华为的 EMUI](https://www.xda-developers.com/emui-9-review-features-apps-huawei-honor-android-pie/) 都有自己的数字健康解决方案，所以这两个品牌的智能手机都没有集成谷歌的健康应用。展望未来，所有预装谷歌应用和 services⁠—basically 的安卓设备每台在 China⁠—must 以外销售的安卓设备都自带数字健康解决方案和家长控制。由于原始设备制造商必须与谷歌签署许可协议才能使用 Android 品牌，而谷歌的应用程序基本上是在国际上销售设备的必需品，这一新要求实际上使数字福利和家长控制成为 Android 的一项要求。

我们获得了一份最新版本的谷歌 GMS 需求文档。该文档详细说明了 Android 智能手机和平板电脑必须满足的技术要求，以便原始设备制造商获得谷歌的批准，预载谷歌移动服务，谷歌的应用和服务套件，包括谷歌 Play 商店、谷歌 Play 服务等。我们的副本日期是 2019 年 9 月 3 日，也就是 Android 10 源代码公开的同一天。文件的第三部分被称为“布局”，它准确地概述了谷歌的应用程序必须如何在设备上实现；例如，谷歌的核心 GMS 应用程序(搜索、Chrome、Gmail、地图等。)必须放在默认主屏幕上名为“Google”的文件夹中。第 3.4 小节详细说明了每个谷歌应用程序的“应用程序特定要求”，第一部分讨论了原始设备制造商必须做些什么来满足谷歌对数字福利和家长控制的新要求。

总之，谷歌要求 2019 年 9 月 3 日之后推出的所有使用 Android 9 Pie 或 Android 10 的新设备都要附带一个健康应用程序和父母 controls⁠—either 谷歌的数字健康/家庭链接或定制解决方案。这一要求也延伸到 9 月 3 日之后升级到 Android 9 Pie 或 Android 10 的设备。因此，您不必再要求制造商在新设备或 Android 操作系统升级上添加健康解决方案。

大多数原始设备制造商将通过预装谷歌的数字福利和家庭链接应用来满足这一要求，但小米和华为等品牌可以继续使用他们的定制解决方案，只要他们满足某些要求。OEM 福利解决方案必须放在设置的顶层，有一个 onboarding 屏幕，让用户在为自己或孩子设置福利之间进行选择，并具有与谷歌解决方案相同的基本功能，包括仪表板、Wind Down 和应用程序计时器。不过，谷歌正在让 OEM 解决方案增加可选功能，如[网站定时器](https://www.xda-developers.com/android-q-google-chrome-digital-wellbeing/)和[聚焦模式](https://www.xda-developers.com/focus-mode-digital-wellbeing/)。有趣的是，“可选功能”列表提到了“屏幕时间目标”，这个功能[还没有添加到谷歌的数字健康应用](https://www.xda-developers.com/digital-wellbeing-screen-time-goal/)中。

我很高兴谷歌要求所有 GMS 认证设备都必须具备数字健康和家长控制功能。对于许多用户来说，仅靠意志力控制智能手机的使用很容易，但对一些人来说，像这样的工具肯定会有所帮助，尤其是在处理儿童问题时。谷歌在发布时将该应用程序限制在 Pixel 智能手机上是没有意义的，但至少他们在一年后让它广泛可用。

我们从多个来源证实了这份文件的真实性，但我们还是联系了谷歌进行确认，如果有回音，我们会更新这篇文章。