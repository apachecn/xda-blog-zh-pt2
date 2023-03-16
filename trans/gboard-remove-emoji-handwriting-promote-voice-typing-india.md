# Gboard 准备移除表情符号手写，在印度推广语音打字，等等

> 原文：<https://www.xda-developers.com/gboard-remove-emoji-handwriting-promote-voice-typing-india/>

GBoard 是 Android 上最受欢迎的键盘之一，凭借其预测文本建议和滑动输入功能，以及与谷歌其他服务的功能集成，它在受欢迎程度排行榜上名列前茅。虽然大多数应用程序的更新都倾向于带来新功能，但 GBoard 的下一次更新正准备删除 emoji 手写功能。为了平衡这一点，该应用程序还将促进英语-印度的语音输入，并添加一个新的语音听写和表情符号快捷方式的清除按钮。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

## 反对表情符号手写

表情符号涂鸦搜索功能是在 2017 年 6.3 版本的应用程序中推出的。在 GBoard v8.8.2.273581900 测试版中发现的代码字符串指向一个新标签，该标签将提醒用户该功能的过早消亡。

```
 <string name="emoji_handwriting_deprecation_notice_content_description">Notice of emoji handwriting keyboard deprecation</string>
<string name="emoji_handwriting_deprecation_notice_label">The emoji handwriting feature will be removed soon</string> 
```

该功能允许用户通过在键盘上涂鸦来查找各种不同的表情符号。虽然它看起来很酷，但这个功能并不直观，大多数用户更喜欢使用表情关键字搜索。

我们并不确定这个特性什么时候会被移除，但是考虑到代码已经存在，用不了多久它就会被移除。

虽然谷歌正在移除表情符号手写功能，但它也准备在应用程序中加入一些新功能。例如，更新还透露，谷歌将推出英语-印度的语音打字功能，并在应用程序中推出一个宣传片，提醒用户这一新功能。

```
 <string name="romanized_indic_voice_typing_banner">Kya haal hai?</string>
<string name="voice_banner_description">a promo to let users know that voice dictation is now available for them.</string>
<string name="voice_promo_input_method_entries_whitelist">en-IN</string>
<string name="voice_typing_banner">How are you?</string>
<string name="voice_typing_notice">Type using your voice. Try it now.</string> 
```

上面的字符串清楚地突出了一个新的横幅，它实际上是一个宣传片，让用户知道语音听写现在对他们可用。同样，我们不确定该功能何时在应用程序上上线，但我们希望在后续更新中了解更多信息。

## 语音听写的清除按钮

此外，使用 Gboard 语音听写功能的用户会很高兴地知道，该公司正在开发一种新的清除按钮，允许他们只需轻轻一点就可以删除信息。

```
 <string name="voice_ime_clear_button_description">Clear Field</string> 
```

正如你在下面的推文中看到的，新按钮将出现在语音输入栏的左侧。与前述功能一样，清除按钮的发布日期也没有明确的时间表。

## 添加表情快捷方式

最后，代码串还表明谷歌正在键盘上添加一个新的表情符号快捷方式，这将允许用户快速选择他们最喜欢的表情符号。

```
 <string name="access_points_order">search;sticker;gif_search;clipboard;settings;theme_setting;one_handed;textediting;share;translate;floating_keyboard</string>
<string name="access_points_order">search;smiley;sticker;gif_search;clipboard;settings;theme_setting;one_handed;textediting;share;translate;floating_keyboard</string>
<string name="id_access_point_smiley">smiley</string> 
```

正如您在上面的字符串中看到的，“smiley”访问点被添加到了键盘的快捷菜单中。下面的推文展示了新的快捷方式最终发布时的样子。

值得注意的是，我们在这里提到的任何特性都有可能在未来的版本中无法实现。然而，从历史上来说，在测试版中上线的功能，如我们在应用程序 8.7.2 版本中看到的[超高和超短键盘高度](https://www.xda-developers.com/gboard-8-7-2-extra-tall-extra-short-keyboard-height/)，通常会在稳定版本中发布。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*