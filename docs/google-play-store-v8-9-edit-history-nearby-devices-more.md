# 谷歌 Play 商店 8.9 版在评论中暗示了公开可见的编辑历史，与附近的设备交换应用更新，等等

> 原文：<https://www.xda-developers.com/google-play-store-v8-9-edit-history-nearby-devices-more/>

谷歌 Play 商店 v8.9 正在向 Android 设备推出，表面上看，没有任何重大变化。然而，我们在 APK 对该应用进行了拆解，发现了不少与尚未上线的新功能相关的字符串，包括新的应用审查历史，设备的点对点应用更新共享机制，“拆分安装”模块化 apk 等等。所以，事不宜迟，让我们开始吧。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

* * *

## 公开查看评论的编辑历史

```
 <string name="edit_history_label">Edit History</string>
<string name="edited_review_tag">"· Edited"</string
<string name="public_reviews_edit_history_message">Edit history is public to anyone who can see this review.</string>
<string name="review_edit_history_choice">View edit history</string>
<string name="review_edit_history_timestamp">%1$s at %2$s</string> 
```

发布到谷歌 Play 商店的应用评论一直是公开的。然而，编辑历史*并不公开——目前，只有撰写评论的用户和应用程序的开发者才能查看。几个月前，Play Store 开始区分编辑过的评论和未编辑过的评论，包括一个“编辑过”的标志，新的字符串显示评论编辑历史将很快被所有人公开查看。*

为什么这很重要？在 Play Store 上写评论的用户通常会在应用程序开发者做出回应后编辑评论。其他用户目前无法查看用户评论的过去版本，但一旦他们能够查看，他们将能够看到用户最初写的内容。用户对应用程序的看法经常会随着时间而改变，公开的编辑历史在这方面可能会有所帮助。

另一方面，它们也可能带来隐私风险。用户可以编辑应用评论以删除任何个人身份信息，但如果编辑历史是公开可见的，这将意味着这些信息在一定程度上仍然可见。

## 与附近的设备交换应用更新

未来，Play Store 用户将能够与附近的设备共享应用更新。这是点对点文件共享的一种形式，在数据连接不理想的地区可能很有用。用户只需在设备之间交换应用程序更新，就能更快地下载它们。

不幸的是，字符串没有解释这个特性在技术层面上是如何工作的。

```
 <string name="mitosis_runtime_notification_message">Exchanging app updates with nearby devices.</string>
<string name="mitosis_runtime_notification_title">Checking for app updates</string> 
```

## 模块化应用

```
 <string name="split_install_confirmation_body_text">%1$s is requesting to download an additional module. This might incur extra data usage charges.</string>
<string name="split_install_confirmation_details_text">Download size: %1$s</string>
<string name="split_install_confirmation_negative_button_text">Cancel</string>
<string name="split_install_confirmation_positive_button_text">Download</string>
<string name="split_install_confirmation_title_text">Download new module for %1$s</string>
<string name="split_install_confirmation_title_text">Download new module for %1$s</string>
<string name="split_install_splash_screen_progress_message_text">Updating %1$s...</string> 
```

这些字符串表明，模块化应用程序可能很快就会出现在 Play Store 中。模块化应用与 [Android 即时应用](https://www.xda-developers.com/google-play-store-android-instant-apps/)相关，支持由应用的部分版本组成的“拆分安装”。一些模块化应用程序可能会提示用户下载额外的模块，此时用户可以选择是否下载它们。

模块化应用程序还没有上线，也没有任何官方发布时间表的暗示。

## 关于恶意软件的更多信息

```
 <string name="package_malware_learn_more">Learn more</string> 
```

谷歌的 Play Protect 会扫描应用程序中的恶意软件，如果发现任何恶意软件，就会向用户发出警告。目前，用户可以通过点击“无论如何安装”来选择忽略该消息，一个新的字符串显示谷歌将开始显示“了解更多”选项。它大概会链接到更多关于检测到的恶意软件的信息。

* * *

**如果你发现任何新的东西，请在评论** **中告诉我们，并关注我们的 [APK 拆解标签](https://www.xda-developers.com/tag/apk-teardown/)以获得更多类似的文章！**