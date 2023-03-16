# [更新 3:现在稳定] Android Q 将把谷歌 Chrome 集成到数字福利中

> 原文：<https://www.xda-developers.com/android-q-google-chrome-digital-wellbeing/>

**更新 3 (10/18/19 @美国东部时间上午 11:55):**谷歌 Chrome 的深度数字福利集成现已在稳定频道上线。

**更新 2(美国东部时间 2019 年 10 月 1 日上午 10:25):**Chrome 中的数字福利将很快进入稳定渠道。

**更新 1(美国东部时间 2019 年 7 月 31 日下午 1:05):**Android Q 中用于 Chrome 的数字福利工具现已在 Canary 上线。

科技公司不时会提出新的想法和趋势，每个人都可以支持。2018 年不仅是分数的一年，也是“[数字福祉](https://www.xda-developers.com/samsung-galaxy-s10-new-software-features/)”的一年。谷歌和苹果等主要厂商认为，用户能够控制和监控自己的智能手机使用情况至关重要。最新版本的 Android 和 iOS 现在可以让你限制特定应用的使用，让你的手机使用起来不那么有吸引力，限制一些服务，等等。显然，谷歌正在 Android Q 中让这一功能变得更加有用。

根据来自谷歌的报道，即将到来的 Android 版本将把谷歌 Chrome 整合到数字福利中。 [Chromium Gerrit 暗示](https://chromium-review.googlesource.com/q/chromeshine)这个功能已经在工作中两个月了，代号为“Chromeshine”由于这项新功能，你不仅可以限制某些应用，还可以限制网站。谷歌将使用[页面视图观察者](https://chromium-review.googlesource.com/c/chromium/src/+/1415931) API 从谷歌浏览器请求信息。同样重要的是，它不会在隐姓埋名模式下追踪任何东西。目前还没有确认，但谷歌很可能会将访问量最大的网站纳入数字健康仪表板。你可以在下面看到这个功能的一些截图。

如果你运行的是 Android Q，你可以通过进入**设置>隐私**并启用“连接到数字福利”来启用该选项。我们已经验证了在运行[泄露的 Android Q 版本](https://www.xda-developers.com/android-q-gestures-back-button/)的 Pixel 3 XL 上就是这种情况。不幸的是，数字福利整合似乎还没有发挥作用。

不幸的是，谷歌*不会*允许第三方应用程序访问这些信息。据一位开发者称，要让每个人都能使用这个 API，还需要更多的安全改进。目前，他们正试图通过利用谷歌浏览器提供的敏感信息来限制应用程序滥用 API。该功能将只在 Android Q 中可用，[离](https://www.xda-developers.com/android-q-privacy-permission-controls/)不远了。

**Via: [9to5Google](https://9to5google.com/2019/02/20/chrome-android-q-digital-wellbeing/) |来源:[Chromium Gerrit](https://chromium-review.googlesource.com/q/chromeshine)**

* * *

## 更新 1:住在金丝雀

Android Q 中用于 Chrome 的数字健康工具现已在金丝雀频道推出。这些新工具不仅允许你为 Chrome 浏览器应用程序本身设置限制，还允许你为单个网站设置限制。在 Digital Wellbeing 的 Chrome 金丝雀页面上，有一个“显示网站”按钮。点击它会显示一个网站列表以及你在上面花了多长时间。您可以点击沙漏图标来设置应用程序计时器。

要在 Chrome Canary 上得到这个，你需要启用一个标志。它被称为“与数字福利分享使用统计”，可以在 chrome://flags/#usage-stats 找到。只有在 Android Q 上，该标志才有效。

**Via:[Chrome Story](https://www.chromestory.com/2019/07/digital-wellbeing-chrome-share-usage/)**

* * *

## 更新 2:很快稳定

创建了一个新的提交，上面写着“默认启用 chromeshine”Chromeshine 是 Chrome 数字福利集成的代号，已经测试了一段时间。7 月，整合通过一面旗帜进入了加那利海峡。现在，在最新的 Canary nightly 构建中，该特性是默认启用的。这意味着我们应该看到它在未来几周内进入稳定渠道。

**来源:[铬革里特](https://chromium-review.googlesource.com/c/chromium/src/+/1832290)**

* * *

## 更新 3:现在稳定

正如几周前承诺的那样，谷歌 Chrome 与数字福利的深度集成现已在稳定频道上线。在 Chrome 版本 77.0.3865.116 上，你可以为特定网站添加计时器。进入数字福利设置，找到 Chrome。您将看到一个“显示站点”的选项(如上面的更新 1 所示)。当您使用网站时，它们会显示在列表中。数字健康显示了你在网站上花了多少时间。点击沙漏图标创建计时器。

[app box Google play com . Android . chrome & HL = en]