# 这就是为什么谷歌浏览器正在尝试隐藏完整的网址

> 原文：<https://www.xda-developers.com/google-chrome-hiding-full-url-experiment/>

我们知道，谷歌已经尝试在 Chrome 浏览器的地址栏中隐藏完整地址几个月了。毕竟，谷歌已经在开源的 Chromium 项目中公开开发了这些变化，正如今年早些时候由 [*AndroidPolice*](https://www.androidpolice.com/2020/06/15/google-confirms-experiment-to-remove-full-address-from-url-bar-in-chrome-details-opt-out-mechanism/) 发现的那样。在今天发布的一篇[博客文章中，谷歌提供了更多关于其实验 Chrome 在桌面上显示 URL 的计划的细节。据谷歌称，其目标是了解显示(或隐藏)网址如何帮助用户避免网络钓鱼和社会工程攻击。](https://blog.chromium.org/2020/08/helping-people-spot-spoofs-url.html)

通过检查 URL，您可以快速识别和确定网站的真实性。然而，许多用户并不熟悉完整 URL 中的所有参数，攻击者可以利用这一点来欺骗用户。谷歌[指出一项研究](https://research.google/pubs/pub49166/)发现，如果一个误导性的品牌名称出现在一个 URL 路径中，超过 60%的用户会被该 URL 愚弄。

作为针对非企业注册设备的谷歌 Chrome 86 实验的一部分，谷歌将为一些用户隐藏部分 URL 默认情况下只保留域名。一旦你悬停在它上面，网址将完全展开。用户也可以右键单击地址栏，启用“总是显示完整的 URL”选项，如果他们喜欢总是看到他们访问的每个网站的 URL 的完整路径。

谷歌没有说这个实验会持续多久，但如果你没有被随机分配到实验组，出于某种原因想成为其中的一员，你可以安装 Chrome Canary 或 Dev，打开 chrome://flags，并启用以下标志:

第三个标志将选择性地显示页面加载的完整 URL，直到您与页面进行交互。

希望谷歌能尽快完成这个实验，并决定如何最好地在地址栏中显示网址。如果他们选择默认隐藏完整的 URL，我们希望他们保留总是显示完整 URL 的选项。