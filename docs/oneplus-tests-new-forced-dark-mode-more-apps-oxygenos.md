# 一加为 OxygenOS 中的更多应用测试新的强制黑暗模式

> 原文：<https://www.xda-developers.com/oneplus-tests-new-forced-dark-mode-more-apps-oxygenos/>

# 一加为 OxygenOS 中的更多应用测试新的强制黑暗模式

一加正在测试 OxygenOS 的一项新功能，即使应用程序不支持，也可以让你在某些应用程序中强制使用黑暗模式。请继续阅读了解更多信息！

[全系统黑暗模式](https://www.xda-developers.com/android-q-beta-3-released/)一直是 Android 10 的亮点功能之一。[黑暗模式](https://www.xda-developers.com/tag/dark-mode/)是 Android 社区，尤其是 AMOLED 智能手机用户长期以来一直要求的功能。在谷歌采用之前，一些应用开发者已经独立地为他们的应用采用了黑暗主题；但随着谷歌全系统黑暗模式的推出，许多其他人抓住了这个机会，为他们的用户提供了一个替代的黑暗主题。但仍有一些人似乎对提供黑暗模式感到奇怪的犹豫，他们花了自己的时间来实现同样的模式([我们在看着你，WhatsApp](https://www.xda-developers.com/whatsapp-dark-mode-android-iphone/) )。尽管黑暗模式选项很受用户欢迎，但出于固执或冷漠，仍有一些应用程序继续以浅色主题为主。Android 10 还提供了一个选项，强制所有应用程序都使用黑暗主题，但这并不是所有应用程序的理想选择。因此，原始设备制造商不得不考虑为他们的用户提供有选择地强制执行这种模式的选项，而[一加](https://onepluscom.pxf.io/c/2233363/916678/12532?subId1=UUxdaUeUpU27716&subId2=exda&u=https%3A%2F%2Fwww.oneplus.in%2F)似乎也在朝着同样的方向发展，它在 OxygenOS 中为更多的应用测试了一种新的强制黑暗模式。

我们找到了字符串(h/t XDA 高级会员 [Some_Random_Username](https://forum.xda-developers.com/member.php?u=8234677) 为提示！)在为一加 7 和一加 7 Pro 发布的[最新 OxygenOS Open Beta 11](https://www.xda-developers.com/oneplus-7-pro-oxygen-os-open-beta-11-oneplus-7t-beta-2/) 的设置应用中。这些字符串表明，一加正在寻求为某些应用程序带来强制黑暗模式:

```
 <string name="oneplus_global_dark_mode_description">"Make apps that don't support dark theme also appear as dark tone. Some apps may not perform as expected, you can disable them in the list below."</string>
<string name="oneplus_global_dark_mode_only_valid_in_dark_mode">This feature is only available under dark tone</string>
<string name="oneplus_global_dark_mode_summary">Make more apps that do not adapt to dark mode turn into dark automatically when dark tone is turned on</string>
<string name="oneplus_global_dark_mode_title">Enable dark tone in more apps</string> 
```

我们设法显示了该功能的设置页面，但我们无法确定该功能将支持哪些应用程序。

这个特性背后的想法似乎与 DarQ 相似。DarQ 允许用户在每个应用程序的基础上启用 Android 10 的内置强制黑暗模式，所以你可以选择你希望变暗的应用程序。这可以让你在不能很好地适应强制深色主题的应用上保留浅色主题，同时仍然可以使那些适应强制深色主题但开发者还没有实现深色主题的应用变暗。我们希望看到该功能很快推出。