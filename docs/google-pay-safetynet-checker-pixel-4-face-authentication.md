# Google Pay 2.94 preps safety net checker 和 Pixel 4 人脸认证

> 原文：<https://www.xda-developers.com/google-pay-safetynet-checker-pixel-4-face-authentication/>

本周，谷歌[再次挑战预期](https://www.xda-developers.com/google-pixel-4-teaser/)，确认了其即将推出的 Pixel 4 智能手机的两大功能: [Soli 雷达手势和面部解锁](https://www.xda-developers.com/google-pixel-4-face-unlock-soli-gestures/)。谷歌表示，即将推出的 Pixel 面部生物识别技术对于移动支付来说足够安全，果然，最新版本的 Google Pay 应用程序暗示支持用你的面部认证支付。该应用的 2.94 版本还准备添加内置的安全网检查器，如果用户的手机因认证失败而无法用于支付，该工具将提醒用户。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

* * *

### 购买前验证安全网认证

为了在 Android 上使用 Google Pay，你的手机必须通过 Google Play 服务中 SafetyNet 认证 API 采用的几项检查。这些检查可以包括检查引导加载器解锁状态、检查根二进制文件的存在、检查系统级篡改的证据等。对于 root 手机的用户来说，使用 Google Pay 的唯一方法就是隐藏所有系统篡改的痕迹。安装 Magisk 可以实现无系统 root，使用 MagiskHide 还可以防止 Google Pay 检测到其他篡改证据，但在你实际尝试支付之前，你无法判断你对 Google Pay 隐藏 root 的努力是否成功。你最终将能够在需要购买之前检查你的手机是否可以支付，而不是在柜台上发现。

```
 <string name="attestation_notification_body">Check if your device meets software standards</string>
<string name="attestation_notification_title">Your phone is no longer ready for contactless payments</string>
<string name="fails_attestation_body">"Your phone can’t make contactless payments as it isn't passing security checks. Your phone may be rooted, or running uncertified or custom software. You can still use Google Pay to pay online and send money to friends."</string>
<string name="fails_attestation_title">Your phone doesn’t meet software standards</string>
<string name="passes_attestation_title">Your phone is ready to make contactless payments</string> 
```

### 购买时的面部认证

正如预期的那样，谷歌正在更新其支付应用程序，以支持新的生物认证方法。这款应用目前允许你使用指纹验证支付，但如果你的设备像谷歌 Pixel 4 一样支持安全面部解锁，它最终会让你使用面部。

```
 <string name="p2p_fingerprint_switch_description">Require a confirmation</string>
<string name="p2p_fingerprint_switch_description_alt">Use biometric authentication, like your face or fingerprint, instead of PIN</string> 
```

Google Pay 2.94 正在谷歌 Play 商店推出。您可以从 Play Store 或 APKMirror 下载该应用程序。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*