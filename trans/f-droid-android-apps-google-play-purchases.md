# F-Droid 上的一些 Android 应用程序将无法访问 Google Play 购买

> 原文：<https://www.xda-developers.com/f-droid-android-apps-google-play-purchases/>

# F-Droid 上的一些 Android 应用程序最终将无法访问 Google Play 购买

从 F-Droid 下载应用的用户最终可能会遇到一个小问题:他们可能无法再使用 Google Play 计费。

如果你对运行免费和开源的 Android 应用感兴趣，那么你可能听说过 F-Droid。虽然其有限的应用程序目录使其远远不是谷歌 Play 商店的实际替代品，但 F-Droid 是唯一一个除了开源 Android 应用程序之外什么都不包含的应用程序源。F-Droid 官方知识库*上发布的每一个应用程序都有*是完全开源的，这意味着它们不能包含任何闭源组件。随着谷歌最近要求开发者[转向玩计费库 v3](https://www.xda-developers.com/google-play-billing-v3-app-bundle-requirement-2021/) ，在 F-Droid 上有开源项目的开发者面临一个问题。据 XDA 公认的开发者 [M66B](https://forum.xda-developers.com/member.php?u=2799345) 、 [NetGuard](https://www.xda-developers.com/netguard-gives-you-back-control-over-apps-internet-access-without-root/) 和 [FairEmail](https://www.xda-developers.com/fairemail-email-app-privacy-conscious-android/) 的开发者称，在 Google Play 和 F-Droid 上发布应用的开发者将需要开始构建一个没有 Play 计费库的单独版本的应用。

*Google Play 计费库版本生命周期。来源:谷歌。*

那么，为什么会出现这种情况呢？事实证明，谷歌在版本 2.0.3 后停止上传其 Play 计费库[的源代码。自从 2.0.3](https://dl.bintray.com/google/play-billing/com/android/billingclient/billing/) 以来，已经有了 [4 个版本，因此是闭源的。到目前为止，这还不是一个问题，因为应用程序可以很好地使用旧的 Play 计费库 v2，但由于谷歌将很快要求在 Google Play 上发布应用程序的开发者转移到 v3(仍然是闭源的)，这就是我们开始遇到问题的地方。](https://mvnrepository.com/artifact/com.android.billingclient/billing)

Play 商店购买没有免费软件的方法:开发者需要使用谷歌的图书馆，以便允许用户通过 Google Play 进行购买。开发人员应该不会有太大的问题，为 Google Play 构建一个带有 Play Billing Library 的应用程序版本，为 F-Droid 构建一个没有 Play Billing Library 的应用程序版本，因为 Gradle 允许不同源代码集的产品风格。然而，这一变化对从 F-Droid 下载应用程序的用户来说有点不方便，因为他们将无法使用 Google Play 进行购买。如果您没有谷歌 Play 商店，那么这对您来说可能不是什么大问题，因为您可能不会使用 Google Play 计费。如果你只是将 F-Droid 作为一个替代应用程序提供商，那么将受到这一变化影响的应用程序很可能也可以在谷歌 Play 商店上使用。

**[F-Droid 网站](https://f-droid.org/)**

https://f-droid.org/en/packages/eu.faircode.email/