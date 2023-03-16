# Tasker v5.2 带来了自定义设置支持、沉浸式模式、运行时权限等等！

> 原文：<https://www.xda-developers.com/tasker-v5-2-immersive-mode-runtime-permissions/>

当人们谈论 Android 上的设备自动化时，很难不提到 Tasker。Tasker 是 Android 上最知名的自动化应用之一，允许有决心的用户实现几乎任何他们下定决心的事情。Tasker 最近经历了一次所有权变更，落入[非常能干的 joo Dias](https://www.xda-developers.com/tasker-autoapps-interview-joao-dias/)手中。从那以后， [Tasker 有了几个测试版](https://www.xda-developers.com/tasker-beta-secure-settings-permission-lock-screen-screenshot-action-android-p/)，但是开发者最终推出了他的[第一个公开 Tasker 版本](https://joaoapps.com/my-first-public-tasker-release/)。

下面重点介绍了一些显著的变化:

### 自定义设置

通过自定义设置，Tasker 现在可以通过一个简单的操作来控制和切换一系列设置。设备上的设置列表各不相同。我们已经发布了多个调整隐藏设置值的教程。系统，设置。全局和设置。安全表格)。只要您授予 Tasker WRITE _ SECURE _ SETTINGS 权限，并且您知道您要切换的设置，您就可以在您的设备上自动执行几乎任何设置！如上面的视频所示，在 Tasker 中找到要切换的设置非常容易。从那以后，您可以使用您可以想象的触发器和场景的任意组合来更改该设置。查看[完整教程](http://forum.joaoapps.com/index.php?resources/change-any-android-setting-from-anywhere-with-autoapps.331/)，了解如何利用这一新功能从任何地方更改任何支持的设置。

### 运行时权限

考虑到 Tasker 可能对您的系统做出的更改程度，它需要一大堆权限才能运行。Tasker 的这个新版本切换到运行时权限，使得只授予那些与您的特定用例相关的权限成为可能。Tasker，[像所有其他应用程序](https://www.xda-developers.com/play-store-updated-requirements-api-level-64-bit/)一样，需要在 8 月前达到 API 等级 26，因此这是达到要求的一步。

### 定位模式和沉浸式模式

您现在可以设置您希望在哪个位置模式之间切换(设置。Secure.location_mode、HIGH_ACCURACY、BATTERY_SAVING、SENSORS_ONLY 或 OFF 中的一个)。您还可以在这个新版本中[切换沉浸式模式](https://www.xda-developers.com/how-to-enable-system-wide-immersive-mode-without-root/)(设置。Global.policy_control，immersive.navigation、immersive.status 或 immersive.all 中的一个，可以选择设置应用此功能的应用程序列表。)

### Magisk 根检测

此版本中还修复了 Magisk 的根检测功能。

* * *

发布的[完整变更日志](https://tasker.joaoapps.com/changes/changes5.2.html)如下:

### 变更日志

增加

*   自定义设置操作:通过简单的用户界面更改/读取任何全局、安全或系统设置
*   定位模式动作:在你的手机上设置定位跟踪的类型(打开和关闭 GPS 等)
*   沉浸式模式动作:隐藏状态栏、导航栏或两者都隐藏。
*   清单权限 WRITE_SECURE_SETTINGS:通过 adb 命令启用-**ADB shell pm grant net . dinglisch . Android . taskerm Android . permission . WRITE _ SECURE _ SETTINGS**
*   认证对话动作:要求认证(pin、密码、模式、指纹或生物特征)。
*   动作输入/锁屏(安卓 P+)
*   动作输入/系统截图(Android P+)
*   动作声音模式(用于类似 Samsung 的设备，它有一个独立的免打扰声音开关)
*   新的或有重大变化的操作现在突出显示，直到您选择它们或 Tasker 的新版本出现
*   图标颜色现在在各种通知操作中受到重视
*   现在可以切换电源模式
*   保持行动现在支持无线充电
*   Toast 提醒尝试“新单元 API ”,如果扫描对附近的单元不起作用

变化

*   移到了运行时权限(Android 6+)。现在，当保存 Tasker 数据时，将询问所需的权限(主应用程序勾选或退出 Tasker)。
*   如果可能的话，通过服务调用插件。会让兼容插件更快更可靠。
*   尝试添加需要 root 用户的操作时询问 root 用户，如果不允许，则取消。
*   使**火炬**行动可用于所有运行 Android 棉花糖或更高版本的设备。
*   使所有运行 Android Oreo 或更高版本的设备都可以使用**接听电话**操作。
*   使**电源模式**动作在安全设置许可下工作。
*   改变了 root 的 **Kill App** 的工作方式，使其更加可靠
*   在没有所需权限的操作运行时通知用户
*   使用户通知不显示在组中，这样它们就不会与持续任务通知捆绑在一起
*   移除了插件为不存在的密钥添加替换密钥时不必要的日志
*   将帮助页面更改为 tasker.joaoapps.com
*   改变警告祝酒辞为黑色文本
*   joo Dias 现在第一次构建应用程序，所以我想检查我的构建脚本是否一切正常:)

错误修复

*   使用 Magisk 进行固定根检测
*   固定 Wifi 系绳动作
*   固定百分比系链变量
*   现在，只要您开始编辑需要特殊权限的状态、事件或动作，就会要求权限
*   固定任务通知文本不变时，通过任务动作设置前景选项
*   修复了与丢失权限相关的崩溃
*   固定任务崩溃，如果改变音量与请勿打扰启用，没有通知访问
*   修复崩溃:菜单>更多>开发者选项>保存数据定义
*   修复了作为新副本的启动应用程序
*   修复了带有 root 的 kill app
*   修复 Google Play 许可问题

你试用过 Tasker 的新版本吗？请在下面的评论中告诉我们您的使用案例！