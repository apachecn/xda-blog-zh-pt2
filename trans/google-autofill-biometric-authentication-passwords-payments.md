# 谷歌自动填充测试密码和支付的生物认证

> 原文：<https://www.xda-developers.com/google-autofill-biometric-authentication-passwords-payments/>

在 Android 8.0 Oreo 中，谷歌[终于添加了](https://www.xda-developers.com/android-os-autofill-framework-will-finally-resolve-a-long-standing-lag-issue-with-password-managers/)高度要求的自动填充 API，允许第三方密码管理器轻松安全地在应用程序中填写密码和支付信息，而不依赖于旧的可访问性变通方法。如果你不想使用第三方解决方案来存储你的凭据，谷歌也有自己的自动填充服务，可以在任何运行 Android 8.0 和更高版本的安装了 Google Play 服务的设备上使用。

进入**设置>系统>语言&输入>自动填充服务**即可访问。它与你的谷歌账户同步，让你添加个人信息、地址、支付方式和密码，这些信息可以在第三方应用程序或谷歌浏览器中自动填写。

就像使用 [LastPass](https://www.xda-developers.com/lastpass-authenticator-update-fixes-security-vulnerability/) 、Dashlane 或其他自动填充服务一样，使用谷歌自动填充，你会在任何支持的输入字段上方看到一个浮动的自动填充框。点击方框将填写您的数据。目前，输入这些数据时不涉及用户身份验证，这反过来可能会允许攻击者登录您的应用程序，并在他们设法侵入您的设备时访问您的敏感数据。作为参考，大多数第三方密码管理器在自动填充应用程序和网站时提供生物认证作为额外的安全层。

谷歌意识到了这一安全问题，目前正在测试生物认证后锁定自动填充的能力。这个过程将由 BiometricPrompt API 处理，这意味着你可以使用指纹、虹膜扫描仪或面部解锁硬件来验证自动填充请求。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

我们的主编米沙·拉赫曼(Mishaal Rahman)能够在他的 Pixel 4 上测试这一功能，并让 Face Unlock 在官方 Reddit 应用程序中验证自动填充。无法捕获验证窗口的屏幕截图，因为自动填充框架不允许拍摄屏幕截图。然而，你可以在下面的截图中看到谷歌自动填充设置中的新安全选项。点击该选项可以打开支付信息和登录凭证的生物认证。

该功能仍在测试中，我们不知道谷歌计划何时向广大用户发布。它可能会被添加到 Google Play 服务的未来更新中，或者甚至可能作为服务器端开关推出——我们还不确定。然而，如果我们从谷歌那里听到任何消息或者发现任何更大范围推广的证据，我们一定会让你知道。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*