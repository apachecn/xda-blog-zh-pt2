# Firebase 在 ML 工具包和 web 应用程序性能监控中增加了 3 项新功能

> 原文：<https://www.xda-developers.com/firebase-3-new-capabilities-ml-kit-performance-monitoring-web-apps/>

谷歌的移动开发平台 Firebase 在谷歌年度开发者大会 Google I/O 上获得了今年最大的更新。今天，谷歌宣布了他们改善开发者机器学习可访问性的新方法；谷歌还在扩展其性能监控工具，以帮助网络开发者加快他们的网络应用程序。

谷歌在去年的 I/O 上宣布了 ML Kit [，为开发者揭开机器学习的神秘面纱。他们从几个最常见用例的 API 开始，今年他们扩展了 SDK，增加了 3 个新的 API:一个用于翻译的设备上 API，一个用于对象检测和跟踪的 API，以及一个用于轻松创建定制 ML 模型的 API。本地应用程序开发人员可以将性能监控 SDK 集成到他们的应用程序中，以收集性能数据，然后在 Firebase 性能监控中进行分析；很快，web 开发人员也将能够在 Firebase 中跟踪他们的 web 应用程序的性能。我与 Firebase 的产品负责人 Francis Ma 进行了交谈，以了解更多关于这些变化的信息。](https://www.xda-developers.com/google-ml-kit-machine-learning/)

## 新 ML 试剂盒 API

谷歌的 ML SDK 目前支持 7 个 API:文本识别、人脸检测、条形码扫描、图像标注、地标识别、智能回复、语言识别。最近的两个是最近在四月增加的[，但是现在他们将被前面提到的三个 API 加入。下面是 3 个面向开发人员的新 ML APIs 的概要:](https://www.xda-developers.com/google-ml-kit-sdk-adds-smart-reply-language-identification-api/)

*   [](https://firebase.google.com/docs/ml-kit/translation)**用于翻译的设备上 API:使用支持谷歌翻译应用程序离线翻译的相同模型，这一新 API 允许开发人员在 58 种语言之间提供快速、动态的翻译。**
***   [**对象检测和跟踪 API**](https://firebase.google.com/docs/ml-kit/object-detection) :这个 API 让一个应用程序定位和跟踪一个直播镜头中最突出的对象，用一个方框围绕它。然后，开发人员可以通过查询云视觉搜索 API 来识别最突出的对象。举例来说，据说宜家正在试验这种用于视觉家具购物的 API。*   [**AutoML Vision Edge**](https://firebase.google.com/docs/ml-kit/automl-vision-edge) :对于希望以最少的专业知识定制 ML 模型的开发人员来说，AutoML Vision Edge 允许您构建和训练自己的定制模型，以便在用户的设备上本地运行。要训练一个模型，只需[将他们的数据库](https://github.com/firebase/mlkit-custom-image-classifier)(例如一组图像)上传到 Firebase 控制台，然后点击“训练模型”，根据数据库训练一个 TensorFlow Lite 模型。谷歌宣布，一家名为 Fishbrain 的公司使用这个 API 训练一个模型来识别一条鱼的品种，而另一家公司则称之为 Lose It！训练一个模型来识别图像中的食物类别。**

 **机器学习是计算机科学中一个快速发展的领域，所以开发者对它表现出兴趣是很自然的。然而，在没有数据科学家的情况下，有效地建立和训练 ML 模型可能会很困难，这就是为什么 Google 通过使用 ML Kit 自动训练模型来简化过程。开发人员可以利用 ML 的力量专注于构建具有强大功能的新应用，而不必投入大量时间和精力来学习数据科学。随着 ML 工具包中这 3 个新 API 的加入，我们将有望在 Google Play 中看到许多新的有用的应用程序。

## 面向 Web 开发人员的 Firebase 性能监控

消费者要求他们使用的应用程序和网站具有良好的性能，但 Firebase 迄今为止只为原生应用程序开发者提供了有效监控其产品性能的方法。在 Google I/O 2019 上，谷歌宣布将为使用 [Firebase 托管](https://www.xda-developers.com/firebase-in-app-messaging-bigquery-jira-integration/)的 web 开发者提供 Firebase 性能监控。Web 开发者可以通过提高 web 应用程序的速度来让用户参与到他们的平台中；为了帮助网站开发者发现网站性能的关键弱点，Firebase 将提供以网络为中心的工具和遥测测量，以显示真实世界的用户如何体验网站。例如，web 开发人员将能够监控一些方面，如首次绘画的时间和输入延迟，人们首次看到网页上的内容并与之交互的时间，以及平均延迟。概览仪表板将显示这些和其他指标，以帮助 web 开发人员优化他们的用户体验，无论是按国家还是全球。

## 其他公告

### 更新了 Google Analytics for Firebase 中的受众生成器

建立目标受众对于最大化用户参与度至关重要。你要确保你把你的用户划分到正确的类别，这样你就知道如何最好地为他们提供个性化的激励和鼓励，这样他们就更有可能继续使用你的应用或服务。[Google Analytics for Firebase](https://firebase.google.com/products/analytics/)帮助开发者更好地了解他们的用户，其[更新的受众生成器](https://support.google.com/firebase/answer/6317509)将通过[远程配置](https://www.xda-developers.com/why-and-how-to-use-googles-firebase-suite-what-its-tools-can-do-for-you/)或通过[应用内消息](https://www.xda-developers.com/firebase-in-app-messaging-bigquery-jira-integration/)重新参与来轻松创建新的受众。更新后的受众构建器功能包括“序列、范围、时间窗口、[和]成员资格期限”等功能例如，谷歌表示，现在可以为兑换优惠券代码并在优惠券兑换后 20 分钟内购买产品的用户创造受众。

## ![](img/a327af04bbf8af89c7527f9ff6a4d6a4.png)

*   Cloud Firestore 是一个完全托管的 NoSQL 数据库，支持[集合组查询](https://firebase.google.com/docs/firestore/query-data/queries#collection-group-query)，这允许你的应用程序“搜索所有同名集合中的字段，不管它们在数据库中的什么位置。”例如，集合组查询将允许具有由艺术家及其歌曲组成的数据结构的音乐应用跨艺术家查询歌曲中的字段，而不考虑艺术家。
*   新的[云函数模拟器](https://firebase.google.com/docs/functions/local-emulator)将让开发者加快本地应用的开发和测试；它与云 Firestore 模拟器通信。
*   如果你需要在你的应用中调试崩溃，那么 Firebase Crashlytics 可以帮助你诊断任何稳定性问题。velocity 警报会告诉您某个特定问题的严重性突然增加，值得研究，但其警报阈值直到现在都无法定制。

想要了解更多关于 Firebase 的新闻，请继续关注官方博客或者加入 [Alpha](https://services.google.com/fb/forms/firebasealphaprogram/) 计划来预览即将到来的特性。**