# Google Messages 为 RCS、Google Fi 集成、手动云恢复准备端到端加密

> 原文：<https://www.xda-developers.com/google-messages-end-to-end-encryption-rcs-google-fi-integration-manual-cloud-restores/>

今天早些时候，我们在 *AndroidPolice* 的朋友拿到了[谷歌消息 6.2.031](https://www.apkmirror.com/apk/google-inc/messenger-google-inc/messenger-google-inc-6-2-031-release/) 并上传到 APKMirror。我们的朋友 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) 通知我们，这个 APK 实际上是一个狗粮版本，这意味着它不应该向公众发布。有时，这些狗粮版本有许多正在开发的特性的有趣代码，Messages 6.2.031 肯定是其中之一。这个狗粮版本暗示谷歌正在为 RCS 消息准备端到端加密，Google Fi 帐户集成以同步呼叫，文本和语音邮件，以及备份的手动云恢复。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

**针对 RCS 的端到端加密**

RCS 被广泛认为是 SMS 的继承者。有了 RCS，用户可以高质量地交换媒体文件，查看阅读回执，查看打字指示器，开始群聊，并通过移动数据甚至 Wi-Fi 做更多事情。谷歌没有等待运营商自己采用 RCS 协议，而是开始在谷歌消息应用[中为英国和法国的每个人推出 RCS 支持](https://www.xda-developers.com/google-android-rcs-support-uk-france/)。后来，他们在 Messages 应用中为美国、[西班牙](https://www.xda-developers.com/google-messages-rcs-support-spain/)、[意大利、新加坡、葡萄牙、阿根廷、巴基斯坦、波兰和土耳其](https://www.xda-developers.com/rcs-google-messages-rolling-out-italy/)的人们推出了 RCS 支持。

WhatsApp 和 Telegram 等流行的消息应用支持但 RCS 不支持的一个功能是端到端加密，但看起来谷歌正准备在他们自己的终端上添加对这一功能的支持。Google Messages 6.2.031 中最大的新特性是“端到端加密富通信服务消息”根据字符串，你可以选择发送端到端加密的信息，或者，如果你的数据连接不好，通过回退到短信/彩信不加密。

```
 <string name="e2ee_conversation_tombstone">Chatting end-to-end encrypted with %s</string>
<string name="e2ee_fail_to_send_retry_description">Resend as chat</string>
<string name="encrypted_rcs_message">End-to-End Encrypted Rich Communication Service message</string>
<string name="encryption_default_fallback_body">"SMS/MMS texts aren't end-to-end encrypted.
To send with end-to-end encryption, wait for improved data connection or send messages now as SMS/MMS."</string>
<string name="encryption_fallback_dialog_accept_button">Send unencrypted</string>
<string name="encryption_fallback_dialog_decline_button">Wait</string>
<string name="encryption_fallback_title">Send unencrypted messages?</string>
<string name="encryption_sent_fallback_body">"SMS/MMS texts aren't end-to-end encrypted.
To send with end-to-end encryption, wait until %1$s has data connection or send messages now as SMS/MMS."</string><string name="not_yet_sent_e2ee_dialog_body">This message is still trying to be sent end-to-end encrypted to the recipient. You can also send the message as SMS/MMS instead.</string> 
```

您甚至可以通过端到端的加密消息发送您的位置:

```
 <string name="location_attachment_picker_send_encrypted_content_description">Send end-to-end encrypted message with selected location %1$s</string> 
```

最后，你似乎可以选择其他应用程序是否可以访问你的端到端加密信息。然而，第三方应用开发者目前还不能在他们的消息应用中实现 RCS 支持。

```
 <string name="etouffee_to_telephony_setting_title">Let other apps access end-to-end encrypted messages</string> 
```

**Google Fi 集成**

许多用户期待的另一个新功能是 Google Fi 集成。虽然 [Google Hangouts 即将退出](https://www.xda-developers.com/google-hangouts-shut-down-20120/)，但对于想要在多个设备上查看和回复来电、短信和语音邮件的用户，它仍然被推荐给[。然而，这种情况可能很快就会改变，因为谷歌信息正准备收拾残局。](https://support.google.com/fi/answer/6188337?hl=en)

一旦对所有用户开放，上述设置页面将允许 Google Fi 用户登录他们的帐户，同步他们在屏幕上的任何文本、电话或语音邮件。Google Messages 的网络应用已经推出近两年了，因此 Google Fi 用户可以在这里阅读和回复他们的短信。

当您登录 Google Messages 中的 Google Fi 帐户时，您可以选择将对话历史从“闲逛”转移到“消息”。不幸的是，如果您在消息中启用 RCS，您将无法将消息或语音呼叫同步到计算机。如果您在设置中禁用多设备同步，您也将无法访问 web 上的呼叫和语音邮件，但您仍可从 web 上发送文本。

### Google Fi 字符串

```
 <string name="fi_account_confirmation_cancel_button">Cancel</string>
<string name="fi_account_confirmation_change_primary_device_dialog_message">"You're already signed in from the primary phone for your Google Account. To replace your primary phone with this one, continue signing in."</string>
<string name="fi_account_confirmation_change_primary_device_dialog_negative">Cancel</string>
<string name="fi_account_confirmation_change_primary_device_dialog_positive">Sign in</string>
<string name="fi_account_confirmation_change_primary_device_dialog_title">"You're signing in on a different phone"</string>
<string name="fi_account_confirmation_hangouts_cancel_button">Cancel</string>
<string name="fi_account_confirmation_hangouts_description">"Before Hangouts SMS/MMS stops working, transfer your conversation histories to Messages
%1$s"</string>
<string name="fi_account_confirmation_hangouts_ok_button">Transfer conversations</string>
<string name="fi_account_confirmation_hangouts_phone_link">Enjoy texts, calls &amp; voicemail on the web even when your phone is off</string>
<string name="fi_account_confirmation_hangouts_security">Conversations stay synced &amp; secure on Google servers</string>
<string name="fi_account_confirmation_hangouts_title">Hangouts SMS/MMS is going away</string>
<string name="fi_account_confirmation_ok_button">Sync conversations</string>
<string name="fi_account_confirmation_phone_link">Text or call on the web while your phone is off</string>
<string name="fi_account_confirmation_security">Messages stores your information securely on Google servers</string>
<string name="fi_account_confirmation_sync">Your conversations stay synced across screens</string>
<string name="fi_account_confirmation_title">Sync your conversations to enjoy texts, calls &amp; voicemail on the web</string>
<string name="fi_account_invalid_fi_account">Wrong account. Sign in with your Google Fi account.</string>
<string name="fi_account_login_pref_key">fi_account_login</string>
<string name="fi_account_login_summary">Sync texts, calls &amp; voicemails across screens</string>
<string name="fi_account_login_title">Sign in to Google Fi</string>
<string name="fi_account_pref_key">fi_account</string>
<string name="fi_account_preference_button">Stop sync &amp; sign out</string>
<string name="fi_account_rcs_enabled_dialog_body">To get messaging &amp; voice calls on your computer, turn off chat features. %1$s</string>
<string name="fi_account_rcs_enabled_dialog_negative_button">Cancel</string>
<string name="fi_account_rcs_enabled_dialog_positive_button">Turn off</string>
<string name="fi_account_rcs_enabled_dialog_title">Using chat features?</string>
<string name="fi_account_verify_fail_message">Failed to validate Google Fi account</string>
<string name="fi_current_sync_pref_key">fi_current_sync</string>
<string name="fi_enable_download_over_wifi_pref_key">fi_enable_download_over_wifi</string>
<string name="fi_settings_delete_backup">Also delete synced conversations?</string>
<string name="fi_settings_delete_backup_dialog_negative">Keep</string>
<string name="fi_settings_delete_backup_dialog_neutral">Cancel</string>
<string name="fi_settings_delete_backup_dialog_positive">Delete</string>
<string name="fi_settings_delete_backup_message">If you delete synced conversations, they’ll be available only on your phone</string>
<string name="fi_settings_device_status_unpaired">Unpaired</string>
<string name="fi_settings_devices_status_key">devices</string>
<string name="fi_settings_devices_status_summary">Pair phone &amp; computer</string>
<string name="fi_settings_devices_status_title">Status: %1$s</string>
<string name="fi_settings_devices_status_title_default">Status: Loading</string>
<string name="fi_settings_disable_multidevice_dialog_message">You’ll be able to text from your phone and computer, but calls and voicemail won’t be available on the web</string>
<string name="fi_settings_disable_multidevice_dialog_negative">Cancel</string>
<string name="fi_settings_disable_multidevice_dialog_positive">Stop syncing</string>
<string name="fi_settings_disable_multidevice_dialog_title">Stop syncing messages, calls &amp; voicemail across screens?</string>
<string name="fi_settings_download_over_wifi_summary">Some video &amp; images will not be available across all devices when Wi-Fi is off</string>
<string name="fi_settings_download_over_wifi_title">Sync media only over Wi-Fi</string>
<string name="fi_settings_opt_out_failed">Can’t stop sync &amp; sign out right now. Try again later.</string>
<string name="fi_settings_opt_out_in_progress">Stopping sync and signing out.</string>
<string name="fi_settings_sync_preference_summary">Messages, calls &amp; voicemail stay current across screens</string>
<string name="fi_settings_sync_preference_title_synced">Sync complete</string>
<string name="fi_settings_sync_preference_title_syncing">Sync in progress</string>
<string name="fi_settings_title">Google Fi</string> 
```

**备份&恢复**

最后，添加了两个布局文件，暗示在新的设置页面中恢复云上备份的消息:restore_activity_layout.xml 和 restore _ fragment _ layout . XML。Google Play 服务中的备份服务，以及 Google One 中的[备份服务，可以在您首次登录新设备时备份和恢复您的消息。看起来 Google Messages 会让你选择手动恢复以前的对话备份。](https://www.xda-developers.com/google-one-backup-restore-photos-videos-mms/)

```
 <string name="backup_detected">Backup detected</string>
<string name="last_backup_datetime_label">Last backup</string>
<string name="restore">Restore</string>
<string name="restore_description">Restore your previous backup. Backups will discontinue from occuring on any of your other devices.</string>
<string name="skip_restore">Skip restore</string>
<string name="skip_restore_dialog_message">This option will delete your existing cloud backup, then backup chats from this device.</string>
<string name="skip_restore_dialog_negative">Cancel</string>
<string name="skip_restore_dialog_positive">Continue</string> 
```

你可以从下面的谷歌 Play 商店链接下载最新版本的谷歌信息应用。然而，请注意，狗粮构建版本 6.2.031 将无法通过 Google Play 获得，只能通过 APKMirror 下载[。](https://www.apkmirror.com/apk/google-inc/messenger-google-inc/messenger-google-inc-6-2-031-release/)

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*