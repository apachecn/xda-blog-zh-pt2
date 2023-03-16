# 谷歌 Chrome 正在测试一个后退按钮手势，以显示 Android 上的历史记录

> 原文：<https://www.xda-developers.com/google-chrome-android-back-button-history/>

**2019 年 1 月 30 日更新:**谷歌 Chrome 版本 72 的稳定版现在默认启用长按显示历史功能。

2018 年 7 月 29 日更新:该功能现已在最新的 Chrome Canary 版本中提供。截图可以在下面找到。

随着谷歌继续试图改善谷歌 Chrome 浏览器的 UX，他们也在 T2 尝试其他方式来改善他们的浏览器。根据 [Chromium Gerrit](https://chromium-review.googlesource.com/c/chromium/src/+/996238/1) 的说法，一个新功能正在开发中，它将允许你长按设备的后退按钮来查看你最近的导航历史。该功能将通过 Chrome 标志启用，并且仅在移动设备上可用。

标志描述简单地说明了该功能由“长按后退按钮以显示导航历史”组成我们不确定导航历史将如何在屏幕上显示，但有可能看到新的 [Chrome Duplex](https://www.xda-developers.com/hands-on-google-chromes-new-duplex-split-toolbar-ui-replaces-chrome-home/) 用于显示它。不管怎样，这都是谷歌试图改进他们的浏览器，为用户提供更多方便查看潜在重要信息的方式。目前，查看你的导航历史并不困难，但是让它变得更容易并没有错。

该功能让人想起谷歌桌面版 Chrome 通过右键单击左上方的后退箭头查看导航历史的功能。这个菜单遵循的风格也可以暗示我们将看到我们的导航历史的风格。因此，它可能不是通过使用新的谷歌双工，而是通过一个来自屏幕右上角或左上角的菜单。Android 版火狐和三星互联网也有这样的功能，所以看到谷歌将其纳入 Chrome 以实现功能对等也就不太奇怪了。

这不是我们最近发现的唯一变化，随着[另一个提交](https://www.xda-developers.com/google-chrome-android-gesture-drag-drop-links/)表明我们可能很快就会看到通过手势拖放链接。如果测试成功，我们可能会在接下来的一两个月内看到谷歌 Chrome 的金丝雀版本中加入这一功能。你可以通过谷歌 Play 商店下载并尝试一下。如果你对谷歌浏览器的其他新功能感兴趣，你可以下载下面的金丝雀版本。

* * *

## 更新 1:功能是活的

上面的截图显示了当你在谷歌浏览器打开的情况下长按后退按钮时的样子。您可以打开一个新标签页或显示历史记录。这在配有高显示屏的设备上会很有用，尤其是如果你不是[分割工具栏 Chrome Duet 功能](https://www.xda-developers.com/google-chrome-duplex-split-toolbar-one-handed/)的粉丝。要启用此功能，只需确保您使用的是最新的 Chrome Canary 或 Chromium nightly，并将以下内容粘贴到地址栏中:

```
 chrome: 
```

## 更新 2:现在稳定

该功能现在出现在 Android 版 Chrome 的稳定版本中。从版本 72 开始，您可以简单地长按导航栏中的 back 按钮来显示当前选项卡的历史。

[app box Google play com . Android . chrome & HL = en]