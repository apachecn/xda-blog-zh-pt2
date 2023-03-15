# 如何修复 Android 8.1 奥利奥上的锁屏滑动手势问题

> 原文：<https://www.xda-developers.com/fix-lock-screen-swipe-gesture-issues-android-81-oreo/>

Android 8.1 是 Android 期待已久的 Android Oreo 更新的第一个维护版本，现在已经发布了一段时间，至少适用于 Google Pixel 和 Nexus 设备。然而，一些运行 Android 8.1(无论是官方版本还是定制 ROM)的谷歌 Pixel 和 Nexus 用户已经注意到，锁定屏幕上的滑动手势，如访问快速设置切换、滑动解锁或滑动取消通知，已经变得相当困难，至少与 Android 8.0 相比。一些用户报告说，现在锁定屏幕上的滑动手势需要几乎整个屏幕范围的滑动。我们已经报道过这个，它似乎影响了许多运行 Android 8.1 软件的用户。

一个潜在的原因是由 XDA 知名开发商 [AdrianDC](https://forum.xda-developers.com/member.php?u=2233641) 发现的[:这是由系统用户界面中一个新的“防伪造功能”引起的，该功能旨在防止设备在你的口袋或手中时意外滑动解锁。然而，这种反虚假功能可能是用户一直存在的滑动手势问题的原因，因此一些定制 Android 8.1 Oreo ROMs 的开发者选择禁用它。](https://review.lineageos.org/#/q/I0c2590f56e2cf6d6cd4ff3af2341a985670168e3)

如果你在谷歌 Pixel & Pixel XL、Pixel 2 & Pixel 2 XL、Nexus 5X 和 Nexus 6P 上运行的是 stock Android 8.1 Oreo，那么这个功能在你的设备上是默认启用的。感谢 Android Oreo 中添加的[原生底层支持](https://www.xda-developers.com/andromeda-substratum-custom-themes-oreo/),我能够创建一个覆盖来禁用这个反伪造功能，并且它不需要 root 来安装！

* * *

## 如何修复 Android 8.1 奥利奥上的锁屏滑动手势问题

如果你还没有，你需要在你的设备上设置底层主题引擎。如果你的设备运行的是 Android 8.0，Android 7.1 或 Android 7.0，那么我的 mod 对你来说完全没有意义，因为这个问题是最新的 Android 8.1 版本所独有的，其中增加了防错功能。

1.  为了在你的设备上正确设置 sub tum 和 Andromeda，请按照本教程进行操作。
2.  [下载我的叠加图](https://www.androidfilehost.com/?fid=817906626617958393)。这是一个简单、轻量级的底层主题，它在 SystemUI 中将反伪布尔值设置为 false。
3.  打开底层，选择我的主题，应用系统界面覆盖。
4.  如有必要，重新启动 SystemUI 以查看更改。您应该会看到锁定屏幕上滑动手势的灵敏度提高了。

*选择“奥利奥锁屏修复”主题，选择 SystemUI 叠加，选择“编译并启用”。*

## 说明

随着 Android 8.1 的推出，谷歌在 AOSP 的主要分支机构引入了一种先进的锁屏防错分类器。这个分类器所做的是使滑动手势更具阻力，以避免意外解锁设备，拉出模式/PIN 解锁屏幕，滑动或打开通知，*等等*。然而，增加的阻力被证明是一种负担，而不是一种改善，至少对一些用户来说是这样，因为与 Android 8.0 和更低版本中的先前行为相比，大多数手势都需要边到边的运动。

这种高级反假分类器在设备的 SystemUI 中定义为布尔值，在 AOSP Android 8.1 中设置为 true。我的覆盖所做的只是简单地将名为“config _ lock screen antifalsingclassifierenabled，的布尔值设置为 false，恢复之前的 Android 8.0 锁屏行为。这个 mod 的初始测试缓解了运行 Android 8.1 的 Google Pixel 和 Nexus 手机上的问题，但由于布尔值在 AOSP 上设置为 true，这个覆盖也可能缓解了一些 AOSP 定制 rom 上的问题。这一修复也在小米 Redmi Note 4 等运行定制 Android 8.1 软件的设备上进行了测试。

少数定制 ROM，如 LineageOS 15.1，已经将这个布尔值设置为 false，所以如果您选择的 ROM 合并了这个更改，您应该不会注意到任何问题。这个 mod 主要是为了解决股票 rom 和某些自定义的问题，所以我们强烈建议你尝试一下，并在评论中给我们反馈！如果它不像你期望的那样工作，或者你看到任何与覆盖相关的错误，请通过我的 Twitter 个人资料联系我，我在我的作者简介中链接了该个人资料，或者给我发电子邮件。

***特别感谢 [/r/AndroidApps 社区](https://www.reddit.com/r/androidapps/)帮助我完成了初始测试！***