# 移动游戏保护为 Android 上的移动游戏带来了 Denuvo DRM

> 原文：<https://www.xda-developers.com/denuvo-drm-mobile-games-android/>

如果电脑游戏是你的爱好之一，那么你可能在某个时候听说过 Denuvo。这家软件公司最出名的是为 PC 游戏制造商提供数字版权管理技术，以尽量减少发布后几周内的盗版。它的功效在网上引起了激烈的争论，因为[盗版集团击败这项技术的速度有多快，](https://arstechnica.com/gaming/2017/10/denuvos-drm-ins-now-being-cracked-within-hours-of-release/)据称减慢了加载时间并加剧了“帧峰值”，这在 PC 游戏玩家中也引起了争议 PC 游戏玩家已经与 Denuvo 打交道多年了(不管他们是否愿意)，但我们可能很快就会看到这项技术在 Android 上崭露头角。今天，Denuvo 的母公司爱迪德[宣布为 Android 游戏开发者提供](https://irdeto.com/news/denuvo-extends-protection-to-games-developed-for-mobile-devices/)手机游戏保护。

在新闻稿中，爱迪德表示，手机游戏保护“防止黑客调试，逆向工程和改变游戏。”爱迪德表示，他们的解决方案不需要游戏的源代码，该解决方案“可以添加到最终的 APK 中”(二进制)，因此开发人员不必再管理另一个 API 或 SDK。事实上，爱迪德的数据表声称，开发者可以将手机游戏保护与“零运营工作”相结合。开发人员也可以“在应用保护之前对游戏进行概要分析，以便为单个游戏定制保护。”这将允许开发者在决定实施移动游戏保护之前，看到他们的游戏的设计和架构是否容易受到逆向工程的攻击。

该工具的主要功能包括“可配置的保护级别、保护点的智能检测、根检测、反挂钩、虚拟化和完整性验证。”Root 检测和反挂钩分别旨在检测 [Magisk](https://www.xda-developers.com/tag/magisk/) /SuperSU 和[exposed](https://www.xda-developers.com/tag/xposed/)，而虚拟化将帮助游戏检测它们是否在模拟的 Android 设备上运行。爱迪德还表示，该技术有助于“防止应用程序代码的静态或动态操作。”爱迪德声称，实施这项技术将“对用户的游戏体验影响最小，同时仍然保证没有误报和最大限度的检测。”

毫无疑问，Android 上盗版猖獗。你可以通过快速的谷歌搜索很容易地找到应用程序和游戏的破解版本，而且与苹果的 iOS 不同，没有什么可以阻止你下载这些盗版版本。有了 APK 改装工具和 root 权限，也有可能篡改游戏文件来欺骗或解锁你通常应该付费的下载软件。为此，很自然会看到 Denuvo 等软件公司带着承诺减少安卓游戏篡改和盗版的技术飞扑进来。然而，Android 游戏场景与 PC 游戏略有不同，因为大多数流行的手机游戏都是在“免费增值”模式下运行的，而不是收取预付费用。因此，我们可能不会在手机上看到海盗和 Denuvo 之间同样的猫捉老鼠游戏。

* * *

**Via:***games industry . biz*