# 新冠肺炎联系人追踪应用程序:印度的 Aarogya Setu 开源，而瑞士和意大利测试谷歌/苹果的曝光通知 API

> 原文：<https://www.xda-developers.com/covid-19-contact-tracing-apps-india-aarogya-setu-open-source-sweden-italy-test-google-apple-exposure-notification-api/>

这种新型冠状病毒，也被称为新型冠状病毒，已经在世界各地肆虐。一些国家已经成功地控制了病毒的传播，但是其他许多国家还在努力控制它。正在测试的遏制策略之一是接触追踪。追踪最近与新冠肺炎病毒检测呈阳性的人有过接触的所有人，然后采取措施隔离这些人。接触者追踪是一项至关重要的任务，因为它影响到个人的隐私和自由，有利于公众健康。对个人隐私的威胁足够大，以至于谷歌和苹果走到一起，合作开发联系人跟踪 API 和蓝牙规范，旨在对用户隐私和安全产生最小影响。虽然这些努力值得称赞，一些国家也采纳了这些措施，但相当多的国家也在着手制定自己的类似解决方案。在这篇文章中，我们试图列出一些联系追踪解决方案，重点是那些开放源代码并向公众提供检查和反馈的解决方案。

## 独立解决方案

### 奥地利—斯托普科罗纳

奥地利政府采用了与奥地利红十字会联合开发的 [Stopp Corona](https://play.google.com/store/apps/details?id=at.roteskreuz.stopcorona) 应用程序。这个应用**不**依赖谷歌和苹果的曝光通知 API。由于该应用程序使用蓝牙，因此没有位置跟踪功能。该应用程序会监控用户身边的手机。如果一个用户怀疑感染了新冠肺炎病毒，或者已经被确诊感染了该病毒，那么他的邻近信息就会被上传到一个据称是分散的数据库中。警报会发送给所有有接近历史记录的用户。据报道，不会收集任何个人信息，如果用户想退出跟踪，他们可以简单地删除应用程序和数据。为了让你更安心，这个应用也是开源的。

**[在 GitHub 上的斯托普电晕源代码](https://github.com/austrianredcross/stopp-corona-android)**

* * *

### 澳大利亚— COVIDSafe

澳大利亚已经采用了 [COVIDSafe](https://play.google.com/store/apps/details?id=au.gov.health.covidsafe) 应用程序。这个应用**不**依赖谷歌和苹果的曝光通知 API。安装后，用户需要注册他们的名字/化名、年龄范围、邮政编码和电话号码，所有这些都被加密存储在政府服务器上。该应用程序依靠蓝牙进行近距离跟踪，交换匿名 id，每两个小时更换一次。这些 id 被加密存储在手机上，并在 21 天后被删除。当有人新冠肺炎病毒检测呈阳性时，他们会从卫生官员那里收到一个独特的代码，然后上传过去 21 天的匿名 ID 列表。该应用程序也是开源的，因此保持了透明度。

**[GitHub 上的 COVIDSafe 源代码](https://github.com/AU-COVIDSafe/mobile-android)**

* * *

### 捷克共和国——eRouska

捷克共和国已经采用了 eRouska 应用程序。这个应用**不**依赖谷歌和苹果的曝光通知 API。与其他仅支持蓝牙的实现类似，eRouska 会扫描附近的其他 eRouska 应用程序用户，并将遇到的数据保存在本地设备上。当用户测试呈阳性时，卫生官员会联系用户，并在双方同意的情况下上传遭遇数据。广播的设备 ID 每小时都会改变，扫描也可以手动打开和关闭。用户可以选择删除他们收集的所有数据，包括电话号码。这款应用也是开源的。

**[GitHub 上的 eRouska 源代码](https://github.com/covid19cz/erouska-android)**

* * *

### 印度-阿罗哈州

印度政府决定不采用谷歌和苹果的解决方案，而是以 T2 Aarogya Setu 应用程序的形式开发自己的解决方案。一旦用户在应用程序上设置了帐户，应用程序就会要求继续蓝牙访问和位置数据。用户还需要提供姓名、年龄、性别、健康状况等信息来建立用户档案。提出了一种自我评估测试，在该测试中，询问用户他们是否表现出任何新冠肺炎症状以及其他问题。当两部装有 Aarogya Setu 应用程序的智能手机相互靠近时，该应用程序会收集信息。如果其中一名接触者测试呈阳性，该应用程序将提醒另一个人，并提供帮助自我隔离的说明。

这个 Aarogya Setu 应用程序的使用首先受到政府的大力鼓励，然后在一些情况下被强制执行。然而，印度对公民隐私的态度并不是最好的，因为该国缺乏监管此类使用案例的关键法律。由于该应用程序收集位置数据并与政府分享数据，这种方法被许多人认为是过度和不必要的，它因对用户隐私的过度侵犯而受到关注，并且在这个过程中没有透明度和问责制。随之而来的是对这些方法的批评。

在这方面有一些好消息，Android 的 Aarogya Setu 应用程序已经开源。Android 应用的源代码现在可以在 GitHub 上获得。有关当局承诺，iOS 版和 KaiOS 版应用程序的源代码也将“在适当的时候”[开源。该应用的隐私政策也被](https://www.medianama.com/2020/05/223-aarogya-setu-code-open-sourced/)[更新，允许对应用](https://www.medianama.com/2020/05/223-aarogya-setu-privacy-policy-terms-of-service-update/)进行逆向工程，并向政府报告漏洞。此外，还有一个 [bug 奖励计划](https://twitter.com/SetuAarogya/status/1265353503221772288)，邀请开发者识别漏洞、bug 和代码改进。

**GitHub 上的 Aarogya Setu 源代码**

所有这些都绝对是好消息，因为缺乏透明度是相当惊人的。关于不透明的后端基础设施和服务器端代码仍有疑问，但[报道暗示](https://www.medianama.com/2020/05/223-aarogya-setu-code-open-sourced/)这也将在下周开源。

* * *

### 新加坡—基于 BlueTrace 协议的 TraceTogether

新加坡的实现采用了 [TraceTogether](https://play.google.com/store/apps/details?id=sg.gov.tech.bluetrace) 的形式，这也是**而不是**依赖于谷歌和苹果的暴露通知 API，但也是仅支持蓝牙而不是基于位置的。该应用程序只需一个手机号码即可启动，不会收集其他个人信息。该号码构成了用户 ID 的一部分，然后用于生成临时 ID。这些临时 id 上的邻近信息以 21 天为周期存储在设备上。当用户测试结果为阳性时，数据被中继到服务器。此外，TraceTogether 的功能将在疫情事件平息后暂停。

虽然 TraceTogether 本身并不是开源的，但是已经以 OpenTrace 的形式发布了一个通用的代码库。这个通用代码库包括一个 Android 应用程序、一个 iOS 应用程序和一个围绕 Google Firebase 构建的中央服务器的参考实现。同时发布的还有构成 TraceTogether 和 OpenTrace 基础的 BlueTrace 协议。BlueTrace 协议试图创建跨辖区的互操作性，以便其他国家可以在这些工作上进行合作。

**[GitHub 上的 OpenTrace 源代码](https://github.com/opentrace-community/opentrace-android)**

* * *

### 英国——新冠肺炎国民健康保险制度

英国的实施采用了 NHS 新冠肺炎应用程序的形式，该应用程序目前处于“beta 测试”阶段，可供怀特岛的居民使用(将来会扩展到其他地区)。该应用不依赖于谷歌和苹果的曝光通知 API，但也依赖于蓝牙。设置时，要求用户输入其 pin 码的前一半，用于识别是否有热点爆发-除非您报告症状，否则不会询问进一步的详细信息。蓝牙邻近数据通过匿名 id 记录 28 天。一旦疫情局势结束，该应用程序也将停止使用。该应用程序的源代码已经开放，可供检查。

**[GitHub 上的 NHS 新冠肺炎源代码](https://github.com/nhsx/COVID-19-app-Android-BETA)**

* * *

## 使用谷歌和苹果曝光通知 API 的解决方案

这些实现建立在谷歌和苹果的曝光通知 API 之上。谷歌还推出了包括新 API 的 Google Play 服务更新。[实现暴露通知 API 的 Android 应用的参考设计也可用](https://github.com/google/exposure-notifications-android)。禁止基于此 API 的应用程序收集设备位置数据。取而代之的是，API 利用蓝牙低能量来检测你是否在其他测试呈阳性的人附近。API 将共享自单个“接触事件”以来已经过去了多少天，以及估计的暴露时间。蓝牙元数据将被 AES 加密。

而在谷歌的情况下，Android 用户将不需要安装应用程序，因为暴露通知 API 是通过对 Google Play 服务的更新来交付的。因此，只要你有一台运行 Android 6.0 棉花糖或更高版本的 Android 设备，你就应该可以访问该服务。尽管如此，如果检测到阳性接触事件，谷歌将提示用户下载相关的公共卫生应用程序。

### 意大利—免疫

意大利的解决方案以 Immuni 应用程序的形式出现，预计将在未来几天内更广泛地公开发布。它依赖于谷歌和苹果的曝光通知系统，利用蓝牙低能耗，无论如何也不会收集地理位置数据。

**[在 GitHub 上免疫源代码](https://github.com/immuni-app/immuni-app-android)**

### 瑞士— SwissCovid DP-3T

瑞士正在研究一种叫做分散隐私保护邻近追踪(DP-3T)的解决方案。这款应用和服务器都有望开源。该应用程序尚未完成并向公众发布，但该应用程序的源代码已经上线，因此它应该作为一个基础。

**[SwissCovid DP-3T 源代码在 GitHub 上](https://github.com/DP-3T/dp3t-app-android-ch)**

* * *

这不是一个详尽的列表，而是为了突出以开源代码形式提供的解决方案，供感兴趣的开发人员检查和构建。