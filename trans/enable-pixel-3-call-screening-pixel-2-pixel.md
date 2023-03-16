# 在 Pixel 2 和 Pixel [Root]上启用 Google Pixel 3 的来电屏蔽

> 原文：<https://www.xda-developers.com/enable-pixel-3-call-screening-pixel-2-pixel/>

谷歌在一个月前发布了 Pixel 3 和 Pixel 3 XL 设备。除了高通骁龙 845、4GB RAM、64/128GB 内部存储、IP68 等级、无线充电和其他基于硬件的功能，这些设备还提供了几个软件专有功能。其中一个功能是夜视，这一相机功能可以帮助用户在弱光条件下拍摄出令人惊叹的照片。我们已经看到[开发者为所有 Pixel 设备启用夜视](https://www.xda-developers.com/google-camera-night-sight-google-pixel-3-google-pixel-2-google-pixel/)，现在我们在这里告诉你如何在谷歌 Pixel 2、谷歌 Pixel 2 XL、谷歌 Pixel 和谷歌 Pixel XL 上启用新的呼叫筛选功能。

提醒你一下，来电过滤是谷歌手机应用中的一项新功能，它可以接收来电，帮助你避开骗子。Google Assistant 告诉来电者留言，你可以随时选择接手。这是一个非常方便的功能。呼叫筛选目前仅适用于谷歌 Pixel 3 和谷歌 Pixel 3 XL，但谷歌承诺在本月晚些时候将它引入到老一代 Pixel 设备中——就像夜视一样。但是，只要你住在美国，你就不必再等了。以下是在 Google Pixel、Google Pixel XL、Google Pixel 2 和 Google Pixel 2 XL 上启用来电过滤的说明。您的设备需要 root 访问权限才能执行该过程。

## 在 Google Pixel 和 Google Pixel 2 上启用来电过滤

*XDA 资深会员[酷派 8](https://forum.xda-developers.com/member.php?u=3667632) 在我们的论坛上分享了这个方法[，XDA 资深会员](https://forum.xda-developers.com/pixel-2-xl/themes/root-enable-call-screening-pixel-t3861350)[传奇人物](https://forum.xda-developers.com/member.php?u=524992)发现了旗帜。*

1.  首先，如果你还没有找到你的设备，就从它开始吧。在此链接上可以找到说明和链接[。](https://www.xda-developers.com/magisk-hub-2/)
2.  下载任何支持 root 的文件浏览器，如 [FX 文件浏览器](https://forum.xda-developers.com/showthread.php?t=1253399)或 [MiXplorer。](https://forum.xda-developers.com/showthread.php?t=1523691)
3.  打开浏览器，从左侧导航菜单导航到根目录。
4.  导航到`/data/data/com.google.android.dialer/shared_prefs`并寻找名为`dialer_phenotype_flags.xml`的文件。
5.  查找`__data_rollout__SpeakEasy.CallScreenOnPixelOneAndTwoRollout__launched__`并将值从“假”更改为“真”。您可以使用文本编辑器中的查找功能。
6.  查找`__data_rollout__SpeakEasy.OverrideUSLocaleCheckRollout__launched__`并将值从“假”更改为“真”。您可以使用文本编辑器中的查找功能。
7.  查找`G__enable_speakeasy_details`并将值从“假”更改为“真”。您可以使用文本编辑器中的查找功能。
8.  查找`G__speak_easy_bypass_locale_check`并将值从“假”更改为“真”。您可以使用文本编辑器中的查找功能。
9.  查找`G__speak_easy_enabled`并将值从“假”更改为“真”。您可以使用文本编辑器中的查找功能。
10.  打开设置，导航到应用程序，然后选择手机。强制停止。
11.  就是这样！来电过滤现在可以在谷歌手机的内部设置下使用。

现在，这种方法不能保证有效。许多用户报告说，它还不能在股票 ROM 上工作，但一些人发现 24 版本的应用程序和 14.5.70 版本的 Google Play 服务很成功。有些人只能在定制的 rom 上使用它。我们还不能确定启用该功能的确切要求，但一旦有新的细节，我们会尽快更新文章。