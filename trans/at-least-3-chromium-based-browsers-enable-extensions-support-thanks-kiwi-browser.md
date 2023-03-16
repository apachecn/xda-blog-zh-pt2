# 多亏了 Kiwi 浏览器，至少有 3 个基于 Chromium 的浏览器支持扩展

> 原文：<https://www.xda-developers.com/at-least-3-chromium-based-browsers-enable-extensions-support-thanks-kiwi-browser/>

开源软件的优势之一是允许主项目分支存在的能力。这些叉子可以采取不同的形式来获得不同的特征。如果事情进展顺利，这些变更和 bug 修复也可以返回到原始项目的上游，然后传递到依赖它的所有其他下游项目。这就是开源的美妙之处，我们很快就会在我们的手机上看到一个引人注目的例子。最近开源的 Kiwi 浏览器的开发者向上游提交的代码现在将使 Chromium forks 更容易在移动设备上启用扩展支持。

Chromium 浏览器是一个[开源项目](https://www.chromium.org/Home)，它是许多网络浏览器的基础，包括谷歌 Chrome、微软 Edge、Vivaldi、Brave 和 Kiwi too。大多数基于 Chromium 的浏览器都提供了一些额外的功能，但是也有一些从根本上改变了用户体验。XDA 资深会员 [arnaud42](https://forum.xda-developers.com/member.php?u=9196003) [的奇异果浏览器属于后一类](https://www.xda-developers.com/kiwi-chrome-browser-dark-theme-ad-blocker/)，具有内置内容拦截器、黑暗模式、背景视频播放、AMP skipper 等功能，而且它是第一批支持 Chrome 的 Android Chrome 浏览器之一[，另一个是 Yandex 浏览器。今年早些时候，Kiwi 浏览器](https://www.xda-developers.com/kiwi-browser-google-chrome-extensions-android/)[开始开源](https://www.xda-developers.com/kiwi-browser-open-source/)，允许其他 Chromium 项目将支持扩展的代码包含到他们自己的项目中。在宣布的时候，开发者提到他们已经在和其他浏览器开发者合作，帮助他们整合 Kiwi 的一些浏览器功能。

正如 Dinsan Francis 发现的那样，arnaud42】已经开始对 Chromium Gerrit 进行错误报告，以便让基于 Chromium 的项目更容易实现扩展。bug 报告中提出的代码可以让 Chromium forks 更容易地启用扩展，而不会影响谷歌 Android 版 Chrome。提交的代码还没有合并到 Chromium 中，澄清一下，没有证据表明谷歌将为 Android 启用 Chrome 的扩展支持。但是仍然有“至少三种猕猴桃变种”在扩展支持下被开发。

> 因此，我们增加了支持扩展或可能尝试这样做的下游玩家的可维护性(例如:微软，当然还有 Kiwi 浏览器，但现在至少有 3 个 Kiwi 的变体正在诞生，包括一个非常非常大的 OEM)

我们要求开发商详细说明所提到的项目，但他们表示他们无法说出这些项目的名称。不管确切的变体是什么，这对消费者来说都是好消息，因为他们很快就会有更多支持扩展的浏览器选择，这反过来会促使其他人也考虑它的实现。

有趣的是， [Chromium Gerrit commit](https://chromium-review.googlesource.com/c/chromium/src/+/2222773) 是由三星的一名工程师提交的，它将改变 Chromium 的构建过程，使其更容易在启用扩展的情况下重新构建 Chromium。然而，我们不认为三星会是 arnaud42 提到的“大型 OEM ”,因为三星互联网浏览器已经支持扩展，尽管能力有限，因为您只能安装 Galaxy 商店批准的扩展。三星仍然会对 arnaud42 提交的代码感兴趣，因为这将使他们更容易将三星互联网浏览器更新为新的 Chromium 版本，例如他们[最近如何将三星互联网从 Chromium 71 更新为 Chromium 79](https://www.xda-developers.com/samsung-internet-11213-adds-option-prevent-sites-stop-going-back/) 。

[appbox xda com . kiwi browser . browser]

* * *

**来源: [Chromium Bug 追踪器](https://bugs.chromium.org/p/chromium/issues/detail?id=1074710)，[Chromium Gerrit](https://chromium-review.googlesource.com/c/chromium/src/+/2222773)**

**故事 Via:[@ _ 丁山](https://twitter.com/_dinsan/status/1266766701649002502)**