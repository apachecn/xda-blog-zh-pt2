# 【更新 2:谷歌账户】Android 现在通过了 FIDO2 认证，允许无密码访问网站和应用程序

> 原文：<https://www.xda-developers.com/android-fido2-certified-passwordless-access/>

**更新 2(美国东部时间 2019 年 8 月 13 日上午 9:50):**谷歌正在 Android 设备上推出 FIDO2 无密码谷歌账户认证。

**更新 1(美国东部时间 2019 年 5 月 7 日下午 1 点 31 分):**谷歌[宣布](https://gsuiteupdates.googleblog.com/2019/05/android-phones-security-key-available.html)这一新功能全面上市，允许你将手机用作两步认证的安全密钥。

生活在无密码的世界是许多科技爱好者梦想的未来。关于这项技术的推进峰值，没有 ETA，也没有进度条，但它的到来是必然的。密码过时，容易忘记，而且通常不安全，[即使你采取了额外的措施](https://www.xda-developers.com/facebook-gave-advertisers-phone-number-2fa/)如双因素认证。像许多即将到来的主要趋势一样，谷歌也是这一趋势的参与者。考虑到这家公司拥有最流行的移动操作系统、网络浏览器和搜索引擎，这一点也不奇怪。过去几年，谷歌一直在与微软和其他科技巨头等合作伙伴一起开发这项技术。昨天，该公司向无密码功能又迈进了一大步。

FIDO 联盟[昨天在世界移动通信大会上宣布【Android 现已通过 FIDO2 认证。如果你以前没有听说过他们，FIDO 联盟是一个致力于并定义无密码认证标准的协会。该联盟的成员包括谷歌、脸书、GitHub、Dropbox、易贝等等。FIDO Alliance 与来自世界各地的合作伙伴一起，在过去几年中一直致力于 FIDO2 认证。](https://fidoalliance.org/android-now-fido2-certified-accelerating-global-migration-beyond-passwords/)

FIDO2 协议除了在方便性和易用性方面明显优于常规日期密码之外，还提供了更好的安全性。你看，传统上，通过密码的认证是这样工作的:用户和服务都有一个存储在服务器和设备上的秘密密钥。在身份验证过程中，用户将密码发送到服务器，在服务器上进行加密，并根据存储的密钥进行检查。如果密钥匹配，用户就可以访问他们的帐户/内容。现在，这种方法有一个很大的缺陷:认证密钥存储在两个不同的位置，这使它们更容易受到攻击。的确，有一些方法，比如端到端加密来防止它们，但是黑客们总是想出新的方法来利用这些明显的缺陷。

FIDO2 协议在离线条件下仅在用户的设备上存储认证密钥。因此，它更加安全、可靠、易于使用。FIDO2 认证现已在所有运行 Android 7.0 牛轧糖或更高版本的移动设备上提供。移动和 web 应用程序的开发人员已经可以使用 API 在他们自己的服务中实现这一特性。

* * *

## 更新 2:谷歌账户

谷歌已经开始在 Android 7+设备上推出 FIDO2 无密码认证，从今天开始在 Pixel 设备上使用。用户可以使用指纹或屏幕锁定方法，而不是在访问某些谷歌服务时输入密码。这意味着用户只需注册一次手指，就可以使用它来获得一系列本地和网络服务。指纹永远不会被发送到谷歌的服务器上。

要立即试用，请转到[passwords.google.com](https://passwords.google.com/)，选择一个站点来查看或管理保存的密码，并按照说明确认您的身份。

**来源:[谷歌](https://security.googleblog.com/2019/08/making-authentication-even-easier-with_12.html)**