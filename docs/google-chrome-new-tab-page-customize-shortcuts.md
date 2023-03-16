# 谷歌浏览器的新标签页将很快让你自定义快捷方式

> 原文：<https://www.xda-developers.com/google-chrome-new-tab-page-customize-shortcuts/>

# 谷歌浏览器的新标签页将很快让你自定义快捷方式

很快，谷歌将开始在谷歌 Chrome 浏览器中提供一个可定制的新标签页。提交刚刚出现在 Gerrit 上。

我们的大多数用户可能正在使用谷歌浏览器阅读这篇文章。我也确信至少你们中的一些人想要改变新标签页上谷歌搜索栏下面的网站快捷方式。事实证明，谷歌将很快赋予我们这样做的能力。Chromium Gerrit 最近出现了一个新的 [commit](https://chromium-review.googlesource.com/c/chromium/src/+/1135849) ，它带有一个实验性的标志，允许你在新的标签页上编辑快捷方式。

要启用此标志，请将此地址粘贴到您的 URL 栏中:

```
 chrome: 
```

目前，启用该标志还会启用“ntp-ui-md”和“ntp-icons”标志。这些标志启用新选项卡页面上的材料设计 UI 和图标。请记住，这可能会在未来发生变化，因为材料设计大修最终将成为谷歌 Chrome 的默认选项。以下是在当前 Chrome Canary 和 Chromium nightly 版本中启用它的方式。你可以清楚地看到修改后的网站快捷方式和改变背景的选项。

启用该功能会使快捷方式保持静态，因此在您访问网站时不会添加新的快捷方式。当前的行为是动态的，会根据您最常访问的站点而频繁变化，这个新功能将取代该行为。

我相信这个即将推出的功能会让一些用户感到高兴。你也可以在最新的金丝雀版本中改变背景，它甚至[支持谷歌照片集成](https://www.xda-developers.com/google-chrome-new-tab-page-google-photos/)。请记住，金丝雀浏览器的版本可能不稳定，所以如果你想在更稳定的版本上使用这一功能，你必须等待几周内达到 Chrome Beta 或 Chrome Stable。