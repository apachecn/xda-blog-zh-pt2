# 谷歌购物测试谷歌镜头快捷方式，并为 AR 项目预览和黑暗模式做准备

> 原文：<https://www.xda-developers.com/google-shopping-tests-google-lens-shortcut-ar-previews-dark-mode/>

Google Play Services for AR(以前称为 [ARCore](https://play.google.com/store/apps/details?id=com.google.ar.core&hl=en_US) )是该公司的增强现实体验平台。你可以用 AR 做很多有趣的事情，但最实际的用途之一是在你的物理空间中看到物体。谷歌购物可能正在准备这样一个功能，以及黑暗模式和谷歌镜头快捷方式。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前还没有在 live build 中实现，可能会在未来的版本中随时被 Google 拉出来。

在 Android 的 Google Shopping v52 中，我们发现了两个新的资产，建议支持在 AR 视图中预览项目。第一个资产被命名为“quantum _ IC _ view _ in _ ar _ new _ white ”,它描绘了一个类似谷歌镜头的盒子中的 3D 立方体。第二个资源被命名为“视图 _ 三维 _ 背景”

我们认为，这里的想法是，你可以在购买之前，在你的物理空间查看产品，如家具。这使用户对物体的比例有了更好的了解。当我们去年发现 [AR 购物功能时，它们是谷歌 Pixel 手机的 Playground 应用程序的一部分。由于新发现的资产来自谷歌购物应用程序，该功能将为更多人所用。](https://www.xda-developers.com/google-pixel-ar-google-shopping-hands-on/)

接下来有证据表明，谷歌购物应用将进入黑暗模式。Google 最近在 values-night 下添加了一个 colors.xml 资源文件。“values-night”中定义的资源在 Android 的全系统黑暗模式启用时使用。颜色资源文件夹还包括暗模式和亮模式的主要文本颜色的文件。

最后，我们激活了一个隐藏设置，在谷歌购物搜索栏中放置一个谷歌镜头快捷方式。正如你所料，点击这个会打开谷歌镜头中的“搜索”模式。这可能已经在应用程序中存在了一段时间，但它仍然不是实时的。

如上所述，AR 相关的资产似乎是谷歌购物 v52 中的新内容，但黑暗模式文件和谷歌镜头图标之前就已经存在了。希望我们能很快看到这些东西上线。