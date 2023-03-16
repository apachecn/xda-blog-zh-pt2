# Android P 增加了新的生物识别 API，支持虹膜、面部和指纹

> 原文：<https://www.xda-developers.com/android-p-new-biometrics-api/>

# Android P 增加了新的生物识别 API，支持虹膜、面部和指纹扫描

随着安全性成为手机最重要的部分之一，谷歌在 Android P 中增加了更多支持生物识别形式的方法。这些变化允许开发人员使用虹膜和面部识别等生物识别形式登录应用程序。

安全性可以说是手机最重要的部分。如果我们不能相信我们的数据在我们的智能手机上是安全的，那么我们就没有理由使用我们的智能手机进行任何金融交易。虽然 Android 中增强的安全性总是受欢迎的，但谷歌也希望使其安全功能更加方便。在 [Android P 开发者预览版 1](https://www.xda-developers.com/everything-new-android-p-developer-preview/) 中，谷歌公布了新的指纹对话 API。在第二个 P 预览版中，这一点现在被替换为[生物计量提示 API](https://developer.android.com/reference/android/hardware/biometrics/BiometricPrompt) 。这个 API 更加通用，允许开发者支持所有形式的生物识别解锁方法。无论设备是否有虹膜扫描仪、指纹扫描仪、面部识别，甚至是显示扫描仪，谷歌都希望新的 API 支持所有的生物识别安全措施。

我们第一次报道这个新的 API 是在二月份，当时我们正在梳理 AOSP Gerrit。当时我们在 Android P 中发现[原生支持虹膜扫描](https://www.xda-developers.com/iris-scanners-native-support-android-p/)。三月晚些时候，我们发现 Gerrit 增加了更多内容，暗示[对面部识别硬件](https://www.xda-developers.com/android-aosp-facial-recognition-hardware/)的原生支持。这个新的 API 是这些变化的顶点。

例如，在三星 Galaxy S9 上，有虹膜扫描、面部识别和指纹扫描仪。一旦 Galaxy S9 运行 Android P，应用程序可以向用户显示生物特征验证提示，用户可以不仅仅使用指纹来验证身份。(我们应该注意到，三星有自己的虹膜扫描 API，但一旦发布变得广泛，谷歌的一个更通用的 API 可能会被更广泛地采用。)

希望开发人员将开始为他们的应用程序实现这种新的生物识别 API。这将使应用程序更加安全，同时让用户可以选择以他们喜欢的方式验证他们的身份。

* * *

[**来源:谷歌开发者博客**](https://android-developers.googleblog.com/2018/05/whats-new-in-android-p-beta.html?m=1)