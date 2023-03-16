# 谷歌、苹果宣布接触追踪技术追踪冠状病毒

> 原文：<https://www.xda-developers.com/google-apple-contact-tracing-coronavirus/>

**更新 6(美国东部时间 2020 年 5 月 20 日下午 1 点 55 分):**谷歌和苹果的暴露通知 API 现已向公共卫生机构开放，因此他们可以为新冠肺炎实施接触者追踪。

**更新 5(美国东部时间 5/4/2020 @下午 3:25):**苹果和谷歌分享了曝光通知 API 的部分截图，并宣布将禁止位置追踪。

**更新 4 (4/29/2020 @美国东部时间下午 2:30):**苹果和谷歌发布了面向公共卫生机构的暴露通知 API 的测试版。

**更新 3(美国东部时间 2020 年 4 月 24 日下午 3:15):**苹果和谷歌将联系人追踪 API 更名为“曝光通知”，增加了更多隐私保护。

**更新 2(美国东部时间 2020 年 4 月 24 日上午 11:30):**苹果和谷歌的联系人追踪 API 将于下周上线，并将包括大多数华为设备。

**更新 1(美国东部时间 2020 年 4 月 13 日下午 5:51):**在与记者的电话会议上，谷歌和苹果澄清了更多关于如何为用户推出联系人追踪的细节。

由于新型冠状病毒带来的持续威胁，谷歌和苹果联手宣布了一个新的 API 和蓝牙低能耗规范，称为“联系追踪”接触追踪背后的想法是通知用户他们最近是否接触过被确诊为新冠肺炎的人。韩国和台湾成功地“拉平了曲线”，通过实施广泛的检测和接触者追踪，他们将新增病例数量限制在了医疗系统的承受能力之下。据 [*美联社*](https://apnews.com/cfd0be05937f89e2c506f8fd7df520e2) 报道，包括捷克、英国、德国、意大利在内的几个欧洲国家正在开发自己的联系人追踪工具。苹果和谷歌希望赋予世界各地的国家和医疗组织追踪新型冠状病毒传播的能力，但这两家公司也认识到这种疫情遏制方法的潜在隐私问题。这就是为什么这两家公司创造了新的 API 和蓝牙规范，“用户隐私和安全是设计的核心。”

谷歌和苹果发布了博客文章和文档，概述了他们推出新的 API 和蓝牙 le 服务的目标。由于迫切需要，两家公司正分两个阶段解决这个问题。首先，在 5 月份，两家公司都将发布一个 API，“使用公共卫生部门的应用程序，实现 Android 和 iOS 设备之间的互操作性。”用户可以在谷歌 Play 商店和苹果应用商店下载这些应用。在 Android 上，通过对 Google Play 服务的更新，该 API 可能会对应用程序可用。其次，在接下来的几个月里，谷歌和苹果都将在 Android 和 iOS 中添加对新蓝牙低能耗服务的支持。对于 iOS，这项新的 BLE 服务可能会通过操作系统更新来实现，而对于 Android，这项服务可能会作为另一项更新的一部分添加到 Google Play 服务中。谷歌表示，增加蓝牙 le 联系追踪服务“是一个比 API 更强大的解决方案，如果他们选择加入，将允许更多的人参与，并实现与更广泛的应用生态系统和政府卫生当局的互动。”

一旦应用程序集成了新的 API 或 BLE 规范，Android 和 iOS 用户就可以收到通知，如果他们最近与被诊断患有新冠肺炎的人有过接触。值得注意的是，BLE 的解决方案不要求用户安装应用程序(假设他们只需要 Google Play 服务)，但如果他们选择安装一个官方应用程序，那么该应用程序可以在他们收到通知后通知他们接下来要采取的步骤。这将允许用户决定他们是否需要自我隔离 14 天或寻求测试和进一步的医疗干预。以下是谷歌和苹果公司对这一新的蓝牙 le 服务的设想流程示例:

*使用蓝牙低能耗追踪新冠肺炎联系人概述。来源:谷歌/苹果。*

以下是谷歌关于他们如何设计新的 Android 联系人跟踪 API 来保护用户隐私和安全的说法:

*   通过 startContactTracing 方法调用 API 的应用程序需要获得用户同意才能开始联系人跟踪。如果这是第一次调用 API，将向用户显示一个对话框，要求允许开始跟踪。
*   为了被列入白名单以使用这种 API，应用程序“将被要求在交付给服务器之前，用授权医疗机构的签名对密钥集进行时间戳和加密签名。”换句话说，未经授权的新冠肺炎应用将不被允许使用这个 API。
*   如果用户卸载应用程序，stopContactTracing 方法“将被自动调用，数据库和密钥将从设备中删除。”
*   用户在确认新冠肺炎阳性诊断后，必须明确同意上传 14 天的每日追踪密钥。如果应用程序调用 startSharingDailyTracingKeys 方法，将向用户显示一个对话框。
*   将向用户显示他们与潜在传染者接触的日期和时间，精确到 5 分钟的增量，但不显示接触发生的人或地点。

以下是新的 BLE 接触检测服务将如何保护用户隐私和安全:

*   该规范不要求用户的位置或任何其他个人身份信息。位置使用是完全可选的，只有在用户明确同意后才能使用。
*   滚动邻近标识符平均每 15 分钟改变一次，这使得“随着时间的推移，用户位置不太可能通过蓝牙被跟踪。”
*   从其他设备检索的邻近标识符“仅在设备上处理”这意味着“你联系过的人的名单永远不会离开你的手机。”
*   由用户决定他们是否愿意参与联系人追踪。被诊断患有新冠肺炎的用户必须同意与服务器共享诊断密钥。用户参与接触追踪将是透明的，“测试呈阳性的人不会向其他用户、谷歌或苹果透露。”事实上，这些信息“将仅被公共卫生当局用于新冠肺炎疫情管理的接触者追踪”
*   如果你想知道，如果硬件和操作系统支持“蓝牙控制器复制过滤器和其他[硬件]过滤器”，以“在公共场所占据大量广告商”，内容检测服务应该不会显著消耗设备的电池扫描是“机会性的”，这意味着它可以在现有的唤醒和扫描窗口周期内发生，但也至少每 5 分钟发生一次。

因为新的接触追踪规范是在考虑用户隐私和安全的情况下设计的，所以它们在限制新冠肺炎病毒传播方面的有效性是有争议的。根据 [*The Verge*](https://www.theverge.com/interface/2020/4/10/21215267/covid-19-contact-tracing-apps-bluetooth-coronavirus-flaws-public-health) 的说法，这种选择加入、非侵入性的接触者追踪措施可能效力有限。这些问题归结为缺乏广泛的人口采用和潜在的大量假阳性蓝牙邻近事件。尽管如此，我还是希望这项新举措取得成功。很少看到谷歌和苹果在任何事情上合作，但非常时期需要非常手段。

**来源:** [谷歌博文](https://www.blog.google/inside-google/company-announcements/apple-and-google-partner-covid-19-contact-tracing-technology/)，[新冠肺炎联系人追踪概述](https://www.blog.google/documents/57/Overview_of_COVID-19_Contact_Tracing_Using_BLE.pdf)，[联系人追踪 BLE 规范](https://www.blog.google/documents/54/Contact_Tracing_-_Bluetooth_Specification.pdf)，[联系人追踪密码术规范](https://www.blog.google/documents/56/Contact_Tracing_-_Cryptography_Specification.pdf)，[安卓联系人追踪 API 规范](https://www.blog.google/documents/55/Android_Contact_Tracing_API.pdf)

* * *

## 更新 1:更多细节

在与记者的电话会议中，谷歌和苹果澄清了关于即将推出的联系人跟踪 API(作为“第一阶段”的一部分，将于 5 月中旬推出)和 BLE 联系人检测服务(作为“第二阶段”的一部分，将于今年晚些时候推出)的一些问题。根据 [*TechCrunch*](https://techcrunch.com/2020/04/13/apple-google-coronavirus-tracing/) 和 [*Axios*](https://www.axios.com/apple-google-limit-how-coronavirus-contact-tracing-tech-can-be-used-ac728c22-bb50-4531-9213-53d28a06fb92.html) 的消息，在 Google Play 服务更新后，联系人追踪 API 和 BLE 联系人检测服务都将在 Android 设备上可用——只要 Android 智能手机运行 Android 6.0 棉花糖。用户不需要手动更新他们的设备，甚至不需要更新他们的操作系统，因为 Google Play 服务的更新会通过谷歌 Play 商店在后台悄悄进行。

尽管 BLE 接触检测服务的引入意味着用户不需要安装应用程序来参与接触追踪，但谷歌表示，如果检测到积极的接触事件，用户仍会被提示下载相关的公共卫生应用程序。这将帮助用户确定他们应该采取的下一步措施。苹果指出，虽然数据在设备上进行本地处理后，可能会被“中继”到世界各地公共卫生组织运行的服务器上，但不会有一个集中的数据服务器。这将使任何政府或其他恶意行为者难以进行监控。根据 Axios 的说法，各国可以运行自己的服务器，或者使用苹果和谷歌的服务器。为了防止人们提交假阳性诊断，苹果和谷歌正在与公共卫生组织合作，研究一种确认诊断的方法。

随着谷歌确认将通过更新 Google Play 服务为 Android 设备带来联系人追踪功能，数百万没有谷歌移动服务的设备将会发生什么？当然，我指的是中国数以百万计的设备，以及华为和 Honor 发布的新款智能手机。据 The Verge 报道，谷歌“打算发布一个框架，这些公司可以用它来复制谷歌和苹果开发的安全匿名跟踪系统。”因此，由第三方决定他们是否要使用该系统。谷歌没有证实其联系人追踪框架是否会开源，但他们表示将向希望采用该系统的公司提供代码审计。

* * *

## 更新 2:初始部署，华为参与

最初计划在“五月中旬”上线，看起来苹果和谷歌的联系追踪时间表已经提前了。据欧盟内部市场专员蒂埃里·布雷顿称，该计划的第一阶段将于 4 月 28 日实施。这些信息是苹果首席执行官蒂姆·库克(Tim Cook)提供给布雷顿的。

联系追踪的第一阶段是关于 API 的。这些 API 将由代表公共卫生机构工作的开发人员使用，而不是第三方应用程序。这些 API 将通过更新 Google Play 服务提供，大多数装有 Android 6.0+和蓝牙低能耗功能的设备都可以支持联系人跟踪。

当然，最近的华为和 Honor 设备没有 Google Play 服务，但许多旧设备仍然有。 *TechRadar* 证实，这些旧设备*不*包括华为 Mate 30、P40、Honor V30 和其他设备，将被包括在首次展示中。至于其他华为/Honor 设备，之前的文章更新称，谷歌“打算发布一个框架，这些公司可以用来复制谷歌和苹果开发的安全匿名跟踪系统。”

**来源 1: [回声报](https://www.lesechos.fr/tech-medias/hightech/tracing-thierry-breton-cherche-a-obtenir-des-garanties-aupres-de-tim-cook-1197352) | Via: [TechCrunch](https://techcrunch.com/2020/04/23/first-version-of-apple-and-googles-contact-tracing-api-should-be-available-to-developers-next-week/) |来源 2: [TechRadar](https://www.techradar.com/news/huawei-confirms-most-of-its-phones-will-get-googles-contact-tracing-update)**

* * *

## 更新 3:更多隐私保护

苹果和谷歌现在将联系人追踪计划称为“曝光通知”，他们说这是对该工具目的的更好描述。我们也有更多关于卫生当局如何微调 API 和隐私保护的信息。

API 使用蓝牙来检测你是否在其他测试呈阳性的人附近，但这有可能不准确(检测不够近或在墙后的人)。API 将共享蓝牙信号的强度，因此卫生当局可以为构成“接触事件”的内容设置自己的阈值。

API 将共享自单个“联系事件”以来已经过去了多少天它不会透露两人接触的确切时间。相反，它将只共享暴露时间的估计值，从最少 5 分钟到最多 30 分钟，增量为 5 分钟。卫生当局可以使用这些信息根据事件发生的时间来改变他们对用户的指导。

蓝牙元数据将被加密，以防止它被用来跟踪反向识别攻击中的个人。该元数据包括信号强度和其他信息。加密算法将改为他们以前使用的 HMAC AES。AES 加密可以在许多移动设备上加速，使 API 更加节能。

最后，用于跟踪潜在联系人的密钥现在是随机生成的，而不是每 24 小时从永久绑定到特定设备的“跟踪密钥”中导出。这就消除了直接访问设备的攻击者能够知道如何从跟踪密钥生成密钥的机会，尽管这已经非常非常困难了。

**来源 1: [Axios](https://www.axios.com/apple-google-tweak-contact-tracing-specs-as-launch-nears-e76dee7c-350d-4143-8024-29dd0d3fd67f.html) |来源 2: [彭博](https://www.bloomberg.com/news/articles/2020-04-24/apple-google-boost-privacy-protections-for-contact-tracing-tool) |来源 3: [TechCrunch](https://techcrunch.com/2020/04/24/apple-and-google-update-joint-coronavirus-tracing-tech-to-improve-user-privacy-and-developer-flexibility/)**

* * *

## 更新 4:测试版 API 可用

苹果和谷歌今天开始在一个私人测试版中推出他们的暴露通知 API(以前称为“联系追踪”)。谷歌正在通过 Google Play 服务发布测试版更新，因此他们可以在任何具有蓝牙低能耗的 Android 6.0+设备上工作。公共卫生机构可以开始在 Android Studio 中使用这些 API，并开始测试。

该 API 的稳定版本仍计划在未来几周内发布。正如这两家公司一直重申的那样，这个 API 不打算被第三方开发者使用。它是为公共卫生机构服务的，当这些机构的开发者完成工作后，你可以从他们那里下载一个应用程序。

**来源:[彭博](https://www.bloomberg.com/news/articles/2020-04-29/apple-google-release-virus-contact-tracing-tools-to-app-makers)**

* * *

## 更新 5:截图，无位置追踪

苹果和谷歌正在继续发布更多关于曝光通知 API 的信息。首先，这两家公司分享了一些公共卫生当局必须遵守的指导原则，以便在各自的应用商店中使用他们的合同追踪应用程序。这些应用被禁止收集设备位置数据，API 仅限于每个国家一个应用，收集的数据不能用于定向广告。

每个国家一个应用程序的 API 限制是为了减少碎片化，但苹果和谷歌将保持灵活性，并与可能需要多个应用程序的国家的政府合作。例如，按地区或州进行接触者追踪的国家。

苹果和谷歌也分享了一些曝光通知设置和应用程序的模拟截图。上图显示了 Google Play 服务中新的“新冠肺炎曝光通知”部分。此部分显示它是否已启用，以及哪些应用程序能够发送暴露通知。用户可以从这里启动应用程序，查看过去 14 天内进行了多少次“暴露检查”，删除随机 id，并关闭通知。

谷歌还分享了一些使用曝光通知 API 的应用程序的示例截图(如上)。这款应用的源代码已经发布在该公司的 Github 页面上，如果卫生机构希望用它来开发应用的话。

**来源: [VentureBeat](https://venturebeat.com/2020/05/04/apple-and-google-prohibit-location-tracking-in-new-contact-tracing-guidelines/) ， [9to5Google](https://9to5google.com/2020/05/04/android-covid-19-settings/) ， [9to5Google](https://9to5google.com/2020/05/04/android-contact-tracing-apps/)**

* * *

## 更新 6: API Live

经过几周的准备，苹果和谷歌现在发布了他们的暴露通知 API，供公共卫生机构使用。具体来说，谷歌正在推出包含新 API 的 Google Play 服务更新。公共卫生机构的开发人员现在可以使用这些 API 来实现新冠肺炎的接触者追踪应用程序。美国三个州已经宣布了使用该 API 的开发项目。总共有 22 个国家获得了 API，但我们不知道具体是哪些国家。

**来源:[谷歌](https://www.blog.google/inside-google/company-announcements/apple-google-exposure-notification-api-launches/)， [The Verge](https://www.theverge.com/2020/5/20/21265052/apple-google-coronavirus-notification-system-states-alabama-north-dakota-south-carolina) ，**