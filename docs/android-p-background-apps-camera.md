# Android P 将阻止后台应用程序访问相机

> 原文：<https://www.xda-developers.com/android-p-background-apps-camera/>

Android P，Android 的下一个主要版本，[可能还有几周](https://twitter.com/mishaalrahman/status/958428092669874176)才会正式发布，尽管它的[核心面向用户的功能](https://www.xda-developers.com/chromium-gerrit-material-design-2-colors/)仍不为我们所知，但由于 Android 的开源特性，我们正在发现许多小花絮。我们知道它会让运营商[隐藏信号强度](https://www.xda-developers.com/android-p-signal-strength-carriers/)和[定义它们如何在状态栏](https://www.xda-developers.com/android-p-carriers-define-lte-signal-bars/)中显示，例如，我们发现有证据表明谷歌可能会取消开发者对[未记录和隐藏的 API](https://www.xda-developers.com/google-undocumented-hidden-apis-android-p/)的访问。*彭博*本月早些时候报道称，下一个版本的 Android 将[支持带有“多屏”和“可折叠显示屏”的手机](https://www.xda-developers.com/android-p-atypical-display-types-material-design-2/)，我们还发现有迹象表明，该更新将支持[通话录音功能](https://www.xda-developers.com/android-p-call-recording-tone-support-record-phone-calls-lawfully/)。

但是 Android P 的改进并不止于此。据 1 月 19 日合并的 Android 开源项目(AOSP) [commit](https://android-review.googlesource.com/c/platform/system/sepolicy/+/588493) 称，Android P 中的新规则集将阻止空闲的后台应用程序访问相机。这将确保当您的屏幕关闭时，在后台运行的恶意应用程序无法拍摄您或您所爱的人的潜在危险照片以进行勒索。

## Android P 有什么变化？

规则的改变针对的是应用程序的 uid(用户 id)，即 Android 在安装时分配给每个应用程序的标识符。它们对每个应用程序都是唯一的，并且不会改变——只要应用程序仍然安装在你的手机或平板电脑上，它就会保留相同的应用程序 ID。

在 Android P 中，当相机服务检测到一个 UID 处于“空闲”状态时——也就是说，当设备处于空闲[瞌睡](https://www.xda-developers.com/xda-external-link/check-for-doze-support-on-your-device/)状态并且[后台应用对 CPU 和网络密集型服务](https://www.xda-developers.com/how-android-n-will-improve-battery-and-memory-management/)的访问受到限制时——Android 将生成一个错误并关闭对相机的访问。来自非活动 UID 的后续摄像机请求将立即产生错误。

它建立在从 Android 6.0 棉花糖开始的相机服务变化的基础上。在 Lollipop 和旧版本的 Android 中，应用程序被授予“先到先得”的摄像头访问权限。但对于 Marshmallow，相机服务强烈支持具有前台和用户可见活动的应用程序。这有点像游乐园里的快速通道队列:排队等待摄像头访问的高优先级应用程序会跳到低优先级应用程序前面。

## 为什么重要？

对后台应用摄像头访问的限制早就应该出台了。2014 年，Android 开发者 Szymon Sidor 发表了一篇博文[解释了应用程序如何通过巧妙地操纵 Android 的相机权限来偷偷拍照和录制视频。通过将相机应用的取景器缩小到 1px，使其几乎不可见，西多尔能够在不提醒用户应用活动的情况下访问 Nexus 5 的相机——即使应用在后台运行，手机屏幕关闭。](http://snacksforyourmind.blogspot.com/2014/05/exploring-limits-of-covert-data.html)

随着 [Android P](https://www.xda-developers.com/tag/android-p/) 后台摄像头限制的到位，像 Sidor 先生的博客文章中描述的恶意应用程序将更容易被检测到，因为这种恶意应用程序需要实现一个前台服务才能生存，并且由于 [Android Oreo 的要求](https://www.xda-developers.com/hide-app-running-background-notification-android-oreo/)，这将意味着应用程序必须显示一个通知，告诉你该应用程序正在运行(并且该应用程序显示在其他应用程序的顶部)。如果这样的应用程序试图隐藏在后台，那将不再有效，因为它将无法访问 p 中的摄像头。