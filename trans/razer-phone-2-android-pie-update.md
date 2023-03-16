# 【更新 2:美国电话电报公司发布】Razer Phone 2 的 Android Pie 更新将于下周为解锁设备发布

> 原文：<https://www.xda-developers.com/razer-phone-2-android-pie-update/>

**更新 2(美国东部时间 2019 年 7 月 26 日上午 09:10):**AT&T Razer Phone 2 的 Android Pie 更新终于推出了。

**更新 1 (2/27/19 @ 06:05 PM ET)** :正如承诺的那样，官方 Android Pie 更新现已为解锁的 Razer Phone 2 推出。我们已经在文章末尾的更新中发布了变更日志。Razer 甚至添加了一些我们最初不知道的额外功能！原文如下。

Razer 是最受欢迎的游戏设备制造商之一，这得益于其时尚的 PC 配件、笔记本电脑和其他硬件系列。回到 2017 年 1 月，他们[收购了一家名为 Nextbit](https://www.xda-developers.com/nextbit-has-officially-been-acquired-by-razer/) 的小型智能手机初创公司。这是我们的第一个线索，表明该公司将把自己的产品引入智能手机行业。这并没有花他们很长时间，因为直到 2017 年 11 月我们才看到第一款 Razer 手机。这款手机凭借其顶级的规格和独特的 120Hz 可变刷新率显示屏，对智能手机爱好者颇具吸引力。该公司随后于 2018 年 10 月发布了几个月前发布的 Razer Phone 2。

Razer Phone 2 与 Android 8.1 Oreo 一起发布，尽管我们知道该设备最终将获得 Android 9 Pie。然而，我们不知道 Android Pie 更新何时会到达设备。现在，Razer 已经正式公布了 Razer Phone 2 的 Android 9 Pie 更新路线图。从 2 月 27 日开始，解锁版机型的消费者将可以获得更新。该更新将于 3 月 14 日在运营商手机(不包括美国电话电报公司)上发布，4 月 4 日在美国电话电报公司机型上发布(这两个日期都有可能发生变化。)

[**雷蛇手机 2 XDA 论坛**](https://forum.xda-developers.com/razer-phone-2)

虽然更新中似乎没有任何新的 Razer 专用功能，但新的 Android Pie 软件功能当然是受欢迎的。此次更新带有最新的【2019 年 2 月安全补丁和 Linux 内核版本 4.9.112。

### 手势导航

围绕 Android Pie 的手势导航一直存在一些争议。一些用户喜欢它，而一些用户非常讨厌它，以至于它带来了新一波导航手势应用([就像我们自己的](https://play.google.com/store/apps/details?id=com.xda.nobar&hl=en))。手势导航成为一些手机的强制功能的事实让事情变得更糟。幸运的是，Razer 正在采取一种更友好的方法，并让用户能够禁用它。更新到 Android Pie 后，你会看到默认启用的新手势导航。我想你现在已经知道该怎么做了，但是为了刷新你的记忆，你可以长时间向上滑动来打开应用抽屉，短时间向上滑动来打开最近的应用菜单。正如我已经提到的，您可以随时禁用它。你只需要进入**设置>系统>手势**，关闭**“在 Home 键上向上滑动”**以下是该功能的一些截图。

编者按:对于所有的修改者，请注意这一点。Android 9 Pie 改变了最近应用概览的处理方式。默认的最近应用程序组件不再是 SystemUI 应用程序(事实上，Android Q [完全去掉了](https://www.xda-developers.com/android-q-gestures-back-button/) SystemUI 的最近应用程序组件)，取而代之的是，通常默认为股票启动器应用程序。QuickStep 是处理横向最近应用概述和手势药丸的组件的名称。在谷歌 Pixel 上，Pixel 启动器集成了 QuickStep，而在一加 6T 上，一加启动器处理它。由于 Razer Phone 2 配备了 Nova Launcher Prime，您可能会认为 Nova Launcher 正在处理最近的应用程序概述和手势。然而，反编译框架证实了它实际上是处理 QuickStep 的 AOSP 启动器，尽管 Nova 仍然是默认的启动器。有趣的是，这意味着 Razer 已经修复了与概览手势相关的问题，当用户在 Android Pie 中切换到第三方启动器时，这些问题臭名昭著地困扰着其他设备。

### 精致的用户界面

接下来你会注意到的是系统重新设计的用户界面。最引人注目的重新设计是在设置应用程序中，它现在符合 Google I/O 2018 上推出的最新 Google Material 主题标准。大多数图标都有新的设计，而应用程序本身的背景更白。分类和层次也符合 Android 9 的标准。你也可以在**系统>设置下看到 Razer 偏好类别。**

### 自适应电池

令人惊讶的是，并不是每部 Android Pie 手机都包含自适应电池。幸运的是，Razer Phone 2 确实包含了这一功能，可以根据当前的使用情况调整内存管理和功率限制。Razer 提供了一个我以前没有想到的非常有趣的例子。假设您喜欢每隔几个小时打开一个特定的应用程序。随着时间的推移，你的设备将了解这一点，并为该应用程序释放内存，以便它不会在后台死亡。您可以在**设置下找到该功能>电池**为**自适应电池**。

### Android 运行时(ART)改进

除了美观和功能上的变化，Android Pie 还包括了大量的改进。其中最重要的是对 Android 运行时的改进。Android Pie 优化了应用程序启动和 DEX 内存使用。这不太容易衡量，但 Razer 声称重写 DEX 文件的次数减少了 11%,这本身将使整个系统的速度稍微快一点。

TK Bay 从我们的 XDA 电视 YouTube 频道截取的所有截图。

更多关于 Razer Phone 2 的信息:

* * *

## 更新 1:推出 4K@60FPS 视频录制和数字福利

Android 9 Pie 更新现已面向解锁机型的用户推出。这是官方的变更日志:

*   自适应电池
*   手势导航
*   通知管理
*   数字福利支持
*   相机现在支持 720p/1080p/4K、60FPS 的视频录制。
*   错误修复和性能改进。
*   截至 2019 年 2 月 5 日的安全更新

更新大小为 1419.7MB. Razer 的 changelog 提到 4K 视频录制速度为 60FPS，这是我们上周发现的。然而，在谷歌[宣布](https://www.xda-developers.com/google-assistant-digital-wellbeing-google-lens-mwc/)更多设备将获得数字健康功能后，此次更新也令人惊讶地增加了数字健康支持。与三星 Galaxy S10 上的[数字福利不同，Razer 使用的是谷歌的数字福利，这意味着它将从谷歌 Play 商店获得更新。](https://www.xda-developers.com/samsung-galaxy-s10-new-software-features/)

从 Razer 软件更新的历史来看，更新现在正在推出，应该会在未来 3-4 天内到达所有解锁的设备。然而，如果你不想等待，你可以下载下面的 OTA，由 XDA 的 j1505243 提供，并侧载它。当其他 Razer Phone 2 型号的 Android Pie 更新推出时，我们将更新您。

**[下载解锁的雷蛇手机 2(aura/Cheryl 2)安卓派更新](https://android.googleapis.com/packages/ota-api/razer_aura_cheryl2/e2152a2c966d6c0950ae58c5360bdf0d49f949a0.zip)**

* * *

## 更新 2:美国电话电报公司 Razer Phone 2 的 Android Pie 更新现已推出

花了一段时间，但美国电话电报公司的 Razer Phone 2 终于获得了 Android Pie 更新。谢天谢地，延迟的一线希望是用户可以在更新时获得 2019 年 7 月的安全补丁。

**来源:[/u/Arthur kot](https://www.reddit.com/r/razerphone/comments/chx6lj/android_pie_update_for_att_is_finally_here/)**