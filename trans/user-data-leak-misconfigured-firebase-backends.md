# 数百万用户的数据通过错误配置的 Firebase 后端泄露

> 原文：<https://www.xda-developers.com/user-data-leak-misconfigured-firebase-backends/>

根据来自 *Appthority* 的一份报告，由于错误配置的 [Firebase](https://www.xda-developers.com/google-ml-kit-machine-learning/) 后端，数百万用户的数据被泄露。由于配置不当，超过 2，271 个数据库中大约 113GB 的数据暴露在公众面前。Firebase 是谷歌提供的后端即服务产品，据报道，它是 2017 年[增长最快的 SDK](https://www.xda-developers.com/firebase-mightysignal-report-sdks/) 。这项服务在顶级安卓开发者中非常受欢迎。它提供了云消息、推送通知、数据库、分析、广告以及开发者可以利用的更多内容，所有这些都由谷歌的高性能服务器提供支持。但是，似乎很多开发者都在误用它。

根据该报告，从 2018 年 1 月开始，研究人员扫描了利用 Firebase 作为后端功能的移动应用程序。在扫描了 270 多万个 iOS 和 Android 应用程序后，他们发现其中约有 2.8 万个应用程序使用了 Firebase。在这些应用程序中，约有 3000 个在公开可见的数据库中泄露数据，可以通过监控应用程序与服务器的通信来发现这些数据。更重要的是，这 3000 个应用程序的总下载量超过了 6.2 亿，这表明一些非常高调的应用程序也可能是罪犯。泄露的数据类型如下。

*   260 万个明文密码和用户 id
*   400 多万条 PHI(受保护的健康信息)记录(聊天消息和处方详情)
*   2500 万条 GPS 定位记录
*   包括银行、支付和比特币交易在内的 5 万条财务记录
*   450 多万个脸书、LinkedIn、Firebase 和企业数据存储用户令牌

目前，没有办法知道你的数据是否也被泄露了，但假设最坏的情况总是最安全的，所以你应该采取相应的行动。Appthority 声称，他们在发布报告之前通知了谷歌，提供了受影响应用程序的列表以及公共数据库的链接。

我们只能希望应用程序列表会在晚些时候发布，因为目前用户对他们的信息是否公开一无所知。虽然可能是可信的，但谷歌和研究人员的眼睛会看到这些数据。在我们找到更多信息之前，我们建议您更改密码以防万一。

* * *

[**来源:Appthority**](http://info.appthority.com/-q2-2018-mtr-download-Firebase-vulnerability)

[**Via:哔哔声电脑**](https://www.bleepingcomputer.com/news/security/thousands-of-apps-leak-sensitive-data-via-misconfigured-firebase-backends/)