# 华为发布用于新冠肺炎联系人追踪的“联系人屏蔽”API

> 原文：<https://www.xda-developers.com/huawei-hms-core-contact-shield-api-covid-19-contact-tracing/>

随着世界上许多国家取消其留在家中的命令，公共卫生机构正在争先恐后地实施接触者追踪，以限制新冠肺炎的死灰复燃。过去几周出现了几个基于应用程序的接触者追踪解决方案，其中一些基于[谷歌和苹果的暴露通知 API](https://www.xda-developers.com/google-apple-contact-tracing-coronavirus/) ，现在公共卫生机构的开发者可以访问另一个新冠肺炎接触者追踪 API:华为的 Contact Shield API。

在 HMS Core 版本 4.1.0.301 的更新中，[华为对 Google Play 服务的替代选择](https://www.xda-developers.com/huawei-hms-core-android-alternative-google-play-services-gms/)，华为新的 Contact Shield APIs 被添加进来，“以提供基本功能来帮助最小化新冠肺炎的传播”

华为尚未正式宣布其新的 Contact Shield APIs，但华为的一位发言人向我们展示了华为开发者网站上的文档。根据 API 的[服务介绍页面](https://developer.huawei.com/consumer/en/doc/development/Contact-Shield-V1/introduction-0000001050738511-V1)，Contact Shield API“为华为设备用户提供隐私保护的联系人追踪服务”该 API“利用蓝牙低能耗(BLE)技术来检测附近的设备，与检测到的设备交换数据，并记录匿名的用户信息。”谷歌和苹果的曝光通知 API 也使用蓝牙进行联系人追踪。

另一页提供了华为新 API 的更多细节。该页面没有明确回答华为的 API 是否与谷歌和苹果的曝光通知 API 有关，但谷歌在 4 月份告诉媒体，该公司“打算发布一个框架，这些公司(如华为)可以用来复制谷歌和苹果开发的安全匿名跟踪系统。”华为的 Contact Shield FAQ 页面继续列出了其联系人跟踪 API 据称如何保护用户隐私的几个要点，所有这些都与谷歌和苹果的实施中概述的隐私指南措辞相似。

为了快速参考，以下是要点:

**华为联系人盾如何保护用户隐私？**

*   用户可以决定是否启用 Contact Shield，是否上传匿名标识符到云端，是否自行获取诊断结果。
*   使用匿名标识符不会记录或存储任何个人信息，如用户位置。这些标识符将仅存储 14 天。
*   用户卸载你的应用后，设备上存储的用户历史数据将被删除。用户也可以手动删除所有历史数据。
*   只有经过政府授权和华为严格考核的开发者才能使用 Contact Shield APIs 开发 app。
*   华为将与符合条件的开发者签署一份附加服务协议，说明用户隐私保护要求。

到目前为止，[只有少数国家](https://www.xda-developers.com/covid-19-contact-tracing-apps-india-aarogya-setu-open-source-sweden-italy-test-google-apple-exposure-notification-api/)将谷歌和苹果的曝光通知联系人追踪 API 应用到了他们的应用程序中。最新版本的 Google Play 服务包括 API，但在美国贸易禁令后[发布的几款华为和 Honor 品牌智能手机没有预装 Google Play 服务。在这些设备上，包括华为 Mate 30、华为 P40 和 Honor 30 系列，一旦公共卫生机构的开发人员实施华为新的 Contact Shield API，用户将能够参与新冠肺炎接触者追踪。](https://www.xda-developers.com/trump-extends-huawei-trade-ban-may-2021/)

*感谢 Discord 用户 SerjSev 的提示* *！*

## 更新 1:更多细节

华为发言人分享了一些关于新 Contact Shield API 的更多细节。据该发言人介绍，华为的 API 遵循国际开发的分散式隐私保护邻近追踪( [DP-3T](https://github.com/DP-3T/documents) )协议。据称，Contact Shield 可以与其他联系人追踪解决方案互操作，包括谷歌和苹果的曝光通知 API。正如常见问题中提到的那样，发言人告诉我们，只有公共卫生组织的开发者与华为签署协议，应用程序才能访问 API。此外，华为告诉我们，他们还将让开发者签署一份附加协议，要求遵守用户隐私保护规定。

该 API 包含在 HMS Core 版本 4.1 和更高版本中。运行旧 HMS 核心版本的用户将被提示更新到本月推出的最新版本。