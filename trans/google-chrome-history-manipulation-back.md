# 谷歌 Chrome 将与阻止你返回的恼人网站作斗争

> 原文：<https://www.xda-developers.com/google-chrome-history-manipulation-back/>

# 谷歌 Chrome 将与阻止你返回的恼人网站作斗争

当一个网站不允许你通过“返回”离开页面时，这是非常令人恼火的，谢天谢地，谷歌 Chrome 正在做一些事情。

互联网上最讨厌的事情之一就是劫持你浏览器的网站。不幸的是，这并不是可疑网站的专利。你可能遇到过一个合法的网站，当你点击后退按钮时，它不允许你返回上一页。这是一种非常令人恼火的做法，谢天谢地，谷歌 Chrome 正在对此采取措施。

如果你足够幸运，从未经历过这个问题，这里有一个简单的例子。你在谷歌上搜索某样东西并选择了一个结果，但你意识到这不是你想要的。当你点击后退按钮离开网站时，它只是刷新页面或拒绝返回。离开页面的唯一方法是反复点击后退按钮，或者打开历史记录，选择上一页。

好消息是谷歌已经有了解决方案。根据三人组 [Chromium commits](https://chromium-review.googlesource.com/c/chromium/src/+/1347491) 的说法，谷歌正在打击这些“历史操纵”策略。这些网站就是这样阻止你用后退键离开的。他们操纵你的浏览历史，所以“返回”不会去你期望的地方。

以下是来自[提交 1344199](https://chromium-review.googlesource.com/c/chromium/src/+/1344199) 的描述

*用户无意添加到后退/前进列表的条目被标记为在后续后退按钮调用时跳过。该 CL 仅添加该位，随后的 CL 将基于该位添加度量和干预逻辑。*

Chrome 将开始悄悄地标记这些网站，谷歌将审查这些指标进行分析。该功能最初会被[隐藏在一个旗帜后面，可以在*# enable-skip-redirection-entries-on-back-forward-*ui 中找到。启用后，Chrome 将检测错误条目并完全跳过这些页面。期待这项功能在未来几周内推出。](https://chromium-review.googlesource.com/c/chromium/src/+/1377524)

* * *

[**Via:9 to 5 Google**](https://9to5google.com/2018/12/17/chrome-sites-wont-go-back/)