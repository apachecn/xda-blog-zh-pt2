# 随着谷歌确认有意限制，Android P 上的无根定制主题已经结束

> 原文：<https://www.xda-developers.com/rootless-custom-themes-android-p/>

Android P (Android 9.0)对于 Android 爱好者来说是一个令人兴奋的版本，因为它给用户界面和用户体验带来了许多变化。由于谷歌在 Project Treble 上的工作，最新的 Android 版本不仅适用于谷歌 Pixel 和谷歌 Pixel 2 设备，还适用于 OnePlus 6、小米 Mix 2S、索尼 Xperia XZ2、Essential Phone 等手机。然而，Android P 中一个不太令人兴奋的变化是操作系统对安装自定义覆盖的[限制](https://www.xda-developers.com/android-p-blocks-custom-overlays-substratum-themes/)。覆盖图用于修改应用程序的资源，底层主题管理器使用它们来使 Android Oreo 上的[无根定制主题](https://www.xda-developers.com/custom-themes-android-oreo-substratum/)成为可能。现在，谷歌已经证实，这些限制是有意的行为，这意味着无根的、全系统的定制主题将不再可能在谷歌智能手机和没有现有主题引擎向前发展的智能手机上实现。

*安卓 8.0 奥利奥无根上的全系统黑暗主题*

在谷歌问题跟踪器中，一名谷歌员工在评论后留下了[，并将该问题标记为“不会修复(预期行为)”:](https://issuetracker.google.com/issues/74354703#comment360)

> #### 我们感谢您的反馈，并愿意分享一些背景信息和澄清。
> 
> #### 覆盖管理器服务(OMS)旨在供设备制造商使用。OMS 目前的形式并不是为了成为一个通用的主题化功能——为了维护 Android 平台的安全性和用户的产品标准，还需要更多的设计考虑。因此，OMS 从未被提倡作为公共开发者特征。
> 
> #### 今年早些时候，Android Oreo 设备的安全补丁(CVE-2017-13263)发布给了 OEM 厂商。该补丁将覆盖安装限制在预装或系统签名的应用程序，以回应 Android Oreo 中提出的合法安全问题。Android P 也包括这个关键的安全补丁，所以它像 Android Oreo 一样限制覆盖。
> 
> #### 我们知道自定义主题对于一些用户来说是一项重要的功能。我们将在这一领域的任何未来工作中考虑您的反馈。

我们之前已经讨论过覆盖管理器服务(OMS)。索尼的主题框架被贡献给了 Android 开源项目。从 Android 8.0 Oreo 开始，与 OMS 交互的命令可以通过 ADB 访问，这就是 Andromeda add-on for substrate[如何将无根定制主题](https://www.xda-developers.com/android-oreo-rootless-system-theme/)引入 Android Oreo。Google 意识到社区正在以一种意想不到的方式使用这些 ADB 命令(因为 ADB 命令是为开发人员调试准备的)，因此他们实现了一种新的检查，防止安装任何非系统覆盖。

这是一个令人失望的，但最终可以预见的谷歌的变化。由于与目标应用程序的资源冲突，第三方覆盖图很容易被破坏，所以 Andromeda 的主题化方法肯定不理想。我们希望 Google 能为主题开发者实现一个 API 来连接应用程序，这样就不会经常出错。就目前而言，定制主题并不适用于谷歌手机的所有用户，这是一个遗憾。来自[雷蛇](https://www.xda-developers.com/razer-phone-theme-engine-oms/)、华为、小米和三星等制造商的设备仍将拥有自己的主题引擎和主题商店，但对于许多设备来说，OMS 是获得原生、全系统黑暗主题的唯一途径。至少未来的 Android P 更新可能会在 Pixel Launcher 中为部分黑暗主题带来一个[手动切换。](https://www.xda-developers.com/google-pixel-launcher-manual-dark-theme/)