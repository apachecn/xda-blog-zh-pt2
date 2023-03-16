# Gboard v7.0 测试版增加了电子邮件地址自动补全、通用媒体搜索以及对中文和韩文的支持

> 原文：<https://www.xda-developers.com/gboard-beta-email-address-autocompletion-chinese-korean-languages/>

Gboard 的前身是 Google Keyboard，是 Google 为 Android 开发的第一方键盘应用。这是一个功能丰富的应用程序，它预装在许多 Android 智能手机上。Gboard 的上一个版本，v6.9，[带来了对手写输入、URL 字段建议、新语言等的支持](https://www.xda-developers.com/gboard-beta-url-field-suggestions-handwriting-support/)。Gboard v7.0 测试版今天开始在 Play Store 上向用户推出，官方变更日志声明它现在支持 Android Oreo ( [Go 版](https://www.xda-developers.com/lineageos-15-android-oreo-go-edition-android-one/))。它还提供了对日语功能的更多支持。

我们安装了应用程序，并做了 APK 拆除它。拆除让我们知道了在最新更新中上线的其他新功能，尽管它们没有在官方变更日志中提及。准确地说，电子邮件地址的自动补全现在已经上线；用户现在可以选择对媒体进行通用搜索；现在支持中文和朝鲜语。一个尚未上线的功能是对自动检测到的其他语言的建议和自动更正。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

* * *

## 电子邮件地址自动完成

Gboard 的自动更正和自动完成功能已经是数一数二的了，但现在，谷歌对它们的改进更甚。键盘现在将自动完成键入的电子邮件地址(因为这个功能已经上线)，尽管值得注意的是，即使我尝试了多次，也无法让这个功能自己工作。当它开始为所有人服务时，它将省去用户手动输入电子邮件地址的麻烦。下面是相同的字符串:

```
 <string name="feature_card_email_completion_description">Gboard now auto-completes email addresses so you no longer need to fully type them out.</string> 
```

## 支持中文和朝鲜语

自推出以来，Gboard 已经获得了对多种语言的支持，这使得它成为多语言用户的福音。不过，到目前为止，它还不支持中文和韩文。现在这种情况有所改变，因为用户可以下载测试版更新，并在 Gboard 上添加中文和韩文键盘。该应用程序现在还会提醒用户有新的语言可用。以下是相同的字符串:

```
 <string name="feature_card_chinese_korean_description">Chinese and Korean are now supported in Gboard.</string>
<string name="feature_card_chinese_korean_title">New languages!</string> 
```

这个特性是不言自明的，现在已经上线了。用户可以进行通用媒体搜索来搜索表情符号、gif 和贴纸。以下是相同的字符串:

```
 <string name="feature_card_universal_media_description">Now when you search for “hungry” on Gboard, you’ll not only get emojis - you’ll also be able to choose from stickers and gifs, too.</string>
<string name="gboard_showing_universal_media_content_desc">Showing %s Media</string>
<string name="gboard_showing_universal_media_no_context_content_desc">Showing Media</string>
<string name="universal_media_emoji_header_text">EMOJI</string>
<string name="universal_media_gifs_header_text">GIFS</string>
<string name="universal_media_plural_suffix">" gifs"</string>
<string name="universal_media_singular_suffix">" gif"</string>
<string name="universal_media_sticker_header_text">STICKERS</string>
<string name="universal_media_sticker_more_results">MORE</string>
<string name="universal_media_sticker_more_results_content_desc">Open more sticker results</string> 
```

## 描述错误报告

```
 <string name="bug_report_dialog_bug_description_comment_message">"Please describe the bug in detail (Used as bug's description)."</string>
<string name="bug_report_dialog_bug_description_title_message">"Please describe the bug in one sentence (Used as bug's title)."</string>
<string name="bug_report_dialog_report_to_buganizer_option_message">Do you want to report this on Buganizer? (Unselecting this option will still upload log to server.)</string>
<string name="bug_report_dialog_span_selection_message">Please unselect any text that you do not want to share with Google.</string>
<string name="dialog_title">Keyboard Decoder Bug Report</string>
<string name="label_quality_bug_report_access_point">Quality Bug Report</string> 
```

这些字符串添加到与错误报告相关的现有字符串中。用户能够详细描述 bug，这将被用作 bug 的描述，并且用一句话来描述，这将被用作 bug 的标题。他们也可以选择在 Buganizer (Google 的问题跟踪器)上报告这一情况，但即使他们取消选择该选项，生成的日志仍然会上传到服务器。

## 自动检测的其他语言中的建议和自动更正

```
 <string name="enable_new_language_dialog_message">"You'll start seeing suggestions and autocorrections for %1$s words."</string>
<string name="enable_new_language_dialog_title">Add %1$s to Gboard?</string> 
```

这个功能还没有上线。当它这样做时，Gboard 将自动检测其他语言，并提供将它们添加到它选择的语言中。然后，用户将开始看到所选语言的建议和自动更正。

* * *

**如果你发现任何新的东西，请在评论** **中告诉我们，并关注我们的 [APK 拆解标签](https://www.xda-developers.com/tag/apk-teardown/)以获得更多类似的文章！**