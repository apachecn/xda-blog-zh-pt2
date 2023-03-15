# Android O 的自动填充框架将最终解决密码管理器的长期滞后问题

> 原文：<https://www.xda-developers.com/android-os-autofill-framework-will-finally-resolve-a-long-standing-lag-issue-with-password-managers/>

谷歌发布第一个 Android O 开发者预览版已经一个月了(时间过得真快！)，就像任何新版本的 Android 一样——有很多东西需要挖掘。我们已经[发表了大量关于 Android O 的文章](https://www.xda-developers.com/tag/android-o/)，但是有一个功能我觉得还没有得到应有的关注:T4 的自动填充框架。

### Android O 中的自动填充

如今，密码管理器随处可见(尽管我们更喜欢开源的 KeePass，但只有在 Android O 上，谷歌才真正正式支持密码管理器。使用 Android O，第三方应用程序可以填充自动填充服务，该服务通过新的自动填充框架与应用程序进行通信。使用标准[视图](https://developer.android.com/reference/android/view/View.html)元素的应用程序将与开箱即用的自动填充框架一起工作，尽管开发者可以采取额外的步骤来[优化自动填充](https://developer.android.com/preview/features/autofill.html#optimizing_your_app_for_autofill)，以确保应用程序的任何自定义视图都可以自动填充。

当自动填充视图成为焦点时，自动填充框架将调用自动填充请求。自动填充服务通过发回某些自动填充数据集(如用户名、密码、地址、信用卡号等)来响应。)用户然后可以选择它。自动填充服务由用户在设置->应用与通知->默认应用->自动填充应用中指定。

 <picture>![](img/defb4d8501a88dda48e614c015a3fc28.png)</picture> 

Autofill App in Android O. Credits: [Lastpass](https://blog.lastpass.com/2017/04/what-lastpass-users-can-expect-in-android-o.html/).

上面对新的自动填充框架的解释只是对请求应用程序和自动填充服务端发生的事情的简要总结。对于你的理解来说，最重要的不是自动填充在 Android O 中如何工作的具体细节，而是这样一个事实，即**密码管理器应用程序本身不再检测视图何时可以被自动填充**。

* * *

**推荐阅读:** [AgileBits 展示 Android O 的自动填充框架会是什么样子](https://www.xda-developers.com/agilebits-shows-off-what-android-os-autofill-framework-will-look-like/)

* * *

### 安卓 O 前自动填充

与 Android O 之前的自动填充相比，在密码管理器有任何官方方法来检测视图何时可以自动填充之前，每个应用程序都必须实现可访问性服务来扫描当前视图，以便找到自动填充字段。

然而，在某些情况下，使用辅助功能服务会导致相当大的延迟。然而，与典型的密码管理器的可访问性服务相关的滞后是如此明显，以至于流行的服务如 LastPass 甚至有关于这个问题的[支持页面](https://lastpass.com/support.php?cmd=showfaq&id=8166)。这些支持页面通常会告诉您，处理由辅助功能服务导致的过度延迟的唯一方法是禁用辅助功能服务或切换到使用他们自己的自定义输入法。无论哪种方式，您都会失去任何自动填充功能。

但是到底为什么 LastPass 的可访问性服务，或者任何其他密码管理器的可访问性服务，看起来会造成这么大的延迟？原因是这些密码管理器必须利用可访问性服务来检测输入字段。辅助功能服务的[属性](https://developer.android.com/reference/android/R.styleable.html#AccessibilityService)是在 APK 内的 [XML 资源文件](https://developer.android.com/reference/android/accessibilityservice/AccessibilityService.html#SERVICE_META_DATA)中定义的，因此我们可以通过反编译 APK 文件来了解服务是如何工作的。

下面是反编译 LastPass APK 的资源文件:

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

由此，我们可以收集以下信息:LastPass 的可访问性服务请求两种事件类型进行监控——TYPE _ VIEW _ FOCUSED 和 TYPE_WINDOW_CONTENT_CHANGED。它这样做是因为它需要知道应用程序/网页的内容何时改变或成为焦点，然后它检索当前窗口内容以寻找任何密码输入字段。但是由于服务经常在两个非常频繁的可访问性事件上这样做，所以会导致延迟。关于可访问性服务如何导致延迟的更深入的讨论，我可以参考我以前关于这个问题的文章。

* * *

**推荐阅读:** [【按预期工作】——安卓无障碍滞后探究](https://www.xda-developers.com/working-as-intended-an-exploration-into-androids-accessibility-lag/)

* * *

### 安卓 O 一石二鸟

在 Android O 之前，密码管理器的开发者并没有多少办法来缓解这种滞后。这是因为如果没有辅助功能服务的持续监控，密码管理员就无法知道自动填充的输入字段何时出现在屏幕上。但由于 Android O 中新的自动填充框架，这些密码管理器现在可以退休他们的可访问性服务了。相反，需要数据输入的应用程序将请求自动填充框架调用自动填充服务，然后自动填充服务将发送数据。有了这个新框架，不仅用户输入密码变得更加容易，因为他们不再需要依赖额外的输入方法，而且与启用密码管理器的可访问性服务相关的延迟也将成为过去。

我知道，对你们中的一些人来说，这个事实可能不是突破性的，但是我认为，由于围绕可访问性服务的讨论是如此沉默，这个话题可能值得重新点燃。只是这个周末的精神食粮！

* * *

**如何看待 Android O 新的自动填充框架？请在下面的评论中告诉我们！**