# Google ARCore Depth API 现已推出，可提供逼真的增强现实体验

> 原文：<https://www.xda-developers.com/google-arcore-depth-api-public-launch/>

# 谷歌的 ARCore Depth API 现在可供开发者制作逼真的 AR 体验

谷歌正在 ARCore 中为所有开发人员提供深度 API，以创建更真实的增强现实体验。

ARCore 是谷歌的 SDK，用于在 Android 和 iOS 上创建增强现实体验。在 Android 设备上，它是作为用于 AR 应用程序的 Google Play 服务的一部分提供的。去年年底，[谷歌预览了](https://www.xda-developers.com/google-arcore-depth-api-create-depth-maps-using-single-camera/)ARCore Depth API，它改善了单摄像头设备的沉浸感。根据谷歌的[博客帖子，现在，这个 API 已经准备好向 Android 和 Unity 上的开发者公开发布。](https://developers.googleblog.com/2020/06/a-new-wave-of-ar-realism-with-arcore-depth-api.html)

ARCore Depth API 使用谷歌的运动深度算法从单个 RGB 相机生成深度图。它通过从不同角度拍摄多幅图像，并在用户移动相机时进行比较来实现这一点。深度 API 的关键功能之一是遮挡，这使得将数字对象*准确地放置在*现实世界对象的后面成为可能。除了遮挡，深度 API 还支持真实物理、与真实世界表面的交互、环境遍历等等。正如你在下面嵌入的 gif 中所看到的，这些功能使增强现实体验更加真实。游戏 [*五夜弗雷迪的 AR:特别递送*](https://play.google.com/store/apps/details?id=com.illumix.fnafar&hl=en_US) 使用了这一功能，Snap Inc .已经将该 API 用于其*跳舞热狗*和新*海底世界* Snapchat 镜头。从今天开始，深度 API 将在 ARCore 1.18 for Android 和 Unity 中面向开发者公开。

Snapchat 镜头创作者可以下载深度 API 模板，为 Android 设备创建他们自己的基于深度的体验。TeamViewer Pilot 是一款用于远程协助的应用程序，它正在使用深度 API 来实现视频通话期间的增强现实注释。谷歌表示，今年晚些时候，我们将能够看到更多深度增强现实体验，将表面互动和环境穿越付诸实践。例如，一款名为 *SKATRIX* 的游戏将把你的家变成一个数字滑板公园，而另一款名为 *SPLASHAAR* 的游戏将让 AR 蜗牛在你的房间里赛跑。开发者可以通过 [GitHub](https://github.com/googlesamples/arcore-depth-lab/) 上的开源项目来构建这些概念。

谷歌还指出，飞行时间(ToF)传感器虽然不是必需的，但可以通过减少扫描时间和改善飞机探测来提高体验质量。例如，三星将更新其快速测量应用程序，在 [Galaxy Note 10+](https://forum.xda-developers.com/galaxy-note-10+) 和 [Galaxy S20 Ultra](https://forum.xda-developers.com/galaxy-s20) 上使用 ARCore Depth API。然而，谷歌指出，这项功能通常可以在[数亿台支持增强现实 Google Play 服务的安卓设备](https://www.xda-developers.com/tag/arcore)上运行，因为它只需要一个 RGB 摄像头。