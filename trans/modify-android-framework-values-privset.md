# 使用 Privset 修改 Android 框架值而不需要 APKTool

> 原文：<https://www.xda-developers.com/modify-android-framework-values-privset/>

你有没有想过在不使用 APKTool 反编译和重编译 framework-res.apk 的情况下，对你的 Android 设备的框架值进行修改？为了绕过可能需要的漫长时间，XDA 资深成员莫德雷德爵士(sir mordred)创建了一个名为 [Privset](https://forum.xda-developers.com/android/apps-games/app-t3694602) 的应用程序，它允许你只需 root 访问权限就可以修改你的系统框架。

## Privset 做什么

该应用可在 [Play Store](https://play.google.com/store/apps/details?id=com.mordred.privset) 获得，你可以用它来让你的手机允许，例如，四向旋转(一些手机默认不允许你上下旋转显示屏)。其他可能性包括微调你的环境显示模式设置，强制你的手机为你的应用程序显示[圆形图标](https://www.xda-developers.com/psa-android-7-1-circular-icon-support-is-determined-by-the-oem/)，或者当你双击电源按钮时改变你的手机的功能。您可以在开发人员发布的以下 YouTube 视频中了解更多有关如何使用 Privset 的信息:

**推荐阅读:** [在 Nexus 6P 上启用谷歌 Pixel 2 的常亮显示](https://www.xda-developers.com/enable-google-pixel-2-always-on-display-on-nexus-6p-pixel-xl/)Pixel，& Pixel XL 无根

* * *

## 如何使用女贞

您可以使用 Privset 对您的系统框架进行许多更改，这些更改按字母顺序列出并可搜索。即使您键入搜索词，搜索功能也能缩小可用设置的列表。当您找到想要更改的设置时，您可以将其更改为设置描述中指定的值，您需要在文本字段中键入该值，然后点击屏幕底部的“运行”按钮。

如果应用程序没有提示您重新启动设备以应用更改，您仍需要手动进行，以使更改生效。您可以通过从溢出菜单中选择“列出修改的设置”来查看您更改的所有设置的列表。如果你想一次抹掉你所做的所有更改并重新开始，你可以在溢出菜单中的“应用程序设置”中这样做。

## 女贞如何修改框架值

听说过流行的主题框架 Substratum 吗？Privset 基于相同的底层 API。它的工作原理是重定向 Android，从它为系统的内置框架-res.apk 创建的覆盖图中提取资源值。由于这些值是从覆盖图中读取的，而不是从原始的 framework-res.apk 中读取的，因此没有必要使用 apktool 或任何类似的实用程序对其进行反编译和重新编译。

**推荐阅读:**[Andromeda Add-on for substrate 为 Android Oreo 带来定制主题](https://www.xda-developers.com/andromeda-substratum-custom-themes-oreo/)

Privset 读取您设备上的现有系统属性，这意味着无论您使用的是 Android 的股票版本、定制 ROM 还是 OEM ROM，Privset 都将允许您基于您特定设备的 framework-res.apk 中存在的任何框架值来生成覆盖图。例如，您可能能够更改定制棉花糖或牛轧糖 ROM 中的框架设置，而您甚至不会在股票中看到这些设置，以 Oreo 为根。你可以在下面的图库中看到更多的例子:

如果你的设备是根设备，你可以从 [Play Store](https://play.google.com/store/apps/details?id=com.mordred.privset) 下载 Privset，并在我们的论坛中关注开发者的[主题，以给出反馈，建议新功能，或关注更多更新。](https://forum.xda-developers.com/android/apps-games/app-t3694602)