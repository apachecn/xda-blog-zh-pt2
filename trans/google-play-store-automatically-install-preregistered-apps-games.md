# 谷歌 Play 商店 v18.6.28 提示自动安装你预先注册的应用和游戏

> 原文：<https://www.xda-developers.com/google-play-store-automatically-install-preregistered-apps-games/>

谷歌 Play 商店对于 Android 生态系统来说是一个非常重要的应用，是向全球数百万用户分发 Android 应用的主要和中心点。因此，应用程序和游戏的成功在很大程度上取决于依赖于 [Play Store](https://play.google.com/store/apps) 的营销策略——接触到多少用户，多少用户安装了该应用程序，他们是否对其做出反应，以及他们的反应有多好。几年前，谷歌为出版商推出了一个选项，可以创建预发布的 Play Store 列表，并允许最终用户通过预注册来表达他们对该应用的兴趣。现在，谷歌 Play 商店可能正准备在最终用户设备上自动安装这些预先注册的应用和游戏。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

谷歌 Play 商店 v18.6.28 包含的字符串表明，应用分发平台可能很快会自动安装用户通过预注册明确表示感兴趣的应用和游戏。

```
 <string name="notification_prereg_auto_install_success">%1$s is installed</string>
<string name="notification_prereg_auto_install_success_explanation_app">"You pre-registered for this app and it's now installed on your device. Enjoy the app!"</string>
<string name="notification_prereg_auto_install_success_explanation_game">"You pre-registered for this game and it's now installed on your device. Enjoy the game!"</string> 
```

目前，当用户预注册一个应用程序或游戏时，他们会在该应用程序或游戏发布并可供下载时收到通知。通知是对行动的呼吁，但是用户可能最终完全忽略通知，或者只是在日常通知的弹幕中真正错过它。这个即将到来的变化可能会自动为你安装应用或游戏，然后通知你它已经安装好了。

谷歌可能还会在 Play Store 设置中添加一个选项来控制下载(WiFi 和移动数据设置)或完全退出自动安装，因为并非所有用户都愿意在移动数据上下载应用程序，或者首先自动下载。与 Play Store 预发布列表所暗示的相比，应用程序或游戏也可能在发布时有所不同，因此在适当的位置设置一些用户定义的控制将是合乎逻辑的。谷歌的这一改变将如何与他们最近决定不显示任何关于[更新应用](https://www.xda-developers.com/the-google-play-store-will-no-longer-show-notifications-for-updated-apps/)的通知一起发挥作用还有待观察(尽管有一个[应用修复了这种行为](https://www.xda-developers.com/play-store-updates-notifications/))。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*