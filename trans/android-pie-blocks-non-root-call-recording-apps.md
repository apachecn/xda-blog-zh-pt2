# Android Pie 阻止非根呼叫记录应用程序工作

> 原文：<https://www.xda-developers.com/android-pie-blocks-non-root-call-recording-apps/>

随着 [Android 9 Pie](https://www.xda-developers.com/android-pie-google-pixel-google-pixel-2/) 的发布，增加了许多可爱的新功能。在新的[手势导航 UI、](https://www.xda-developers.com/android-p-iphone-x-gestures-official/) [RAM-heavy 游戏保护](https://www.xda-developers.com/android-pie-ram-heavy-games-exit/)、[切片和应用程序动作](https://www.xda-developers.com/slices-app-actions-android-p-google-assistant/)API 之间，谷歌已经为他们最新版本的移动操作系统投入了大量工作。然而，似乎确实有一些倒退。虽然我们注意到今年二月添加的电话录音音[的存在，但这似乎只是为了一致性而添加的，而不是 Android 将获得更好的电话录音功能的信号。相反，看起来 Android Pie 已经完全屏蔽了没有 root 的通话记录。](https://www.xda-developers.com/android-p-call-recording-tone-support-record-phone-calls-lawfully/)

这不是谷歌第一次挑战电话录音。其实公司已经做了一段时间了。早在 Android Marshmallow 发布时，谷歌就取消了官方的电话录音 API，让开发人员自己创造方法。这很好，因为这些解决方案和官方 API 一样好，甚至更好。 *CallRecorder - ACR* 和*bold beast Android Call Recorder*的开发者已经证实，谷歌已经关闭了他们用来记录通话的变通办法，只剩下 root-only 方法是记录电话通话的唯一方法。

虽然通话记录的合法性因国家而异，但奇怪的是谷歌会采取措施完全阻止它。有些国家只要求一方同意，即使双方同意，也有很多原因可能会对电话进行录音。增加一个哔哔声被认为是接受了通话录音，然而，谷歌仍然完全禁止它。将来可能会发现一个非根方法，不要抱太大希望。现在，你将被迫使用根功能的应用程序来记录你的任何电话。有可能*也许*这种变化不是有意的，但不管怎样，它对许多人来说都是一种阻碍。如果将来 Android Pie 上的通话记录状态发生变化，我们一定会及时通知您。

[appbox googleplay com.nll.acr]

* * *

[**Via:PiunikaWeb**](http://piunikaweb.com/2018/08/14/android9pie-closes-all-doors-to-call-recording-sans-root-say-third-party-app-devs/)

[**来源 1: CallRecorder - ACR**](https://bitbucket.org/copluk/acr/issues/2418/kb-android-9-p-call-recording-issues)

[**来源二:BoldBeast**](https://www.boldbeast.com/forum/post6730.html#p6730)