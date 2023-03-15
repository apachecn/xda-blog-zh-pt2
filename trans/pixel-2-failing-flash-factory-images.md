# 一些 Pixel 2 型号无法刷新出厂映像，OTA 更新也无法安装

> 原文：<https://www.xda-developers.com/pixel-2-failing-flash-factory-images/>

昨天，谷歌似乎出人意料地宣布了针对 Pixel 和 Nexus 设备的 Android 8.1 Oreo 预览计划，该计划可追溯到 Nexus 5X。谷歌花了一些时间来更新他们的预览程序注册网站，以支持新发布的 Pixel 2 和 Pixel 2 XL 手机，所以我们许多人开始更新工厂图像。

然而不幸的是，在尝试闪光这些图像时，似乎出现了许多错误，特别是对于较小的像素 2。我和 ArsTechnica 的 Ron Amadeo 以及 Stephen Hall 昨天在 twitter 上尝试解决我们的问题。虽然所有问题略有不同，但我们的 Pixel 2 设备或提供的图像有问题。重新连接数据线后，Stephen 通过刷新 OTA 解决了这个问题。Ron 无法从引导加载程序中退出，尽管它看起来可以正常刷新。我的问题是我不能刷新任何引导程序，即使是原来的那个。我们整个晚上都在尝试各种 PC、快速启动版本、电缆，甚至尝试切换启动插槽来尝试更新闪存，但就是不行。在我的例子中，一个问题是没有引导加载程序会刷新，即使是从侧面加载 OTA 失败，并出现状态 22 错误。不幸的是，即使使用新引入的 Fastboot 命令:“Unlock_Critical”也不起作用。

 <picture>![](img/ebf8b2fbc591d059e29774692427357e.png)</picture> 

Powershell is so much more pleasant to look at vs command prompt

闪存测试版、定制软件，甚至只是闪存恢复映像，是 Nexus 和 Pixel 程序对我们这样的爱好者如此有吸引力的部分原因，因此即使这些系统出现故障，也会令人不安。更麻烦的是 Ron 不能从引导装载程序中出来的问题，Pixel 的双分区系统应该有助于避免这个确切的问题。我们正在等待谷歌关于这些问题的消息，看看是否有已知的问题和解决方法可供我们这些有问题的人使用，并将相应地更新。

我们还不知道这是否是一个普遍的问题，或者这是一个硬件问题还是软件问题。与此同时，最好不要试图刷新工厂图像，而是坚持使用 [OTA 进行预计将于今天推出的预览程序](http://android.com/beta)，尤其是如果你使用 Pixel 2 的话。然而，一些 reddit 用户也报告说[甚至那些空中更新也无法](https://www.reddit.com/r/GooglePixel/comments/78z2n2/android_81_developer_preview_megathread/)安装，这可能指向一个更广泛和/或更严重的问题。如果 OTA 失败了，最好等着看谷歌是否会推出一个修订版，而不是尝试可能会失败的工厂镜像。

***将 8.1 图像闪烁到像素 2 是否有问题？请在评论中告诉我们！***