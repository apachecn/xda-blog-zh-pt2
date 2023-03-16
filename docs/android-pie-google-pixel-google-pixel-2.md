# Android Pie 是为 Google Pixel & Google Pixel 2 准备的

> 原文：<https://www.xda-developers.com/android-pie-google-pixel-google-pixel-2/>

Android P 似乎并没有存在太长时间，但第一个开发者预览版大约在 5 个月前下降了。在此期间，谷歌已经发布了 4 个 Android 测试版更新。这是谷歌迄今为止最大的版本更新之一。他们引入了大量新功能和改进。在上一次开发者预览版之后，人们普遍预期 Android P 将在本月完成最终版本，现在这一天已经到来。安卓 9.0 派终于正式了。

## 为谷歌 Pixel 和谷歌 Pixel 2 下载 Android 9 Pie

[**安卓派工厂图片**](https://developers.google.com/android/images) [**安卓派 OTA 图片**](https://developers.google.com/android/ota)

## Android 9 Pie 有什么新功能？

我们已经检查了每个 Android P Beta 版本中的所有新功能和变化。你可以看看我们下面的“Android P 中的所有新东西”的深入列表。

让我们回顾一下 Android 9 Pie 中的一些重要亮点。

### 手势导航

*自从这些 gif 创建以来，用户界面已经得到了改进*

手机正朝着更加基于手势的导航方向发展，谷歌也在追赶这一趋势。Android Pie 手势不像大多数其他手机那样工作。屏幕底部还有一个导航栏。home 键现在是药丸形状，可以向上滑动或左右滑动。向上滑动可以打开最近的应用切换器，也可以从任何地方打开应用抽屉。快速向左滑动将转到上一个应用程序，或者你可以来回滑动药丸来滚动所有最近的应用程序。

### 最近应用切换器

为了配合新的手势，Android Pie 为最近的应用程序提供了全新的用户界面。应用程序窗口的垂直通讯录已经一去不复返了。新的用户界面是一个水平列表，窗口不重叠。这让你更容易看到你在应用程序中做了什么。长按应用程序图标也更容易启动分屏模式。如果你使用股票启动器，你也可以在最近应用用户界面中找到一个应用停靠和搜索栏。

### 新材料设计

Android 的很多外观都进行了视觉上的更新。它的官方名称不是“材料设计 2”，但它显然是一个新的外观。从设置到通知阴影的一切都已刷新。这种新的外观与谷歌的新设计以及他们的许多 Android 应用程序相匹配。

### 数字福利和切片即将推出

谷歌关于 Android P 的 IO 展示中很大一部分是一个名为“数字福利”的新功能。奇怪的是，数字福利就是帮助用户少用手机。谷歌包括了一套新的工具来帮助人们摆脱手机。数字福利将于今年秋季面向非测试版用户推出。[你可以在这里报名](https://android-developers.googleblog.com/2018/08/introducing-android-9-pie.html)。

切片是一种在另一个应用程序中显示应用程序交互片段的方式。切片是一个交互式片段，显示应用程序外部的应用程序内容。谷歌展示的例子是寻找一个 Lyft。你只需在谷歌中搜索“Lyft ”,就会看到 Lyft 应用程序的搜索结果。当你点击这些结果时，它将直接启动应用程序中的那个动作。这将会节省你进入和退出应用程序的时间。非测试版用户也要到秋季才能获得 Slices。

## 如何在谷歌 Pixel & Pixel 2 上安装 Android 9 Pie

### OTA 图像说明

1.  为您的设备下载 OTA 图像
2.  将其移动到设备的内部存储器中
3.  如果你还没有设置好 [ADB](https://www.xda-developers.com/install-adb-windows-macos-linux/) ，请确保你已经设置好了
4.  使用以下命令重新启动以进行恢复:`adb reboot recovery`
5.  选择“应用亚行更新”选项
6.  使用以下命令加载 OTA:`adb sideload <OTA_image.zip>`

### 工厂图像说明

1.  为您的设备下载工厂映像
2.  在您的电脑上解压缩工厂图像压缩文件
3.  如果你在 Windows 上运行 flash-all.bat，或者如果你在 Mac/Linux 上运行 flash-all.sh。这将擦除您设备上的所有数据！如果您想在不丢失任何数据的情况下刷新更新，请[遵循这些说明，而不是](https://www.xda-developers.com/flash-monthly-security-update-google-pixel/)。