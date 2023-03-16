# 谷歌在 Chrome 浏览器中禁用 WebUSB，引发网络钓鱼担忧

> 原文：<https://www.xda-developers.com/google-disables-chrome-webusb/>

# 谷歌在 Chrome 浏览器中禁用 WebUSB，引发网络钓鱼担忧

Chrome 中的 WebUSB 允许网站直接连接 USB 设备。研究人员发现它可能被用于网络钓鱼攻击，所以谷歌禁用了它。

如果你在互联网上生活了很长时间，网络钓鱼是一个主要问题。有很多方法可以通过软件来防止网络钓鱼攻击，但最好的方法之一是硬件 USB keys。即使攻击者知道您的用户名和密码，身份验证设备也可以保护您。至少他们会这么告诉你。一对研究人员证明了这些设备并不是不可战胜的。Chrome 的一个叫做 WebUSB 的特性使得绕过保护成为可能。

WebUSB 是允许网站直接连接 USB 设备的功能；[在 Chrome 61](https://www.xda-developers.com/google-chrome-61-beta-web-share-api/) 中加入。攻击者可以通过附带的网站使用该功能，说服某人输入他们的用户名和密码，并将其直接发送到身份验证设备以解锁帐户。显然，Chrome 是这个星球上最流行的浏览器，这是一个相当严重的漏洞。

当被问及此事时，谷歌的安全产品经理表示，他们知道这一情况。他们认为这种类型的攻击是一种边缘情况，但他们正在努力解决这个问题。目前，谷歌已经完全禁用了 WebUSB 功能。这是昨天在铬中发现的。如果用户真的想重新启用该功能，他们可以应用命令行标志。目前，通过移除移动部件，问题已经得到解决。

* * *

[**来源:连线**](https://www.wired.com/story/chrome-yubikey-phishing-webusb/) [**来源:铬**](https://bugs.chromium.org/p/chromium/issues/detail?id=819197#c11)