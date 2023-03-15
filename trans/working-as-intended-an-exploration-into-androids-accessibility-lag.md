# “按预期工作”——安卓易访问性滞后探究

> 原文：<https://www.xda-developers.com/working-as-intended-an-exploration-into-androids-accessibility-lag/>

Android 的魅力在于第三方应用程序可以通过许多不同的方式与系统进行交互。密码管理器应用程序，如 [LastPass](https://play.google.com/store/apps/details?id=com.lastpass.lpandroid&hl=en) 能够自动将相关用户名/密码数据输入到几乎任何登录屏幕。[文本助手](https://play.google.com/store/apps/details?id=com.arjerine.textxposed&hl=en)允许你创建文本扩展宏，让你大大缩短给朋友发短信的时间。[原生剪贴板](https://play.google.com/store/apps/details?id=com.dhm47.nativeclipboard&hl=en)通过允许你双击任何输入字段来打开剪贴板，减少了频繁切换应用程序以复制大量文本的麻烦。谁能忘记 [Greenify](https://play.google.com/store/apps/details?id=com.oasisfeng.greenify&hl=en) ，这可能是发烧友最推荐的应用，它可以控制流氓后台应用，从而延长电池寿命。最后，尽管大多数用户不太熟悉，还有[auto input](https://play.google.com/store/apps/details?id=com.joaomgcd.autoinput)——一个 Tasker 插件，旨在自动化屏幕点击、文本输入、滑动手势等等。这些应用程序都服务于非常不同的用例，但每个应用程序都依赖于一个被误解的 Android 核心功能:**可访问性。**

对于普通的 Android 用户来说，你最喜欢的应用程序所使用的许多这些令人惊叹的功能是由*辅助功能*子菜单下的一个设置控制的，这可能看起来很奇怪。让一个应用程序*可访问*通常意味着一个安卓应用程序可以被一个有*残疾的人*使用。那么，为什么 LastPass、原生剪贴板、文本助手、Greenify 或 AutoInput 会有一个*可访问性*服务呢？此外，为什么启用一个可访问性服务似乎 **[会导致这么多 UI 延迟](https://www.reddit.com/r/Android/comments/3i31fs/psa_accessibility_can_cause_your_phone_to_appear/)** ？你使用的是什么版本的 Android 似乎并不重要——无论是 [Android 5.0 Lollipop](https://code.google.com/p/android/issues/detail?id=81950) 还是[Android 7.0 Nougat](https://code.google.com/p/android/issues/detail?id=203107&q=accessibility&colspec=ID%20Status%20Priority%20Owner%20Summary%20Stars%20Reporter%20Opened)——因为某些辅助功能服务造成的滞后会影响你的体验。这个问题的一个简单的解决方案是仅仅禁用您可能已经启用的可访问性服务——但是这样做的话，我们会失去很多有用的功能。另一个解决方案是请求谷歌“修复”Android 的可访问性滞后，但谷歌声称 Android 的可访问性 **[正在按预期](https://code.google.com/p/android/issues/detail?id=203107#c4)工作。**我们已经与一些非常熟悉辅助功能服务的开发人员进行了交谈，并研究了该功能是如何工作的，我们在这里测试这一说法:*Android 的辅助功能滞后是一个缺陷还是一个功能？*

* * *

**了解 Android 可访问性**

顾名思义，易访问性主要是为开发人员提供额外的功能给残疾用户。事实上，快速浏览一下关于可访问性的官方文档页面就会发现，Google 对于可访问性服务应该提供什么样的服务有一个非常狭隘的观点。

> #### 许多 Android 用户有不同的能力，需要他们以不同的方式与他们的 Android 设备进行交互。这些用户包括因视觉、身体或年龄限制而无法完全看到或使用触摸屏的用户，以及可能无法感知听觉信息和警报的听力损失用户。
> 
> #### Android 提供辅助功能和服务，帮助这些用户更轻松地导航他们的设备，包括文本到语音、触觉反馈、手势导航、轨迹球和方向键导航。

谷歌的 [TalkBack](https://play.google.com/store/apps/details?id=com.google.android.marvin.talkback&hl=en) ，预装在每一部安卓手机上，是‘典型’无障碍服务应该是什么样子的一个很好的例子。[语音访问](https://play.google.com/store/apps/details?id=com.google.android.apps.accessibility.voiceaccess&hl=en)将可访问性又向前推进了一步，仅用语音就可以几乎完全控制你的手机。但是 Google 打算以这种方式使用可访问性服务的事实并不妨碍开发人员以他们想要的任何方式实现它们——这正是开发人员所做的。正是因为可访问性的工作方式，使得这个功能**对有残疾或无残疾的用户都非常有用。**

简单来说，这里有一个 Android 可访问性工作原理的基本纲要。开发人员创建一个[可访问性服务](https://developer.android.com/reference/android/accessibilityservice/AccessibilityService.html)，它订阅各种[可访问性事件](https://developer.android.com/reference/android/view/accessibility/AccessibilityEvent.html)，这些事件由系统根据是否满足特定标准发送给服务。在设置- >辅助功能下禁用所有服务时，Android 不会收集或发送任何辅助功能事件。但是当用户开始启用辅助功能服务时，Android 将开始监控和收集**辅助功能服务请求的那些辅助功能事件**。例如，订阅辅助功能事件[TYPE _ WINDOW _ CONTENT _ CHANGED](https://developer.android.com/reference/android/view/accessibility/AccessibilityEvent.html#TYPE_WINDOW_CONTENT_CHANGED)的辅助功能服务将在每次当前窗口发生变化时被系统*通知。另一个叫做 [TYPE_VIEW_CLICKED](https://developer.android.com/reference/android/view/accessibility/AccessibilityEvent.html#TYPE_VIEW_CLICKED) 的可访问性事件在每次用户点击某种按钮*时触发*。*

*Android 可访问性演示。在这个视频中，我启用了应用程序 [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm&hl=en) 来监控窗口标题的[变化。这需要启用 Tasker 的辅助功能服务。您可以通过在 Tasker 中创建一个新的配置文件，将“Event”上下文设置为“Variable Set ”,并选择%WIN 作为要监控的变量来复制这一点。总的来说，这个大约 1 分钟的视频捕获了当前窗口中的 **107 个变化。**](http://tasker.dinglisch.net/userguide/en/faqs/faq-problem.html#app)*

在正常的用户交互过程中，这类可访问性事件会频繁发生。所以想象一下，当一个用户**启用多个请求高频率可访问性事件的可访问性服务**时会发生什么。没错——**滞。**为了缓解这种情况，开发人员可以更精确地定义他们的服务应该在什么样的环境中对什么类型的可访问性事件作出反应，比如限制服务只在[某些应用](https://developer.android.com/reference/android/R.styleable.html#AccessibilityService_packageNames)中作出反应，或者限制事件之间的[轮询周期](https://developer.android.com/reference/android/accessibilityservice/AccessibilityServiceInfo.html#attr_android:notificationTimeout)。但是除此之外，辅助功能服务产生的开销主要取决于它订阅了什么类型的辅助功能事件。本质上，并不是每一个无障碍服务都会造成滞后。需要高频率事件的单个可访问性服务可能会导致延迟，特别是如果所述服务与需要监控另一个高频率事件的另一个服务相结合。

* * *

**随着 APK 的解散，深入探讨可及性**

从上面发布的视频中可以看出，监视窗口内容变化的可访问性服务会导致 UI 性能发生相当明显的变化，因为系统会触发大量的可访问性事件。然而，很难确定特定的可访问性服务会导致多少开销。监视 LogCat 通常不会有任何结果，因为只有当可访问性服务的开发人员选择这样做时，可访问性事件才会被打印到 LogCat。幸运的是，所有 Android 辅助功能服务之父， [AutoInput](https://play.google.com/store/apps/details?id=com.joaomgcd.autoinput&hl=en) 正是这么做的。LogCat 的输出和您想象的一样混乱。

AutoInput 并没有对我们隐瞒真相。根据您监控的事件，该应用程序导致的开销可能非常巨大。但是这种开销是应用程序运行所必需的。为了让 AutoInput 拦截每一次按键、每一次屏幕手势、每一次 UI 更新和每一次按钮按下，它*需要*来监控各自的可访问性事件。没有这些事件，AutoInput 就不能挂钩到系统中，并提供它目前所允许的几乎无限制的 UI 自动化。因此，AutoInput 的所有功能在可访问性的上下文中都很有意义。但对于其他应用程序，我们需要更深入地了解它们的可访问性服务是如何处理的。

辅助功能服务的[属性](https://developer.android.com/reference/android/R.styleable.html#AccessibilityService)在 APK 内的 [XML 资源文件](https://developer.android.com/reference/android/accessibilityservice/AccessibilityService.html#SERVICE_META_DATA)中定义。因此，我们可以在一个带有可访问性服务的应用程序上执行 **APK 拆除**来找出服务的属性。每个应用程序的功能不同，所以我将尝试解释他们的服务属性如何与它执行的特定功能相关联。

***原生剪贴板***

谈到剪贴板管理器，本机剪贴板是我的首选。如果你正在寻找一个高度可定制的剪贴板管理器，原生剪贴板是一个非常好的应用程序。它甚至有一个 Xposed 模块组件，允许你长按“粘贴”按钮来打开剪贴板管理器！不幸的是，如果您不能访问 Xposed 框架(比如 Nougat 上的每个用户)，那么您将不得不满足于启用可访问性服务，这将允许您双击任何文本输入来打开剪贴板管理器。这就是需要做的事情。

```
 <?xml version="1.0" encoding="utf-8"?>
<accessibility-service android:description="@string/access_decs"
android:accessibilityEventTypes="typeViewClicked|typeViewFocused|typeViewLongClicked|typeWindowStateChanged"
android:accessibilityFeedbackType="feedbackGeneric"
android:notificationTimeout="100"
android:accessibilityFlags="flagReportViewIds|flagRetrieveInteractiveWindows"
android:canRetrieveWindowContent="true"
xmlns:andro /> 
```

每当单击、长时间单击、聚焦视图时，或者当窗口状态发生变化时，本地剪贴板的可访问性服务请求触发一个可访问性事件。由于无法访问源代码，我无法确切地说出本机剪贴板是如何工作的，但很可能本机剪贴板会等待窗口状态指示软键盘当前是打开的，然后它会监视输入字段上的点击。该应用程序的轮询周期为 100 毫秒，因此绝对足够快，可以对软键盘可见性的变化以及双击做出基本上即时的反应。每当用户使用软键盘键入任何文本时，这可能会导致一些 UI 开销，从而可能导致延迟。

***绿色化***

接下来是大家最喜欢的电池节电器，Greenify。Greenify 使用可访问性事件来增强其非根功能。

```
 <?xml version="1.0" encoding="utf-8"?>
<accessibility-service android:description="@string/accessibility_service_description" 
android:settingsActivity="com.oasisfeng.greenify.accessibility.AccessibilitySettings" 
android:accessibilityEventTypes="typeAnnouncement|typeNotificationStateChanged|typeWindowStateChanged" 
android:accessibilityFeedbackType="feedbackGeneric" android:notificationTimeout="0" 
android:accessibilityFlags="flagReportViewIds" 
android:canRetrieveWindowContent="true"
xmlns:andro /> 
```

它使用窗口状态的变化来确定手机屏幕何时关闭，并要求您通过更改安全设置中的选项来延迟锁屏激活。Greenify 还将接收公告或通知状态更改类型的事件，后者在 Android 5.0+设备上是不必要的，因为有通知访问功能。但是，不管事实如何，它仍然会接收这些事件。Greenify 本身应该不会导致太多的开销，但是可能性仍然存在。

***新星发射器***

Nova Launcher 可能是市场上最受欢迎的第三方启动器应用程序，它是使用辅助功能服务的应用程序的一个很好的例子，几乎没有开销。这项服务存在的唯一原因是帮助某些设备执行手势。

```
 <?xml version="1.0" encoding="utf-8"?>
<accessibility-service android:description="@string/accessibility_service_description" 
android:accessibilityEventTypes="" 
android:packageNames="com.teslacoilsw.launcher" 
android:accessibilityFeedbackType="" 
android:notificationTimeout="10000" 
android:canRetrieveWindowContent="false"
xmlns:andro /> 
```

如您所见，XML 文件中没有定义可访问性事件。提到的只是一个包的名字——Nova Launcher。这里发生的事情是对 Nova Launcher 的手势不起作用的某些设备的变通办法。该服务将只在 Nova Launcher 中为 Nova Launcher 提供从[触发的所有可访问性事件。这听起来很奇怪，但显然这是一种修复 Nova 主屏幕手势的方法，如果你的设备不能使用它们的话。因为这只从 Nova 本身请求事件，所以该服务的开销很小。](https://developer.android.com/reference/android/R.styleable.html#AccessibilityService_packageNames)

***LastPass***

最后，可能是最臭名昭著的导致延迟的辅助服务(可能是因为它的广泛流行)——LastPass。LastPass 中的延迟问题是如此引人注目，以至于该公司有一个官方的 T2 常见问题页面来描述这个问题。正如 FAQ 所述，除了禁用服务之外，您对延迟无能为力。为什么 LastPass 的服务在滞后方面显得如此异乎寻常？让我们来看看服务的属性。

```
 <?xml version="1.0" encoding="utf-8"?>
<accessibility-service android:description="@string/accessibility_service_description" 
android:accessibilityEventTypes="typeViewFocused|typeWindowContentChanged" 
android:accessibilityFeedbackType="feedbackGeneric" 
android:notificationTimeout="200" 
android:accessibilityFlags="flagReportViewIds" 
android:canRetrieveWindowContent="true" 
android:canRequestEnhancedWebAccessibility="true"
xmlns:andro /> 
```

事实是，LastPass 的服务并没有什么特别之处。它只请求监视两种事件类型——TYPE _ VIEW _ FOCUSED 和 TYPE_WINDOW_CONTENT_CHANGED。它这样做是因为它需要知道应用程序/网页的内容何时改变/成为焦点，然后它检索当前窗口内容以寻找任何密码输入字段。但是由于服务经常在两个极其频繁触发的可访问性事件上这样做，这导致了延迟。这就是不幸的事实。

* * *

**与滞后一起生活**

当我们第一次读到谷歌关闭了关于可访问性滞后的错误报告，因为该功能“按预期工作”时，我们和你们许多人一样困惑和不安。但是我们没有接受表面上的解释，而是决定亲自调查此事以确定真相。所以当谷歌人在错误报告页面上说:

> #### 在 Android 版本中，这个问题一直存在，而且在启用辅助功能服务时，总会有额外的延迟。这是因为除了标准用户界面之外，该设备还为辅助功能服务提供了大量信息，因此它们可以为这些用户提供替代用户体验。

我们已经开始理解**为什么**这是**有意为之的行为。**以非谷歌所愿的方式使用辅助功能服务的应用程序总是会产生一些性能开销；这一成本对于向服务提供 Android 可访问性在后台发出的大量信息是必要的。Android 在无障碍服务方面的滞后是**不是一个错误，而是一个特性**。除非整个系统重新设计，否则我们将不得不接受这个特性，我无法想象如何适应来自这么多不同应用程序的这么多不同特性集。

至少，LastPass 的开发者不会坐视不管。他们的开发人员已经与 Chromium 开发人员合作[优化可访问性支持](https://bugs.chromium.org/p/chromium/issues/detail?id=428494)，可能是通过使用 API 启用 LastPass 支持[，而不是启用可访问性服务。围绕可访问性服务产生的开销进行优化是一种可能性，但正如许多开发人员在 Chromium 论坛上暗示的那样，这只是一个权宜之计，无法解决非预期使用可访问性服务可能导致延迟的事实。](https://bugs.chromium.org/p/chromium/issues/detail?id=467123)

* * *

特别感谢 AutoInput 的开发者 joaomgcd，他回答了我很多关于可访问性的问题！