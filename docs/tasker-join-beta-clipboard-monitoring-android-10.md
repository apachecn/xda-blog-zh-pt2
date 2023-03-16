# 最新的 Tasker 和 Join 测试版在 Android 10 上恢复了剪贴板监控

> 原文：<https://www.xda-developers.com/tasker-join-beta-clipboard-monitoring-android-10/>

# 最新的 Tasker 和 Join 测试版在 Android 10 上恢复了剪贴板监控

Tasker 和 Join 开发人员 u/joaomgcd 已经成功地找到了一种解决方法来修复 Android 10 上的剪贴板监控。看看这里！

回到今年一月，我们了解到 [Android 10/Q 可能会考虑阻止剪贴板访问](https://www.xda-developers.com/android-q-block-background-clipboard-external-storage-permissions-downgrading-apps/)后台运行的应用程序。当我们在三月份第一次在 Android 10 测试版上拿到[的时候，](https://www.xda-developers.com/android-q-dp1-google-pixel-2-google-pixel-3/)[同样被证实是真的](https://www.xda-developers.com/android-q-blocks-background-clipboard-access/)。这意味着需要访问剪贴板数据才能正常工作的剪贴板管理器的终结。虽然这一变化无疑是安全性的一大胜利，但它伤害了许多第三方开发人员。现在，似乎 Tasker 和 Join 背后的开发者已经设法找到了一种变通办法，在 Android 10 上恢复剪贴板监控。

在 Reddit 上的单独帖子中，强调了应用程序的最新测试版更新，开发者 [u/joaomgcd](https://www.reddit.com/user/joaomgcd/) 透露他们已经成功实现了一个修复，允许剪贴板监控在 Android 10 上工作。Tasker 版本 5.9.beta.2 和 Join 版本 2.2.beta 中已经包含了该修复，它将允许这两个应用程序在后台运行时访问剪贴板数据。开发者还发布了一个视频，强调了在 Join 中打开剪贴板监控的方法。

来自用户的评论表明，该变通办法正在按预期工作。但是，当您尝试在手机上使用此功能时，仍可能会遇到一些无法预料的问题。除了修复之外，Tasker 的最新测试版更新还为该应用程序带来了许多其他变化。

以下是 Tasker v5.9.beta.2 中所有新增功能的完整变更日志:

*   修正了 Android 8+上的媒体按钮状态
*   增加了设置助手的动作:设置你手机的助手(谷歌，AutoVoice，Tasker 等)
*   修正了 Android 10 上与剪贴板相关的功能
*   使 Tasker 总是显示为一个助手选择，然后，当作为一个助手使用时，给用户指示如何使用
*   现在，创建新配置文件时，默认情况下禁用恢复设置
*   当系统 UI 黑暗模式启用时，自动主题改为黑色(而不是黑暗)
*   修正了 Android 10 上的输入法选择动作
*   修正了从 Taskernet 导入需要新版本 Tasker 的东西时出现的难以辨认的错误信息
*   修正了在必要的时候要求在其他应用程序上绘图的问题
*   固定允许手机进入睡眠时，黑暗模式启用，而机器人自动运行
*   如果用户手动输入值，允许场景以任何垂直偏移显示
*   修正了使用地图元素破坏场景时的崩溃问题
*   修正了一个错误，如果你导入一个配置文件，有时会启用另一个禁用的配置文件
*   启用媒体控制操作中的使用通知(如果可用)选项时，请求通知访问权限
*   增加了 Pixel 用户可以挤压手机呼叫 Tasker 作为助手的提醒
*   在 Tasker >菜单>更多> Android 设置中添加了助手设置
*   使细胞附近的条件工作更可靠
*   使后台服务检测在更多的设备上工作
*   使 NFC 操作更加可靠
*   小的崩溃修复

* * *

**来源:Reddit ( [1](https://www.reddit.com/r/tasker/comments/del3yn/dev_tasker_59beta2_fixed_clipboard_on_android_10/) )，( [2](https://www.reddit.com/r/JoinApp/comments/deimyz/dev_join_22beta_fix_for_clipboard_monitoring_on/) )**