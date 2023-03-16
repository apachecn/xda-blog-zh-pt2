# 可能是第一个已知的 Android Q 详细功能:所有人的辅助拨号

> 原文：<https://www.xda-developers.com/android-q-feature-assisted-dialing/>

现在[移动世界大会](https://www.xda-developers.com/tag/mwc/)已经结束，Android 爱好者们正把注意力集中在即将发布的 [Android P](https://www.xda-developers.com/tag/android-p/) 上。我早就推测第一个 Android P 开发者预览版将会在 3 月 14 日圆周率日发布，由于来自埃文·布拉斯的[新消息，这种可能性似乎越来越大。虽然我们只能在这里或那里了解到关于新版本的一些小花絮，但我们对它的继任者 Android Q 几乎一无所知。考虑到我们距离 Android Q 的发布日期还很远，我们不太可能在短期内了解到关于它的重要细节。但是多亏了我在 Android 开源项目(AOSP) gerrit 中发现的一点信息，我们可能已经找到了 Android Q 的第一个已知功能:辅助拨号。](https://twitter.com/MishaalRahman/status/969822517002211328)

* * *

## Android Q 中的辅助拨号

什么是辅助拨号？这是为国际旅行的人提供的一项功能，它只需通过添加适当的国家代码来更正您拨出的任何电话号码。这当然是一个很好的功能，因为当你在国外旅行一段时间后，你不必手动添加国家代码到你在国内的所有联系人中。

该功能已经在不同设备制造商的许多智能手机上提供，但它不是 Android 的原生功能。事实上，谷歌 Nexus 和 Pixel 智能手机只是最近才随着第 15 版[谷歌手机](https://www.xda-developers.com/tag/google-dialer/)应用的推出获得了这一功能。

*运行[安卓 8.1 奥利奥](https://www.xda-developers.com/tag/android-8-1/)的[谷歌 Pixel 2 XL](https://www.xda-developers.com/tag/google-pixel-2/) 上谷歌手机应用的辅助拨号设置*

大量有用的基本功能是非谷歌设备的主要功能，可能需要很长时间才能进入 AOSP，这意味着它们将在大多数(如果不是所有)安卓设备上普遍可用。最近，我们在 Android P 中看到了一个正在进行的新工作[增强的呼叫阻止功能](https://www.xda-developers.com/android-p-blocking-calls-unknown-private-pay-phone-numbers/)和 [Wi-Fi 直接打印](https://www.xda-developers.com/wi-fi-direct-printing-android/)，但还有无数的例子可供选择。随着 Android Q 的推出，谷歌手机应用程序的辅助拨号功能似乎将被纳入 Android 框架——这意味着它将对所有人开放。

乍一看，上面的 [commit](https://android-review.googlesource.com/c/platform/packages/apps/Dialer/+/632265) 并没有说 Android Q 的什么特别之处。然而，当您检查代码更改时，对 Q 的引用变得非常清楚。

如果您查看这一行的之前和之后，构建代码上限之前被设置为 O MR1 (Android 8.1 Oreo)，目标构建代码被设置为 P。然而，现在，上限已被更改为 Android P，目标现在是 Android Q。这告诉我们，Google 最初计划在 Android P 中引入辅助拨号功能，但可能时间不够了，他们现在将 Android Q 作为该功能的发布目标。

现在，我们意识到这是一个非常小的变化。对于国际旅行者来说，辅助拨号当然是一个非常有用的功能，但它不是那种会成为 Android Q 发布头条的功能。它肯定无法与 Android 8.0 Oreo 中引入的[通知通道](https://www.xda-developers.com/notification-importance-controls-all-apps-android-oreo/)、[画中画模式](https://www.xda-developers.com/netflix-pip-mode-picture-android-8-1/)、[自适应图标](https://www.xda-developers.com/custom-icons-adaptive-icons-adapticons/)或[自动填充框架](https://www.xda-developers.com/keepass2android-beta-autofill-android-oreo/)等功能相提并论。

无论如何，这是 Android 未来版本中一个功能的第一个暗示，这个功能离发布还有很长很长的路要走，最初只会对那些拥有谷歌 Pixel 2/2 XL 或计划拥有即将到来的谷歌 Pixel 3 的幸运儿开放。鉴于我们已经对 Android P 了解了多少，我们肯定会在 Android Q 中发现更多的特性，无论何时 P 源代码和系统文件被删除。