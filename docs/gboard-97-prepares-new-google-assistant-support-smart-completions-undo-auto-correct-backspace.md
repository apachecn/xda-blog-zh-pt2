# Gboard 9.7 准备了新的 Google Assistant 支持、智能补全和退格撤销自动纠正

> 原文：<https://www.xda-developers.com/gboard-97-prepares-new-google-assistant-support-smart-completions-undo-auto-correct-backspace/>

谷歌的 [Gboard](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.latin) 是最受欢迎的键盘应用之一，并且不断更新新功能。在过去的几周里，我们已经看到 Gboard 准备了[谷歌镜头快捷方式，系统兼容的暗/亮主题，以及谷歌助手听写支持](https://www.xda-developers.com/gboard-google-lens-dark-light-themes-system-assistant-dictation-support/)，[添加表情符号快捷栏](https://www.xda-developers.com/google-adds-emoji-shortcut-bar-gboard-android/)，[图片粘贴](https://www.xda-developers.com/gboard-image-pasting-google-lens/)，[智能回复建议](https://www.xda-developers.com/gboard-adds-3-new-suggestions-smart-replies-gif-search-stickers/)，甚至添加[支持 Android 11 表情符号](https://www.xda-developers.com/gboard-android-11s-new-emojis/)。现在，Gboard 似乎正准备为新的谷歌助手添加一个询问助手按钮，智能完成设置，以及在退格键上撤销自动更正的功能。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

## Gboard v9.7.03 测试版

我们在刚刚开始推出的 Gboard v9.7.03 测试版中发现了以下新特性:

### 新谷歌助手的询问助手按钮

```
 <string name="nga_ask_assistant_button_description">Ask Assistant Button</string>
<string name="nga_ask_assistant_text">Ask Assistant</string> 
```

虽然这个字符串可能看起来像键盘只是表面上添加了一个用于召唤助手的专用按钮，但它实际上是指[新的谷歌助手](https://www.xda-developers.com/new-google-assistant-support-german-french-spanish-italian-pixel-4a-pixel-4/)(因此字符串名称中有“nga”)，这就是设备上经过改进的谷歌助手所指的，正如在谷歌 Pixel 4、Pixel 4 XL 和 Pixel 4a 上发现的那样。

### 通过 Gboard 智能完成

```
 <string name="setting_enable_inline_suggestion_title">Smart completions</string> 
```

该字符串可能指的是之前详述的[智能完井功能](https://www.xda-developers.com/google-smart-compose-gboard-android-messages-telegram-whatsapp/)的设置。

### 在退格键上撤消自动更正

```
 <string name="setting_enable_ac_revert_summary">Return to original text when backspacing after an autocorrection</string>
<string name="setting_enable_ac_revert_title">Undo auto-correct on backspace</string> 
```

此功能将有助于恢复到不必要的自动更正，只需用一个退格键取消自动更正，而不需要返回并重新键入单词。因为字符串出现在 setting 子类中，所以它可能是一个可以切换的特性。

* * *

*感谢 PNF 软件为我们提供了使用* *[JEB 反编译](https://www.pnfsoftware.com/?aid=xdadev)* *的许可，这是一款针对 Android 应用的专业级逆向工程工具。*