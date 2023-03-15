# 用一个有用的工具捕捉你的恢复或香气的画面

> 原文：<https://www.xda-developers.com/capture-the-screen-of-your-recovery-or-aroma-with-a-useful-tool/>

*一图抵千言*。那是一句众所周知的谚语。在安卓系统中，图片被用来显示你的主屏幕，正在进行的开发，或者仅仅是演示一个错误。截图功能在很久以前就实现到了股票 Android 中，但在恢复中抓取截图仍然是相当有问题的。你可以尝试使用 Android SDK 的 monitor 工具，但它并不总是正确的。

幸运的是，几乎每个问题都有解决方法，XDA 是找到答案的好地方。XDA 论坛成员 [makers_mark](http://forum.xda-developers.com/member.php?u=5448769) 创建了一个从恢复和 Aroma 安装程序中抓取快照的工具。这个工具使用 FFmpeg 进行屏幕捕获，没有帧缓冲问题。除了必需的 ADB 和 FFmpeg 库之外，一个批处理脚本可以处理所有的问题。

这个工具应该适用于所有的恢复，所以你可以很容易地展示你的 TWRP 主题或修复你的*更新脚本*的问题。这个工具的唯一缺点是它只适用于 Windows。当然，要正确运行它，你的手机需要启用 ADB。

你可以通过访问[原始线程](http://forum.xda-developers.com/showthread.php?t=2635736)找到关于这个工具的更多信息。所以如果你想在恢复中截图，试试这个工具吧。