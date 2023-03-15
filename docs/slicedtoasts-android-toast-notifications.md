# 使用切片 Toast 控制 Toast 通知

> 原文：<https://www.xda-developers.com/slicedtoasts-android-toast-notifications/>

# 使用切片 Toast 控制您的 Toast 通知

SlicedToasts 允许您控制 toast 通知长度或完全禁用它

吐司很好吃，即使是机器人口味的。在安卓系统中，吐司不会带来美味的三明治，而是一种通知。谷歌决定使用这些简短的提示来告知正在发生的各种事情。例如，当应用程序被授予超级用户访问权限时，您可能会看到一个提示。

尽管 toast 通知背后的想法很棒，但谷歌在实现细节方面仍有很大的改进空间。开发人员不喜欢等待，所以他们开始玩通知这样的细节。因此，XDA 论坛成员 [abellujan](http://forum.xda-developers.com/member.php?u=5958333) 创建了一个 Xposed 模块，让你的祝酒时间短于最短持续时间，长于默认最长持续时间。使用此模块，您还可以完全禁用 toast 通知。它不是可用的最大的 Xposed 模块，但是对于许多想要对这些通用 UI 元素有更多控制的 Android 用户来说，它可能是有用的。

因为这个 mod 是作为一个 Xposed 框架模块交付的，所以您需要在您的设备上运行 Xposed。当一切都设置好了，应用模块并重启你的设备来看看效果。

你对目前的祝酒通知外观和感觉很不满意吗？如果是这样，只需几个步骤就能改变它。您可以通过访问 [SlicedToasts 模块线程](http://forum.xda-developers.com/xposed/modules/mod-slicedtoast-1-0-shortens-toasts-t2826174)开始。