# 谷歌信息很快会在 24 小时后自动删除 OTP

> 原文：<https://www.xda-developers.com/google-messages-6-7-prepares-automatically-delete-otp-after-24-hours/>

如今，许多任务和服务都依赖于电子邮件帐户或我们的电话号码来验证我们的身份。因此，我们经常会在几周内收到大量的一次性密码——每当你在新设备上登录服务时，当你访问服务时，在一些国家，每当你通过网上银行、信用卡和借记卡付款时。这些 OTP 会开始堵塞你的收件箱，使你以后很难找到值得你注意的邮件。谷歌似乎已经意识到了这个问题，因为最新的[谷歌消息](https://play.google.com/store/apps/details?id=com.google.android.apps.messaging)更新准备让你在收到 24 小时后自动删除 OTP。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

Google Messages v6.7.067 包含以下新字符串:

```
 <string name="otp_auto_deletion_promo_banner_body_text">Auto-delete OTPs after 24hrs</string>
<string name="otp_auto_deletion_promo_banner_negative_button_text">No thanks</string>
<string name="otp_auto_deletion_promo_banner_positive_button_text">Continues</string>
<string name="otp_content_description">This message is categorized as a one-time password</string> 
```

根据这些字符串，Google Messages 正在开发一个功能，可以在收到 OTP 消息 24 小时后自动删除该消息。OTP 本质上是临时性的，大多数 OTP 的有效期很短，大约为 10 分钟，这取决于服务的需要。一旦有效期到期，保留这些信息就没什么用了。用户可能也不总是记得删除这些邮件，所以一天后自动删除它们似乎是一个有用的补充。

[其他原始设备制造商](https://www.xda-developers.com/oneplus-messages-app-lands-google-play-store-adds-copy-button-otps/)通过在单独的二级收件箱中显示 OTP 和其他促销信息来清理主收件箱。谷歌的清理方法似乎更好，因为 OTP 实际上没有未来的效用。该功能可能会作为一个选项推出，所以如果您确实想保留您的 OTP 消息，您也应该包括在内。

*感谢 PNF 软件为我们提供了使用* *[JEB 反编译](https://www.pnfsoftware.com/?aid=xdadev)* *的许可，这是一款针对 Android 应用的专业级逆向工程工具。*