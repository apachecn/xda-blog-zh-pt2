# Android Auto 5.7 准备让你添加一个谷歌助手命令的快捷方式

> 原文：<https://www.xda-developers.com/android-auto-5-7-prepares-add-shortcut-google-assistant-command/>

谷歌最近更新了 Android Auto 的设置 UI，增加了一些新元素，旨在简化连接过程。[更新增加了](https://www.xda-developers.com/android-auto-settings-redesign-rolling-out/)一个新的“连接汽车”按钮，帮助用户使用 USB 电缆连接的说明，以及一个无线连接按钮。现在，谷歌推出了另一个 Android Auto 更新，增加了一个有趣的内容。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

Android Auto v5.7.603944 不包括任何值得注意的面向用户的变化。此次更新只带来了一些对请勿打扰功能的改进，对黑暗模式的优化，以及一些错误修复。但最新 APK 的拆解发现了一系列代码，指向即将推出的一项功能，该功能将使该应用程序上的谷歌助手更加有用。

```
 + <string name="settings_customize_add_assistant_shortcut_activity_title">Assistant Action</string>
+ <string name="settings_customize_add_assistant_shortcut_add_button">Add</string>
+ <string name="settings_customize_add_assistant_shortcut_error_label_empty">Please enter a valid label</string>
+ <string name="settings_customize_add_assistant_shortcut_error_query_empty">Please enter a valid query</string>
+ <string name="settings_customize_add_assistant_shortcut_label_hint">Label</string>
+ <string name="settings_customize_add_assistant_shortcut_launcher_icon_title">LAUNCHER ICON</string>
+ <string name="settings_customize_add_assistant_shortcut_query_hint">Assistant command</string>
+ <string name="settings_customize_add_launcher_shortcut_button">Add a shortcut to the launcher</string>
+ <string name="settings_customize_add_launcher_shortcut_deleted">Item removed</string>
+ <string name="settings_customize_add_shortcut_dialog_option_assistant">an assistant action</string>
+ <string name="settings_customize_add_shortcut_dialog_option_contact">a contact to call</string>
+ <string name="settings_customize_add_shortcut_dialog_title">Add a shortcut to</string> 
```

这些字符串表明，谷歌正在努力为 Android Auto 中的谷歌助手命令添加快捷方式。我们的主编[米沙·拉赫曼](https://www.xda-developers.com/author/mishaalrahman/)已经设法手动启用了这个功能，下面是它的样子:

这些截图显示了在 Android Auto 中为一个助手操作添加新快捷方式的设置过程。该功能将允许您在此过程中为快捷方式选择一个辅助命令和启动器图标标签。设置快捷方式后，您将能够在应用程序中执行自定义助手操作。

值得注意的是，尽管 Mishaal 能够启用该功能的入职流程，但他无法让该功能实际工作。这表明该功能目前处于早期开发阶段，谷歌可能会在即将到来的 Android 自动更新中充实它。到目前为止，我们还没有从谷歌获得关于该功能或其发布时间表的官方信息。

* * *

*感谢 PNF 软件为我们提供了使用* *[JEB 反编译](https://www.pnfsoftware.com/?aid=xdadev)* *的许可，这是一款针对 Android 应用的专业级逆向工程工具。*