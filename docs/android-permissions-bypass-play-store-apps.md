# 超过 1000 个 Android 应用程序可以在没有适当权限的情况下访问用户数据

> 原文：<https://www.xda-developers.com/android-permissions-bypass-play-store-apps/>

尽管用户认为，Android 作为移动操作系统实际上是相当安全的。我们普遍接受的前提是，最薄弱的环节是用户；只要您注意安装的内容和授予的权限，您的数据就不会受到未经授权的访问和分发。如果你拒绝一个 Android 应用程序访问你的位置，那么这个应用程序就没有办法知道你在哪里或者你去过哪里。然而，据国际计算机科学研究所(ICSI)的研究人员称，一些应用程序开发者已经找到了绕过 Android 权限模型的方法。

据[](https://www.cnet.com/news/more-than-1000-android-apps-harvest-your-data-even-after-you-deny-permissions)*报道，这项研究在去年 9 月负责任地向谷歌和联邦贸易委员会披露后，于上月在 [PrivacyCon](https://www.cnet.com/news/more-than-1000-android-apps-harvest-your-data-even-after-you-deny-permissions) 发表。尽管发表在 FTC 网站上的[论文没有列出该团队在他们的分析中标记的确切应用程序(这些细节将在下个月的](https://www.ftc.gov/system/files/documents/public_events/1415032/privacycon2019_serge_egelman.pdf) [Usenix 安全会议](https://redirect.viglink.com/?format=go&jsonp=vglnk_156261870297011&key=ce074976249105acf14d8c9cf69bdcd1&libId=jxutwb2m01003n6p000DAkr108zzv&loc=https%3A%2F%2Fwww.cnet.com%2Fnews%2Fmore-than-1000-android-apps-harvest-your-data-even-after-you-deny-permissions%2F%3Futm_source%3Dreddit.com&v=1&out=https%3A%2F%2Fwww.usenix.org%2Fconference%2Fusenixsecurity19%2Ftechnical-sessions&ref=https%3A%2F%2Fwww.reddit.com%2Fr%2FAndroid%2Fcomments%2Fcakugb%2Fmore_than_1000_android_apps_harvest_data_even%2F&title=More%20than%201%2C000%20Android%20apps%20harvest%20data%20even%20after%20you%20deny%20permissions%20-%20CNET&txt=presents%20the%20study%20at%20the%20Usenix%20Security%20conference)上公布)，但它确实提供了他们的分析方法以及这些应用程序如何绕过 Android 权限模型的细节。值得一提的是，谷歌表示，谷歌[在 Android Q](https://www.xda-developers.com/android-q-security-privacy-features/) 中引入的安全和隐私变化将关闭这些绕过方法，因此本文为谷歌在 Android 10 中所做的一些平台变化提供了有价值的见解。让我们开始吧。*

 *## 超过 1000 个应用程序如何绕过 Android 的权限模型

研究人员区分了两种不同的安全规避技术:侧通道和隐蔽通道。辅助渠道技术包括以一种不被安全机制覆盖的方式访问特定信息；例如，应用程序过去可以使用 MAC 地址来跟踪设备的位置，直到 Android Pie 引入了 MAC 地址随机化。隐蔽信道技术包括两个服务合作，将数据从一个具有有效访问权限的服务发送到另一个不具有有效访问权限的服务；例如，已被授予位置访问权限的应用程序可能会与未被授予访问权限的应用程序共享该数据。

ICSI 团队分析了来自美国谷歌 Play 商店的 88，113 个最受欢迎的 Android 应用程序，并发现了超过 1，000 个应用程序和第三方库，它们利用侧信道和/或秘密信道来绕过 Android 的安全措施，以便能够访问用户设备的位置数据和永久标识符。他们的完整数据集由 252，864 个 apk 组成，因为该团队定期从 Play Store 中搜索他们计划分析的 88，113 个应用程序的新版本。他们最初在运行 Android 6.0.1 棉花糖的[谷歌 Nexus 5X](https://forum.xda-developers.com/nexus-5x) 上测试了每个应用的行为，但后来在运行 Android Pie 的[谷歌 Pixel 2](https://forum.xda-developers.com/pixel-2) 上重新测试了他们的发现，以证明他们的发现在披露时的最新版本中仍然有效。

利用这个数据集，该团队开发了一种使用动态和静态分析的方法来检测 Android 权限模型的规避。换句话说，该团队通过审计应用的运行时行为(动态分析)或扫描代码以发现潜在的恶意行为(静态分析)来研究应用行为。)当然，恶意应用程序开发人员知道这些技术，他们使用代码混淆和动态代码加载来增加静态分析的难度，或者使用 TLS 拦截来检测应用程序何时在虚拟化环境中运行，因此 ICSI 团队在测试中混合使用了静态和动态分析(混合分析)。结果，该团队发现以下数据被没有所需权限的应用程序抓取:

*   IMEI 是一个唯一的、持久的标识符，所以在线服务收集它是很有用的，这样他们就可以跟踪单个的设备。该团队发现 [Salmonads](http://www.salmonads.com/) 和[Baidu](https://lbsyun.baidu.com/)SDK 正在使用秘密渠道读取 IMEI。合法访问 IMEI 的应用程序在包含设备 IMEI 的外部存储器上存储隐藏文件，以便其他没有合法访问权限的应用程序可以读取 IMEI。以这种方式使用百度 SDK 的应用包括香港和上海的迪士尼主题公园应用、三星健康和三星浏览器。
*   **网络 MAC 地址:**网络 MAC 地址也是一个唯一的标识符，通常受 ACCESS_NETWORK_STATE 权限保护。根据研究人员的说法，应用程序使用 C++本机代码来“调用大量无保护的 UNIX 系统调用”该团队发现 42 个应用程序使用 Unity SDK 来打开网络套接字和 ioctl 以获取 MAC 地址，尽管他们指出 12，408 个应用程序中的 748 个包含有问题的代码，但缺乏 ACCESS_NETWORK_STATE 权限。
*   **路由器 MAC 地址:**ACCESS _ WIFI _ STATE 权限保护 BSSID，但是读取/proc/net/arp 中的 ARP 缓存允许一个 app 在不需要任何权限的情况下获取该数据。研究人员发现 [OpenX](https://www.openx.com/publishers/mobile/openx-mobile-sdk/) SDK 使用了这种旁道技术。
*   **地理定位:**研究人员发现 Shutterfly 应用程序正在访问照片的 EXIF 元数据的位置标签。所需的只是 READ_EXTERNAL_STORAGE 权限。

在 Android Q 中，谷歌现在要求应用程序具有读取 IMEI 的 READ_PRIVILEGED_PHONE_STATE 权限。运行 Android Q 的设备现在默认传输随机 MAC 地址。最后，Android Q 的[范围存储](https://www.xda-developers.com/android-q-storage-access-framework-scoped-storage/)的变化削弱了应用程序从照片中读取位置数据的能力。因此，这些问题已经在最新的 Android 版本中得到解决，但正如我们所知，最新更新的传播需要[相当长的时间](https://www.xda-developers.com/google-hasnt-published-updated-android-distribution-statistics-last-6-months/)。

* * *

## 结论

总的来说，这项研究对一些应用程序如何访问应该在权限背后保护的数据提供了一个启发性的视角。这项研究只关注了谷歌所谓的“危险”权限的一个子集，特别是跳过了蓝牙、联系人和短信等权限。关于这份报告的全部细节，我推荐阅读提交给 FTC 的[论文。](https://www.ftc.gov/system/files/documents/public_events/1415032/privacycon2019_serge_egelman.pdf)*