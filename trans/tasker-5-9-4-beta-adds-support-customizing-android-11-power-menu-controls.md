# Tasker 5.9.4 测试版增加了对定制 Android 11 电源菜单控件的支持

> 原文：<https://www.xda-developers.com/tasker-5-9-4-beta-adds-support-customizing-android-11-power-menu-controls/>

# Tasker 5.9.4 测试版增加了对定制 Android 11 电源菜单控件的支持

Tasker 的最新测试版支持在 Android 11 的电源菜单控件中添加自定义磁贴，让您可以将其映射到几乎任何东西！

如果你认为自己是安卓超级用户，你很可能已经听说过 [Tasker](https://www.xda-developers.com/tag/tasker/) 。而且你也听说过 [Android 11](https://www.xda-developers.com/tag/android-11/) 和它的[电源菜单设备控制](https://www.xda-developers.com/android-11-power-menu-device-controls-smart-home-dream/)。随着 Android 11 ，谷歌改变了长按电源按钮时出现的选项，现在呈现出新的用户界面和智能家居设备控制，以便快速访问。这是一个添加快捷方式的好地方，但谷歌将这些快捷方式仅限于家庭控制。这就是 Tasker 的用武之地，因为最新的测试版增加了对定制 Android 11 电源菜单控制的支持。

Tasker 开发者 *joaomgcd* 和[已经开始在电源菜单](https://www.xda-developers.com/tasker-test-hijacks-android-11-power-menu/)中集成快捷键。 [Tasker 5.9.4 beta](https://www.reddit.com/r/tasker/comments/iy7xib/dev_tasker_594beta_android_11_power_menu_tiles_oh/) 是这些努力的延续，现在已经到达用户手中，因为之前的测试没有向用户发布。这次更新的主要亮点是，你可以在电源菜单中添加 Tasker 磁贴作为可点击的按钮，这些磁贴可以触发你能想到的几乎任何 Tasker 任务。这些小块可以是用于在点击时调用任务的简单按钮，或者是具有开/关状态的开关，或者是具有进度状态的开关。开发人员展示了一个快速演示，其中创建了一个按钮来触发屏幕截图任务:

如果您需要更多的控制，您可以使用 Tasker 中的“Power Menu Action”操作来创建具有给定 id、类型、标题、副标题、图标和命令的按钮。这进一步让您创建可以在一天中变化的按钮。新的更新还带来了 Tasker 命令系统，新的命令事件和命令动作，让用户重复使用任务，避免重复任务。也支持第三方命令。

### Tasker v5.9.4 beta 变更日志

此测试版的完整变更日志如下:

*   增加了动作“电源菜单动作”，允许你为 Android 11+电源菜单创建图块
*   添加了“显示电源菜单”事件，当 Android 11+上显示电源菜单屏幕时会触发该事件
*   为 Android 11+上的每个可用任务添加了电源菜单
*   添加了操作“命令”，允许您使用自动 pps 命令系统触发“命令”事件
*   增加了事件“命令”,可以通过“命令”动作触发
*   增加了第三方应用程序发送触发“命令”事件的命令的能力，但它们必须明确要求用户许可才能这样做
*   更改了选择图标的对话框，以便为每个选项显示一个图标
*   当儿童应用程序通过应用程序操作使用联系人时，添加了电话呼叫权限
*   在“通过应用程序联系”操作中增加了信号和电报信息的文本选项
*   添加了从 Taskernet 导入配置文件或任务时添加到新项目的选项
*   修复了 Termux 命令，使其与即将发布的 Termux 版本兼容
*   修正了当屏幕旋转时对话框不会取消的问题
*   删除了将短信插入信息数据库的选项，因为这是不可能的了
*   修正了当读取一个太大而无法读取的文件时的崩溃问题
*   修正了复制/移动带有奇怪扩展名的文件到外部 SD 卡的问题
*   修复了没有最近网络视图的设备的 javascripts
*   修正了一些崩溃

你可以[在谷歌 Play 商店](https://joaoapps.com/beta-testing/)上注册测试版，或者从 [Reddit 帖子](https://www.reddit.com/r/tasker/comments/iy7xib/dev_tasker_594beta_android_11_power_menu_tiles_oh/)中的下载链接下载。