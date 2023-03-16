# Google Home 2.19.1.18 在 Feed 中添加了 Nest Cam，Light 快捷方式等等

> 原文：<https://www.xda-developers.com/google-home-nest-cam-feed-light-shortcuts-nest-aware/>

谷歌 2.19.1.18 主页正在谷歌 Play 商店推出。我在一个小时前收到了我的 Pixel 4 的更新，尽管 Play Store 的 changelog 还没有为我更新。以下是苹果应用商店同一版本的变更日志:

> #### “改进了从灯光快速动作中快速打开和关闭灯光的支持。
> 
> #### “Feed”选项卡为您和其他家庭成员突出显示来自支持设备的重要活动。现在，您可以在主页中看到 Nest Cam 事件。"

我可以确认，这两个功能现在都出现在 Android 应用程序中。这是它们的样子。

**新的照明快捷方式**

“灯”快速操作用一个“灯”图标取代了顶部的“关”和“开”按钮，点击该图标会弹出一个页面，让您控制所有连接的灯。下面是截图:

**嵌套进给中的 Cam 事件**

如果你收到 Nest Cam 或 Nest Hello 视频门铃的通知，你现在可以在 Google Home 应用程序的“Feed”选项卡中看到该事件。您可以查看活动的预览、关闭活动，或者轻按“查看更多”来观看最近录制的一些片段。您可以播放/暂停录像、快进/快退 10 秒、打开直播视频或检查触发事件的细节(动作/检测到的人/听到的声音)。)Feed 标签是作为 Google Home 版本 2.15 的[部分引入的。](https://www.xda-developers.com/google-home-215-new-ui-features/)

**Nest Cam 事件的完整历史**

如果你在 Google Home 应用程序中查看 Nest Cam 或 Nest Hello 视频门铃的实时摄像头反馈，你可以通过点击三点式菜单，然后点击“完整历史”来查看完整的事件历史在这里，您可以按时间顺序查看每天发生的事件。您可以通过检测到事件的摄像机或门铃或触发事件的原因来过滤事件。一些事件触发过滤器包括是否检测到包裹、是否检测到运动，或者是否听到特定的声音事件，例如烟雾警报、玻璃破碎或狗叫声。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

**嵌套感知集成**

在谷歌制造 2019 活动上，谷歌承诺，Nest 应用程序的功能最终将包含在谷歌 Home 应用程序中。谷歌还详细介绍了新的 Nest Aware 订阅服务。看起来我们越来越接近这两个应用程序的融合，因为我们设法在 Google Home 应用程序的设置页面中推出了一个新的“Nest Aware”设置。在我的 Nest Hello 视频门铃的设备设置页面中，我还发现了“[熟面孔检测](https://support.google.com/googlenest/answer/9268625?co=GENIE.Platform%3DiOS)”的文本

在 Google Home 应用程序中，还为新的 Nest Aware 订户提供了一个新的入职活动。onboarding 屏幕会告诉您新的 Nest Aware 订阅提供了什么。

**紧急呼叫**

作为新的 Nest Aware 订阅服务的一部分，Google Home 应用程序将允许您为您的家触发呼叫当地紧急服务。

### 谷歌主页 2.19.1.18 巢感知 e911 字符串

```
 <string name="e911_address_confirmation_no_unit_number">No unit #</string>
<string name="e911_address_confirmation_subtitle">"Emergency services will use this exact address when responding. To set up emergency calling, you'll need to be at this address."</string>
<string name="e911_address_confirmation_title">Confirm your address</string>
<string name="e911_intro_footer">This feature is only available with a paid subscription, and either sound detection turned on or at least one eligible camera. To set up emergency calling, Google will share your home address and phone number with Bandwidth Inc. Bandwidth helps us direct your call to the closest emergency call center. Read their privacy policy and terms to learn more. You can always opt-out by turning off emergency calling or removing your address in the Google Home app settings.</string>
<string name="e911_intro_subtitle">Call emergency services from the Google Home app and reach the call center closest to your home</string>
<string name="e911_intro_title">Set up emergency calling</string>
<string name="e911_location_allow_button">Allow</string>
<string name="e911_location_allow_in_settings_subtitle">"You'll need to be at this address to set up emergency calling. You can allow location in your settings."</string>
<string name="e911_location_emergency_off_subtitle">You can always set this up later in your Nest Aware settings</string>
<string name="e911_location_emergency_off_title">Emergency calling is off</string>
<string name="e911_location_mock_location_subtitle">"You'll need to be at this address to set up emergency calling. Check your settings to remove any mock location app."</string>
<string name="e911_location_pre_allow_subtitle">"You'll need to be at this address to set up emergency calling"</string>
<string name="e911_location_pre_allow_title">"Allow Google Home to use your phone's location"</string>
<string name="e911_location_set_up_later_button">Set up later</string>
<string name="e911_location_try_again_subtitle">"You'll need to be at this address to set up emergency calling. You can always set this up later in Nest Aware settings."</string>
<string name="e911_location_try_again_title">Your phone is outside the address area</string>
<string name="e911_proxy_connection_failed_body">Use the dialer app or another device to call emergency services</string>
<string name="e911_proxy_connection_failed_title">Connection failed</string>
<string name="e911_settings_address_title">Address</string>
<string name="e911_settings_button_action_sheet">Show Action Sheet</string>
<string name="e911_settings_button_e933">Call 933</string>
<string name="e911_settings_button_turn_off_e911">Turn off emergency calling</string>
<string name="e911_settings_dialog_body">"You'll no longer be able to make emergency calls from the Google Home app"</string>
<string name="e911_settings_dialog_title">Turn off emergency calling?</string>
<string name="e911_settings_status_badge_issue">Issue</string>
<string name="e911_settings_status_badge_verified">Verified</string>
<string name="e911_settings_status_badge_verifying">Verifying</string>
<string name="e911_settings_subtitle">Call emergency services from the Google Home app</string>
<string name="e911_settings_title">Emergency calling</string> 
```

最后，一个新的“安全提示”文件概述了一些提示，谷歌可能会在紧急情况下提供。例如，如果你为入侵者或烟雾报警器拨打紧急电话，你可能会得到这些提示中的[。](https://pastebin.com/raw/6V0y1neA)

谷歌 2.19.1.18 主页现在正在谷歌 Play 商店推出。此次更新给应用带来了许多面向用户的变化，所以我们将做更多的挖掘，看看是否还有其他有趣的面向用户或幕后的变化。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*