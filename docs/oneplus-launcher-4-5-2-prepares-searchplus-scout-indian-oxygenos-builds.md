# 一加启动器 4.5.2 准备在印度 OxygenOS 版本中添加统一搜索的 SearchPlus

> 原文：<https://www.xda-developers.com/oneplus-launcher-4-5-2-prepares-searchplus-scout-indian-oxygenos-builds/>

本月早些时候，一加发布了一个新的[应用切换器 UI 和快速搜索手势](https://www.xda-developers.com/oneplus-launcher-4-4-app-switcher-quick-search/)到股票 [OxygenOS](https://www.xda-developers.com/tag/oxygenos/) launcher 应用——一加 launcher。此次更新(4.4 版)让应用切换器 UI 中的应用预览卡变得更小、更统一，将应用图标移到了卡片底部，并用长按手势取代了三点式菜单按钮。另一方面，快速搜索手势为用户提供了一种用一只手在设备上搜索应用的简单方法。现在，该公司正准备在印度 OxygenOS 版本的一加启动器上添加一个新的统一搜索功能，名为 SearchPlus。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

一加最近为一加 7T 系列推出了 [OxygenOS Open Beta 5。测试版包括一加启动器版本 4.5.2，包含以下变更日志:](https://www.xda-developers.com/oneplus-7t-pro-oxygenos-open-beta-5-one-handed-mode-dark-mode-shortcut-more/)

尽管变更日志提到新的 SearchPlus 功能已经被添加到启动器中，但我们询问的印度 OxygenOS 用户都无法在他们的设备上访问该功能。我们检查了 APK 以了解该功能的确切功能，并发现了以下字符串:

### 一加启动器 4.5.2 中的 SearchPlus 字符串

```
 <string name="opsp_apps">Apps</string>
<string name="opsp_calculator">Calculator</string>
<string name="opsp_cancel">Cancel</string>
<string name="opsp_choose_number">Choose number</string>
<string name="opsp_clear_history">Clear History</string>
<string name="opsp_contact_call_action">Call</string>
<string name="opsp_contact_message_action">Message</string>
<string name="opsp_contacts">Contacts</string>
<string name="opsp_continue">Continue</string>
<string name="opsp_disable_history">Disable History</string>
<string name="opsp_enable_history">Enable History</string>
<string name="opsp_files">Files</string>
<string name="opsp_go_to_settings">Settings</string>
<string name="opsp_got_it">Got it</string>
<string name="opsp_history_disabled">History disabled</string>
<string name="opsp_notes">Notes</string>
<string name="opsp_search_in">Search in</string>
<string name="opsp_search_settings">Search Settings</string>
<string name="opsp_settings">Settings</string>
<string name="opsp_settings_section_three_title">Other Preferences</string>
<string name="opsp_settings_section_two_title">Customisation</string>
<string name="opsp_setup_later">Setup Later</string>
<string name="opsp_setup_later_message">OnePlus Scout can be setup anytime using options provided in the search bar</string>
<string name="opsp_setup_search">Setup OnePlus Scout</string>
<string name="opsp_shortcuts">Shortcuts</string>
<string name="opsp_suggestion">Suggestion</string>
<string name="opsp_try">Try</string>
<string name="opsp_weather">Weather</string>
<string name="opsp_weather_temp_details">min %s | max %s</string>
<string name="opsp_web_result">Web Results</string>
<string name="opuni_s_about_copyright_txt">OnePlus All rights reserved. © 2013 - %d OnePlus inc.</string>
<string name="opuni_s_about_screen_title">About OnePlus Scout</string>
<string name="opuni_s_about_title_text1">@net.oneplus.launcher:string/search_plus_name</string>
<string name="opuni_s_about_version_text">Version V1.0.01</string>
<string name="opuni_s_aboutpref_title">About</string>
<string name="opuni_s_contacts">Contacts</string>
<string name="opuni_s_data_tip_action">Turn on Wi-Fi/Mobile data</string>
<string name="opuni_s_data_tip_desc">Connect to the internet</string>
<string name="opuni_s_data_tip_title">Get the latest updates</string>
<string name="opuni_s_drawerpref_info">Display all apps in Drawer</string>
<string name="opuni_s_drawerpref_title">Drawer</string>
<string name="opuni_s_feedbackpref_title">Give Feedback</string>
<string name="opuni_s_hint_search">Search</string>
<string name="opuni_s_location">Location</string>
<string name="opuni_s_location_tip_desc">Turn on location to get localised and updated results</string>
<string name="opuni_s_location_tip_title">Get accurate results</string>
<string name="opuni_s_messages">Messages</string>
<string name="opuni_s_more">More</string>
<string name="opuni_s_onboarding_desc_text1">Introducing SearchPlus</string>
<string name="opuni_s_onboarding_desc_text2">Easy to access from everywhere, anytime</string>
<string name="opuni_s_onboarding_title1">Search apps, files, music & more! </string>
<string name="opuni_s_onboarding_title2">Access from notification panel and app drawer</string>
<string name="opuni_s_perm_contact_desc">Find contacts to call or message</string>
<string name="opuni_s_perm_location_desc">Find relevant places</string>
<string name="opuni_s_perm_message_desc">Find notifications, alerts and promotions</string>
<string name="opuni_s_perm_storage_desc">Find images, documents, music, etc.</string>
<string name="opuni_s_permsnpref_title">Permissions</string>
<string name="opuni_s_permsns_btntxt1">Allow all</string>
<string name="opuni_s_permsns_btntxt2">Open system settings</string>
<string name="opuni_s_permsns_item_desc3">Speak to search for content</string>
<string name="opuni_s_permsns_item_desc4">Find contacts to call or message</string>
<string name="opuni_s_permsns_label1">Unlock OnePlus Scout</string>
<string name="opuni_s_permsns_label_desc2">To modify permission access</string>
<string name="opuni_s_permsns_tip_desc">Give permissions to search apps, files, contacts, music and much more at one place</string>
<string name="opuni_s_permsns_tip_title">Find relevant results</string>
<string name="opuni_s_plachldr_permsminfo">%d Left: Allow access for relevant results</string>
<string name="opuni_s_plachldr_permsminfo_allselected">Control results based on your preferences</string>
<string name="opuni_s_searchbar_pref_title">Display the search bar in notifications</string>
<string name="opuni_s_searchpref1_desc">Search for contacts, files, messages, etc.</string>
<string name="opuni_s_searchpref1_title">Across OnePlus apps</string>
<string name="opuni_s_searchpref2_desc">Search for music, movies, news, etc.</string>
<string name="opuni_s_searchpref2_title">Across other installed apps</string>
<string name="opuni_s_searchpref3_desc">Search for content on the web</string>
<string name="opuni_s_searchpref3_title">Across apps not yet installed</string>
<string name="opuni_s_searchtips_pref_title">Enable search tips</string>
<string name="opuni_s_storage">Storage</string>
<string name="opuni_s_title_permissions">Permissions</string>
<string name="opuni_s_title_settings">OnePlus Scout Settings</string>
<string name="opuni_s_txt_all">All</string>
<string name="opuni_s_txt_recent">Recent</string>
<string name="opunis_get_results_from">Results preferences</string>
<string name="opunis_s_dismiss">Dismiss</string>
<string name="opunis_s_turn_on">Turn on</string>
<string name="opunis_terms_of_use">Terms Of Use</string> 
```

正如你在前面提到的代码中看到的，SearchPlus 本质上是一个统一的搜索功能，允许用户从主屏幕上搜索他们设备上的任何内容。我们预计该功能的工作方式很像[芝麻应用](https://play.google.com/store/apps/details?id=ninja.sesame.app.edge&hl=en_IN)，这意味着它可以让用户从一个统一的搜索栏搜索已安装的应用、联系人、设置、快捷方式等。该代码表明，一加将让用户能够在设置搜索功能时定制自己的搜索偏好，并启用/禁用搜索历史、位置访问、网页结果等。

用户还可以搜索音乐、电影、新闻等。跨一加应用和其他已安装的应用。此外，SearchPlus 还将提供一些提示，帮助用户充分利用这一新功能。值得注意的是，该功能似乎也被命名为“一加侦察兵”，但我们无法在启动器设置中找到启用它的开关。截至目前，尚不清楚该功能将于何时在一加发射器上上线。当这个功能在测试频道上推出时，我们会更新这篇文章。

*感谢 XDA 资深会员 [Some_Random_Username](https://forum.xda-developers.com/member.php?u=8234677) 的提示！*