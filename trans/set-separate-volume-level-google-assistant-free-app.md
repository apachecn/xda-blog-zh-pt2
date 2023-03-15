# 使用这款免费应用为谷歌助手设置单独的音量级别

> 原文：<https://www.xda-developers.com/set-separate-volume-level-google-assistant-free-app/>

Android 智能手机上的 Google Assistant 在少数市场的所有 Android 棉花糖设备上以特定语言正式提供。智能助理可以通过语音或文本输入来访问，但只有当通过语音向助理发送查询时，才会给出口头反馈。

* * *

**推荐阅读** : [下面介绍如何在没有 Root 的 Android 5.0+平板电脑上获取谷歌助手](https://www.xda-developers.com/get-google-assistant-on-android-lollipop-marshmallow-nougat-tablets-without-root/)

* * *

当你无法使用手机进行搜索时，比如在开车时，与谷歌助手的语音交互就能派上用场。在这种情况下，如果你和谷歌助手说话，它的回应却是静音，这可能会特别令人沮丧，因为你的设备的媒体音量太低了。当你在路上时，你不能分心，比如瞥一眼看你的助手查询的视觉输出(如果你甚至可以看到你的屏幕，取决于你把它停靠在哪里)，或者摸索着用你的手机增加音量，以便你可以重复你的命令。

/r/GooglePixel subreddit 上的许多 Redditors 想知道为什么 Google Assistant [不能使用自己单独的音量级别](https://www.reddit.com/r/GooglePixel/comments/6e5i9m/google_assistant_really_should_have_its_own/)。尽管 Assistant 不能在每台设备上都添加自己的音量流，但它肯定应该能够在与您通话之前设置自定义的媒体音量。我猜谷歌不想让用户面对相反的问题，当你晚上在一个安静的房间里时，助手会以最大音量发出回应。

无论如何，如果你希望能够独立于你的设备当前的媒体音量来控制谷歌助手的音量，我已经制作了一个粗糙但完全免费的应用程序，没有广告可以做到这一点。我之所以说粗糙，是因为该应用程序是使用 Tasker 及其 Tasker 应用程序工厂扩展构建的。

这意味着漂亮设计的机会是有限的(在某些屏幕分辨率上它可能看起来不可靠，因为 Tasker 不支持动态缩放其场景)，但老实说，你可能会花最多 5 秒钟来看这个应用程序，因为你真正需要做的只是扳动开关，改变几个滑块，然后就可以愉快地上路了。

[appbox xda com . tasker . assistant volume]

你所要做的就是安装应用程序，启用其辅助功能服务，切换应用程序中的开关以启动其谷歌助手监控服务，并更改一些设置。该应用程序将在后台完成其余的工作。它可以在任何支持谷歌助手的设备上工作，如谷歌 Pixel、谷歌 Pixel XL、OnePlus 3、OnePlus 3T、三星 Galaxy S8、Galaxy S8+等。你不再需要记得在与谷歌助手交谈之前手动设置你的媒体音量，这个应用程序会帮你解决这个问题。

尽管如果你真的真的不能忍受这款应用的设计或者想要更多的长期支持，你可以在谷歌 Play 商店上花 1.49 美元购买助手应用的[音量控制。我制作这个应用程序的想法来自这个开发者，尽管我没有抄袭他们的代码。我自己制作了这个应用程序，更多的是作为对自己概念的证明，因为这个概念似乎足够简单，我想看看用 Tasker 可以制作什么样的应用程序。](https://play.google.com/store/apps/details?id=com.nyelito.volumecontrol)

在另一篇文章中，我将详细介绍我是如何使用 Tasker 制作这个应用程序的，并给出一些提示，这样你就可以开始制作简单的应用程序，而不需要接触一行代码。

* * *

关注 [XDA 教程 RSS 源](https://www.xda-developers.com/category/tutorials/feed/)获取更多类似的内容。下载 [XDA 实验室](https://www.xda-developers.com/xda-labs/)，快速了解 XDA 门户网站上发布的所有最新新闻和原创专题。