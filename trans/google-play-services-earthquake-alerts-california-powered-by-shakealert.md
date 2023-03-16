# 谷歌将展示由 ShakeAlert 驱动的加州地震警报

> 原文：<https://www.xda-developers.com/google-play-services-earthquake-alerts-california-powered-by-shakealert/>

随着六月初[第三次 Pixel 功能下降](https://www.xda-developers.com/google-pixel-drop-june-2020-adaptive-battery-safety-check/)，谷歌在 Pixel 设备上为 Android 10 添加了一堆新功能。其中，谷歌对个人安全应用程序进行了一些改进，将[碰撞检测功能从 Pixel 4/4XL](https://www.xda-developers.com/google-pixel-car-crash-detection/) 扩展到 Pixel 3 系列，并添加了两个新功能——“安全检查”，如果你没有回应预定的检查，就让紧急联系人了解你的最新行踪，以及“危机警报”，通知你所在地区的自然灾害。

虽然危机警报不是针对任何特定类型的自然灾害，但谷歌正准备增加一个专门针对地震的警报机制。我们在 Google Play 服务 20.26.12 测试版中发现了该公司专门为加州地震警报添加的参考资料。这些警报由 ShakeAlert 提供支持，这是一项专门为 T2 西海岸提供地震预警的服务。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

在 APK 对 Google Play 服务 20.26.12 测试版的拆解中，我们发现以下字符串暗示了其功能和应用:

```
 <string name="about">About</string>
<string name="about_details">Earthquake alerts and info are provided by Google &amp; ShakeAlert®.</string>
<string name="about_details_link">Learn more or change settings</string>
<string name="demo_take_action_title">Earthquake Demo</string>
<string name="distance_to_epicenter_km">%.1f km away</string>
<string name="distance_to_epicenter_mile">%.1f miles away</string>
<string name="google_setting_eew_nearby_notification">Earthquake Nearby Notification</string>
<string name="google_setting_eew_occurred_notification">Earthquake Occurred Notification</string>
<string name="google_setting_take_action">Take action alert</string>
<string name="google_setting_take_action_delay">Take action alert after 3 minutes</string>
<string name="local_map_source">Source: ShakeAlert®</string>
<string name="quake_notification_high_importance_channel_name">Earthquake Early Warning Alert</string>
<string name="quake_notification_low_importance_channel_name">Earthquake Early Warning Updates</string>
<string name="ealert_activity_debug_google_setting_title">EEW System Debug</string>
<string name="ealert_latest_update_search_word">earthquake near me</string>
<string name="ealert_local_map_magnitude">Est. mag %.1f earthquake</string>
<string name="ealert_more_safety_tips">More safety tips</string>
<string name="ealert_nearby_notification_text" formatted="false">Expect shaking. Estimated magnitude %.1f about %s away.</string>
<string name="ealert_notification_nearby">Earthquake nearby</string>
<string name="ealert_notification_occurred">Earthquake occurred nearby</string>
<string name="ealert_notification_sender">Google - ShakeAlert®</string>
<string name="ealert_occurred_notification_text" formatted="false">Estimated magnitude %.1f about %s away. Tap to learn more.</string>
<string name="ealert_safety_demo">See a demo</string>
<string name="ealert_safety_info_label">Earthquake safety info</string>
<string name="ealert_safety_tip_content_1">Identify hazards and secure movable items</string>
<string name="ealert_safety_tip_content_10">If you live in a coastal area, relocate as soon as shaking stops to avoid tsunamis</string>
<string name="ealert_safety_tip_content_11">" "<li>"Don't touch downed or damaged utility lines"</li>"
"<li>"Don't use a damaged chimney. Approach downed or damaged chimneys with caution"</li>" "</string>
<string name="ealert_safety_tip_content_12">You may receive an alert if an aftershock is expected</string>
<string name="ealert_safety_tip_content_2">Create a disaster plan and decide how you will communicate in an emergency</string>
<string name="ealert_safety_tip_content_3">Put supplies in convenient locations</string>
<string name="ealert_safety_tip_content_4">Organize important documents, fix any structural issues on your property, and consider insurance</string>
<string name="ealert_safety_tip_content_5">During an earthquake, take cover under a table and hold on</string>
<string name="ealert_safety_tip_content_6">Evacuate if you smell gas or see building damage, help the injured, and stay away from anything that may fall</string>
<string name="ealert_safety_tip_content_7">Reach out to others, take pictures of any damage, and contact your insurance</string>
<string name="ealert_safety_tip_content_8">If water is shut off, use emergency supplies like a water heater or melted ice cubes</string>
<string name="ealert_safety_tip_content_9">" "<li>"Put out small fires. If you can't, evacuate."</li>"
"<li>Check electric, water lines, and appliances for damage. If you see a broken line, shut off the main valve.</li>"
"<li>Clean up spilled medicines, drugs, or other harmful materials</li>" "</string>
<string name="ealert_safety_tip_page_subtitle">Source: Earthquake Country Alliance</string>
<string name="ealert_safety_tip_page_title">Earthquake safety steps</string>
<string name="ealert_safety_tip_title_1">1\. Secure your space</string>
<string name="ealert_safety_tip_title_10">Move to higher ground</string>
<string name="ealert_safety_tip_title_11">Avoid fallen objects</string>
<string name="ealert_safety_tip_title_12">Expect aftershocks</string>
<string name="ealert_safety_tip_title_2">2\. Make a plan</string>
<string name="ealert_safety_tip_title_3">3\. Organize disaster supplies</string>
<string name="ealert_safety_tip_title_4">4\. Minimize financial hardship</string>
<string name="ealert_safety_tip_title_5">5\. Drop, cover, and hold on</string>
<string name="ealert_safety_tip_title_6">6\. Act quickly and cautiously</string>
<string name="ealert_safety_tip_title_7">7\. Reconnect and restore</string>
<string name="ealert_safety_tip_title_8">Get your emergency supplies</string>
<string name="ealert_safety_tip_title_9">Use caution when cleaning up</string>
<string name="ealert_safety_tips_title">Learn earthquake safety tips</string>
<string name="ealert_settings_detected_text">"You'll get an alert with the estimated magnitude and distance from your location"</string>
<string name="ealert_settings_detected_title">When an earthquake is detected nearby</string>
<string name="ealert_settings_how_it_works_body_2_text">"Keep in mind:
"<li>Not all earthquakes can be detected</li>"
"<li>Magnitude and shaking intensity estimates may have errors</li>"
"<li>You may receive an alert before, during, or after shaking begins</li>"
"</string>
<string name="ealert_settings_how_it_works_body_text">Android uses your approximate location to send information about nearby earthquakes. Earthquakes are detected by ShakeAlert®.</string>
<string name="ealert_settings_how_it_works_title">How it works</string>
<string name="ealert_stay_safer_content_1">Before going anywhere, even to the next room</string>
<string name="ealert_stay_safer_content_2">"If you smell gas, turn off the gas main to the building. If you can't, evacuate."</string>
<string name="ealert_stay_safer_content_3">Check for cracks and damage. Evacuate if it looks like the building may collapse.</string>
<string name="ealert_stay_safer_title">Stay safer after an earthquake</string>
<string name="ealert_stay_safer_title_1">Get shoes</string>
<string name="ealert_stay_safer_title_2">Check gas</string>
<string name="ealert_stay_safer_title_3">Avoid damaged buildings</string>
<string name="ealert_take_action_cover">Cover</string>
<string name="ealert_take_action_drop">Drop</string>
<string name="ealert_take_action_hold">Hold</string>
<string name="ealert_take_action_magnitude">Estimated magnitude %.1f</string>
<string name="ealert_take_action_next_steps">Tap for next steps</string>
<string name="ealert_take_action_source">Google alert powered by ShakeAlert®</string>
<string name="ealert_take_action_title">Earthquake</string>
<string name="eew_share_link">Share</string>
<string name="eew_update_link">See latest updates</string> 
```

地震预警功能应该分享细节，包括你离震中的距离，分享如何保持你的安全的提示，以及在你需要撤离的情况下要遵循的行动要点。