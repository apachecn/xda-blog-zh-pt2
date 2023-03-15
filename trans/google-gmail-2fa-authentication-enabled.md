# 不到 10%的 Gmail 用户启用了双重认证

> 原文：<https://www.xda-developers.com/google-gmail-2fa-authentication-enabled/>

如果你不使用 Gmail 的双因素认证，你不是唯一的一个。在本周举行的 Usenix Enigma 2018 安全会议上，谷歌软件工程师 Grzegorz Milka 透露，超过 90%的活跃 Gmail 用户没有在他们的账户上启用双因素认证，而 10%的*激活了*的用户在弄清楚如何使用发送到他们手机的短信验证码方面有困难。

当被问及谷歌为什么不默认启用双因素认证时，米尔卡说:“这关系到如果我们强迫他们使用额外的安全性，我们会赶走多少人。”“答案是可用性。”

双因素身份验证(2FA)是一种在登录过程中增加额外一层身份验证的协议。当你在一个在线服务上启用 2FA 并输入你的用户名和密码时，在你被允许登录之前，系统会提示你输入额外的信息——通常是通过短信或类似 [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=en) 的应用程序随机生成的一串字母和数字。其他形式的 2FA 需要一个由 FIDO 联盟认证的特殊硬件令牌(通常以 USB 密钥卡的形式，如 [Yubico 的 yubi key](https://www.yubico.com/)), FIDO 联盟是一个负责开发互操作安全标准的行业联盟。

那么为什么人们不用它呢？根据一些研究人员的说法，他们不信任它。在网络安全公司 Sophos 于 2016 年进行的一项研究中，超过 15%的受访者提到了对 2FA 的隐私担忧。他们的担心不是没有根据的:一些专家指出了基于 SMS 的 2FA 的弱点，指出了被设法伪造电话号码的攻击者拦截的风险。

就谷歌而言，它让企业客户主动禁止弱短信认证令牌，并正在研究替代方案。

10 月，它为 2FA 推出了一种新方法，用“ [Google Prompt](https://support.google.com/accounts/answer/6361026?co=GENIE.Platform%3DAndroid&hl=en) ”取代了短信，这是一种内置于 Android 上 Google Play 服务和 iOS 上 Google app 的验证屏幕。它不需要你输入密码，而是使用诸如你手机的地理位置和一天中的时间来验证你的身份。该公司还推出了一项新服务，[高级保护程序](https://landing.google.com/advancedprotection/)，要求高知名度的账户使用基于硬件的 USB 2FA 安全密钥，而不是谷歌提示或短信。

“我们发现的一个事实是，人们不会接受比他们认为自己需要的更多的安全性，”谷歌身份系统团队的经理马克·里舍在 7 月的一次采访中告诉《The Verge*。“作为一家大规模的消费者互联网提供商，我们希望找到正确的平衡。”*

* * *

[**来源:登记簿**](https://www.theregister.co.uk/2018/01/17/no_one_uses_two_factor_authentication/)