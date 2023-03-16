# 可达性光标使得单手使用高大的安卓手机变得容易

> 原文：<https://www.xda-developers.com/use-tall-android-phone-one-handed/>

每天，许多开发者都会在我们的[应用和游戏论坛](https://forum.xda-developers.com/android/apps-games)上发布新的应用或游戏。我们在 XDA 论坛上搜寻有趣的新 Android 应用，我们认为你可能会喜欢，我们最喜欢的一些应用甚至得到了我们在[的特别关注。每天都有如此多的应用发布，要找到一个真正独特而迷人的应用就像大海捞针，但这正是我们今天所做的。我们论坛上的一位开发者想出了一个创新的解决方案，来解决单手使用高大的 Android 手机的问题。这款名为“可达性光标”的应用程序创建了一个屏幕光标，你可以拖动它来执行点击、长按和拖动手势。](https://www.xda-developers.com/tag/xda-spotlight/)

了解这款应用的卓越之处的最简单方法是观看一个快速演示:

https://i.imgur.com/cEUbjfw.gifv

*点击[此链接](https://imgur.com/a/RlQiqMV)可以看到完整的演示视频。*

华为、三星和小米的智能手机都内置了单手模式功能，华为甚至一度试图将他们的单手模式功能贡献给 AOSP。我们[做了一个应用](https://www.xda-developers.com/one-handed-mode-brings-apples-reachability-any-android-phone/)，它使用 Android 内置的过扫描功能，试图将单手模式带到任何设备上，但可达性光标采用了不同的、公认更好的方法来解决同样的问题。

## 可达性光标功能

有了这个应用的免费版本，你可以很好地使用可达性光标，但你会错过所有我认为值得的定制选项。专业版售价 4.49 美元，但如果你发现自己经常在你的高手机上使用这个应用程序，你就不会觉得很难证明这个价格是合理的。

### 如何使用

您可以设置所谓的“滑动板”来触发可达性光标。滑动垫可以位于屏幕的底部、左+右、左或右边缘。(左右滑动垫都从屏幕的下半部分开始。)当您从选定的屏幕边缘开始手势时，您的手指将悬停在跟踪器上。跟踪器允许您将屏幕上的光标移动到您想要执行点击、长按或滑动手势的区域。如果您不进行任何操作，光标会自动消失。这相当简单，在我看来，非常直观。

### 用户化

您可以自定义滑动垫的宽度、是否有触觉反馈、不活动超时、光标和跟踪区域、光标大小/颜色以及效果颜色。您还可以添加所谓的“边缘动作”这些动作，比如打开通知、快速设置、最近应用等。是通过将光标推向选定的屏幕边缘来执行的。

### 实验设置

由于应用程序的工作方式(它使用辅助功能服务)，您可能会在启用后遇到一些轻微的口吃或延迟。幸运的是，开发者已经意识到了这个问题，并且已经提供了一个实验性的服务来解决这个问题。我可以证实，启用实验性的“特权模式”设置在 OnePlus 6 和三星 Galaxy Note 9 上产生了奇迹。

特权模式的工作原理是在需要时自动启用应用程序的辅助功能服务，在不需要时禁用它。这要求您通过以下 ADB 命令授予应用程序 WRITE_SECURE_SETTINGS 权限:

```
 adb shell pm grant com.niftyui.reachability android.permission.WRITE_SECURE_SETTINGS 
```

然后，这将授予可达性光标写入`Settings.Secure.enabled_accessibility_services`的权限，以切换应用程序的辅助功能服务`com.niftyui.reachability/com.niftyui.reachability.service.LiteService`。因此，应用程序可以在没有用户干预的情况下打开和关闭自己的辅助功能服务。这是一个巧妙的技巧，可以避开易访问性服务可能导致的[已知性能问题](https://www.xda-developers.com/working-as-intended-an-exploration-into-androids-accessibility-lag/)。

## 下载可达性光标

你可以从下面的谷歌 Play 商店链接下载这个应用程序。你可以不用花一分钱就能很好地使用这款应用，但在使用几天后，你会像我一样忍不住支付 4.49 美元购买高级版。

如果你想给开发者留下一些反馈，一定要看看下面的 XDA 论坛链接。

[**查看我们论坛上的可达性光标**](https://forum.xda-developers.com/android/apps-games/app-reachability-cursor-phone-t3846525)

我认为这是一款出色的应用，值得关注。我已经在我的 OnePlus 6 上使用这个应用程序超过一周了，OnePlus 6 在 OxygenOS 中缺少单手模式。结合我们自己的[导航手势应用](https://forum.xda-developers.com/android/apps-games/official-xda-navigation-gestures-iphone-t3792361)，我可以隐藏导航条来使用手势控制，而不必再担心需要到达我的手机顶部。