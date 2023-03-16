# 应用分发、扩展和 Web 应用分析即将成为 Firebase

> 原文：<https://www.xda-developers.com/firebase-app-distribution-extensions-analytics-web-apps/>

如果你是一名 Android 应用程序开发人员，那么你可能已经在使用谷歌的移动开发套件 Firebase。除非你计划在 Google Play 之外发布你的应用[，否则实现 Firebase 提供的一个或多个工具没有坏处(当然，这取决于你能负担多少)。)通过 Firebase，您可以实施 Google Analytics 来洞察应用使用情况和用户参与度，通过远程配置执行 A/B 测试，通过云消息传递的定向消息提高用户保留率，通过 Crashlytics 跟踪崩溃，通过托管托管网站，以及](https://www.xda-developers.com/appgallery-huawei-alternative-google-play-store-android/)[等等](https://www.xda-developers.com/tag/firebase/)。每月有超过 200 万个活跃应用程序使用 Firebase，谷歌希望让这个平台对 Android 应用程序开发者更加有用，所以他们继续扩展 Firebase 的功能集。

今天，谷歌公布了移动开发平台的几个新功能。该公告的亮点包括扩展、应用分发和谷歌分析对网络应用的支持，但还有其他重要公告需要注意。这些声明是在今天于西班牙举行的谷歌 Firebase 峰会上宣布的。我们采访了 Firebase 的两位产品经理弗朗西斯·马(Francis Ma)和克里斯汀·约翰逊(Kristen Johnson)，为您带来一份公告摘要，以防您无法参加活动或无法观看[的直播](https://www.youtube.com/watch?v=k5qJ6F_g5f0)。

## Firebase 扩展

减少编写样板代码的时间是新扩展特性背后的主要思想。“扩展”正是它在这里的发音；想想 Chrome 扩展，它为谷歌 Chrome 浏览器增加了功能，但不是为任何使用谷歌云的无服务器产品(如云功能)的项目。Firebase Extensions 是预打包的代码包，可以处理诸如调整缩略图大小、翻译字符串、将人员添加到电子邮件列表、缩短 URL 等任务。在发布时，将有 9 个扩展可供所有开发者使用——全部由 Google 发布。

谷歌表示，他们所做的扩展解决了常青树的问题(即开发人员经常会遇到的问题)，但是如果需要的话，他们会更新扩展。这些扩展是开源的，并与其他谷歌云平台和 Firebase 产品集成，你可以通过在[扩展目录页面](https://firebase.google.com/products/mods/)或 [Firebase 扩展 GitHub repo](https://github.com/firebase/extensions) 上寻找它们来开始。

## 应用分发

在 Google Play 或 Apple App Store 上发布应用程序之前，你肯定会希望将你的应用程序分发给一组可信的测试人员。这样做的公司是“吃他们自己的狗粮”，或“狗粮”，他们的应用程序。虽然您可以使用 Google Play 为您的组织托管一个私人应用程序，但如果您的应用程序是跨平台的，您也必须为苹果应用程序商店做同样的事情。不过，使用 Firebase 应用程序分发，您可以管理 Android 和 iOS 应用程序预发布版本的分发。您可以管理多个测试组，发送邀请链接，上传新发行版的应用程序，并从仪表板添加发行说明。App Distribution 甚至为 Gradle for building、浪子 for automation 和 Firebase CLI for deployment 提供了 CLI 支持。

谷歌表示，在 2019 年 I/O 首次发布 alpha 版本后，应用程序分发正在升级为公共测试版。这里可以开始[。随着应用程序的发布，谷歌现在提供了](http://firebase.google.com/products/appdistribution)[过渡 Fabric 用户](https://www.xda-developers.com/google-ending-fabric-developers-firebase/)正在寻找的所有功能。面料将于 2020 年 3 月 31 日日落。

## 扩展 Web 应用的分析

正如我前面提到的，Firebase 的一个主要特性是分析。使用谷歌分析，你可以跟踪用户如何参与你的应用程序，这样你就可以优化用户体验，以增加保留。原生移动应用程序可以使用分析已经有一段时间了，但现在谷歌将允许开发者将分析与网络应用程序集成在一起。网络开发者将能够记录事件和用户属性，这在手机上已经成为可能。开发者也将能够执行封闭的漏斗分析，找出用户在他们的网络应用中采取的导致转化的路径。

通过 Firebase 托管的网站的分析扩展将为开发者提供一个关于其业务的整体视图，无论平台如何。现在，开发人员可以在 Analytics 中创建一个受众，然后使用远程配置或 Firebase 云消息传递锁定该受众。

## 仿真器套件、更新的预测 UI、开源 SDK 等等

概括地说，Firebase 峰会上将要发布的其他一些公告包括:

*   实时数据库触发功能，对客户端和服务器端 SDK 的更广泛支持，针对安全规则更改的热重新加载，以及一个用于收紧 Firebase Emulator Suite 的持续集成(CI)的新命令。点击了解更多[。](https://firebase.google.com/docs/emulator-suite)
*   Firebase 预测用户界面现在向您显示“用户预测行为的全部范围”,因此您可以更好地针对您的用户群。点击了解更多[。](https://firebase.google.com/docs/predictions)
*   用于远程配置和分析的 Web SDK 版本是开源的。谷歌已经测试了转化酶的 [React Native Firebase](https://invertase.io/oss/react-native-firebase) 模块，以确保它们适用于所有 Firebase 产品；新的 v6 版本支持所有 Firebase 服务，并提供了一个包含文档、快速入门指南和升级 SDK 的新网站。
*   谷歌云平台的身份和访问管理[现在已经普遍可用](http://www.firebase.google.com/docs/projects/iam/overview)。这将帮助您创建角色来限制对项目的访问。
*   您现在可以将图像添加到通过 Firebase Cloud Messaging 发送的通知中。
*   [测试分片](https://firebase.gooogle.com/docs/test-lab/android/instrumentation-test#sharding)通过将测试分成子组并并行运行来加速 [Firebase 测试实验室](https://firebase.google.com/products/test-lab/)中的测试。
*   谷歌正在继续投资项目，以培育开发者生态系统。除了谷歌开发人员团体和女性技术人员之外，谷歌现在还在 google.dev 上推出了一个学习门户。该学习门户将于下周开放，将提供自学材料和教程，专门用于提高您对使用谷歌云平台和 Firebase 等谷歌开发人员工具的理解。

如果你有兴趣观看直播，你可以在 YouTube 上观看。

* * *

本文中的所有图片均由谷歌提供。