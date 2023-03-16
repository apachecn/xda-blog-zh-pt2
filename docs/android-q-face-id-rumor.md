# 独家报道:谷歌正在为 Android Q 开发一个类似 Face ID 的功能

> 原文：<https://www.xda-developers.com/android-q-face-id-rumor/>

虽然最好的 Android 智能手机早在苹果 iPhone 之前就支持指纹扫描仪，但 Android 设备在安全生物面部认证硬件方面正在迎头赶上。苹果 iPhone X 是主要设备制造商的第一款智能手机，结合了飞行时间(TOF)传感器、红外照明器、点投影仪和其他传感器，用于硬件面部识别(苹果称之为“Face ID”)。我们已经看到一些 Android 设备制造商的智能手机采用了类似 Face ID 的实现，如[华为的 Mate 20 Pro](https://www.xda-developers.com/huawei-mate-20-pro-review-video/) 和[小米的 Mi 8 探索版](https://www.xda-developers.com/xiaomi-mi-8-mi-8-explorer-edition-mi-8-se-china-launch/)，但这些设备制造商不得不大量定制 Android 以支持这种新硬件。不过，谷歌似乎正在努力在 Android Q 中引入对安全面部识别硬件的原生支持。

我们已经在我们获得的 Android Q 的[泄露的 AOSP 版本中的框架、SystemUI 和设置 apk 中发现了几十个字符串和多个与面部识别相关的方法、类和字段。我们发现的代码没有一个出现在 AOSP 大师或者](https://www.xda-developers.com/android-q-dark-theme-desktop-mode-permission-revamp/)[最新的 Android Pie 公开版本](https://www.xda-developers.com/january-2019-android-security-google-pixel/)中。此外，现有的“面部解锁”功能已经在 Android 设备上存在了多年，“可信面部”功能是 Google Play 服务的一部分，是旧的，不安全的，所以我们有信心这是 Android Q 中的新功能。

*特别感谢 PNF 软件公司为我们提供了使用 [JEB 反编译器](https://www.pnfsoftware.com/?aid=xdadev)的许可。JEB Decompiler 是一款针对 Android 应用的专业级逆向工程工具。*

### 框架-res

从我们在 Android Q 的框架-res APK 中发现的面部解锁相关的字符串中，最重要的行是关于当设备没有面部识别硬件时显示的错误信息。这告诉我们，Android Q 确实希望该设备具有硬件面部识别传感器，不同于小米、华为/Honor 和一加等公司的大多数现代智能手机上的面部解锁功能。

### 设置

就像设置新指纹一样，新的人脸认证设置流程要求用户设置密码、PIN 或模式作为备份。用户还可以选择要求在启动时解密设备数据之前使用密码、PIN 或模式。以下字符串是我们发现的最重要的一个字符串，因为它明确表示您的面部不仅可以用于解锁手机，还可以用于授权购买或登录应用程序。

```
 <string name="security_settings_face_enroll_introduction_message">Use your face to unlock your phone, authorize purchases, or sign in to apps.</string> 
```

然而，设备管理员仍然可以停用面部解锁。

### 这是它的样子

这里有一些截图展示了 Android Pie 中面部识别的设置过程。不幸的是，我们不能让它实际工作，因为面部解锁哈尔失踪。

### 这对 Android 意味着什么？

如果你认为这些字符串是谷歌 Pixel 4 将拥有 Face ID 的证据，那么让我打断你。这些字符串唯一证明的是，AOSP 现在支持面部识别硬件，用于面部解锁、支付和应用程序认证。我们希望像华为 Mate 20 Pro 和小米 8 探索版这样运行 [Android Q GSI](https://www.xda-developers.com/google-test-android-q-project-treble-gsi/) 的设备能够实现面部识别。其他拥有必要硬件传感器的设备应该也可以在 Android Q 中使用它们进行面部识别。

不过，我不怪你猜测谷歌未来的硬件计划。谷歌在 Android Q 中支持面部识别硬件的事实自然意味着他们有一个正在测试的设备。它可能是 Mate 20 Pro，Mi 8 EE，像[三星 Galaxy S10+](https://www.xda-developers.com/samsung-galaxy-s10-rumors-leaks-specs-features/) 这样尚未发布的智能手机，定制开发板，或者原型 [Pixel 4](https://www.xda-developers.com/pixel-watch-code-names/) 。没有提交，我们不知道他们在测试什么。我们可能会在定于 2019 年 5 月 7 日举行的[谷歌 2019 年 I/O](https://www.xda-developers.com/google-io-2019-may-7-9/)上了解更多信息。

* * *

*本文更新于 2019 年 2 月 8 日，截图为 Android Pie 中安全面部识别的设置流程。*