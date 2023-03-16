# 【更新:5 月更新修复】安卓 8.1 奥利奥多点触控 Bug 将在 6 月更新修复

> 原文：<https://www.xda-developers.com/android-8-1-oreo-multi-touch-bug-fixed-june-update/>

# 【更新:5 月更新修复】安卓 8.1 奥利奥多点触控 Bug 将在 6 月更新修复

谷歌已经修复了影响 Android 8.1 Oreo 中一些设备的不稳定多点触摸行为。合并提交修复了多个指针的重采样。但是，该修补程序不会在 5 月的安全更新中发布，因为更改在一个月前就被锁定了。它将在六月更新中发布。

**5/7 更新:**谷歌已经提前一个月修复了这个问题。可以在 5 月的安全修补程序中找到该修补程序。其他原始设备制造商将需要合并修复。

谷歌 Pixel 2 和 Pixel 2 XL 被列入受 Android 8.1 Oreo 多点触摸漏洞影响的设备列表中。当两个手指放在显示屏上时，两个手指之间会产生不稳定的触摸屏事件。这个问题在游戏中很普遍，但在谷歌照片等其他应用程序中也很明显。经历过触摸屏问题的用户将其描述为令人沮丧。更糟糕的是，从谷歌问题跟踪页面上的报告数量来看，这种情况似乎很普遍。

上周，[我们向您展示了 Pixel 2 根用户如何刷新 Magisk 模块来修复问题](https://www.xda-developers.com/fix-multi-touch-bug-google-pixel-2-xl-android-oreo/)。XDA 资深成员 [Freak07](https://forum.xda-developers.com/member.php?u=3428502) 成功编译了更新的库(libinput 和 libinputflinger)来对抗谷歌 Pixel 2 和 Pixel 2 XL 的最新[4 月安全补丁构建](https://www.xda-developers.com/nexus-pixel-security-april-2018-ota-factory-images/)。因此，谷歌设备的根用户现在可以通过安装该模块轻松解决这个问题。安装模块的步骤已经在我们的教程中详细说明了。

然而，到目前为止，股票用户运气不佳。其他设备的用户也不能刷新模块来解决触摸屏问题。因此，他们一直在等待谷歌在更新中解决这个问题。

现在，谷歌已经修复了 Android 8.1 奥利奥上不稳定的多点触摸行为问题。[AOSP 640606 号提交已合并为 f0d877c](https://android-review.googlesource.com/c/platform/frameworks/native/+/640606/) 。它的标题写道:**“修复多个指针的重采样。”**

commit 上的多个评论表示，它修复了在几个 Android 8.1 设备上观察到的不良触摸重采样问题，如 Pixel 2 和 Razer 手机。提交的一个评论员说，自从应用补丁以来，他没有观察到 Pixel 2 上有跳动的指针移动。

坏消息是:补丁**将不会成为五月份安全补丁更新的一部分。这大概是因为这些变化在一个月前就被锁定了。该修补程序的时间范围意味着它只会作为 6 月安全修补程序更新的一部分出现。这意味着受影响设备的用户将不得不等待两个月，这令人失望。因此，我们鼓励 Pixel 2 的根用户现在刷新 Magisk 模块来修复这个问题，而不是等到 6 月份正式修复。**