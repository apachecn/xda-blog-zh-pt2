# 如何(最终)改变三星键盘的滑动轨迹颜色

> 原文：<https://www.xda-developers.com/how-to-finally-alter-a-samsung-keyboards-swipe-trail-color/>

[定制主题的谷歌键盘](http://www.xda-developers.com/android/custom-themed-google-keyboards-for-any-mood/)一切都很好，因为第一方谷歌键盘随着 Android 的最后几次迭代确实突飞猛进。然而，一些设备，例如 [Galaxy Note II](http://forum.xda-developers.com/galaxy-note-2) ，预装了一个完全适合该设备的键盘，给了用户多种理由坚持使用 OEM 产品而不是第三方选项。

然而，从可定制性的角度来看，三星键盘有点麻烦。这并不是说普通键盘不能满足你的审美偏好——它当然可以，而且一直如此。然而，有一个改动让开发者和主题躲避了很长一段时间，那就是输入文本后留下的滑动轨迹。当然，那个小小的蓝色痕迹并不是最紧迫的问题，但我敢肯定，对于一个拥有完美主题键盘的人来说，它令人难以置信地讨厌。多亏了 XDA 认可了 主题[guntheral](http://forum.xda-developers.com/member.php?u=3824019)，那种难以捉摸的价值现在已经被追寻到了，他已经给其他人留下了如何效仿的指示。

需要对包含在键盘 APK 文件本身中的 Smali 进行调整，使用诸如 [VTS](http://www.xda-developers.com/android/updates-to-virtuous-ten-studio-and-remote-theme-injector/) 之类的工具很容易访问该文件。Note II 和 Note 3 的论坛主题中清楚地列出了所有需要对代码进行的更改，以及一些关于颜色代码的建议。如果你正在寻找键盘主题的润色，或者如果你正在寻找一个简单快捷的小编辑入门，那就去看看吧。