# APK 签名方案 v3 将支持密钥轮换

> 原文：<https://www.xda-developers.com/apk-signature-scheme-v3-key-rotation/>

如果您是一名开发人员，或者您熟悉反编译、修改和/或安装修改过的 APK 文件，那么您可能熟悉应用程序签名。简而言之，Android 要求一个应用程序**必须用同一个密钥签名，这样系统才能允许更新这个应用程序。Android 通过检查 APK 签名来验证这一点。**

APK 签名是 Android 中一个非常基本的安全措施，我们之前已经讨论过了。基本上，所有签名对于某个开发人员或开发人员组都是唯一的，因此如果 APK 中的签名/证书无效或与原始应用程序的签名/证书不匹配，安装将会失败，从而防止在您的 Android 设备上安装被篡改或伪造的 APK 文件。开发人员还必须安全保管签名密钥，因为它们对于验证和最终推出应用程序更新至关重要。幸运的是，用于签署 apk 的签名方案得到了另一个修订版——v3——它似乎增加了一个方便的特性，同时保持了较高的安全性标准。

* * *

## APK 签名方案 v1 和 v2

当前的 APK 签名方案版本 v2[面向开发者](https://www.xda-developers.com/android-7-0-compatibility-document-released-plenty-of-changes-in-tow/)发布还没多久。毕竟是随着 2016 年底安卓 7.0 牛轧糖的推出才勉强介绍给我们的。在 Android 7.0+应用中使用 v2 签名方案受到了高度鼓励，因为它带来了一系列重要的补丁和安全改进:虽然 v1 只对 JAR 进行了签名，但 v2 采取了额外的步骤来保护整个文件的完整性。不过，签名方案不是向后兼容的，Android Marshmallow 和更低版本的应用程序需要 v1 签名。

 <picture>![APK Signature Scheme V3](img/94071330d974c1a8641f8dfccb76494a.png)</picture> 

APK Validation Process. Source: Google.

除非您专门迎合 Nougat 或更高版本的用户，否则理想的情况是同时使用两种签名方案，首先用 v1 签名，然后用 v2 重新签名。这样牛轧糖和更高的会识别 v2 签名，棉花糖和更低的会识别 v1 签名。

然而，由于一系列漏洞和其他安全问题，仅使用 v1 是非常不鼓励的，其中最值得注意的是[Janus 漏洞](https://www.xda-developers.com/janus-vulnerability-android-apps/)，它允许攻击者直接攻击和修改 apk 而不影响签名。Instagram 或 Snapchat 等不常更新的流行应用程序仅使用 v1 签名进行签名，这意味着它们容易受到这些问题的影响。

 <picture>![](img/736f86084b7332354456a9c1f61c3607.png)</picture> 

Checking the APK signing versions of popular social media/payment apps.

## APK 签名方案 v3

v3 最大的亮点是对 v2 的修正，将是**键旋转支持**。 [v3 签名方案](https://android-review.googlesource.com/#/c/platform/tools/apksig/+/587834/)引入了 APK 签名者血统，根据提交之一的[，它“包含了与每个祖先签署证书的历史，以证明其后代的有效性。每个额外的后代代表一个新的身份，可用于签署 APK。以这种方式，血统包含轮换的证明，通过该证明，包含血统的 APK 可以向其他方证明，它能够被信任其当前的签名证书，就好像它是由它的旧证书之一签名的一样。”](https://android-review.googlesource.com/#/c/platform/tools/apksig/+/589594/)

从几个方面来看，密钥轮换对开发人员来说是一个很好的特性。首先，这对于开发单个应用程序的团队中的开发人员非常有用，因此开发人员不必与团队共享他们的签名密钥。由于应用程序需要完全相同的签名来更新，因此目前所有应用程序都需要由同一个开发人员或一组开发人员使用相同的密钥来编译，这降低了安全性(密钥被盗的可能性更大)并降低了开发速度。

此外，在开发人员的签名密钥被盗/丢失的情况下，这也很有用，这通常意味着应用程序必须以不同的包名重新加载到 Play Store。这种情况并不少见，因为很久以前，甚至谷歌也丢失了 Google Authenticator 应用程序的签名密钥，导致他们以不同的包名重新发布它。从那以后，谷歌提供了安全地将你的签名密钥存储在云中的方法，使用 [Google Play 应用签名](https://www.xda-developers.com/google-play-console-new-features/)，但是密钥轮换将允许你在假设的混乱情况下继续更新你的应用。

### 它什么时候推出？

虽然您可能急于尝试它以获得更多的便利，但是 v3 签名方案被发现在 AOSP Gerrit 代码审查网站上到处流传，并且提交本身现在还没有被合并到主分支中，所以它还没有准备好。如果之前发布的带有 Android 牛轧糖的 v2 告诉我们什么的话，我们应该期待 v3 签名方案随着即将发布的 Android P 到达开发者手中。

我们还应该注意到，密钥轮换很可能不是 v2 的唯一区别。APK 签名方案 v3 仍然是一个进行中的工作，所以当将来完整的文档出来时，我们将看到 v3 签名方案的实际改进。