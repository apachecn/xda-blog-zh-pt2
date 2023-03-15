# Gmail 准备让你选择不个性化其他谷歌服务

> 原文：<https://www.xda-developers.com/gmail-opt-out-personalize-google-services/>

鉴于电子邮件在我们的日常生活中变得如此重要，注册一个你可以信任的电子邮件服务是很重要的。大多数人都在使用 Gmail 这样的免费电子邮件服务，正是由于 Gmail 庞大的用户群，谷歌才能够收集大量关于我们电子邮件习惯的聚合数据。谷歌利用这些数据向你展示更有针对性的广告，但他们也利用这些数据来改善自己的服务。智能回复和轻推等功能是 Gmail 变得更加智能的两种方式，但也有各种跨产品集成，如 [Google Pay 显示你的积分卡](https://www.xda-developers.com/google-pay-import-loyalty-cards-tickets-offers-gmail/)，谷歌助理提醒你的账单，以及[谷歌地图显示你的餐厅预订](https://www.xda-developers.com/google-maps-ar-navigation-timeline-sharing-features/)。

一旦你启用了这些功能，如果你想控制其他谷歌服务可以从你的电子邮件中收集到的信息，你必须进入多个应用程序的设置来关闭所有这些集成。幸运的是，Gmail 应用程序似乎正准备添加一个表格，以便更容易地退出跨产品信息共享。该表格还将告知用户 Gmail 的各种“智能”功能，谷歌可能很快会要求用户选择继续使用这些功能(如果他们已经在使用的话)。)

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

Gmail 应用程序的 2020.09.20 版本今天在谷歌 Play 商店推出，它包含的字符串表明，将有应用程序内的表格，供用户选择加入或选择退出基于你的 Gmail、聊天或会议内容的个性化其他谷歌产品。看起来选择退出的过程是全有或全无，因为你不能选择退出分享你的 Gmail、聊天和会议内容。一旦你选择退出，你就不能让谷歌助理提醒你即将到来的账单，你不能让谷歌地图显示你的餐厅预订，你不能让 Travel 捆绑你的行程，你也不能让 Google Pay 从你的电子邮件中提取你的会员卡和机票。

```
 <string name="cross_products_form_description_paragraph_1">Get the most out of products like Assistant, Maps, Travel, and GPay with personalization based on your Gmail, Chat, and Meet content and how you use these products.</string>
<string name="cross_products_form_description_paragraph_2">By agreeing, you grant other Google products access to your Gmail, Chat, and Meet information. Other Google products use this information under their own terms, such as the Google <annotation type="google_term_of_service_link">Terms of Service</annotation> and <annotation type="google_privacy_policy_link">Privacy Policy</annotation>. Depending on your settings, some Google products may show you ads personalized with your information, including information you share from Gmail, Chat, and Meet. <annotation type="smart_features_learn_more_link">Learn more</annotation></string>
<string name="cross_products_form_done">Done</string>
<string name="cross_products_form_footer">2 of 2</string>
<string name="cross_products_form_opt_in_bullet_1">Assistant reminders of your bills due</string>
<string name="cross_products_form_opt_in_bullet_2">Maps displaying restaurant reservations</string>
<string name="cross_products_form_opt_in_bullet_3">Travel bundling your itineraries</string>
<string name="cross_products_form_opt_in_bullet_4">GPay surfacing loyalty cards &amp; tickets</string>
<string name="cross_products_form_opt_in_description">Google can continue to help you via:</string>
<string name="cross_products_form_opt_out_description">This <annotation type="opt_out_description_highlight">disables the features above and more (effective by the end of this year).</annotation> You can turn this back on in Gmail settings.</string>
<string name="cross_products_form_opt_out_title">Use limited versions of other Google products</string>
<string name="cross_products_form_title">Personalize other Google products with your Gmail, Chat, and Meet data</string>
<string name="cross_products_opt_out_confirmation_bullet_travel">Travel showing places of interest</string>
<string name="cross_products_setting_opt_in_confirmation_bullet_title">Google can help you via:</string>
<string name="cross_products_setting_opt_in_confirmation_button_proceed">Personalize</string> 
```

此外，该表格的第一页将允许您选择退出 Gmail 中的其他“智能功能”，如轻推、智能回复、智能撰写、自动电子邮件过滤/分类、重要电子邮件的高优先级通知以及从电子邮件中提取日历事件。

```
 <string name="in_gmail_form_description_paragraph_1">Get the most out of Gmail, Chat, and Meet with smart features and personalization based on your content and how you use these products.</string>
<string name="in_gmail_form_footer">1 of 2</string>
<string name="in_gmail_form_next">Next</string>
<string name="in_gmail_form_opt_in_bullet_1">Automatic email filtering/categorization (Primary/Social/Promotions)</string>
<string name="in_gmail_form_opt_in_bullet_2">Smart Compose (suggested text) in email</string>
<string name="in_gmail_form_opt_in_bullet_5">Summary cards above emails (travel, package tracking, and more)</string>
<string name="in_gmail_form_opt_in_bullet_6">Extracting event details to create calendar entries</string>
<string name="in_gmail_form_opt_in_bullet_high_priority_notification">High priority notifications for important emails</string>
<string name="in_gmail_form_opt_in_description">Gmail will continue to offer you:</string>
<string name="in_gmail_form_opt_in_title">Continue with smart features</string>
<string name="in_gmail_form_opt_out_description">This will <annotation type="opt_out_description_highlight">disable or degrade the performance of the features above and more.</annotation> You can turn this back on in Gmail settings. <annotation type="smart_features_learn_more_link">Learn more</annotation></string>
<string name="in_gmail_form_opt_out_title">Turn off smart features</string>
<string name="in_gmail_form_title">Allow smart features in Gmail, Chat, and Meet to use your data</string>
<string name="in_gmail_opt_out_confirmation_bullet_nudge">Nudges to reply forgotten emails</string>
<string name="in_gmail_opt_out_confirmation_bullet_smart_reply">Smart Reply (suggested quick replies) in email</string>
<string name="in_gmail_setting_opt_in_confirmation_bullet_title">Gmail will offer you:</string>
<string name="in_gmail_setting_opt_in_confirmation_button_proceed">Allow</string> 
```

一些字符串表明，至少有一些“智能功能”将在今年年底关闭，除非你选择重新加入。

```
 <string name="smart_feature_opt_in_teaser_dismiss">Dismiss</string>
<string name="smart_feature_opt_in_teaser_main"><annotation type="opt_in_teaser_link">Turn on smart features and personalization</annotation> in Gmail, Chat, and Meet to <annotation type="purpose_placeholder">%1$s</annotation></string>
<string name="smart_feature_opt_in_teaser_purpose_filter_inbox_category">use inbox categories</string>
<string name="smart_feature_opt_in_teaser_purpose_high_priority_notification">use high priority notifications</string>
<string name="smart_feature_opt_in_teaser_purpose_important_first_inbox">use important first inbox</string>
<string name="smart_feature_opt_in_teaser_purpose_inbox_tip">receive inbox tips</string>
<string name="smart_feature_opt_in_teaser_purpose_notify_important_section">be notified about important emails only</string>
<string name="smart_feature_opt_in_teaser_purpose_nudges">use nudges</string>
<string name="smart_feature_opt_in_teaser_purpose_personalize_google_product">personalize other Google products</string>
<string name="smart_feature_opt_in_teaser_purpose_search_suggestion">get better search suggestions</string>
<string name="smart_feature_opt_in_teaser_purpose_smart_compose_mail">use Smart Compose in mail</string>
<string name="smart_feature_opt_in_teaser_purpose_smart_folder">categorize emails as %1$s</string>
<string name="smart_feature_opt_in_teaser_purpose_smart_inbox_types">use smart inbox types with this account</string>
<string name="smart_feature_opt_in_teaser_purpose_smart_reply_chat">use Smart Reply in chat</string>
<string name="smart_feature_opt_in_teaser_purpose_smart_reply_mail">use Smart Reply in mail</string>
<string name="smart_feature_opt_in_teaser_purpose_use_inbox_category">use inbox categories</string>
<string name="smart_feature_opt_out_back">Back</string>
<string name="smart_feature_opt_out_confirmation_description_both_in_gmail_and_cross_products">The following features and more will be turned off until you change your settings. Features in other Google products will be turned off by the end of this year:</string>
<string name="smart_feature_opt_out_confirmation_description_only_cross_products">The following features and more will be turned off (effective by the end of this year) until you change your settings:</string>
<string name="smart_feature_opt_out_confirmation_description_only_in_gmail">The following features and more will be turned off until you change your settings:</string>
<string name="smart_feature_opt_out_confirmation_title">Turn off these features?</string>
<string name="smart_feature_opt_out_proceed">Turn off features</string>
<string name="smart_feature_usage_form_bullet">•</string>
<string name="smart_features_setting_opt_in_confirmation_button_cancel">Cancel</string> 
```

2019 年年中，[谷歌披露了 Google Pay 的 3 个隐藏隐私设置](https://www.xda-developers.com/google-pay-hidden-privacy-settings-opt-out/)，用户可以选择退出。今年早些时候，谷歌宣布，该公司将不再为助理的所有用户默认存储[的录音。谷歌似乎想解决隐私倡导者的担忧，他们声称谷歌的服务收集和使用数据的方式对用户来说并不十分清楚。通过告知用户收集哪些数据来实现这些功能，并要求他们选择返回以继续使用这些功能，谷歌可以满足希望继续使用这些功能的普通用户和希望限制其数据共享服务的隐私意识。](https://www.xda-developers.com/google-assistant-disables-saving-audio-recordings-all-users/)

我无法在最新版本的 Android 版 Gmail 应用程序中显示这些设置。如果谷歌宣布这项功能，我们当然会提供该公告的报道。