# 【更新:合并】从 Android 11 R 开始，飞行模式可能最终停止关闭蓝牙音频

> 原文：<https://www.xda-developers.com/airplane-mode-stop-shutting-down-bluetooth-audio-android-11-r/>

# 【更新:合并】从 Android 11 R 开始，飞行模式可能最终停止关闭蓝牙音频

飞行模式有一些方便的用法，但它不是一个非常微妙的工具:一次点击就关闭所有的收音机。但是，在 Android 11 R 中，它可能会变得更加智能。

**更新(1/24/20 @美国东部时间下午 4:15):**Android 11 中飞行模式不关闭蓝牙音频的提交已合并。

飞行模式是一个已经在手机中存在了很长时间的功能。这个名字来自于手机中的无线电会干扰飞机的想法，所以这允许你在没有完全关闭手机的情况下关闭它们。当然，飞行模式还有其他用途，但它并不是一个非常微妙的工具:一次点击就能关掉所有的收音机。但是，在 Android 11 R 中，它可能会变得更加智能。

如果你想快速禁用手机和 Wi-Fi，这种一刀切的方法可能会很烦人，但你正在通过蓝牙听音乐。如果你熟悉 ADB，已经有一个[方法可以定制在飞行模式下关闭哪些无线电](https://www.xda-developers.com/customize-radios-airplane-mode-android/)。当然，这不是一个面向消费者的功能，也不是大多数人会在意的。[AOSP Gerrit](https://android-review.googlesource.com/c/platform/frameworks/base/+/1179105)中的一项新承诺名为“环境感知蓝牙飞行模式”,听起来像是一个非常受欢迎的功能。

*当开启飞行模式且蓝牙处于以下情况之一时，不要自动关闭蓝牙:*

1.  1.  *蓝牙 A2DP 已连接。*
    2.  *蓝牙助听器模式已连接。*

Android 将足够聪明地意识到，如果你目前正在使用蓝牙，你可能不想在打开飞行模式时禁用它。“A2DP”是大多数蓝牙耳塞和耳机用于媒体流的配置文件。提交还没有合并，但我们可以期待在 Android 11 R 中看到它，这是该操作系统的下一个主要版本。这是一件小事，但如果你经常使用飞行模式和蓝牙，它会产生很大的影响。

*感谢 XDA 公认的开发者 [luca020400](https://forum.xda-developers.com/member.php?u=5778309) 的提示！*

* * *

## 更新:合并

在上个月提交之后，看起来上下文感知蓝牙飞行模式正在向前发展。提交被合并，这意味着我们将在 Android 11 中看到这个功能。这将允许飞行模式理解蓝牙的上下文，并且在使用时不关闭它。

**来源:[AOSP](https://android-review.googlesource.com/c/platform/frameworks/base/+/1179105)**