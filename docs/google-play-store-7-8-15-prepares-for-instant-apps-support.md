# 谷歌 Play 商店 7.8.15 准备支持即时应用

> 原文：<https://www.xda-developers.com/google-play-store-7-8-15-prepares-for-instant-apps-support/>

谷歌即时应用(Google Instant Apps)是一项功能，允许用户“流式传输”现有 Android 应用的部分内容，这样他们就可以在不安装应用的情况下以其原生外观试用该应用。即时应用程序需要开发者进行一些小的修改，但是一旦[谷歌批准实施这些修改](https://developer.android.com/topic/instant-apps/index.html)这些应用程序将能够接触到更广泛的受众，因为用户可以有机地分享他们朋友和家人的链接。即时应用最初是在[谷歌 I/O 2016](https://www.xda-developers.com/google-io-2016-roundup-part-2/) 期间推出的，但直到今年 1 月，[的少数设备和少数应用](https://support.google.com/googleplay/answer/7240211?hl=en)才可以利用即时应用。

然而，随着谷歌 Play 商店 v7.8.15 的发布，即时应用程序可能会开始看到更广泛的发布。在这个版本的 APK 拆解中，我们发现了新的字符串和一个活动，将允许用户选择即时应用程序。

虽然 APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都有可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

* * *

## 7.8.15 APK 拆弹商店

像往常一样，我们可以通过查看 APK 文件中添加了哪些字符串来找到新特性的证据。在这种情况下，我们可以看到谷歌 Play 商店将增加支持选择您的谷歌帐户使用即时应用程序。

### 游戏商店 7.8.15 即时应用

```

<string name="instant_app_settings_menu_help">Help</string>
<string name="instant_apps_settings_change_account_dialog_cancel">cancel</string>
<string name="instant_apps_settings_change_account_dialog_description">All instant apps and associated app data, including app permissions, will be removed for the current account.</string>
<string name="instant_apps_settings_change_account_dialog_ok">change account</string>
<string name="instant_apps_settings_change_account_dialog_title">Change account?</string>
<string name="instant_apps_settings_description">You can use apps without installing them. Choose a Google Account to use for app sign-in and payments.</string>
<string name="instant_apps_settings_open_links_dialog_cancel">cancel</string>
<string name="instant_apps_settings_open_links_dialog_description">For this feature to work also turn on Open links in apps</string>
<string name="instant_apps_settings_open_links_dialog_ok">turn on now</string>
<string name="instant_apps_settings_open_links_dialog_title">Turn on required setting</string>
<string name="instant_apps_settings_opt_out_dialog_cancel">cancel</string>
<string name="instant_apps_settings_opt_out_dialog_description">All instant apps and associated app data, including app permissions, will be removed for the current account.</string>
<string name="instant_apps_settings_opt_out_dialog_ok">turn off</string>
<string name="instant_apps_settings_opt_out_dialog_title">Turn off Instant Apps?</string>
<string name="instant_apps_settings_title">Instant Apps account</string>
<string name="instant_apps_settings_turn_instant_apps_off">None</string>

<string name="debug_run_instant_apps_hygiene_summary">Immediately trigger Instant Apps Hygiene service</string>
<string name="debug_run_instant_apps_hygiene_title">Run Instant Apps Hygiene</string>

<string name="publisher_name_instant_app">Instant App</string> 
```

根据这些字符串中的内容来判断，即时应用程序将是一个选择退出的过程。其应用程序支持即时应用程序服务的发行商可能会在 Play Store 中显示一个特殊的指示符，表明他们的应用程序也支持该服务。

此外，APK 中有几个 XML 文件，用于定义即时应用程序设置屏幕如何显示给用户。这些文件被命名为 instant _ apps _ settings _ account _ row . XML、instant_apps_settings.xml 和 instant_apps_settings_menu.xml。

[tabs][tab title = " instant _ apps _ settings _ account _ row . XML "]

```
 <?xml version="1.0" encoding="utf-8"?>
<LinearLayout android:orientation="horizontal" android:background="?android:selectableItemBackground" android:paddingLeft="@dimen/instant_apps_settings_account_list_row_padding_left" android:paddingTop="@dimen/instant_apps_settings_account_list_row_padding_top" android:paddingRight="0.0dip" android:paddingBottom="@dimen/instant_apps_settings_account_list_row_padding_bottom" android:layout_width="fill_parent" android:layout_height="wrap_content" android:paddingStart="@dimen/instant_apps_settings_account_list_row_padding_left" android:paddingEnd="0.0dip"
xmlns:andro>
<TextView android:textAppearance="@android:style/TextAppearance.Material.Subhead" android: android:layout_width="0.0dip" android:layout_height="wrap_content" android:layout_weight="1.0" android:labelFor="@id/account_selected" />
<RadioButton android: android:layout_width="wrap_content" android:layout_height="wrap_content" style="@android:style/Widget.Material.CompoundButton.RadioButton" />
</LinearLayout> 
```

[/tab][tab title = " instant _ apps _ settings . XML "]

```
 <?xml version="1.0" encoding="utf-8"?>
<LinearLayout android:orientation="vertical" android: android:layout_width="fill_parent" android:layout_height="fill_parent" android:divider="?android:dividerHorizontal"
xmlns:andro xmlns:app="http://schemas.android.com/apk/res-auto">
<android.support.v7.widget.Toolbar android:theme="@style/ThemeOverlay.AppCompat.ActionBar" android: android:background="?colorPrimary" android:layout_width="fill_parent" android:layout_height="?actionBarSize" app:popupTheme="@style/ThemeOverlay.AppCompat.Light" />
<android.support.v7.widget.RecyclerView android: android:paddingTop="@dimen/instant_apps_settings_account_list_padding_top" android:paddingBottom="@dimen/instant_apps_settings_account_list_padding_bottom" android:layout_width="fill_parent" android:layout_height="wrap_content" android:paddingStart="?android:listPreferredItemPaddingStart" android:paddingEnd="?android:listPreferredItemPaddingEnd" app:layoutManager="android.support.v7.widget.LinearLayoutManager" />
<TextView android: android:paddingTop="@dimen/instant_apps_settings_description_padding_top" android:layout_width="wrap_content" android:layout_height="wrap_content" android:text="@string/instant_apps_settings_description" android:drawablePadding="@dimen/instant_apps_settings_description_drawable_padding" android:paddingStart="@dimen/instant_apps_settings_description_padding_start" android:paddingEnd="@dimen/instant_apps_settings_description_padding_end" />
</LinearLayout> 
```

[/tab][tab title = " instant _ apps _ settings _ menu . XML "]

```
 <?xml version="1.0" encoding="utf-8"?>
<menu
xmlns:andro xmlns:finsky="http://schemas.android.com/apk/res-auto">>
<item android:icon="@drawable/ic_help" android: android:title="@string/instant_app_settings_menu_help" finsky:showAsAction="ifRoom" />
</menu> 
```

[/tab]

[/tabs]

最后，由于即时应用活动本身是可访问的，如果您手动启动正确的意图，我们能够启动它，看看它会是什么样子。这是即时应用程序帐户选择屏幕的屏幕截图，您可以选择哪个帐户来存储应用程序数据并进行与即时应用程序相关的支付。

* * *

如果我在实时构建中或者通过 APK 的拆除发现了什么有趣的东西，我会继续挖掘并更新这篇文章。如果你正在寻找谷歌 Play 商店应用程序的最新版本，你现在可以在 APKMirror 下载。关注我们的 [APK 拆卸标签](https://www.xda-developers.com/tag/apk-teardown/)获取更多类似的文章！