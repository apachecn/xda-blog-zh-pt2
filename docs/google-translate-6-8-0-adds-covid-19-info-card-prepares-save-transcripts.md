# 【更新:文字稿截图】谷歌翻译 6.8.0 增加了新冠肺炎信息卡，准备让你保存文字稿

> 原文：<https://www.xda-developers.com/google-translate-6-8-0-adds-covid-19-info-card-prepares-save-transcripts/>

**更新 1 (05/14/2020 @ 04:48 AM ET):** 谷歌翻译即将推出的“保存抄本”功能截图浮出水面。滚动到底部了解更多信息。下面保留了 2020 年 5 月 12 日发表的文章。

今年 3 月早些时候，谷歌终于在谷歌翻译中推出了实时翻译功能，允许用户录制一种语言的演讲，并在你的手机上进行近乎实时的翻译。这项名为“转录”的功能不同于谷歌翻译较早的转录功能，后者要求你输入文本或语音，然后等待翻译。然而，尽管它很有用，令人惊讶的是该功能不允许用户保存文字记录。但这种情况可能很快就会改变，因为最新版本的谷歌翻译(6.8.0)的拆卸揭示了代码，表明谷歌正在努力在应用程序中包括一个保存抄本的功能。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

一旦上线，实时翻译功能中的保存文字记录选项将显示一个提示，提醒用户在翻译完成后保存文字记录。新的代码字符串还显示，用户将能够删除保存的抄本，重命名它们，并查看所有保存的抄本。如果用户试图在不保存抄本的情况下退出转录功能，该应用程序还会推送一条警告:“如果您退出转录，您将会丢失当前未保存的抄本。您确定要退出吗？

```
 <string name="delete_transcript">Delete transcript?</string>
<string name="hint_save_transcript">Name</string>
<string name="msg_delete_transcript">Are you sure to delete the transcript \"%s\"?</string>
<string name="msg_exit_session_transcribe">If you exit Transcribe, you will lose your current unsaved transcript. Are you sure you want to exit?</string>
<string name="rename_transcript">Rename transcript</string>
<string name="save_transcript">Save transcript</string>
<string name="saved_transcript_title">Saved transcripts</string> 
```

此外，其他一些字符串暗示了一个即将到来的选项，该选项将允许您为实时翻译功能选择音频输入源。通过该选项，用户可以选择手机麦克风或耳机麦克风进行实时翻译。

```
 <string name="label_listen_choose_microphone">Choose microphone</string>
<string name="label_listen_headset_microphone">Headset</string>
<string name="label_listen_phone_microphone">Phone</string> 
```

在面向用户的变化方面，谷歌翻译 6.8.0 版增加了一个新的新冠肺炎卡，每当用户翻译一个与正在进行的疫情有关的单词时，它就会弹出。正如你在下面的截图中看到的，翻译冠状病毒这个词会带来新的卡片，其中包括一个超链接，帮助用户轻松获得疫情的最新信息。

虽然新的新冠肺炎卡已经在最新版本的谷歌翻译上上线，但我们目前还不知道其他两个功能何时会添加到应用程序中。一旦谷歌在该应用的未来版本中发布该功能，我们将立即更新这篇文章。

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*

* * *

## 更新:谷歌翻译即将推出的保存文本功能截图

以逆向工程技能闻名的简·满春·王女士分享了一张截图，展示了谷歌翻译即将推出的保存文字记录功能。

这与我们在 APK 拆解中的发现是一致的。

**来源:[@ wong Jane](https://twitter.com/wongmjane/status/1260448701941719040)**