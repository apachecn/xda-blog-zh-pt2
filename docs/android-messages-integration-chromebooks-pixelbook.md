# Android Messages 与 Chromebooks 的集成在 Pixelbook 上推出

> 原文：<https://www.xda-developers.com/android-messages-integration-chromebooks-pixelbook/>

# Android Messages 与 Chromebooks 的集成在 Pixelbook 上推出

Chrome OS 中的 Android Messages 集成现在正在 Chromebooks 上推出，首先是 Chrome OS 开发频道上的 Google Pixelbook。

Android Messages 应用程序(现在只称为“Messages”)最令人期待的功能之一是它的网络客户端(T1)，至少在仍然通过短信发送信息的美国人中是如此。Messages 的网络客户端支持包括 Chrome OS 在内的所有桌面操作系统上的大多数桌面浏览器，但我们发现谷歌正在为 Chrome book 进行[更深入的整合。作为谷歌“Better Together”功能套件(在市场上被简单称为“Android phone”)的一部分，Messages 功能允许你从 Chromebook 发送和接收文本信息，即使你没有打开 Android Messages web 客户端。这是可能的，因为 Android Messages 应用程序将被安装为一个](https://www.xda-developers.com/chrome-os-android-messages-integration/)[渐进式网络应用程序](https://www.xda-developers.com/progressive-web-apps-replace-google-chrome-apps/)，它现在已经与谷歌 Pixelbook 上的 Better Together 功能一起[上线](https://chromium-review.googlesource.com/c/chromium/src/+/1279426)。

如果你访问[messages.android.com](https://messages.android.com/)并在支持安装渐进式网络应用的浏览器(如[谷歌 Chrome 70](https://www.xda-developers.com/chrome-70-google-sign-in-pwa-support-av1-decoder/) )上打开菜单，你应该会看到一个“安装安卓信息”按钮。点击这个将会安装 Messages Progressive Web 应用程序，您可以像启动任何其他应用程序一样启动它。(有趣的是，谷歌似乎忘了从 PWA 的名字中去掉“Android”。)

在 Chrome OS 上，安装这个 PWA 并设置客户端将允许你发送和接收文本消息，而不必保持 web 客户端打开。PWAs 可以在消息中心显示通知，就像本地应用一样，你甚至可以在线回复。我在谷歌制造活动上得到了一个演示，因为展出的谷歌 Pixel 平板电脑运行的是比当时版本更新的 Chrome 操作系统。我被告知，Android Messages 集成将适用于任何 Chromebook 和 Android 智能手机组合，尽管我在 Chrome OS Canary channel(运行 Chrome OS 72)上的惠普 Chromebook X2 没有 Messages 集成，也不能访问 Better Together 功能集。如果你在 Dev 频道上使用的是 Chrome OS 71 以上的版本，你可以尝试自己启用它，方法是访问 chrome://flags，搜索所有与“MultiDevice”相关的标志。Google Pixelbook 上至少有一个用户在/r/[Crostini](https://www.reddit.com/r/Crostini/comments/9p2afk/17october_dev_channel_update_71035788/e7yltgy/)subredit 上发帖称，他们可以使用 Better Together，所以如果你对这个新功能感兴趣，一定要试试。

提醒一下，下面是对新的“一起更好”功能集的描述:

*   智能锁:用手机解锁你的 Chromebook。所有的 Chromebooks 和 Android 手机都可以支持这个功能。
*   [即时共享](https://www.xda-developers.com/chrome-os-instant-tethering-enabled/):如果你的 Chromebook 失去连接，立即切换到你手机的数据连接。只有谷歌 Pixel 智能手机支持即时共享。
*   信息:从你的 Chromebook 发送和接收文本信息。据我所知，所有的 Chromebooks 和 Android 手机都应该支持这一功能。