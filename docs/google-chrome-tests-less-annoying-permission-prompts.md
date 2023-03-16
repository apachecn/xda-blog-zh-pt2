# 谷歌个人电脑浏览器测试不那么烦人的权限提示

> 原文：<https://www.xda-developers.com/google-chrome-tests-less-annoying-permission-prompts/>

谷歌最近一直在努力应对烦人的通知请求和许可提示。在 Chrome 80 中，谷歌为启用[“更安静”的通知提示](https://www.xda-developers.com/google-chrome-annoying-notification-prompts/)做了一个切换。我们看到这个[在 Chrome 84](https://www.xda-developers.com/google-chome-84-abusive-notifications-permissions-requests/) 中更进一步，辱骂性的提示被自动最小化。现在，谷歌正在测试一项功能，这项功能可以让其他请求变得不那么烦人。

像位置这样的许可请求仍然很烦人。很多网站在没有必要的时候会征求你的同意。一个网站只需要我的 5 位数邮政编码，却要求访问我的位置，这有点过分。谷歌正在测试一项功能，将这些权限请求放在一个不太显眼的位置。

上图显示了权限请求前后的情况。顶部的截图显示了我们在用 Chrome 浏览网页时都见过数百次的典型弹出窗口。底部的屏幕截图显示了启用了新功能标志的相同提示。该提示不会在网页内容上弹出，而是在地址栏显示一个“芯片”。

谷歌正在测试这项名为 *#permission-chip* 的功能，可以在*chrome://flags # permission-chip 上获得。*标志描述写着“启用在地址栏中使用芯片的实验许可提示。”这项功能适用于 macOS、Windows、Linux 和 Chrome OS。该标志出现在 Chrome 版本 84.0.4140.1 中，但权限芯片功能本身被我们的线人发现在金丝雀频道中与 Chrome 85.0.4159.0 一起工作。

有点可笑的是，谷歌做了这么多工作来尽量减少这些提示有多烦人。毕竟，他们一开始就让 Chrome 中的提示成为可能。但是很多网站都正确使用通知和权限提示，所以很高兴看到谷歌去追那些不正确的网站。

*感谢 XDA 资深会员 [Some_Random_Username](https://forum.xda-developers.com/member.php?u=8234677) 的截图！*