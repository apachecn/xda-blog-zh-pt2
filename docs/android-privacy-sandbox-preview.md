# 谷歌发布首个 Android 隐私沙盒预览版，主题为 API

> 原文：<https://www.xda-developers.com/android-privacy-sandbox-preview/>

谷歌一直在 Chrome 浏览器中试验新的定向广告方法，旨在取代几十年来推动在线广告(和侵犯隐私)的跨站点浏览器 cookies。该公司的最新尝试是今年 1 月推出的 Topics API ，现在谷歌[开始将其扩展到浏览器之外](https://www.xda-developers.com/google-details-sdk-runtime-design-proposal-android-privacy-sandbox/)。

谷歌周四发布了首个 Android 隐私沙盒开发者预览版，由两个部分组成。第一个是新的 SDK 运行时，旨在供开发人员使用，而无需授予与主机应用程序相同的权限级别——谷歌表示，未来这可以用于更多类型的 SDK 和开发库，但目前仅限于广告。Privacy Sandbox 的第二个组件是 Topics API，听起来类似于 Google Chrome 中的 Topics API。从本质上讲，该系统不是将使用数据发送到外部服务器进行广告定位，而是挑选出您可能感兴趣的主题，并允许广告基于这些主题进行定位。

谷歌表示，新的预览版可以用来测试主题 API 和检索测试值，以及运行一些示例应用程序。与通常的 Android 测试版和开发者预览版不同，这里没有任何让非开发者兴奋的东西——其他人都更适合使用[常规 Android 13 测试版](https://www.xda-developers.com/android-13-beta-1-released/)。

隐私沙盒开发者预览版基于 Android 13 测试版。它在 Android 模拟器中作为[选项提供，以及 Pixel 6 Pro、Pixel 6、Pixel 5a (5G)、Pixel 5、Pixel 4 和 Pixel 4a 的系统图像。你必须](https://developer.android.com/design-for-safety/privacy-sandbox/setup)[下载并手动刷新版本](https://developer.android.com/design-for-safety/privacy-sandbox/download)才能在 Pixel 手机上试用，因为谷歌只打算让开发者试用。

看到主题 API 在 Chrome 中全面推出之前就出现在 Android 上有点令人惊讶——在网络浏览器中的测试从 4 月份开始。谷歌 2019 年最初的 Chrome 隐私沙盒提案因其隐私问题受到了电子前沿基金会(EFF) 、 [DuckDuckGo](https://spreadprivacy.com/block-floc-with-duckduckgo/) 和其他团体的[的批评。尽管对新主题 API 提议的抱怨没有达到同样的程度，但它仍然归结为同一个想法:在你的设备上运行有针对性的广告算法。](https://www.eff.org/deeplinks/2021/03/googles-floc-terrible-idea)

**来源:** [安卓开发者](https://developer.android.com/design-for-safety/privacy-sandbox/program-overview)