# Xposed Framework 2.4 退出测试版，带来官方 KitKat 支持和错误修复

> 原文：<https://www.xda-developers.com/xposed-framework-2-4-exits-beta-brings-official-kitkat-support-and-bug-fixes/>

不到一周前，我们报道了 Xposed Framework 2.4 beta 的[发布。对于那些刚刚收听的人来说，2.4 测试版带来了一个非常重大的变化:支持 Android 4.4 KitKat。现在仅仅几天后，XDA 承认开发者](http://www.xda-developers.com/android/xposed-framework-now-compatible-with-android-4-4/ "Xposed Framework Now Compatible with Android 4.4") [rovo89](http://forum.xda-developers.com/member.php?u=4419114) 已经将 2.4 从测试版中拿出来并进入正式流通。

除了带来对 Android 4.4 的官方支持，Xposed 2.4 final 还带来了一些其他的改进和错误修复。也许最引人注目的将是框架性能的显著提高。UI 也得到了改进，因为现在有了一个调试日志查看器和诊断工具来验证 Xposed 是活动的和工作的。

需要注意的是，即使在 2.4 最终版中，Xposed 也与新的 ART 编译器不兼容。目前，还不清楚它是否会兼容，因为如果有可能的话，它将需要一次大的重写。因此，为了防止引导循环，如果您意外地启用了 ART，Xposed 框架会自动将您重置为 Dalvik。

要开始，只需前往[应用线程](http://forum.xda-developers.com/showthread.php?t=1574401)。要了解更多关于 2.4 版本的信息，请前往[这篇文章](http://forum.xda-developers.com/showthread.php?p=47991707#post47991707)详细介绍所有的变化。