# Android P 终于在 Chrome 和其他浏览器中实现了自动填充

> 原文：<https://www.xda-developers.com/android-p-autofill-browsers/>

# Android P 终于在 Chrome 和其他浏览器中实现了自动填充

Android 自动填充引擎在 Chrome 等浏览器中不起作用。这将不再是 Android P 的问题，也不需要你使用特殊的辅助服务。

当宣布 Android 8.0 Oreo 将带来备受期待的自动填充 API 时，Android 社区中的许多人都欢欣鼓舞。这意味着 LastPass、1Password、Dashlane 等密码管理器可以用来登录 Android 上的应用程序。它在大多数情况下工作良好，但有时自动填充请求没有被检测到。这种实现还会阻止您使用这些应用程序登录网站。Chrome、Microsoft Edge、Samsung Browser 和 Firefox 使用自定义渲染来提高性能，但会阻止自动填充引擎正常工作。这将不再是 Android P 的问题，也不需要你使用特殊的辅助服务。

一些密码管理器能够通过使用可访问性服务绕过这个限制。对于那些新手或对未知设置有疑虑的人来说，这不是很用户友好，但它确实有效。谷歌意识到这不是让密码管理器在浏览器中工作的最佳方法，所以他们一直在研究一种在下一个版本的 Android 中实现这一点的方法。本周早些时候，我们看到了[发布的第一个 Android P 开发者预览版](https://www.xda-developers.com/everything-new-android-p-developer-preview/)。许多开发人员已经开始修补新的变化。

有了 Android P，不再需要手动启用辅助功能服务的过程。谷歌正在默认启用它。因此，它不仅减少了最终用户必须启用的步骤(有些人一开始就担心启用)，而且还极大地减少了设备上的 CPU 使用率。Dashlane 的开发人员很快开始使用 Android P Developer Preview 1 开发原型。事情现在就像你在谷歌的 Chrome 浏览器中所期望的那样。

我们还被告知，当使用 Dashlane 的应用内气泡功能时，它很可能与其他移动浏览器如微软 Edge 和三星浏览器一起工作。他们希望在 Firefox 中也能实现这一功能，但目前我们还无法在这款浏览器上访问网页。

* * *

[**来源:Dashlane**](https://blog.dashlane.com/android-p-autofill/)