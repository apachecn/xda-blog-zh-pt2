# Chrome 将锁定 Gamepad API，因为它可以用于跟踪

> 原文：<https://www.xda-developers.com/chrome-gamepad-api-changes/>

几年来，大多数网络浏览器都提供了 Gamepad API，允许网络应用和游戏访问物理游戏控制器。然而，除了它的预期用途之外，API 还可以用来跟踪网络上的人，这就是为什么 Firefox 和其他一些浏览器限制了它的使用。谷歌现在也紧随其后，对 Chrome 处理游戏手柄的方式做了一些改变。

早在 2012 年，随着 Chrome 21 的发布，Gamepad API 首次出现，Firefox 等其他浏览器后来也实现了它。[苹果在 2017 年将其添加到 Safari 10.1 中](https://webkit.org/blog/7477/new-web-features-in-safari-10-1/)，这就是 GeForce Now 和 Google Stadia 等游戏流媒体平台如何能够[在没有 App Store 应用的情况下支持 iPhones 和 iPads】。Gamepad API 为当前连接的任何 Gamepad 提供了一个 ID，以及一个受支持的按钮和轴的列表——当这些数据被记录下来并与其他收集的数据进行比较时，它可以用于在不同的网站上跟踪某人。这种做法被称为指纹识别。](https://www.xda-developers.com/nvidia-geforce-now-ios-safari-browser-bypasses-apple-app-store/)

谷歌有两个用 Gamepad API 打击指纹识别的计划。首先，除非当前网站支持 HTTPS，否则 API 将不再工作，这与火狐自 2020 年以来所做的事情相匹配。谷歌还将在 chrome://flags 中添加一个永久的#restrict-gamepad-access 标志，以恢复这一变化，主要针对那些希望在本地页面或服务器上测试自己游戏而不设置 SSL 证书的开发者。第二，API 在嵌入式框架中的行为会有所不同，尽管具体的实现还没有出来。

似乎还没有任何网站或跟踪脚本使用 Gamepad API 进行指纹识别的重大案例，因为它需要连接一个控制器来返回任何数据，这大大限制了收集数据的范围。尽管如此，网络浏览器应该尽可能的安全，通过 Gamepad API 限制数据收集是朝着这个方向迈出的又一步。

谷歌尚未决定更新后的 Gamepad API 行为何时会在 Chrome 中向所有人推出。

**来源:** [谷歌集团](https://groups.google.com/a/chromium.org/g/blink-dev/c/B1QUuICApvc/m/RRxZLqG4HQAJ)