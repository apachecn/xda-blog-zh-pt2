# 谷歌 Pixel 4 用户将不得不等待开发者添加面部解锁支持

> 原文：<https://www.xda-developers.com/google-pixel-4-users-wait-developers-add-face-unlock-support/>

在最近的谷歌制造活动上，该公司终于揭开了新的 Pixel 4 系列的盖子。尽管我们已经知道了关于新设备[的几乎所有事情，这要感谢永无止境的泄露](https://www.xda-developers.com/tag/google-pixel4/)，谷歌确实有一些惊喜。其中一个令人震惊的消息是[的 Pixel 4 设备不会在印度](https://www.xda-developers.com/google-pixel-4-not-available-in-india/)上市，这对印度的 Pixel 粉丝来说绝对是一个打击。我们还了解到，Pixel 4 设备只包括一个用于生物认证的安全面部解锁功能，没有指纹扫描仪的迹象。这种突然转向面部解锁作为生物认证唯一手段的做法现在给全球 Pixel 4 买家带来了麻烦。

Pixel 4 是第一款包含与 Android 10 完全兼容的安全面部识别硬件的设备，它允许面部解锁功能被识别为使用 BiometricPrompt API 的有效生物认证形式。然而，早期的 Pixel 4 审查人员注意到，只有少数应用程序允许通过面部识别进行身份验证。Keepass 和许多银行应用程序等密码管理器仍然使用旧的 FingerprintManager API 来显示指纹认证对话框。这意味着用户必须等待开发人员用 BiometricPrompt API 更新他们的应用程序，然后才能使用它们。

值得注意的是，FingerprintManager API 在 API level 28 (Android 9 Pie) [中被弃用，取而代之的是新的 BiometricPrompt API](https://www.xda-developers.com/android-p-new-biometrics-api/) 。而在 Android 10 中，API 进行了[更新，增加了隐式确认](https://www.xda-developers.com/android-q-security-privacy-features/)，这意味着用户在成功认证后不必点击“确认”。现在，为了让应用程序能够通过 Pixel 4 的面部解锁进行身份验证，它们必须更新到目标 API 级别 28，并实现生物计量提示。一旦完成，BiometricPrompt API 将显示一个系统提供的对话框，该对话框将与设备上可用的任何安全生物识别方法(指纹或面部解锁)配合使用。

现在，如果你是一个 Android 老手，你应该已经知道等待开发者更新他们的应用程序通常需要很长时间。不过幸运的是，谷歌在 Pixel 4 发布前几个月就开始着手这项工作了。自 2019 年 8 月以来，该公司要求所有提交到 Play Store 的新应用程序都要针对 Android 9。因此，对于任何开发新应用的开发者来说，他们没有理由使用被否决的 API 而不是更新的 BiometricPrompt API。此外，从 2019 年 11 月开始，谷歌还要求现有应用的所有更新都针对 Android 9。因此，当更新应用程序以支持较新的 API 级别时，开发人员将被警告旧 API 被弃用，鼓励他们切换到 BiometricPrompt，从而为 Pixel 4 添加面部解锁支持。

* * *

*美国东部时间 2019 年 10 月 17 日上午 11:00 更新了这篇文章，以澄清不需要切换到 BiometricPrompt，因为旧的指纹 API 在 API level 28 中已被否决。*