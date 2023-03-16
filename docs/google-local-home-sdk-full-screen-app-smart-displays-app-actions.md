# 【更新 2:出预览版】谷歌宣布本地 home SDK，对智能显示器的全屏应用支持，以及应用动作的第三方可用性

> 原文：<https://www.xda-developers.com/google-local-home-sdk-full-screen-app-smart-displays-app-actions/>

**更新 2(美国东部时间 4/6/20 @下午 2:25):**谷歌本地 Home SDK 达到 1.0 版本，退出开发者预览版。

**更新 1(美国东部时间 7/9/19 @下午 2:25):**谷歌今天推出本地 Home SDK 开发者预览版。

Google I/O 即将结束，但仍有一些公告没有引起注意。毕竟，会议期间有太多的演讲和活动，很难全部跟上。一个被忽视的领域是谷歌上的行动。在 Google I/O 2019 上，该公司宣布了新的本地家庭 SDK，对智能显示器的全屏应用支持，以及第三方访问应用操作。

对于那些可能不熟悉 Google 上的操作的人来说，这基本上是 Google Assistant 集成的开发者方面。它允许开发者创建我们每天使用的令人敬畏的 Assistant 集成，谷歌一直在扩展功能。该平台正在为网络、移动和智能家居提供新的工具。让我们来看看这一切意味着什么。

## 本地家庭 SDK

智能家居集成是谷歌助手的重要组成部分，谷歌表示，现在有超过 3 万种兼容的联网设备。本地家庭软件开发套件(Local Home SDK)向更好地集成智能设备迈出了一步。

Local Home SDK 允许智能家居代码在 Google Home 扬声器和 Nest 显示器上本地运行，然后这些扬声器和显示器可以使用它们的无线电与智能设备进行本地通信。这加快了命令的速度，并通过减少云调用的数量使它们更加可靠。

Local Home SDK 还改善了智能设备的设置体验。谷歌去年已经开始与通用电气合作，你可以直接从谷歌主页应用程序设置他们的灯。对于用户来说，这是一个更加容易和无缝的体验。谷歌已经开始与包括飞利浦、Wemo 和 LIFX 在内的合作伙伴合作开发这个 SDK。

## 全屏应用程序

智能显示器正在成为谷歌助手硬件生态系统中更大的一部分。在今年的 I/O 大会上，谷歌[推出了带有 10 英寸大显示屏的 Nest Hub Max](https://www.xda-developers.com/google-nest-hub-max-officially-announced/) 。谷歌让开发者通过预览“交互式画布”来充分利用这些展示。这允许应用程序使用全屏进行语音、视觉和触摸，但这不仅限于智能显示器。它也可以在 Android 手机上工作。互动画布目前可用于游戏(如 HQ 大学)，但很快谷歌将增加更多类别。

## 更多应用操作

最后，我们来谈谈[应用动作](https://developers.google.com/actions/appactions/overview)的新特性。在去年的谷歌 I/O(T3)上，[宣布了应用程序的动作，但是到目前为止还很有限。现在谷歌正在向更多的应用开放。应用程序动作允许开发者使用从助手到应用程序特定部分的深度链接。本质上是一个语音启动的快捷方式，但功能更强大。](https://developers.google.com/actions/appactions/overview)

谷歌宣布了针对这些意向的四个新类别:健康和健身、金融和银行、拼车和订餐。新用途的一个例子是在健身应用程序中开始锻炼。你可以说“嘿，谷歌，在耐克跑步俱乐部开始我的跑步”，应用程序将打开并开始跟踪你的跑步。无需找到应用程序并手动开始锻炼。

他们说开发人员添加这些集成非常容易。显然，添加了 Actions.xml 文件后，Nike Run Club 特性在不到一天的时间内就实现了。在上面的例子中，Assistant 直接进入了应用程序，但它也可以在 Assistant 对话中显示卡片(切片)。

这些工具将允许开发人员使用谷歌助手做更多的事情，这对消费者来说非常好。家庭只会变得越来越智能，显示器只会变得越来越普遍，用户将依赖语音助手来完成任务，现在更是如此。查看 [Actions 网站](https://developers.google.com/actions/)了解更多关于使用这些工具构建应用的信息。

**来源:[谷歌](https://developers.googleblog.com/2019/05/Actions-on-Google-at-IO-2019.html)**

* * *

## 更新 1:开发者预览版

在 5 月份谷歌 I/O 大会上宣布了本地家庭软件开发工具包之后，该公司现在正在开发者预览版中推出该软件开发工具包。谷歌一直在与合作伙伴一起测试该平台，他们准备引入更多内容。正如在 I/O 期间提到的，SDK 将允许开发人员将其智能设备深度集成到 Assistant 中。Google 已经发布了 API 参考、开发者指南和示例来帮助人们开始使用。测试期间的反馈可以通过 [bug tracker](https://issuetracker.google.com/issues/new?component=655104&template=1284327) 和 [/r/GoogleAssistantDev](https://www.reddit.com/r/GoogleAssistantDev) 提交。

**来源:[谷歌](https://developers.googleblog.com/2019/07/developer-preview-of-local-home-sdk.html)**

* * *

## 更新 2:超出预览

谷歌的本地 Home SDK 于去年 7 月进入开发者预览版，现在它已经准备好进入黄金时间了。本地 Home SDK 已经离开了开发者预览阶段，现在在 1.0 版本中可以通过动作控制台获得。

该版本增加了许多新功能。开发人员可以将本地实现添加到智能家居操作中，通过本地网络而不是云将命令路由到设备。这减少了延迟并提高了可靠性。SDK 可以通过 mDNS、UDP 或 UPnP 协议在 Wi-Fi 上发现本地设备。然后，应用程序可以使用 TCP、UDP 或 HTTP 发送命令。

谷歌还改进了动作控制台中的扫描配置。开发人员可以输入多个扫描配置，这允许本地实现应用程序处理可能使用不同发现协议的多个设备。最后，SDK 配置页面现在接受上传本地履行应用程序的 JavaScript 文件。

**来源:[谷歌](https://developers.googleblog.com/2020/04/local-home-sdk-ready-for-actions.html)**