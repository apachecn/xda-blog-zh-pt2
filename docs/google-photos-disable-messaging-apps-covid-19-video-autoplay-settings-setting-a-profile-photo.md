# Google 相册可能会禁用消息应用、视频自动播放的备份

> 原文：<https://www.xda-developers.com/google-photos-disable-messaging-apps-covid-19-video-autoplay-settings-setting-a-profile-photo/>

Google 相册是管理图片和图片库最方便的应用之一。除了让你在一个地方收集来自不同设备的所有图片，Photos 还使用谷歌的机器学习洞察力来建议可以删除哪些图片，以释放本地和云存储空间。现在，谷歌可能正在开发两项新功能；一个是限制不想要的媒体挤占你的 Google Drive 存储空间，另一个是防止动态照片和视频自动播放。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

**暂时禁用媒体备份**

如果你在谷歌照片上启用了自动备份和同步，WhatsApp 等消息应用程序的媒体会占用你手机和云存储的大量存储空间。随着 Google Photos 版本的推出，该公司正在测试自动禁用链接到消息应用程序的文件夹中的媒体备份和同步的能力。在对该应用程序的上述版本的拆解中，我们发现了对该功能的以下引用:

```
 <string name="photos_backup_settings_disablefolderbackup_promo_message">"People are sharing more photos &amp; videos than ever, due to COVID-19\. In an effort to conserve internet resources, backup &amp; sync has been turned off for messaging apps. &lt;a href=help:>Learn more&lt;/a>You can change this any time in Settings."</string> 
```

根据该功能的描述，其目的是限制互联网的使用，因为由于新冠肺炎，许多人在家里分享的照片比平时更多。如果用户愿意，他们可以在“设置”中重新激活消息应用的自动备份和文件夹同步功能。

**控制视频自动播放**

除此之外，该应用程序的代码中还增加了一个选项，当你在应用程序中滚动主时间轴时，可以禁用动态照片和视频的自动播放。自动播放功能于去年 7 月被添加到应用程序中，但可能没有得到用户的好评。

以下字符串暗示用户将很快能够选择性地选择哪些项目要自动播放，哪些项目不要自动播放:

```
 <string name="photos_photoadapteritem_videoplayerbehavior_settings_impl_motion_photos_toggle_title">Motion photos</string>
<string name="photos_photoadapteritem_videoplayerbehavior_settings_impl_page_description">Choose what items will automatically play in your photo grid. Recommended for a more seamless experience in the app.</string>
<string name="photos_photoadapteritem_videoplayerbehavior_settings_impl_subtitle">Manage automatic playback in your photo grid</string>
<string name="photos_photoadapteritem_videoplayerbehavior_settings_impl_title">Photo grid playback</string>
<string name="photos_photoadapteritem_videoplayerbehavior_settings_impl_videos_toggle_title">Videos</string> 
```

**设置谷歌账户资料照片**

最后，你可能很快就可以在照片应用程序中设置你的谷歌个人资料图片了。知名逆向工程专家[简·满春·王](https://wongmjane.com/)发现并演示了这一功能，从她的推文中可以看到。