# 当您的密码被盗时，Chrome 密码泄漏检测功能会有所帮助

> 原文：<https://www.xda-developers.com/google-chrome-password-leak-detection/>

# [更新:Android too]谷歌 Chrome 增加了密码泄露检测功能，当你的密码泄露时会告诉你

谷歌已经在密码保护方面做了一些工作，并继续通过在 Chrome 中添加密码泄露检测功能来推进这项工作。

**更新(美国东部时间 8/22/19 @ 12:05PM):**Android 版 Chrome 也将提供密码泄露检测。

保持账户安全的责任通常是公司放在用户肩上的。然而，大众使用密码的方式表明，它们并不像它们应该的那样安全。围绕这个问题已经建立了整个行业([密码管理器](https://www.xda-developers.com/4-password-manager-alternatives-to-1password-and-lastpass/)、 [U2F 钥匙](https://www.xda-developers.com/google-titan-security-key-online-security/)等等)，我们实际上应该完全远离密码系统。谷歌已经在这方面做了一些工作，并通过在谷歌 Chrome 浏览器中添加密码泄露检测功能来继续推进这一工作。

一些公司也非常重视安全问题，并在密码泄露时警告用户。谷歌似乎想通过在浏览器层面也这样做来帮助这场运动。首先由 *Techdows* 报道，在 Chromium 问题跟踪器中发现的一个错误导致我们提交了 Chromium Gerrit，这表明 Chrome 中添加了一个开关，可以启用或禁用这一新的密码泄露检测功能。你可以在 chrome://flags 页面中搜索“leak”这个词，在最新的 Chrome 78 Canary build 中试用这个新功能。

一旦启用，谷歌 Chrome 就会显示你在网站上输入的密码是否与谷歌拥有的公共数据泄露信息相匹配。这项功能只对登录谷歌账户的用户可用，但它可以帮助数百万人。如果谷歌 Chrome 检测到用户输入了泄露的密码，他们会看到一个弹出提示，告诉用户该密码已在不安全密码的公共列表中找到。

谷歌浏览器会建议你尽快修改密码。最终，还是要由用户来解决这个问题，但至少他们会被告知这个问题。

**Via:[Techdows](https://techdows.com/2019/08/google-chrome-gets-password-leak-detection-feature.html)**

**来源 1: [铬 Gerrit](https://chromium-review.googlesource.com/c/chromium/src/+/1761605) |** **来源 2: [铬发行跟踪器](https://bugs.chromium.org/p/chromium/issues/detail?id=986298)**

* * *

## 更新:安卓也是

添加到 Chrome 78 Canary 的密码泄露检测功能也将应用于 Android。[最近的提交](https://chromium-review.googlesource.com/c/chromium/src/+/1746251)标题为“[Android]在设置中添加泄漏检测开关”，描述如下:

此 CL 在“设置”>“密码”中添加了一个开关，用户可以通过它禁用密码泄露检查。如果 pref 被管理，此开关被禁用。