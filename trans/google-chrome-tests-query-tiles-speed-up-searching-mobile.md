# 谷歌 Chrome 测试“查询磁贴”以加快手机搜索速度

> 原文：<https://www.xda-developers.com/google-chrome-tests-query-tiles-speed-up-searching-mobile/>

谷歌 Chrome 浏览器中的[新标签页](https://www.xda-developers.com/google-chrome-new-tab-page-customize-shortcuts/)自问世以来已经经历了多次重新设计，谷歌继续尝试不同的功能，使之前的空白页面更加有用。回到去年 12 月，谷歌[开始测试](https://www.xda-developers.com/google-tests-radically-new-ui-chromes-new-tab-page/)Chrome 新标签页的全新用户界面，它将所有用户界面元素移至更靠近显示顶部的位置，并用标签组织功能取代了推荐文章。虽然之前的重新设计仍然没有在 Chrome 的稳定频道上推出，但谷歌现在已经开始测试另一项设计变化，即在新的标签页上添加新的“查询磁贴”，以帮助你快速开始搜索。

根据 Android Police 最近的一份报告，新的查询磁贴只不过是带有图像的预定义搜索快捷方式，让你无需在搜索栏中键入关键词就能获得与一些不同主题相关的最新结果。截至目前，谷歌在美国提供 13 个一级磁贴类别:新闻、电影、食谱、时尚、音乐、健康、电子产品、电视节目、体育、占星术、教育、投资和汽车。点击每一个磁贴都会在下面显示几个子类别，比如新闻下面的新冠肺炎或者电子产品下面的视频游戏。

 <picture>![](img/ffa4a8c3f649a5b27066f1bb432b2981.png)</picture> 

Query editing flag disabled.

一旦你做了选择，Chrome 会根据你选择的关键词自动开始搜索，结果会显示在同一个标签中。或者，您也可以选择在提交之前编辑搜索，以获得更多定制的结果。您可以通过启用/禁用*# query-tiles-enable-query-editing*标志在这两种行为之间进行切换。

 <picture>![](img/4f93dba9b69efec4860bf6f6b1b1fc18.png)</picture> 

Query editing flag enabled.

磁贴功能目前在 Chrome Dev 和 Canary 上可用，但它可能会在未来的更新中进入测试版和稳定版。如果你希望在你的设备上尝试新的查询磁贴，你需要前往 *chrome://flags* ，搜索“查询磁贴”，然后启用*#查询磁贴*标志。

共有六种不同的标志与该功能相关，您可以使用它们来进一步自定义查询切片在设备上的工作方式。以下是所有相关的标志，以及简短的解释:

*   *#query-tiles* :启用新标签页中的查询 tiles 功能。
*   *#query-tiles-omnibox:* 使查询平铺显示在 omnibox 下方，无论是在新的选项卡页面上，还是在您单击选项卡中的 Omnibox 时。
*   *#查询-磁贴-国家代码:*根据位置个性化磁贴内容。现在，你可以选择美国、印度、巴西、尼日利亚和印度尼西亚。
*   *# query-tiles-enable-query-editing:*让您在提交搜索查询之前对其进行编辑。
*   *# query-tiles-single-tier:*将查询限制在单个级别，没有子类别。
*   *#查询-磁贴-即时获取:*没有面向用户的变化。

由于 Chrome 标志本质上是实验性的，我们不能确定谷歌是否会很快在稳定频道上发布查询磁贴标志，或者它们是否会像谷歌最近取消的 Duet 实验一样被丢弃。

* * *

**Via: [安卓警察](https://www.androidpolice.com/2020/06/04/chrome-is-testing-query-tiles-to-help-you-start-a-quick-search-from-any-tab/)**