# 谷歌地图准备添加一个“照明”层来突出灯火通明的街道，以确保夜间出行安全

> 原文：<https://www.xda-developers.com/google-maps-prepares-lighting-layer-highlight-brightly-lit-streets-night-travel/>

谷歌地图是最受欢迎的导航应用之一，数百万用户依赖它在熟悉的路线上进行日常通勤，并引导他们前往陌生的领域。例如，当你第一次访问一个新的地区时，谷歌已经努力引入了一些功能，如名称和地址的[翻译按钮](https://www.xda-developers.com/google-maps-update-translate-place-names-addresses/)、为你的电动汽车寻找兼容插头的[功能](https://www.xda-developers.com/google-maps-10-30-electric-vehicle-charging-payments-compatible-plugs/)，甚至还有当你的出租车偏离路线时发出的[警报](https://www.xda-developers.com/google-maps-taxi-goes-off-route/)。现在，谷歌正准备为谷歌地图引入一个名为“照明”的新图层，旨在突出灯火通明的街道。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

[谷歌地图 v10.31.0 测试版](https://www.apkmirror.com/apk/google-inc/maps/maps-10-31-0-release/)包含的字符串表明谷歌正在开发一项新功能，该功能将有助于使您的夜间旅行更加安全。根据字符串描述，这种新的照明图层将以黄色高亮显示照明良好的街道，进而帮助用户避开照明较差或没有照明的街道。

```
 <string name="LAYER_SAFETY">Lighting</string>
<string name="SAFETY_LAYER_ONBOARDING_DIALOG_BODY">Yellow lines show streets with good lighting</string>
<string name="SAFETY_LAYER_ONBOARDING_DIALOG_BUTTON_START">Start</string>
<string name="SAFETY_LAYER_ONBOARDING_DIALOG_NO_LIGHTING_INDICATOR">No lighting info available</string>
<string name="SAFETY_LAYER_ONBOARDING_DIALOG_POOR_LIT_INDICATOR">Poor to no lighting</string>
<string name="SAFETY_LAYER_ONBOARDING_DIALOG_TITLE">See how brightly lit the streets are</string>
<string name="SAFETY_LAYER_ONBOARDING_DIALOG_WELL_LIT_INDICATOR">Good lighting</string>
<string name="SAFETY_LAYER_TOOLTIP_PROMO">New! See how brightly lit the streets are</string>
<string name="SAFETY_LAYER_UNAVAILABLE">"Lighting view isn't available at this zoom or in this region"</string>
<string name="SAFETY_LAYER_ZOOM_IN_SNACKBAR">Zoom in more to see lighting data.</string> 
```

我们没有该功能的截图，因为它仍在开发中，还没有上线。

没有迹象表明这一功能将针对任何地区，但有根据的猜测是，这将首先在印度试点，然后推广到世界其他地区。印度最近发生了震惊全国的可怕强奸事件。虽然对这种社会罪恶的根源的讨论超出了我们网站的范围，但谷歌地图中的这一功能将帮助女性在夜间旅行时感到比以前相对更安全。这也将有助于所有人在夜间穿越陌生的地域，比如说在一个新的国家，因为游客更喜欢穿越灯光明亮的街道。目前还不清楚谷歌将如何收集街道照明数据，以及如何保持数据的实时更新。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*