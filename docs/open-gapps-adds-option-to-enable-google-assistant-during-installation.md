# Open GApps 增加了在安装过程中启用谷歌助手的选项

> 原文：<https://www.xda-developers.com/open-gapps-adds-option-to-enable-google-assistant-during-installation/>

# Open GApps 增加了在安装过程中启用谷歌助手的选项

流行的谷歌应用套件提供商“Open GApps”增加了一个在安装过程中启用谷歌助手的选项。继续阅读，了解更多信息！

尽管谷歌助手已经推出了几个月，但官方仍然只限于少数设备。支持的设备包括 Google Pixel 和 Google Pixel XL、Google Home、NVIDIA SHIELD TV (2017)以及部分通过 [Google Allo](https://www.xda-developers.com/say-hello-to-google-allo-googles-ai-powered-messaging-app/) 。

尽管是非正式的，谷歌助手已经[对任何愿意在 Android 7.x 牛轧糖上编辑 build.prop 的用户](https://www.xda-developers.com/xda-external-link/google-assistant-has-been-ported-to-the-nexus-6p/)开放(只需在文件末尾添加`ro.opa.eligible_device=true`)。你甚至可以在安卓棉花糖上试用助手，只要你不介意安装一个[曝光模块](https://forum.xda-developers.com/xposed/modules/xposed-assistant-enabler-enable-google-t3479587)。

现在，流行的 Google Apps 包提供商'[Open gapp](http://opengapps.org/)'增加了一个 **[选项，在安装 Open gapp 时启用 Google Assistant](https://github.com/opengapps/opengapps/pull/419)** 。对于那些抱怨重启后必须记得修改 build.prop 的定制 rom 用户来说，这应该很方便。当然，build.prop 的调整是一个人可以做的最简单的修改，但是在恢复期间为我们做这些是非常方便的。

启用 Google Assistant 的选项应该会在 OpenGapps 的下一个版本中启用(2 月 3 日及以后)。在 AROMA 安装环境中，将提示用户启用 build.prop 修改。由于 Google Assistant 还没有完全取代 Google Now，因为它仍然缺少一些功能，因此该选项将继续对任何希望利用它的用户开放。

你经常在官方不支持的设备上使用谷歌助手吗？你的体验如何？请在下面的评论中告诉我们！

* * *

[**来源:GitHub**](https://github.com/opengapps/opengapps/pull/419)