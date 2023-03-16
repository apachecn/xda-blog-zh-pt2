# 谷歌新的 Block Store 库将使在新设备上登录应用变得更加容易

> 原文：<https://www.xda-developers.com/google-new-block-store-library-easier-sign-in-apps-new-devices-migration/>

Android 落后于 iOS 的一个领域是迁移到另一个设备并进入与您开始时相同的状态的能力，至少在您的应用程序数据的上下文中是如此。当您从不同的 OEM 迁移到新手机时，这个问题会更加突出，因为特定的 OEM 备份和恢复解决方案通常是针对特定的生态系统量身定制的。谷歌一直试图通过利用 Google Play 服务框架和 [Google Drive 为谷歌的 Android](https://www.xda-developers.com/android-pie-manual-google-drive-backup/) 提供内置的备份管理器服务来解决这个问题。这种内置的解决方案会自动将联系人、通话记录、短信以及某些应用程序数据和设备设置备份到 Google Drive，但它仍然是一个不完整的解决方案，因为它会注销已登录的帐户(并选择退出)。在 Android 11 中，由于新的 Block Store 库，设备迁移情况将得到改善。

**[安卓 11 XDA 新闻](https://www.xda-developers.com/tag/android-11/)**

谷歌一直在通过[官方 Android 开发者 YouTube 频道](https://www.youtube.com/channel/UCVHFbqXqoYvEWM1Ddxl0QDg)上的短视频详细介绍 Android 11 即将到来的一些[变化。在最近一个题为“Android 上的身份:登录的新功能”的视频中，谷歌人 Vishnu Kalugotla 总结了两个新的 API，它们是谷歌身份服务库的一部分:一个点击和阻止存储。](https://www.xda-developers.com/android-11-beta-1-update-live-google-pixel-2-3-3a-4-xl-device-controls-api-quick-settings-media-controls/)

几个月前发布了 One Tap,这是一个专注于让使用谷歌账户只需一次点击就能登录或注册服务变得更容易的库。

但是，本文的重点是块存储。Block Store 是一种基于令牌的登录机制，建立在 Google 现有的备份和恢复基础架构之上。当前的基础设施允许开发者选择将精选的私人应用文件备份到用户的 Google Drive 账户。Block Store 旨在在设置过程中恢复新手机上的应用程序和数据时，可以恢复应用程序的登录凭据。块存储不是以加密形式存储用户名和密码，而是以加密形式保存特定于应用程序的用户验证令牌。

虽然块存储的采用不会完全模仿 iOS 的无缝备份和恢复体验，但它有望减少频繁迁移设备的摩擦。用户仍然需要打开每个应用程序，让设置自动完成，但至少，你不再需要为手机上的每个应用服务再次输入登录信息。

然而，挑战在于采用这个库，因为它的使用是可选的。开发者可以选择是否存储用户的凭证，或者是否希望用户重新登录。这意味着应用程序有可能不会采用这个系统。所以最终，Android 上的迁移过程可能仍然是一个痛苦。但是有希望的是，开发人员可以使用这样的解决方案可能会导致更多的采用，并在某种程度上使用户设置新设备更容易。