# 如何立即在 Android 上启用 YouTube 黑暗模式

> 原文：<https://www.xda-developers.com/enable-youtube-dark-mode-android/>

# 如何立即在 Android 上启用 YouTube 黑暗模式(Root)

谷歌为 YouTube 应用程序添加了一个黑暗模式，但它还不适用于 Android。如果你有 root 权限，你现在可以在 YouTube 应用中进入黑暗模式。

谷歌最近[在 YouTube 移动应用](https://www.xda-developers.com/youtube-app-dark-mode-android/)中添加了一个黑暗模式(紧随桌面网站的黑暗模式)，但只有一个问题:iOS 用户先得到它。黑暗模式仍然是“即将到来”的 Android，我们并不确切地知道需要多长时间。好消息是 Android 开发者社区又一次帮助了我们。如果你在 Android 设备上有 root 权限，你现在就可以在应用程序中进入黑暗模式。

**2018 年 6 月 29 日**更新:距离这篇文章最初发表已经过去了 3 个多月，黑暗主题仍然没有正式提供给 Android 用户。然而，启用黑暗主题的标志已经改变，所以我们更新了这篇文章。

此方法需要修改应用程序数据文件夹中共享偏好设置文件夹的值。这就是为什么 root 访问是必要的。如果您的设备还没有根，请查看您设备的论坛以获取说明。一旦你有了 root 权限，你就需要 Preferences Manager 应用，当然还有 YouTube。

以下是如何做到这一点:

1.  从谷歌 Play 商店安装偏好设置管理器。
2.  在列表中找到 **YouTube** 。(如果它没有出现，您可能需要在菜单中启用“显示系统应用程序”。)
3.  轻按它以打开其偏好设置文件。
4.  你应该在 **youtube.xml** 上。如果不是，向左/向右滑动直到你是。
5.  搜索**黑暗**
6.  将两个值从**假**更改为**真。**
    *   如果看不到数值，手动添加( **app_theme_dark_developer** 和 **app_dark_theme** )并设置为**T5【真**
7.  保存更改。
8.  强制关闭 YouTube。

当你再次打开应用程序时，它应该处于黑暗模式。该应用程序将有一个漂亮的深灰色背景和黑底白字图标。你可以在没有炫目的白色界面的情况下浏览视频。感谢 XDA 成员 [AL_IRAQI](https://forum.xda-developers.com/member.php?u=4648515) 发来这个方法并提供截图。