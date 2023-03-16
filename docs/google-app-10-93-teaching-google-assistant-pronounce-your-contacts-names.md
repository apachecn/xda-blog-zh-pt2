# 谷歌应用 10.93 提示教谷歌助手如何读你的联系人的名字

> 原文：<https://www.xda-developers.com/google-app-10-93-teaching-google-assistant-pronounce-your-contacts-names/>

谷歌应用程序提供来自搜索巨头的各种不同的服务。它不仅包括谷歌搜索，也是谷歌发现、谷歌播客、谷歌助手和谷歌镜头的所在地。最重要的是，谷歌不断发布新功能和设计变化。有时，我们能够在 APK 拆除谷歌应用程序的过程中识别出一些[即将到来的变化。例如，早在去年 10 月，APK 拆除了该应用的 10.81.6.29.arm64 版本，这表明谷歌正在测试应用上的](https://www.xda-developers.com/google-app-suggestions-lens-shortcut-search-widget-new-at-a-glance-discover-interests-podcasts-redesign-photos-sharing-assistant/)[新收藏 UI、智能截图和链接广播服务](https://www.xda-developers.com/google-app-tests-collections-ui-smart-screenshots-linking-radio-services/)。这让我们初步了解了谷歌为这款应用准备的一些新东西。类似地，谷歌应用程序 10.93.8.29 版本的拆卸现在发现了一个新功能，允许用户训练助手正确发音。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

众所周知的事实是，谷歌英语助手很难将一些名字读得比其他名字更准确。如果助手不能正确读出你的名字，谷歌会让你选择进入助手设置并记录你自己的发音(如下图所示)。目前，没有办法训练助手正确读出联系人列表中的人名。虽然你可以去谷歌通讯录，编辑你的联系人的名字，添加语音发音，这个过程可能有点麻烦。最新版本的谷歌应用程序的拆卸显示，该公司正在努力使这一过程更加简单。

在最新版本的谷歌应用程序中发现的一串代码表明，谷歌将很快让你能够为你的联系人记录你自己的发音。该功能基本上可以让你训练助手读出联系人的名字，就像你训练它读出你的名字一样。您将获得记录您的发音、回放、删除发音或使用默认发音的能力。到目前为止，谷歌还没有发布任何关于这项功能的信息，我们也不知道它的发布时间。然而，由于与该功能相关的代码已经出现在应用程序中，该功能应该很快就会出现在应用程序的测试版中。

```
 <string name="assistant_settings_people_pronunciation_custom_option_subtitle">"Teach the Assistant to pronounce this contact's name by recording your own"</string>
<string name="assistant_settings_people_pronunciation_custom_option_title">Record your own</string>
<string name="assistant_settings_people_pronunciation_default_option_title">Use default</string>
<string name="assistant_settings_people_pronunciation_delete_button_label">Delete</string>
<string name="assistant_settings_people_pronunciation_editor_title">Name pronunciation</string>
<string name="assistant_settings_people_pronunciation_play_button_label">Play</string>
<string name="assistant_settings_people_pronunciation_record_button_label">Record</string> 
```

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*