# Updato 的“三星更新”应用被从 Google Play 中移除

> 原文：<https://www.xda-developers.com/updates-for-samsung-firmware-download-android-app-removed-google-play/>

与苹果不同，大多数 Android 设备制造商从来不会立即在全球范围内推出更新。由于运营商的干扰和区域定制，不同国家的用户可能会在一个地区首次推出更新后几周甚至几个月才收到更新。例如，三星 Galaxy S10 的相机夜间模式更新于 4 月首次在国际型号[推出，但直到本月](https://www.xda-developers.com/samsung-galaxy-s10-bright-night-mode/)[的一些美国型号](https://www.xda-developers.com/samsung-galaxy-s10-att-us-snapdragon-camera-night-mode/)才推出。因此，拥有兼容智能手机型号的发烧友通常会求助于第三方来提前获得更新。第三方三星固件下载网站之一， *Updato* 因被指控诈骗用户钱财而陷入困境。

谷歌、一加和小米等公司提供各自设备最新固件的下载链接，但三星没有提供这种服务。根据官方说法，为三星手机获取新更新的唯一方法是使用设置中的内置检查器或使用三星智能开关服务。这两种方式都不能保证你会得到最新的更新，但是像 *Updato* 和 *SamMobile* 这样的第三方网站提供了三星固件下载的数据库。这些网站收集三星服务器的最新固件版本，并按照型号、运营商/地区和操作系统版本进行分类。他们都没有做的是实际的固件刷新； *Updato* 和 *SamMobile* 都使用三星 Odin 的泄露版本为用户提供固件，三星 Odin 是三星的内部工具，用于更新固件。

有争议的是，这两项服务都向高速下载三星固件的用户收费。在 *Updato* 的情况下，免费下载速率被限制在 56 KBps，用户将需要为更快的下载速度支付 34.99 美元的年费。按照免费下载的速度，下载大约 700MB 的固件至少需要 4 个小时。然而，特别是 *Updato* 陷入困境的原因是，来自 CSIS [的安全研究员发现](https://medium.com/csis-techblog/updates-for-samsung-from-a-blog-to-an-android-advertisement-revenue-goldmine-of-10-000-000-166585e34ad0)Updato 在谷歌 Play 商店上有一个名为“三星更新”的安卓应用该应用程序显然旨在吸引用户在他们的三星 Galaxy 设备上寻找最新更新。该应用程序被发现只是作为 *Updato* 网站的 WebView 运行，绕过了 Google Play 的应用内计费要求。

在这一事实引起了开发者的注意后，他们从 Google Play 中移除了 Android 应用。开发者与 [*出血电脑*](https://www.bleepingcomputer.com/news/security/samsung-update-app-with-10m-installs-charges-for-free-firmware/) 对话，告知他们他们的服务不是为“典型的安卓手机用户”设计的他们认为他们的服务为他们的观众提供了“便利”,因为他们的数据库“允许人们在任何地方为任何设备的任何版本轻松地搜索固件”...为他们节省了大量的潜在搜索时间和文件来源/安全性的不确定性。”最后，开发者承诺从应用中移除固件服务部分，转而使用谷歌的应用内计费，他们说“这是我们诚实的无知，我们将立即补救。”

## Updato 是骗局吗？

在关于“三星更新”应用程序的文章中，有一个词被广泛使用，那就是“骗局”。是否真的兑现了他们的承诺？如果你已经在我们的论坛呆了足够长的时间，你可能知道这项服务是由两个 XDA 论坛成员 [zxz0O0](https://forum.xda-developers.com/member.php?u=3975929) 和 [peterjitg](https://forum.xda-developers.com/member.php?u=7435428) 于 2016 年年中[开始的。起初，该服务没有任何下载速度限制，但在 2019 年 6 月 12 日， *Updato* 团队](https://forum.xda-developers.com/galaxy-s7/how-to/updato-largest-online-firmware-archive-t3413785)[宣布](https://forum.xda-developers.com/showpost.php?p=79716953&postcount=546)他们将进行“免费增值”，以跟上他们不断增长的数据库和带宽需求。除了政策上的这一变化，我们的论坛成员长期以来一直推荐 Updato 作为获取最新三星固件的一种方式。

如果你知道你在做什么，[你可以通过使用 SamFirm 工具免费获得最新的固件](https://www.xda-developers.com/download-stock-odin-firmware-samfirm/)，该工具实际上是由 *Updato* 的创始成员 zxz0O0 开发的。然而，并不是每个人都对这一过程感到满意，该工具只获取最新的可用更新，而 *Updato* 提供了一个庞大的、不断更新的固件数据库。因此，称 *Updato* 为骗局是不公平的，尽管很明显他们的 Play Store 应用程序已经针对搜索进行了优化，以吸引只寻找最新更新的普通用户，这与 *Updato* 声称他们的服务不面向普通用户的说法相矛盾。 *SamMobile* 通过不提供类似的 Play Store 应用程序来逃避批评，而 Team MT 的[华为](https://play.google.com/store/apps/details?id=com.teammt.gmanrainy.huaweifirmwarefinder)设备固件查找器直接从华为免费提供固件下载。

我们将继续关注 *Updato* 来看看这个故事如何发展。我们个人建议[按照我们的教程](https://www.xda-developers.com/download-stock-odin-firmware-samfirm/)免费安装最新的三星固件，但是我们理解你是否喜欢像 *Updato* 或 *SamMobile* 这样的服务的便利性。