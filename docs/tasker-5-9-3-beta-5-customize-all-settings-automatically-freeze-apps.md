# tasker 5 . 9 . 3 . beta 5 帮助你自定义手机上的所有设置，并自动冻结应用

> 原文：<https://www.xda-developers.com/tasker-5-9-3-beta-5-customize-all-settings-automatically-freeze-apps/>

Tasker 是 Android 最受欢迎的自动化应用程序，理由很充分。该应用程序允许你创建基于特定条件自动触发的配置文件来执行任务，它提供了各种各样的插件，可以帮助你自动化几乎任何你可以想象的事情。最重要的是，该应用背后的开发者定期发布更新，支持更多新功能。例如，该应用程序最近的测试版引入了一个名为“通过应用程序联系”的[新功能，允许你自动拨打 WhatsApp 的电话。现在，该应用程序在测试频道又有了重大更新，带来了更多的东西。](https://www.xda-developers.com/tasker-5-9-3-beta-4-contact-via-app-wireguard-integration/)

**[XDA Tasker 提示&招数论坛](https://forum.xda-developers.com/u/tasker-tips-tricks)**

根据 *Reddit* 上[最近的一篇帖子](https://www.reddit.com/r/tasker/comments/gf6z0u/dev_tasker_593beta5_supercharged_custom_settings/)，Tasker v 5 . 9 . 3 beta 5 现在向用户推出，它包括了不少有趣的新功能。以下是最新 Tasker 测试版中一些最值得注意的变化:

### 查找所有自定义设置

Tasker v5.2 [增加了自定义设置支持](https://www.xda-developers.com/tasker-v5-2-immersive-mode-runtime-permissions/)，允许您修改手机中存储在设置中的值。全局，设置。安全，和设置。系统表，如果您授予 Tasker WRITE _ SECURE _ SETTINGS(通过 ADB/root)和 WRITE_SETTINGS(通过系统权限页面)权限。虽然这对于自动完成设备上的各种设置非常有用，但它需要用户自己找出设备上可用的设置，因为每个设备/OEM 软件都有不同的设置。

到目前为止，用户找到可用设置的最简单方法是在他们的 PC 上或手机的根 shell 中通过 ADB 运行以下 3 个命令:

*   设置列表安全
*   设置列表全局
*   设置列表系统

然而，今年早些时候，Tasker 5.9.2 测试版[增加了一个新的“ADB WiFi”选项](https://www.xda-developers.com/tasker-5-9-2-beta-run-adb-shell-commands-without-tethered-pc/)，允许您使用 ADB shell 类权限启动 Tasker。从而允许用户运行 ADB shell 命令，而无需首先将他们的电话连接到他们的 PC。为了利用这个任务，5 . 9 . 3 beta 5 将在内部运行上述 3 个命令来列出所有可用的设置值。

### 发送 WhatsApp 短信

如前所述，Tasker 5 . 9 . 3 . beta 4 增加了“通过 App 联系”选项，可以在 WhatsApp 和其他消息服务中自动呼叫。在最新的测试版中，Tasker 现在还允许你在 WhatsApp 中自动发送短信。若要开始，请在任务中选择“通过应用程序联系”操作，然后按照下面视频中的说明为您设备上的任何联系人设置自动文本。

### 新的 ADB WiFi 助手操作

除了前面提到的查找所有自定义设置的功能，Tasker 中的 ADB WiFi 功能现在还提供了对更多操作的支持。其中包括:

*   清除应用程序的数据
*   冻结/解冻应用程序
*   在没有用户交互的情况下截图
*   打开或关闭 SIM 卡
*   卸载应用程序

请观看下面的视频演示，了解如何设置这些操作:

虽然这些操作在 Tasker 的早期版本中已经是可能的，但该应用程序要求您知道正确的 ADB 命令(pm、screencap、svc 等)。)来执行它们。随着最新的更新，Tasker 现在为您处理。然而，值得注意的是，你需要在你的电脑上运行一个脚本来设置该功能，并且你需要在每次启动手机时重新运行这个脚本。

### 完整变更日志

*   增加了通过“通过应用程序联系”操作打开 Whatsapp 档案时发送文本的选项
*   “通过应用程序联系”动作现在将显示正常的 Android 系统联系人选择器来选择一个联系人，如果没有应用程序被选中的话
*   在“通过应用程序联系”操作中，当发送一些文本时，增加了退出消息窗口的选项
*   使“通过应用程序联系”操作中的“联系人”和“应用程序”字段可选。如果留空，将在任务运行时询问。
*   当您在“自定义设置”操作中使用帮助器并启用“ADB Wifi”时，您将从您的设备中获取实际值，而不是从开发人员那里获取预先设定的值，因此您更有可能找到特定设备的设置
*   在 ADB Wifi 助手中添加了“清除应用数据”、“冻结/解冻应用”、“截图”、“切换 SIM 卡”和“卸载应用”
*   更改了没有活动配置文件时的主任务通知，以显示现有配置文件的总数
*   当一个变量的值是一个空字符串时，在应用程序的任何情况下，Tasker 都会认为它是一个未设置的变量
*   从 Taskernet 导入任务或配置文件时，Tasker 会询问您要将导入的项目放在哪个项目中
*   修复了在 Javascript 操作中使用“eval(variable)”的问题，其中“variable”包含一些 Javascript 代码
*   默认情况下，使“列表对话框”0 中的第一个可见索引，以便默认情况下不显示所选项目的箭头
*   在多重选择模式下，单击“列表对话框”动作中的项目文本也会选中复选框
*   使退出 Tasker 时显示的对话框不可取消
*   当无法访问在线帮助文件时，仅当用户有可用的互联网连接时，才提供电子邮件支持
*   不允许新任务名称中包含“%”字符
*   修正了某些情况下移动文件的问题
*   修复了“文件关闭”事件
*   在“列表对话框”动作中增加了对 HTML 的支持
*   使“文件已修改”事件中的%evtprm(1)(文件路径)被 url 解码，以便可以立即使用
*   修正了某些情况下启动时的崩溃
*   修正了在某些特殊情况下使用“键盘”动作中的“写”功能
*   在“移动网络类型”操作中添加了对 5G 的支持
*   修正了一些小错误

除了这些新功能之外，最新的 Tasker beta 更新还包括其他几个变化，您可以在上面的 changelog 部分中看到。如果您有兴趣亲自尝试这些功能，您可以通过点击[此链接](https://joaoapps.com/beta-testing/)注册 Tasker 测试版，然后从下面的 Play Store 链接下载最新版本。或者，您也可以直接从下面的 Dropbox 链接下载 Tasker 5 . 9 . 3 beta 5。

**[下载 Tasker v 5 . 9 . 3β5](https://www.dropbox.com/s/7j58vurja7vm4hj/Tasker.28.apk?dl=0)**