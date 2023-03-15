# 有人正在对 Galaxy S8 的 LED View Cover 中使用的三星 Cover SDK 进行逆向工程

> 原文：<https://www.xda-developers.com/someone-is-reverse-engineering-the-samsung-cover-sdk-used-in-the-galaxy-s8s-led-view-cover/>

reddit 上的 */r/GalaxyS8* 子编辑的一名开发人员最近为他们的 [Galaxy S8](http://forum.xda-developers.com/galaxy-s8) 购买了一个 LED 视图盖，最终对其功能有点印象不足。开发者想知道为什么三星没有添加一些其他功能，并提到它可能会在未来更新。直到那时，他们才开始对 LED 图标编辑器和 LED 外壳服务应用程序进行逆向工程，以了解更多关于该系统的信息。

在浏览这些应用程序时， *fonix232* 表示，他们能够发现一些关于这种 LED 视窗盖如何工作的东西。首先，他们发现这款机箱实际上可以通过低功耗控制器进行固件更新。三星正在使用这个控制器来处理所有的图形，所以人们应该可以上传自己被黑的固件。然而，他们警告说，搞砸这一点可能会损坏 LED 观察盖。

他们还发现 LED View Cover 使用常规 NFC，但不确定他们如何能够解决 NFC 标签串扰，因为 NFC 读取器仍然可用。由于它使用了 NFC，他们认为该框架可以被移植到 AOSP，并有可能在 LineageOS 中实现。三星正试图保持锁定，这样你就必须使用原来的应用程序，到目前为止，它似乎不像股票固件将使用任何扩展功能。

三星正在使用一种专有格式的图像，因为他们使用的是. spr 扩展名。一些旧的视频游戏使用这种文件扩展名作为精灵，但这实际上是一种三星专有的格式，称为 SemPathRendering。这种特殊的盖子还可以检测顶部和底部的触摸，因此它不仅仅可以显示东西。底部有第二个 LED 显示屏，他们感觉有未使用的命令将数据发送到第二个显示屏。

如果你想投稿并了解更多，请查看下面的 Reddit 帖子！

[**来源:/r/GalaxyS8**](https://www.reddit.com/r/GalaxyS8/comments/6dvcv1/dev_reverse_engineering_the_samsung_cover_sdk/)