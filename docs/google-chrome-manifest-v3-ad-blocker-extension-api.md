# 谷歌的 Manifest V3 将改变广告拦截 Chrome 扩展的工作方式:是削弱它们，还是为了安全？

> 原文：<https://www.xda-developers.com/google-chrome-manifest-v3-ad-blocker-extension-api/>

[谷歌 Chrome](https://www.xda-developers.com/google-chrome-secure-cookie-controls-anti-fingerprinting-history-manipulation/) 是目前市场上最受欢迎的跨平台网络浏览器，[声称截至 2019 年 5 月，全球浏览器使用份额](http://gs.statcounter.com/browser-market-share)为 62.7%，苹果的 Safari 以 15.89%的份额位居第二，Mozilla 的 Firefox 声称为 5.07%。由于其巨大的份额，谷歌 Chrome 对其平台进行的最小改变最终都会影响到全球数百万用户。因此，当谷歌以谷歌 Chrome 扩展清单 V3 的形式宣布下一个扩展清单版本时，我们知道我们将面临一些重大变化，特别是当谷歌在 Chrome 本身中内置一个内容拦截器 API 时。

## 什么是清单 V3？

如果你是 Chrome 的活跃用户，你无疑会使用一些扩展。扩展是使用浏览器提供的 API 定制浏览体验的小软件程序，允许用户定制功能和行为，以适应他们的个人需求和偏好。这些扩展主要通过 [Chrome 网上商店](http://chrome.google.com/webstore)发布，那里有超过 180，000 个扩展。

自去年年底以来，谷歌一直致力于“清单 V3”，这是一组对 Chrome Extensions 平台的拟议更改，可以被归类为“突破性更改”。正如清单 V3 的[公共讨论文档所述，扩展清单版本是一种将某些功能限制到某类扩展的机制。这些限制可以是最低版本或最高版本的形式。限制到最低版本允许较新的 API 或功能仅对较新的扩展可用，而限制到最高清单版本允许较旧的 API 或功能逐渐被废弃。](https://docs.google.com/document/d/1nPu6Wy4LWR66EFLeYInl3NzzhHzc-qnk4w4PX-0XMw8/edit#)

更简单地说，一个新的清单版本允许 Chrome 将 API 和功能限制在这个新的清单版本上，以迫使扩展开发者从某些旧的 API 迁移出来，因为它们对用户体验有负面影响。从安全、隐私和性能的角度来看，在 Manifest V3 中实现扩展理论上应该提供更强的保证。

虽然清单 V3 中列出了广泛的变化，但最有争议的变化与谷歌的决定有关，即限制现有*[chrome . webrequest](https://developer.chrome.com/extensions/webRequest)*API 中存在的阻止能力(并将 API 的重点放在观察上，而不是阻止)，然后通过新的*[chrome . declarativenetrequest](https://developer.chrome.com/extensions/declarativeNetRequest)*API 来提供这些阻止能力。这一特殊的变化激怒了社区[，因为它最终针对著名的广告拦截扩展](https://bugs.chromium.org/p/chromium/issues/detail?id=896897) [uBlock Origin](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm?hl=en) 的广告拦截机制，并直接影响其 1000 多万用户。

在我们解决这个问题之前，让我们来看看 *webRequest* API 与*declarativeNetRequest*API 的比较。

## Web 请求 API 和声明性网络请求 API

### 现状

Web Request 的官方描述对 API 的描述如下:

```
Use the chrome.webRequest API to observe and analyze traffic and to intercept, block, or modify requests in-flight.
```

通过 Web 请求，Chrome 将网络请求中的所有数据发送给监听它的扩展。然后，扩展有机会评估请求，并指示 Chrome 如何处理请求:允许、阻止或修改后发送。

按照事件的顺序来理解当扩展使用 Web 请求 API 时会发生什么。当安装了 Web 请求扩展的用户点击一个链接时，Chrome 会在请求到达服务器之前通知该扩展已经发出了一个数据请求。扩展可以选择在这个阶段修改请求。然后服务器响应，但是响应再次通过扩展，扩展可以决定是否需要修改响应。然后 Chrome 最终呈现页面，用户能够查看他的点击操作的结果。

随着 Chrome 将网络请求中的所有数据移交给用户，使用 web 请求 API 的扩展可以读取和修改用户在 Web 上做的任何事情。因此，虽然像 uBlock Origin 这样的内容拦截器明智地利用了这种 API 的潜力，但谷歌声称，其他恶意扩展也滥用了这种 API 来获取用户的个人信息。根据谷歌的数据，自 2018 年 1 月以来，42%的恶意扩展使用了 Web 请求 API。谷歌还声称，该 API 存在“显著的性能成本”，因为它的阻塞版本需要一个持久的、通常长期运行的进程，这与“懒惰”进程根本不兼容。

在 Manifest V3 中，Google 提议以阻塞形式限制这个 API。作为替代，Google 正在提供声明性的 Net Request API。

### 今后

Declarative Net Request 的官方描述对 API 的描述如下:

```
The chrome.declarativeNetRequest API is used to block or modify network requests by specifying declarative rules.
```

使用声明性网络请求，Chrome 不需要向监听扩展发送关于请求的所有信息。相反，该扩展向 Chrome 注册了规则，这些规则预先告诉浏览器在看到特定类型的请求时应该做什么。

扩展预先指定了它的规则。然后，浏览器(而不是扩展)将用户的请求与该规则进行匹配，浏览器也执行该操作，随后呈现页面。谷歌提到，这使他们能够确保效率，因为他们可以控制决定结果的算法，并可以防止或禁用低效的规则。它还向最终用户提供了更好的隐私保证，因为网络请求的细节不会暴露给扩展。由于不再需要持久和长期运行的流程(因为规则是预先注册的)，Google 声称这种方法还带来了性能改进，将使扩展在资源受限的平台上更加可行。

声明性网络请求对清单 V2(当前)和清单 V3 都可用，但它将是 Google 允许在清单 V3 中修改网络请求的主要方式。

### 争议

谷歌的变化似乎是有意义的，直到你听到故事的另一面，主要是广告拦截器。这种特殊的 API 迁移被视为谷歌消灭广告拦截器的方式，因为它从根本上改变了最受欢迎的广告拦截器之一的工作方式。这与“理论”相联系，即谷歌更多地从商业角度而不是从用户安全角度推动这一变化。毕竟，谷歌严重依赖广告收入，广告拦截器被视为谷歌客户在这方面的直接威胁，正如 [Alphabet 的 2018 年 SEC Form 10-K 文件](https://www.sec.gov/Archives/edgar/data/1652044/000165204419000004/goog10-kq42018.htm#sA4821B00C1F65450B0EF326C4BE12DCC)(通过)所揭示的那样:

新的和现有的技术可能会影响我们定制广告的能力和/或屏蔽在线广告，这将损害我们的业务。

技术的发展使得定制广告变得更加困难，或者完全阻止广告的显示，一些在线服务提供商已经集成了可能会损害第三方数字广告核心功能的技术。我们谷歌的大部分收入来自支付给我们的在线广告展示费用。因此，这些技术和工具可能会对我们的经营业绩产生不利影响。

谷歌不得不[发布一份声明](https://security.googleblog.com/2019/06/improving-security-and-privacy-for.html)来解决这个问题，重申其立场，这一变化是为了用户隐私的利益，而不是对广告拦截器的直接攻击:

我们不会阻止广告拦截器的发展，也不会阻止用户拦截广告。相反，我们希望帮助开发者，包括内容拦截器，以保护用户隐私的方式编写扩展。

需要提到谷歌 Chrome 上最受欢迎的两种广告拦截器: [uBlock Origin](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm?hl=en) 和 [Adblock Plus](https://chrome.google.com/webstore/detail/adblock-plus-free-ad-bloc/cfhdojbkjhnklbpkdaibdccddilifddb?hl=en) ，这两种方法都采用不同的方法来实现相同的内容拦截效果。uBlock Origin 很大程度上依赖于 Web Request API，社区多年来一直偏爱这种扩展。Adblock Plus 和其他内容阻止扩展也依赖于 Web 请求的阻止部分，因此对该 API 的更改最终将至少在某种程度上影响大多数内容阻止程序。

谷歌反对 Web Request 的努力将从本质上扼杀当前格式的 uBlock Origin，这确实会影响很多用户。虽然没有忠诚度的用户(也不打算为广告拦截是如何实现的而烦恼)会找到具有自身缺点的替代解决方案，但忠诚者和爱好者将不可能提出新的过滤引擎设计来绕过网站最终将提出的各种技术，以打击特定 API 上的广告拦截器。

声明性网络请求也被提议成为一个相当有限的过滤引擎，因为最初[计划](https://developer.chrome.com/extensions/declarativeNetRequest#property-MAX_NUMBER_OF_RULES)对每个扩展的静态过滤规则(在安装期间声明的规则)有 30，000 个规则限制；和 5，000 个规则限制(可在安装后添加的规则)。任何多余的规则都将被忽略，这是一个问题，因为 Adblock Plus 的 EasyList 本身有 70，000 条规则，而 uBlock Origin 可以配置为运行超过 100，000 条规则。在最初遭到社区的强烈反对后，[谷歌做出回应](https://security.googleblog.com/2019/06/improving-security-and-privacy-for.html)，承诺将静态规则限制从每次扩展 30，000 条改为全球最多 150，000 条。这样做的副作用是阻止用户将其他规则繁重的脚本与广告拦截器结合使用，因此用户将不得不根据自己的偏好进行调整。

除了有限的过滤限制，声明性网络请求[只能重定向到静态 URL](https://www.ctrl.blog/entry/removing-webrequest-api.html)，因此不支持模式匹配。uBlock Origin 严重依赖模式匹配，扩展开发者[声明不可能改进](https://twitter.com/gorhill/status/1134127701583904770)他的扩展的匹配算法来满足 API 的要求。API 还需要一个完整的扩展更新来简单地更新过滤器列表，考虑到这些过滤器列表更新的[频率](https://github.com/easylist/easylist/commits/master)，这将是一个过于频繁的活动。当然，这些更新也取决于谷歌的延期审查标准和程序。

另一方面，谷歌一直坚持其立场，即从安全角度出发，它打算放弃 Web Request，因为 Web Request API 在其当前形式下过于强大，为滥用留下了非常广阔的空间。这种滥用不仅仅是理论上的，因为 Google 已经提到 42%的恶意扩展滥用了这个 API。出于类似的原因，苹果 Safari 的[内容拦截器 API](https://developer.apple.com/documentation/safariservices/creating_a_content_blocker) 的设计类似于声明式网络请求，因为流氓开发者可以利用的空间较小。在被削弱的 Web 请求上，网络请求仍然是可观察到的，但是它们需要相关主机上的权限。在 Manifest V3 中，主机权限也发生了显著的变化，它们不再能够在安装时以一揽子的方式被授予。

谷歌也将性能开销作为转换的动力。对网络请求的评估发生在扩展的 JavaScript 线程中，这可能会影响性能。作为反驳，uBlock Origin 的开发者提到，即使有多达 140，000 个静态过滤器要执行，他的扩展[也不会导致任何显著的性能损失](https://twitter.com/gorhill/status/1134127719502045191)。据称，所产生的成本可以很容易地通过阻止从远程服务器下载并因此不被浏览器处理的资源来收回。

即使谷歌没有使用这种推理，反对网络请求的一个理由也可以是广告拦截的效率。对于 Web 请求，如果一个扩展没有及时响应(因为延迟或崩溃)，网络处理请求显然是允许的，这让广告逃过广告拦截器。另一方面，声明性 Net 请求不会有这个缺点。相反，如果广告没有被静态规则捕获，它们就会通过，这种情况经常发生。

## 结论

从上面的解释中可以清楚地看到，声明性 Net Request 并不是 Web Request API 的阻塞功能的 1:1 功能克隆，当扩展开发人员的辛勤工作被这样的变化所阻碍时，他们肯定会感到恼火。但是谷歌的理由也有分量——网络请求太强大了，为了用户群体的更大利益(包括普通用户和狂热爱好者)，它的权力需要被削弱。

向声明式网络请求的转变也可能是一个积极的公关举措——毕竟，谷歌正在 Chrome 上添加一个内置的内容拦截器 API！但是由于新的 API 有它自己的严格限制，社区理所当然地认为这是对他们翅膀的一次修剪。在理想的情况下，谷歌应该在推出新的 API 之前探索像 uBlock Origin 这样的广告拦截器的工作原理。按照现在的情况，新的 API 可以进一步放宽规则限制，以适应用户希望使用两个大量过滤扩展的场景。

根据 *[注册表](https://www.theregister.co.uk/2019/06/21/google_chrome_manifest_v3/)* 显示，首批包含清单 V3 变更的 builds 将于 2019 年 7 月起上市。我们希望 Google 在这些构建中考虑到来自扩展开发者社区的反馈。

* * *

特别感谢 XDA 主编米沙·拉赫曼的投入和帮助！

这篇文章错误地将 Adblock Plus 的工作等同于声明性 Net Request API 的工作。该条已作相应修改。Adblock Plus 也将受到删除 Web 请求 API 的阻止功能的影响。