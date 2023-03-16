# 研究人员指责小米网络浏览器收集浏览数据

> 原文：<https://www.xda-developers.com/xiaomi-mi-web-browser-pro-mint-collecting-browsing-data-incognito-mode/>

**更新 3 (05/21/2020 @ 01:48 AM ET):** 小米更新了浏览器设置，目的更加明确，消除了之前的困惑。

**更新 2 (05/03/2020 @美国东部时间上午 10:14):**在其博文更新中，小米提到其浏览器将更新一个选项，允许用户选择退出匿名模式下的跟踪。

**更新 1(美国东部时间 05/01/2020 @ 03:36PM):**小米已发表博文回应这些指控。向下滚动查看更新。美国东部时间 2020 年 5 月 1 日上午 06:18 发布的原故事如下。

小米智能手机在任何时候都被一致认为是市场上最值得购买的产品之一。以非常有利可图的价格点包装一些疯狂的硬件，特别是在低端智能手机市场，这些手机提供了很多人无法拒绝的报价。小米也已经接受了开发者社区的需求，例如[允许引导加载程序解锁而不牺牲制造商的保修](https://www.xda-developers.com/xiaomi-india-clarifies-bootloader-unlocking-does-not-void-warranty/)——这是许多其他受欢迎的原始设备制造商放弃的组合，也大大改进了他们的[内核源代码版本](https://www.xda-developers.com/xiaomi-mi-10-kernel-source-code/)。这些原因使它们成为我们论坛中最受欢迎的设备之一，它们理所当然地赢得了这一地位。

然而，安全研究人员最近的报告指出，小米的网络浏览器存在令人担忧的隐私问题。《福布斯》网络安全撰稿人兼助理编辑托马斯·布鲁斯特(Thomas Brewster)与网络安全研究人员 T2(Gabriel Cirlig)和 T4(Andrew tier ney)最近在一份报告中得出结论，小米的各种网络浏览器正在向远程服务器发送数据。他们声称，被发送的数据包括所有访问过的网站的历史记录，包括网址、所有搜索引擎查询和小米新闻订阅上查看的所有项目，以及设备元数据。更令人担忧的是，即使你似乎是在开启“匿名模式”的情况下浏览，这些数据也会被收集。

这种数据收集似乎发生在 MIUI 上预装的股票浏览器，以及通过谷歌 Play 商店下载的 [Mi Browser Pro](https://play.google.com/store/apps/details?id=com.mi.globalbrowser) 和 [Mint Browser](https://play.google.com/store/apps/details?id=com.mi.globalbrowser.mini) 上。这些浏览器在 Play Store 上的下载量合计超过 1500 万次，而股票浏览器则预装在所有小米设备上。测试的设备包括小米 Redmi Note 8、小米 Mi A1、小米 Mi 10、小米 Redmi K20 和小米 Mi Mix 3。小米的 Android One 和 MIUI 设备之间没有区别，因为收集代码反正是在默认浏览器中找到的。因此，这个问题似乎不是以 MIUI 为中心的，而是取决于你是否在你的设备上使用这三种浏览器中的任何一种，而不考虑底层的操作系统。其他浏览器，如谷歌 Chrome 和苹果 Safari 收集的数据要少得多，仅限于使用和崩溃分析。

小米的回应似乎是确认其收集的浏览数据完全符合当地关于用户数据隐私问题的法律法规。收集的信息是用户同意的和匿名的。然而，该公司否认了研究中的说法。

> 研究声称是不真实的。隐私和安全是首要问题。
> 
> 该视频展示了匿名浏览数据的收集，这是互联网公司通过分析非个人身份信息来改善整体浏览器产品体验的最常见解决方案之一。

然而，研究人员发现这种匿名的说法是可疑的。小米发送的数据被公认为是“加密的”，但它是以 base64 编码的，很容易被解码。由于浏览数据可以以相当简单的方式被[解码，并且由于收集的数据还包含设备元数据，该浏览数据看起来可以与单个用户的动作相关联，而不需要很大的努力。](https://gchq.github.io/CyberChef/#recipe=URL_Decode()From_Base64('A-Za-z0-9%2B/%3D',true)Gunzip()&input=SDRzSUFBQUFBQUFBQU8yWVVXdmpPQkRIdjBwd1NsNFN1NWFkeEhZZ0hPa3Q3Zldoc05DOXZZWHJJUlJMc1VWdHlTZko5WWFsMyUyRjFHZHBKbTI5NUNsMTNZZ1BNUTdMJTJGR285SE0lMkZHSXBmMzl4c0ZFa3ZjZWNPZ3MzanBKWkhJVUJtamlHbDh4Wm9Ga2NCMUU4RDZKNUhJTzRyVUIwMmllY2lWTXBXVEZsT05QTzRvdHpWdkExREs0RVZSSzhUWnd6cWZFRFU1cExBWHBpRlRBNWtnSVBlWUdWUzBsWkFjSU5INnhROSUyQlRYbm5TcUdCTzQ0ZFRrRUpVZiUyQjA5aXpuaVdHMUNUd0tvbEVmV0dwS1pXVElHVFQ1eklrbHNmcEtxTzVnNjlxZWVEWE5kMjVRNWR6emN4b2RSTnB6NXlwOU13ZE5jQlRWM3FUNk9Rb0UyRTVpbFljMkdZRXN4Z2JZaXBJVWpJVkZVUXM1R3FmSXA0VlZWZ1clMkZLYUgwMzRFZm1lNzZFUXZ0NiUyRiUyQiUyQlBtJTJCdFBOM2theHJETzV1Z0JKYjdWaEpTNkl5R3FTMlhRelljTnYlMkJJWTdDNk5xQmpjUVFpUFZQZDRWNUslMkZyeSUyQnVqTkVuRm1ZQUFPNiUyQlZWRkF3YnF4dlJsU2E0MHBxdmh2c2xBdWljTVBXb0RLYkVzMG83Z2FZeUxpd00xeEptUlVNMyUyQlpFc1NkSEVJTk5IaCUyQlFjdEJKWEdRRFNNWkF5NUtaOWk2SDZoUmJHQloyMG9lanA2MkZwSWNnOEpvb3V3aXU4WVlyYlRBbFcyZXhJWVZtanhPSGNtMjRTQTElMkJTN25ham55dE0lMkYlMkJuRDE5dmtkYjZFR3dLdmJvWEtUT0VGNjFZZW5hRlVtbEtEUEdJSU1YVzhGVERWVHVwcCUyQm05ZDl0WnZBT0wxZnZyTSUyQlFQaDZvV3clMkJHdHJGWEtMbm5CaGtQa3dHTFpBOVR2a0JpWURXJTJCS1d1ZjRheWluUWVRbmo1Tm5DSWNKcENTY3g2OGduSVE5d3FlT3NLeHN1eFVjNm4zb2pxcWJaSWNSMFZxbW5MUW85ekE5d1NSWWclMkZjJTJGZ0pBd0xLdHZnSVg4NTJDaElFcW1NeiUyRndaNiUyQlJsZlJrblRwWmV3TkJiSEhiTHJRUmVGSmxYcG9yU0ZSZGRoZk1XeXZaYUthODM5dmJEMlM5Wm5TVnd1dU5tNjExWmJncFdGc3pZUVlYbmZFcDQlMkZoZGlSaTJuMk1FejZENEh6bHJidHRNdndXJTJGQlBteiUyQlN6MnB5JTJGaGkxcXhoNiUyQkhyNGZ2eDhDSG5yJTJGNzVpaUswVHdJWDc3NjRqanhlJTJGcE9uYjVhMlN6bnhsUjZjWGQlMkJkOTQwalplMUp6NFBHdkR1dk5zMiUyRlpZWFN5YmNxNHNSWjhzJTJGUDF5NjhVaTNtNjNsYmwlMkZtN2hweTlPJTJCU2owazVQaHdKeDVDSDhlRklPTzZPaE9QRGtYQUUlMkIxa0liRmxxZCUyQiUyRnBjMXNlVjdHSFlKUTFHaXU2MUxvNFpZcCUyRndvNjIzY1lXa2xEY0tyYjVsSGtUMkFoa0ZJYkpMSHhCZGhJbHFDZTdKN3NuJTJCeGNnZThNRjE5JTJGNkl3Z0ZqJTJGJTJGOEIyaGI4azNORlFBQQ)

此外，研究人员发现，小米浏览器正在搜索与 Sensors Analytics 相关的领域，Sensors Analytics 是一家中国初创公司，也称为 Sensors Data，以提供行为分析服务而闻名。这些浏览器还包含一个名为 SensorDataAPI 的 API。小米也被列为[传感器数据网站](https://www.sensorsdata.cn/auto)的客户。

小米在几个方面对《福布斯》的报道进行了否认:

> 虽然 Sensors Analytics 为小米提供了数据分析解决方案，但收集的匿名数据存储在小米自己的服务器上，不会与 Sensors Analytics 或任何其他第三方公司共享。

研究人员对小米的否认做出回应，提供了他们数据收集实践的进一步证据。

根据现有的信息，这些浏览器的运行方式确实存在令人担忧的隐私问题。我们联系了小米，请其进一步评论这些说法。

**来源:[福布斯](https://www.forbes.com/sites/thomasbrewster/2020/04/30/exclusive-warning-over-chinese-mobile-giant-xiaomi-recording-millions-of-peoples-private-web-and-phone-use/#25382c281b2a)**

## 更新 1:小米在博文中回应

在 Mi.com 的一篇官方博客文章中，小米强烈否认了他们侵犯用户隐私的指控。

> #### “小米看了《福布斯》最近的文章很失望。我们认为他们误解了我们就数据隐私原则和政策所传达的内容。我们用户的隐私和互联网安全是小米的重中之重；我们确信我们严格遵守并完全符合当地的法律法规。我们已经向《福布斯》寻求澄清这一不幸的误解。”

该公司证实，他们收集“聚合的使用统计数据”，其中包括“系统信息、偏好、用户界面功能使用、响应能力、性能、内存使用和崩溃报告。”他们表示，这些信息“不能单独用于识别任何个人。”他们确认收集了 URL，但这样做是为了“识别加载缓慢的网页”，以便他们可以找出“如何最好地提高整体浏览性能”

接下来，该公司表示，个人浏览数据历史是同步的，但这只有在“用户登录 Mi 帐户”时才能完成...并且数据同步功能在设置下被设置为‘开’。”他们否认，当用户启用匿名模式时，除了上述聚合的使用统计数据之外，浏览数据正在被同步。

小米随后公布了一个浏览器应用程序的代码片段截图(不过他们没有说明是哪个浏览器)，声称这些截图证明了他们的观点。根据小米的说法，第一个代码片段显示了一个反编译的方法，用于“如何[他们]创建随机生成的唯一令牌，以添加到聚合使用统计数据中。”他们声明“这些令牌不对应任何个人。”下一个代码片段似乎来自浏览器的源代码，并显示了“Mi 浏览器如何在匿名模式下工作，其中没有用户浏览数据将被同步”的方法。第三个代码片段演示了小米收集的聚合使用统计数据“存储在小米的域上”，并且不会传递给传感器分析。最后，第四个图像“显示了使用 TLS 1.2 加密的 HTTPS 协议传输的使用统计数据。”

最后，小米列举了他们的软件从 TrustArc 和英国标准协会(BSI)获得的 4 项认证。这些认证包括 ISO27001:2013、ISO27018:2014、ISO29151:2017 和 TRUSTe。

作为对这篇博文的回应，网络安全研究员安德鲁·蒂尔尼[在推特](https://twitter.com/cybergibbons/status/1256275170802745345)上反驳了小米的说法。他表示，他和其他几个人在多种设备上再次确认了这一发现——毫无疑问，薄荷浏览器在匿名模式下发送搜索词和网址。他表示，小米发布的代码并没有证明他们的“随机生成的唯一令牌”不能与个人相关联。研究人员注意到，UUID 似乎会在整个浏览会话中持续存在，并且只有在浏览器被重新安装时才会改变。对于研究人员来说，小米是否只将数据存储在他们自己的服务器或其他地方也不是争论的焦点。此外，这位研究人员表示，小米没有被指控通过不安全的方法将数据发送到远程服务器——蒂尔尼指出，眼下的问题是正在发送的数据本身。

我们很高兴看到小米直接解决这些指控，但在这一点上，这个解释似乎并不能让研究人员满意。我们将继续关注这一事件的进一步发展。

* * *

## 更新 2:小米将在下一次浏览器更新中提供退出选项

小米更新了其博客文章,宣布 mint 浏览器和 Mi 浏览器的下一次更新将包括一个匿名模式选项，以关闭“聚合”数据收集。软件更新将于今天提交给谷歌 Play 商店审批，应该很快就可以提供给用户了。

这种数据收集是否会在隐名模式下默认保持启用还有待观察。我们希望不是。尽管如此，拥有选择退出的权利可以解决一些隐私问题。

* * *

## 更新 3:小米正在更新其 mi 浏览器和 Mint 浏览器，以澄清其匿名数据收集切换

虽然小米确实通过新的设置切换解决了隐私问题，但实际情况是切换所用的语言具有误导性，达到了与所写的相反的效果。正如 [*安卓权威*指出的](https://www.androidauthority.com/xiaomi-mi-browser-privacy-1120707/),“*增强隐姓埋名模式*”开关说:“*隐姓埋名模式开启*时不会上传汇总数据统计”，这让用户相信打开开关会让这种说法成真。但事实并非如此。措辞反映了开关的当前状态，而不是通过扳动开关来改变的对/错陈述。

*旧行为*

现在，小米更新了 mi 浏览器和 Mint 浏览器，在这个 toggle 上有了更好的语言。这个开关现在被称为“*帮助我们改进 Mi/Mint 浏览器*”，附带的文本显示“*打开，以便在微服模式打开*时与我们共享使用统计”，当你翻转开关时，文本保持不变。这对于设置的目的和活动状态更加清楚。

*新行为*

在这两个版本中，如果您不希望在匿名模式下收集数据，则开关需要处于关闭状态。只是文本发生了变化，以更好地反映状态。两种浏览器的新更新正在被推送到谷歌 Play 商店。