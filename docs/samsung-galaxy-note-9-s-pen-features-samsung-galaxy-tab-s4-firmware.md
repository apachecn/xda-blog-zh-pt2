# 三星 Galaxy Note 9 S 笔功能通过 Galaxy Tab S4 固件得到确认

> 原文：<https://www.xda-developers.com/samsung-galaxy-note-9-s-pen-features-samsung-galaxy-tab-s4-firmware/>

三星 Galaxy Note 9 将在不到 3 周的时间内发布，这意味着是时候开始加剧泄露了。三星 Galaxy Note 系列智能手机上的 S Pen 是 Note，嗯，Note 的来源。今年 Galaxy Note 系列的升级将包括一款[更新的蓝牙 S Pen](https://www.xda-developers.com/samsung-galaxy-note-9-s-pen-bluetooth-controller/) ，它具有一些新的智能功能。新款 S Pen 的智能功能一直在传言中，但现在我们能够确认其中的许多功能，这要归功于运行 Android 8.1 Oreo(唯一一款运行 Android 8.1 的三星设备)的三星 Galaxy Tab S4 泄露的固件。由于三星 Galaxy Note 9 也将运行 Android 8.1 Oreo，因此可以检查三星 Galaxy Tab S4 固件的文件，以寻找任何支持蓝牙的 S Pen 的参考资料——有很多参考资料。

我从泄露的三星 Galaxy Tab S4 固件中拆卸了 AirCommand 应用程序(版本 3.0)，发现了许多基于无线“遥控”笔的字符串和图像。这些字符串证实了 S Pen 确实会有电池，但我们无法在固件中找到电池的大小。

### 三星 Galaxy Note 9 蓝牙 S 笔功能在三星 Galaxy Tab S4 的固件中透露

```

<string name="remotespen_aircommand_guide_collapse">Collapse</string>
<string name="remotespen_aircommand_guide_expand">Expand</string>
<string name="remotespen_app_actions">App actions</string>
<string name="remotespen_app_actions_desc">Choose what happens when you press the Pen button in various apps.</string>
<string name="remotespen_battery">Battery</string>
<string name="remotespen_camera_controller">S Pen camera controls</string>
<string name="remotespen_connected">Connected.</string>
<string name="remotespen_connecting">Connecting…</string>
<string name="remotespen_disconnected">Disconnected</string>
<string name="remotespen_disconnected_description">Insert your S Pen into your phone to connect it.</string>
<string name="remotespen_disconnected_menu_get_help_from_samsung_members">Get help from Samsung Members</string>
<string name="remotespen_do_nothing">Do nothing</string>
<string name="remotespen_guide_primary_title">Single press</string>
<string name="remotespen_guide_secondary_title">Double press</string>
<string name="remotespen_guide_you_can_add_primary">"You haven't added a single press action yet. You can add one in the Air command settings."</string>
<string name="remotespen_guide_you_can_add_secondary">"You haven't added a double press action yet. You can add one in the Air command settings."</string>
<string name="remotespen_header_media">Media</string>
<string name="remotespen_header_shutter">Shutter</string>
<string name="remotespen_hold_spen_key_to">Hold down Pen button to</string>
<string name="remotespen_hold_spen_key_to_off_description">Hold down the Pen button to open an app or access an S Pen feature.</string>
<string name="remotespen_hold_spen_key_to_open">Open %s</string>
<string name="remotespen_hold_spen_key_to_subtext">Tap here to choose what happens when you hold down the Pen button.</string>
<string name="remotespen_hold_spen_key_to_suggested_apps">Suggested apps</string>
<string name="remotespen_low_battery">Low battery</string>
<string name="remotespen_media_controller">S Pen music controls</string>
<string name="remotespen_next">Next page</string>
<string name="remotespen_none">None</string>
<string name="remotespen_noti_channel_disconnect">S Pen disconnected</string>
<string name="remotespen_noti_channel_low_battery">S Pen battery low</string>
<string name="remotespen_noti_channel_miscellaneous">Miscellaneous</string>
<string name="remotespen_noti_desc_connection_failed">Tap here to connect to it again.</string>
<string name="remotespen_noti_desc_disconnected">Insert your S Pen to use it as a remote.</string>
<string name="remotespen_noti_desc_low_battery">Insert your S Pen into your phone to recharge it.</string>
<string name="remotespen_noti_new_update_available">New update available</string>
<string name="remotespen_noti_tap_here_to_update_your_spen">Tap here to update your S Pen.</string>
<string name="remotespen_noti_title_connection_failed">Reconnect S Pen</string>
<string name="remotespen_noti_title_disconnected">Connect your S Pen</string>
<string name="remotespen_noti_title_low_battery">S Pen battery low</string>
<string name="remotespen_off">Off</string>
<string name="remotespen_on">On</string>
<string name="remotespen_play_next_track">Play next track</string>
<string name="remotespen_play_pause">Play/Pause</string>
<string name="remotespen_play_pause_track">Play/pause track</string>
<string name="remotespen_previous">Previous page</string>
<string name="remotespen_reset">Reset S Pen</string>
<string name="remotespen_retry">Retry</string>
<string name="remotespen_s_pen_actions_for_ps">S Pen actions for %s</string>
<string name="remotespen_s_pen_remote">S Pen remote</string>
<string name="remotespen_sbody_available">Available</string>
<string name="remotespen_settings_firmware_upgrade_already_installed">The latest version is already installed.</string>
<string name="remotespen_settings_firmware_upgrade_error_popup_title">"Couldn't update S Pen"</string>
<string name="remotespen_settings_firmware_upgrade_error_try_again_later">Try again later.</string>
<string name="remotespen_settings_firmware_upgrade_status_text">Installing update…</string>
<string name="remotespen_settings_firmware_upgrade_success">Installed</string>
<string name="remotespen_settings_firmware_upgrade_warning_text">"Don't remove your S Pen from your phone."</string>
<string name="remotespen_settings_main_help_description">Remotely control apps with your S Pen.</string>
<string name="remotespen_settings_pairing_guide_connecting_spen_desc">This may take a while.</string>
<string name="remotespen_settings_pairing_guide_connecting_spen_main">Connecting to your %s…</string>
<string name="remotespen_settings_pairing_guide_disconnected_close">"Can't connect to your %s."</string>
<string name="remotespen_settings_pairing_guide_disconnected_retry">"Couldn't connect to your %s."</string>
<string name="remotespen_settings_pairing_guide_insert_spen">Insert your S Pen into your phone.</string>
<string name="remotespen_settings_pairing_guide_spen">S Pen</string>
<string name="remotespen_shutter">Take picture</string>
<string name="remotespen_skip">Skip</string>
<string name="remotespen_tile_label">S Pen remote</string>
<string name="remotespen_unlock_dont_use">"Don't use"</string>
<string name="remotespen_unlock_spen_unlock_guide_content">"If your phone locks while you're using your S Pen, just press the Pen button to unlock it.

This feature only works when your S Pen is connected to your phone."</string>
<string name="remotespen_unlock_spen_unlock_title">Unlock with S Pen remote</string>
<string name="remotespen_unlock_use_spen_unlock">Unlock with S Pen remote</string>
<string name="remotespen_welcome_more">More</string>
<string name="remotespen_welcome_start">Start</string>
<string name="remotespen_welcome_text_main">S Pen remote</string>
Press the Pen button to take pictures, control music, and more in a wide range of apps.
<string name="remotespen_welcome_text_sub2">You can also press and hold the Pen button to open any app or S Pen feature you choose.</string>

```

有许多字符串告诉我们遥控器笔的功能。以下是您可以做的事情的摘要:

*   用 S 笔控制音乐。这将允许你像使用耳塞一样通过按下播放/暂停按钮来控制音乐。S Pen 按钮可以让你播放和暂停音乐，也可以让你跳过音乐曲目。
*   将 S Pen 用作遥控相机快门。这在你想给自己拍照和支撑手机的时候会很有用。
*   如果从手机上取下 S Pen，然后手机锁定，您将能够远程解锁手机。
*   你可以按下 S Pen 按钮在一系列应用程序中执行更多操作。不过，由于三星 Galaxy Note 9 尚未推出，我们不知道 S Pen 还会与哪些应用程序集成。
*   按住笔按钮可打开任何应用程序或笔功能。
*   设置单按和双按笔动作。

由于三星 Galaxy Tab S4 固件包含了三星 Galaxy Note 9 将要推出的 S Pen AirCommand 应用程序，三星 Galaxy Tab S4 [也有可能推出相同的](https://www.xda-developers.com/samsung-galaxy-tab-s4-white-model-keyboard-accessory-leak/)蓝牙 S Pen。请记住，三星 Galaxy Tab S3 没有像 Galaxy Note 系列手机那样配备 S Pen 插槽，因此您无法将其插入设备进行连接。三星可以找到一种给笔充电的方法，这种方法有望比 Apple Pencil 的充电方法更好。

三星 Galaxy Note 9 即将发布，因此我们将能够确认这些细节，并获得更多关于手机的细节。从目前我们看到的情况来看，三星 Galaxy Note 9 将是一款出色的设备。它将拥有一个[4000 毫安时电池](https://www.xda-developers.com/samsung-galaxy-note-9-4000-mah-battery/)、[三星 Bixby 2.0](https://www.xda-developers.com/samsung-galaxy-note-9-bixby-2-0-2/) 、[升级版摄像头](https://www.xda-developers.com/samsung-isocell-plus-technology/)、[更快的无线充电](https://www.xda-developers.com/samsung-galaxy-note-9-4000-mah-battery/)，以及一个高通骁龙 845 或 Exynos 9810 片上系统。所有这些结合在一起，成就了一部伟大的旗舰手机。如果我们从三星 Galaxy Tab S4 的固件中了解到更多关于该设备的细节，我们一定会让你们都知道。