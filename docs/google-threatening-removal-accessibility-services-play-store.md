# 谷歌威胁要从 Play Store 中移除带有辅助功能服务的应用

> 原文：<https://www.xda-developers.com/google-threatening-removal-accessibility-services-play-store/>

**更新** : LastPass 刚刚[回应了](https://blog.lastpass.com/2017/11/lastpass-android-accessibility-services.html/)这一消息，并声明对他们的 Android 应用程序“没有直接影响”。这是否意味着其他申请将被宽大处理，还有待观察。

Play Store 上一些最具创新性的应用程序是以谷歌从未想过的方式使用 API 构建的。有些应用程序可以重新映射音量键以跳过音乐曲目，记录和播放网页或游戏上的触摸输入，甚至提供替代导航键，以便您可以使用设备的整个屏幕。我刚刚提到的所有这些例子都依赖于 Android 的可访问性 API。但这可能很快就会改变，因为谷歌 Play 商店团队正在向开发者发送电子邮件，告诉他们不能再实现无障碍服务，除非他们遵循谷歌的指导方针。

* * *

## 什么是辅助功能服务？

为了理解为什么这很重要，我们首先需要解释什么是与 Android 相关的可访问性。一般来说，可访问性是指使 Android 应用程序更容易被某些残疾用户(如视力障碍者)访问。虽然让残疾用户更容易访问他们的应用程序符合每个开发人员的最佳利益，但有一类特殊的应用程序旨在增强所有 Android 应用程序对残疾用户的可用性。这些被称为可访问性服务。

辅助功能服务，通常被称为 a11y，是一个应用程序，系统可以根据辅助功能服务注册监听的[事件](https://developer.android.com/reference/android/accessibilityservice/AccessibilityServiceInfo.html#eventTypes)向其提供某些信息。希望实现辅助功能服务的应用程序必须将`android.permission.BIND_ACCESSIBILITY_SERVICE`权限添加到 AndroidManifest 文件，这样只有系统可以绑定到应用程序的服务。

例如，如果构建一个可访问性服务来监听`TYPE_VIEW_CLICKED`事件，那么该服务将从系统接收关于用户可能按下的任何按钮的信息。辅助功能服务还可以在其他应用程序收到某些手势和按键事件之前做出反应并使用它们。最后，辅助功能服务还可以注入某些按键事件，比如后退、分屏或最近应用按钮。

因此，可访问性服务可能**非常强大和有用**。谷歌 Play 商店上几个最受欢迎的创新应用程序都依赖 a11y 来履行它们的职责。以下是我随口想到的几个例子:

*   [自动输入](https://play.google.com/store/apps/details?id=com.joaomgcd.autoinput) -拦截按键事件并执行点击/滑动手势
*   [按钮映射器](https://play.google.com/store/apps/details?id=flar2.homebutton) -截取按键事件并将它们重新映射到其他按键事件
*   [绿色化](https://play.google.com/store/apps/details?id=com.oasisfeng.greenify) -在屏幕关闭前强制关闭应用程序，使其自动休眠
*   [输入+](https://play.google.com/store/apps/details?id=com.catchingnow.undo) -检测键盘应用程序何时打开以显示浮动操作按钮
*   [LastPass](https://play.google.com/store/apps/details?id=com.lastpass.lpandroid) -扫描页面中的用户名/密码条目(在 Android Oreo 之前是必需的)
*   [快速切换](https://play.google.com/store/apps/details?id=org.de_studio.recentappswitcher.trial) -返回按钮发送按键事件
*   任务器 -检测应用程序何时打开，以便您可以执行任何用户定义的操作
*   [打字机器](https://play.google.com/store/apps/details?id=fi.rojekti.typemachine) -记录所有的文本输入，这样你就不会丢失任何文本输入

这些应用程序都没有按照谷歌的意图使用 a11y，即帮助残疾用户。我敢打赌，绝大多数实现可访问性服务的应用程序都是为了谷歌权限之外的功能。但这就是 Android 和可访问性等 API 的魅力所在——谷歌通常不会限制开发者能做什么和不能做什么。然而，随着谷歌 Play 商店团队向开发者发送电子邮件，警告他们关于 a11y 的政策即将发生变化，这种使用辅助功能服务的松散方法似乎正在改变。

* * *

## 谷歌到底在做什么？

该公司通知开发者，如果他们的应用程序出于任何原因使用辅助功能服务，而不是为了帮助残疾用户，那么他们**必须在 30 天内移除该权限的使用，否则他们的应用程序将从 Play Store** 中移除。未能遵守这一要求可能会导致违反开发商的 Play Store 帐户，这可能**最终导致帐户终止**。

对于少数使用 a11y 来帮助残疾用户的应用程序，谷歌表示，这些开发人员只需添加一个突出的、面向用户的披露，说明他们的应用程序需要许可的原因。然而，正如我之前提到的，易访问性服务在应用程序中使用得更多，最终会违反这个新政策。

### 发送给开发人员的完整电子邮件

****的开发者们好，

我们之所以联系您，是因为您的软件包名称为****的应用程序* * * * *，正在请求“[Android . permission . bind _ ACCESSIBILITY _ SERVICE](https://developer.android.com/reference/android/Manifest.permission.html#BIND_ACCESSIBILITY_SERVICE)。”请求辅助功能服务的应用程序应仅用于帮助残疾用户使用 Android 设备和应用程序。您的应用程序必须符合我们的[权限](https://play.google.com/about/privacy-security-deception/permissions/)政策以及我们的[用户数据](https://play.google.com/about/privacy-security/personal-sensitive/)政策的重要披露要求。

**所需行动**:如果你还没有这样做，你必须向用户解释你的应用程序如何使用“[android . permission . bind _ ACCESSIBILITY _ SERVICE](https://developer.android.com/reference/android/Manifest.permission.html#BIND_ACCESSIBILITY_SERVICE)”来帮助残疾用户使用 Android 设备和应用程序。在 30 天内未能满足这一要求的应用程序可能会从 Google Play 中删除。或者，您可以移除应用程序中对辅助功能服务的任何请求。您也可以选择取消发布您的应用程序。

**如果您需要更改您的应用程序，请遵循以下步骤:**

*   通读[权限](https://play.google.com/about/privacy-security-deception/permissions/)和[用户数据](https://play.google.com/about/privacy-security/personal-sensitive/)政策了解更多详情，并确保您的应用符合[开发者计划政策](https://play.google.com/about/developer-content-policy.html)中列出的所有政策。
*   如果您的应用程序中不需要 BIND_ACCESSIBILITY_SERVICE 权限，或者该权限正用于帮助残疾用户使用 Android 设备和应用程序之外的其他用途:
    1.  从你的应用清单中删除对此权限的请求。
    2.  [登录您的游戏控制台](https://play.google.com/apps/publish)并上传您修改后符合政策的 APK。
*   或者，如果您需要应用程序中的 BIND_ACCESSIBILITY_SERVICE 权限来帮助残障用户使用 Android 设备和应用程序:
    1.  在你的应用商店列表描述中包含以下片段:“此应用使用辅助功能服务。”
    2.  在要求用户在您的应用程序中启用此权限之前，请向用户公开此用法。您的披露必须符合以下各项要求:
        *   公开必须通过 AccessibilityServiceInfo 类的 [android:summary](https://developer.android.com/reference/android/accessibilityservice/AccessibilityServiceInfo.html#attr_android:summary) 和 [android:description](https://developer.android.com/reference/android/accessibilityservice/AccessibilityServiceInfo.html#attr_android:description) 元素来提供
        *   披露必须描述辅助功能服务权限为您的应用程序启用的功能。与可访问性服务请求一起使用的每个特性都必须在您的公开中声明，并提供正当理由。

另外，您也可以选择取消发布应用程序。

所有违规都会被跟踪。任何性质的严重或重复违反将导致终止您的开发者帐户，并调查和可能终止相关的谷歌帐户。

如果您已经查看了政策，并认为我们可能有错误，请联系我们的[政策支持团队](https://support.google.com/googleplay/android-developer/contact/emailappeals)。我的一位同事将在 2 个工作日内回复您。

问候，

Google Play 审核团队

* * *

## 为什么谷歌要从 Play Store 中移除辅助功能服务？

虽然无障碍服务的使用[被认为会导致相当大的延迟](https://www.xda-developers.com/working-as-intended-an-exploration-into-androids-accessibility-lag/)，但谷歌开始打击这些应用的真正原因可能与利用 a11y 的日益增长的问题有关。尽管我上面提到的应用程序将 a11y 用于有益的目的，但它们很容易被恶意开发者利用来达到邪恶的目的。例如，可访问性服务**可用于实现键盘记录、勒索软件攻击或网络钓鱼利用**。

谷歌保护用户免受恶意访问服务的努力主要围绕着信息披露。目前，启用为某些事件(如`TYPE_VIEW_TEXT_CHANGED`)注册的辅助功能服务会导致一个警告对话框，提示应用程序可能会窃取您的密码。你可能认为这样的信息可以有效地防止用户不负责任地授予应用 a11y。然而，有大量记录在案的应用程序欺骗用户授予 a11y 的案例。一些攻击甚至走得更远，如[斗篷和匕首利用](https://www.xda-developers.com/cloak-and-dagger-exploit-uses-overlays-and-accessibility-services-to-hijack-the-system/)和[吐司消息覆盖攻击](https://www.xda-developers.com/android-toast-message-overlay-attack/)，这些攻击通过歪曲用户在屏幕上交互的内容，在社交上操纵用户授予 a11y。

诸如此类的攻击在绝大多数 Android 设备上都很有效。谷歌在防止覆盖或 toast 消息攻击方面取得了重大进展(如果你搜索 a11y，就可以在 AOSP 看到)，但事情已经到了谷歌决定完全限制可访问性服务的使用的地步。这是有道理的，但这真的很糟糕，因为这一举措会扼杀许多创新应用的功能。

* * *

## 开发者能做什么？

不幸的是，对于这些变化，开发人员没有太多的事情可以做。开发者可以通过移除他们的可访问性服务来满足谷歌的要求，或者面临他们的应用被移除和他们的账户可能被终止的威胁。如果他们的应用程序合法地旨在帮助残疾用户，简单地增加一个为什么他们的应用程序使用 a11y 的披露将会起作用，这并没有描述目前使用 a11y 的大多数应用程序。

对于我们提到的一些应用程序，重构应用程序使其不再使用可访问性服务是可能的，但不是全部。LastPass 等密码管理器可以[迁移到自动填充框架](https://www.xda-developers.com/android-os-autofill-framework-will-finally-resolve-a-long-standing-lag-issue-with-password-managers/)，但前提是用户运行的是 Android 8.0 Oreo 及以上版本。如果一个应用程序使用 a11y 来监控其他应用程序何时打开，那么这个应用程序可以使用 UsageStats API 编写一个轮询服务。像 Tasker 这样的应用程序可以在这样的变化中生存下来。其他的按钮映射器和自动输入器就没那么幸运了——没有 root，就没有拦截按键事件的好方法。

虽然我们认识到允许恶意应用程序访问可访问性 API 的危险，但看到一些真正有用的应用程序被谷歌阉割是一种耻辱。我们希望谷歌制定的政策被逆转，或者他们只是声称它被曲解了。照目前的情况来看，邮件中的措辞非常明确——要么遵守我们的指导方针，要么滚出 Play Store。这是一个严峻的提醒，谷歌拥有 Play Store 中应用程序的所有权力，他们可以随时从你的身下拉出地毯。

* * *

### 更新 1:混乱的开发者文档

谷歌为[构建无障碍服务](https://developer.android.com/guide/topics/ui/accessibility/services.html)的开发者文档似乎与谷歌 Play 商店团队的这一新焦点相矛盾。在撰写本文时，该页面具有以下措辞:

> #### 辅助功能服务是一种应用程序，它提供用户界面增强功能，以帮助残疾用户或暂时无法与设备完全交互的用户。例如，正在开车、照顾小孩或参加喧闹聚会的用户可能需要额外的或替代的界面反馈。

此外，如果你将该页面上的措辞与 7 月日的[存档版本进行比较，你会发现，关于建立无障碍服务只是为了帮助残疾用户的说明并不存在。](https://web.archive.org/web/20170716140234/https://developer.android.com/guide/topics/ui/accessibility/services.html)

*感谢 joo Dias 提供这些信息。*