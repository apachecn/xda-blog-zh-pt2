# [更新:来自网飞的声明]网飞应用程序目前对根用户/解锁用户不可用

> 原文：<https://www.xda-developers.com/netflix-app-currently-unavailable-for-rootedunlocked-users/>

**更新** **下午 5:50 CT:**网飞已经[确认](http://www.androidpolice.com/2017/05/13/netflix-confirms-blocking-rootedunlocked-devices-app-still-working-now/)到 *AndroidPolice* 他们确实在阻止 rooted 或解锁 bootloaders 的用户下载 Play Store 应用。他们提到他们使用谷歌的 Widevine DRM，尽管我们的测试显示 Play Store 列表似乎被 SafetyNet API 屏蔽了。他们最新的 5.0.4 版本在从第三方下载应用程序并安装后，似乎也能在根/解锁设备上保持完整的功能。以下是提供给 *AndroidPolice* 的完整声明:

*“在我们最新的 5.0 版本中，我们现在完全依赖 Google 提供的 Widevine DRM 因此，许多未经谷歌认证或被改动的设备将不再与我们的最新应用程序兼容，这些用户将不再在 Play Store 中看到网飞应用程序。”*

* * *

近年来，我们听说越来越多的应用程序阻止根用户，甚至所有解锁 bootloaders 的用户。谷歌的安全网服务使这种封锁广泛传播，像 Pokémon Go 这样的应用程序禁止根用户玩游戏，这一点我们在时间已经报道过了。

对于 snapchat 和 Pokémon Go 这样的应用程序，人们可以提出这样的论点，即自定义 ROM 或 root 方法将允许玩家或用户从本质上违反游戏或服务的“精神”，例如保存 Snapchat 图片或捕捉几英里外的 Pokémon。网飞最近推出了多平台离线下载，允许用户下载电影并离线观看。虽然这被普遍认为是一个很好的举措，但它也可能与我们现在看到的情况无关:网飞的最新版本对根用户来说是不可见的，因为如果你的设备解锁，它似乎不会出现在 Play Store 上。

我用两台设备测试了这个，其中一台运行的是未锁定的引导程序，但有一个普通的非根 ROM，另一台设备运行的是 Magisk。即使我安装了应用程序，也无法在 Play Store 上找到网飞。启用 Magisk Hide 后，我就可以在我的一台设备上找到该列表。**果然不出所料，** **如果你有 Magisk 并开启 Magisk Hide，应该没问题。**

与此同时，我们在 reddit 上看到来自不同用户的其他报告，称[兼容性问题](https://www.reddit.com/r/GooglePixel/comments/69h72b/us_netflix_no_longer_compatible/?st=j2nh7kes&sh=b1bb9fc4)似乎与根/解锁设备块无关。我们不知道这是网飞的一个永久性的、有意识的决定，还是一个将被纠正的错误或问题。但是，如果您在设备上下载网飞时遇到问题，您的设置可能就是问题所在。

你认为这是网飞有意识的决定，还是会很快得到解决？下面报数！

* * *

[**Via: r/Android**](https://www.reddit.com/r/Android/comments/6avu1s/netflix_app_gone_for_romed_and_or_rooted_devices/?st=j2nha3t2&sh=99da1e5a)