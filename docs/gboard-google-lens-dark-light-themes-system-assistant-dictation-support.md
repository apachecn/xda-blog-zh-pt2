# Gboard 准备了谷歌镜头快捷方式，自动黑暗主题，等等

> 原文：<https://www.xda-developers.com/gboard-google-lens-dark-light-themes-system-assistant-dictation-support/>

谷歌的 Gboard 是最受欢迎的键盘应用之一，并不断更新新功能。最近，谷歌[在 Gboard 上增加了对 Android 11 表情符号](https://www.xda-developers.com/gboard-android-11s-new-emojis/)的支持，就在一周前[激活了智能撰写预测消息应用](https://www.xda-developers.com/google-smart-compose-gboard-android-messages-telegram-whatsapp/)。现在，谷歌准备在 Gboard 上增加一个 [Google Lens](https://www.xda-developers.com/google-lens-tests-education-mode-solving-math-problems-places-mode-look-up-buildings/) 快捷、 [Google Assistant](https://www.xda-developers.com/google-assistants-overview-recipe-suggestions/) 听写、支持明暗主题自动切换等功能。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

我们发现了本周早些时候发布的 Gboard 9 . 6 . 3 测试版的功能参考，增加了 Android 11 的表情符号。以下新字符串是 Gboard 应用程序最新测试版的一部分，暗示了谷歌首次在谷歌 I/O 2019 上展示的新的谷歌助手支持的语音听写功能:

```
 <string name="nga_clear_button_description">Clear Button</string>
<string name="nga_clear_text">Clear</string>
<string name="nga_close_button_description">Close Button</string>
<string name="nga_close_text">Close</string>
<string name="nga_onboarding_close_button_description">Close</string>
<string name="nga_onboarding_mic_button_description">Mic Button</string>
<string name="nga_search_button_description">Search Button</string>
<string name="nga_search_text">Search</string>
<string name="nga_send_button_description">Send Button</string>
<string name="nga_send_text">Send</string>
<string name="nga_start_dictating_default">Speak now to type hands free</string>

```

不过，新的谷歌助手功能仍然是 Pixel 4 和 Pixel 4 XL 独有的。

* * *

除了使用谷歌助手打字，谷歌还增加了一个新的“默认黑色”主题，以补充“默认白色”主题。谷歌 通过对最新版本中新添加的功能进行逆向工程展示了这一点。新的黑色主题没有彩色回车键，可能会有一个“系统自动”功能，作为改进主题的一部分，允许它在默认的亮暗主题之间自动切换。

此外，谷歌正在添加[谷歌无字体，以取代 Gboard 中字母键上的 Roboto](https://www.xda-developers.com/roboto-android-fall-rise-default-font/) 。

在 Gboard 数字行上方的快捷方式行中，Google 还突出显示了 Google Lens 和 Google Assistant 的新快捷方式。根据他们的报告，谷歌镜头快捷方式只启动应用程序，并没有更深层次的整合。与此同时，从去年的 Gboard 8.5 开始就一直在工作的助手快捷方式仍然处于非活动状态。然而，正如我们发现的上面这组字符串可能暗示的那样，该功能可能很快就会开始工作。

为了在大多数用户之前获得这些功能，你可以通过[点击这里](https://play.google.com/apps/testing/com.google.android.inputmethod.latin)或者向下滚动谷歌 Play 商店列表并点击测试版下的“加入”来注册 Gboard 测试版。