# Warden 是一款开源应用，可以让你禁用跟踪器和记录器

> 原文：<https://www.xda-developers.com/warden-open-source-app-aurora-store-disable-trackers-loggers/>

众所周知，我们在互联网上经常被跟踪。虽然营销人员和组织声称跟踪用户有助于他们了解自己的行为和偏好，从而可以改善服务，但许多用户认为这种程度的跟踪具有侵犯性。许多用户甚至可能最终泄露了比他们预期更多的关于他们浏览习惯的信息，通常是通过浏览一些不安全或不可信的网站。虽然人们普遍认为大部分在线跟踪是在我们的个人电脑上浏览互联网时发生的，但有数百款 Android 应用程序内置了跟踪器，不仅可以存储你的信息，还可以与潜在的第三方客户(如广告商)分享这些信息。

如果你比普通用户更重视隐私，并且绝对想阻止被手机上的应用程序跟踪，你应该尝试一个新的开源应用程序[叫做**监狱长**，它声称可以阻止隐藏在应用程序中的跟踪器和记录器。典狱长是由 XDA 资深成员](https://gitlab.com/AuroraOSS/AppWarden/-/tags)*[WhyOrean](https://forum.xda-developers.com/member.php?u=5678465)* 创造的，他因在[极光商店](https://labs.xda-developers.com/store/app/com.aurora.store)背后的工作而闻名，极光商店是一个流行的、非官方的、开源的谷歌 Play 商店客户端。使用 root 访问权限，Warden 允许用户禁用应用程序中包含的所有检测到的跟踪器和记录器。它还有一个基于配置文件的“解包器”，支持[脚本](https://auroraoss.com/Warden/Scripts/)。该应用支持 Android 及以上版本。

典狱长应用程序管理器使用由法国非营利组织 [Exodus Privacy](https://exodus-privacy.eu.org/en/) 编辑的[追踪者](https://gitlab.com/AuroraOSS/AppWarden/-/blob/master/app/src/main/assets/trackers.json)和[记录者](https://gitlab.com/AuroraOSS/AppWarden/-/blob/master/app/src/main/assets/loggers.json)的静态列表。它读取安装在手机上的每个应用程序中的 dex (Dalvik 可执行文件)文件，以查看是否有任何类名与上述列表中的已知跟踪器或记录器相匹配。在这个上下文中，Loggers 指的是“所有用于记录用户在应用程序或 logcat 上的活动的工具”WhyOrean 指出，并不是所有的日志记录程序都是邪恶的，有些可能会被用于记录用户的活动以达到各种(合法的)目的。然而，有几个日志工具“像 ACRA，xLog”是强大的工具，可以“在没有用户同意的情况下将用户数据发送到开发人员”

除了提供对讨厌的追踪器的洞察，沃登还提供了一个“去膨胀器”和“核武器！”模式，这两种模式都需要 root 访问权限。虽然*去膨胀器*允许用户禁用、隐藏或卸载带有可疑追踪器的应用程序，但*用核武器摧毁了它！*该功能允许用户扫描设备上安装的所有应用程序，并自动禁用所有已知的跟踪器组件(活动、服务、提供商和接收者)。“去膨胀”和“核化它！”目前被认为是实验性的特性，所以如果你遇到任何问题或有任何建议，请一定要访问下面的线程给开发者反馈。

[**下载区长- App 管理器**](https://forum.xda-developers.com/android/apps-games/warden-app-manager-t4122227)