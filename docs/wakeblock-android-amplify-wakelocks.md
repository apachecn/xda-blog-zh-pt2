# 使用唤醒锁停止根 android 设备上的唤醒锁

> 原文：<https://www.xda-developers.com/wakeblock-android-amplify-wakelocks/>

那些错过了牛轧糖的人(虽然如果你很绝望，我猜有一种工作端口)可能会特别错过名为 Amplify 的模块。大约两年前，我购买了捐赠版本，但这不足以吸引我继续吃棉花糖。尽管如此，我还是很怀念。让我在手机上限制一些烦人的唤醒锁。对于那些不太熟悉的人来说，唤醒锁是一个在屏幕关闭时唤醒手机的过程。这通常很好，因为它允许你接收文本、听音乐等等。然而，应用程序可以(并且经常)滥用它，所以 Amplify 是一种流行的方法来限制应用程序可以保持唤醒锁-提高性能和电池寿命。

然而，现在有一个新的应用程序准备做几乎和 Amplify 完全一样的事情，但它不需要 Xposed 框架，所以它可以在 Android 牛轧糖设备上工作。 [WakeBlock](https://forum.xda-developers.com/android/software/wakeblock-blocking-drain-late-t3526313) 在我们的应用程序上&游戏论坛最近刚刚到来，你可以向它投掷任何设备，最初是在谷歌 Nexus 6P 论坛上实现的！WakeBlock 几乎和 Amplify 一模一样，但稍后会详细介绍。这个应用程序修补了你的 services.odex 文件，**，所以你需要 root** ，允许它访问你的手机来限制唤醒锁。**修改该文件仍需通过安全网**。还有计划支持在未来阻止警报，这是 Amplify 所做的。根方面，我推荐使用 Magisk 或 SuperSU。

我们的论坛上有许多关于 Amplify 的指南，但也可以用于 WakeBlock。[看看这个充满各种唤醒锁的线程](https://forum.xda-developers.com/showpost.php?p=60429417&postcount=4)吧！但是要小心，因为弄乱错误的东西会导致不良后果。

WakeBlock 也可以用 ROM 编译，以前是在非 Nexus 6P 设备上使用它的唯一方式。**根据开发者的说法，该应用程序可以在任何时间**付费，因此也要注意这种可能性。尽管如此，如果你有设备无法睡眠的问题，我建议试一试，看看它如何为你工作。**根据开发者的说法，安装核心 mod 可能需要 5-30 分钟，这取决于你的设备和 ROM。**

* * *

[**从我们的论坛**](https://forum.xda-developers.com/android/software/wakeblock-blocking-drain-late-t3526313) 查看 WakeBlock