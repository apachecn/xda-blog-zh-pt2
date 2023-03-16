# 谷歌 Chrome 将很快屏蔽 HTTPS 页面上的不安全下载

> 原文：<https://www.xda-developers.com/google-chrome-block-insecure-downloads-https-pages/>

谷歌最近[推出了 Android 和桌面的 Chrome 80](https://www.xda-developers.com/google-chrome-80-rolling-android-desktop/) 稳定更新。作为更新的一部分，谷歌引入了许多新功能，包括自动升级混合内容功能[，我们在去年 10 月](https://www.xda-developers.com/google-chrome-block-insecure-content-loading-https-pages/)了解到了这一功能。这项新功能是谷歌[与 HTTPS 合作保护网络](https://www.blog.google/topics/safety-security/say-yes-https-chrome-secures-web-one-site-time/)计划的一部分。现在，为了让 HTTPS 页面更加安全，谷歌 Chrome 也将很快阻止安全页面上的不安全下载。

在博文中，谷歌声称不安全下载的文件对用户的隐私和安全构成风险。这样的文件很容易被攻击者换成恶意软件，并且它们也有被窃听者读取的风险。为了应对这些风险，该公司计划最终取消谷歌 Chrome 对不安全下载的支持。屏蔽 HTTPS 网页上不安全的下载是谷歌采取这一措施的第一步。这一点至关重要，因为目前 Chrome 不会向用户提示他们在安全页面下载内容时的隐私和安全风险。

从预计于 2020 年 4 月发布的 Chrome 82 开始，Chrome 将逐渐开始警告用户(如上所示)混合内容下载。这些下载将在稍后阶段被完全阻止。这一变化将首先影响对用户构成最大风险的文件类型，如可执行文件，然后在后续版本中处理更多的文件类型。谷歌声称，逐步推出“旨在快速缓解最糟糕的风险，为开发者提供更新网站的机会，并尽量减少 Chrome 用户必须看到的警告。”

首先，谷歌将从 Chrome 81 开始，在桌面平台上推出混合内容下载的这些限制。以下是桌面平台限制的详细时间表:

*   在 Chrome 81(2020 年 3 月发布)和更高版本中:
    *   Chrome 将打印一个控制台消息，警告所有混合内容下载。
*   在 Chrome 82 中(2020 年 4 月发布):
    *   Chrome 会对混合内容下载或可执行文件发出警告。exe)。
*   在 Chrome 83 中(2020 年 6 月发布):
    *   Chrome 将阻止混合内容的可执行文件
    *   Chrome 会对混合内容存档发出警告。zip)和磁盘映像(。iso)。
*   在 Chrome 84 中(2020 年 8 月发布):
    *   Chrome 将阻止混合内容的可执行文件、档案和磁盘映像
    *   Chrome 将对除图像、音频、视频和文本格式以外的所有其他混合内容下载发出警告。
*   在 Chrome 85 中(2020 年 9 月发布):
    *   Chrome 会对图像、音频、视频和文本的混合内容下载发出警告
    *   Chrome 将阻止所有其他混合内容下载
*   在 Chrome 86(2020 年 10 月发布)及更高版本中，Chrome 将阻止所有混合内容下载。

这些限制将被推迟一个版本，用于 Android 和 iOS 用户，警告从 Chrome 83 开始。谷歌声称，由于移动平台对恶意文件有更好的本地保护，延迟将让开发者在用户受到影响之前更新他们的网站。开发者可以确保下载只使用 HTTPS，以防他们不希望用户看到下载警告。

此外，在 Chrome Canary 的当前版本中，或者在 Chrome 81 发布后，开发人员还可以通过启用“将不安全连接上的危险下载视为活动混合内容”标志，激活对所有混合内容下载的警告以进行测试。谷歌计划在未来进一步限制谷歌浏览器中的不安全下载，为此，该公司敦促开发者完全迁移到 HTTPS，以避免限制。

* * *

**来源:[谷歌安全博客](https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html)**