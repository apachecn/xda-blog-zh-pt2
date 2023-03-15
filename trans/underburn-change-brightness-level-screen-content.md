# Underburn 是一款根据屏幕内容改变亮度级别的应用程序

> 原文：<https://www.xda-developers.com/underburn-change-brightness-level-screen-content/>

多年来，自动亮度功能已经出现在几乎所有的 Android 设备上。在 Android 5.0 Lollipop 之前，[自动亮度](https://www.xda-developers.com/tweak-the-automatic-brightness-levels-on-your-desire/)功能会根据环境光传感器的读数来改变手机的亮度，但快速的缩放很麻烦。Android Lollipop 的自动亮度演变为自适应亮度，它将自动亮度与用户手动设置的亮度水平相结合，因此亮度水平通常保持在用户希望的水平附近。

Android 的自适应亮度多年来一直运行良好，其算法也经历了几次调整。有一些像 [Lux](https://play.google.com/store/apps/details?id=com.vitocassisi.luxlite) 这样的应用程序可以让你自己调整自动亮度曲线，但很少有人敢偏离依赖环境光传感器的可靠的自动亮度算法。这正是一款名为 **Underburn** 的新应用所做的。它重新想象了你的设备的亮度水平的计算方式，以努力改善你的深夜 Reddit/insta gram/脸书会话。

Underburn 是由 XDA 资深会员 [out386](https://forum.xda-developers.com/member.php?u=6015092) 开发的，他好心地向我们提供了一些关于他的申请的细节。欠烧背后的概念非常简单:它不是根据环境光线条件改变亮度，而是根据屏幕内容改变亮度**。**

想象一下，你躺在床上用手机或平板电脑。你已经使用底层在你的设备[上设置了](https://www.xda-developers.com/andromeda-substratum-custom-themes-oreo/)[黑暗主题](https://www.xda-developers.com/install-dark-theme-android-oreo-without-root/)，所以你的大多数应用程序都是舒适的黑暗。然而，并非每个应用程序都可以有主题，所以如果你遇到一个必须在谷歌浏览器中打开的链接，当页面打开时，你可能会经历短暂的眩目白光。然后继续受苦，因为整个页面背景通常是明亮的白色。

欠烧正是为了解决这个问题而开发的。如果出现以白色为主的屏幕，屏幕将变暗，以避免夜间使用智能手机时眼睛疲劳。相反，如果一个黑暗的图像出现，亮度会稍微提高，以便可以舒适地阅读。该应用程序通过使用 Android Media Projection API 每秒拍摄 4 张截图，然后分析每张图像的点的颜色值，来识别屏幕何时以白色或黑色为主。

从表面上看，这似乎相当耗费电池，但开发者向我们保证，所涉及的处理只需要很少的 CPU 时间，并且在屏幕关闭时不会保持唤醒锁。性能影响也应该很小。该应用程序不需要 root 权限，所以只要你的设备在 Android 5.0+上，每个人都可以利用它。请记住，虽然这个应用程序主要是为了延长夜间使用，并不意味着完全取代您的手机的自适应亮度功能。

*显示设置和选项的欠烧截图*

这个应用程序有 4 个亮度等级，第 5 个将在未来的更新中添加。用户只需设置其中的两个，最低和最高水平，而应用程序将动态计算其他 2。

如果你想尝试一下，这款应用可以在谷歌 Play 商店上买到，价格为 0.99 美元，没有隐藏的应用内购买或订阅。该应用程序使用了运行所需的最低限度的权限，甚至不使用分析，也不需要互联网访问权限。

[app box Google play com . out 386 . underburn]