# 增加允许的锁屏模式尝试次数

> 原文：<https://www.xda-developers.com/increase-the-number-of-allowed-lock-screen-pattern-attempts/>

数据安全非常重要，这一点我们都很清楚。 [Heartbleed](http://www.xda-developers.com/announcements/heartbleed-what-xda-did-to-patch-this-critical-internet-flaw/) 只是强调了我们对数字数据安全性的依赖。在移动设备方面，有几种方法可以保护我们的数据免受窥探。其中一个是锁屏。你可以用几种方式保护你的锁屏，包括[一个可变设备解锁密码](http://www.xda-developers.com/android/thwart-password-stealing-eyes-with-timepin/)，面部检测，密码，传统密码，当然还有模式解锁。但是过度安全的设备也会成为其所有者的负担。毕竟，我们的记忆并不完美，我们可能会忘记解锁密码。

五次输入不正确的密码会迫使您等待 30 秒，然后才允许您重试。但是我们都不喜欢等待。考虑到这一点，XDA 的高级成员 [hamzahrmalik](http://forum.xda-developers.com/member.php?u=5290145) 为 Xposed 框架创建了更多模式尝试模块。

顾名思义，模式尝试次数越多，在设备将自身锁定为 20 次之前，可以尝试的错误模式的数量就越多。关于五次失败的通知仍然存在，但是您可以立即进入下一个模式。在 20 次错误组合后，设备被锁定，只能通过登录您的 Google 帐户解锁。因为它是以 Xposed 模块的形式出现的，所以它只能在安装了 Xposed 框架的根设备上工作。

你可以在[模块线程](http://forum.xda-developers.com/showthread.php?t=2711498)中找到更多信息。