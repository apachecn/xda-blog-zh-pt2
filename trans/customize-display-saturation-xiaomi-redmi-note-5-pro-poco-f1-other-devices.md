# 在小米 Redmi Note 5 Pro、Poco F1 和其他设备上自定义显示饱和度

> 原文：<https://www.xda-developers.com/customize-display-saturation-xiaomi-redmi-note-5-pro-poco-f1-other-devices/>

显示屏是智能手机的基本组成部分。现在任何现代手机都需要一个大显示屏。根据分辨率、亮度、黑电平、视角和色彩准确度来判断显示质量。色彩精确度是一个广义的术语，包括灰度精确度和灰度精确度、饱和度精确度和色域精确度。谷歌去年用 Android Oreo 做了一次大的推动，这是第一个支持颜色管理的 Android 版本。不幸的是，Android Oreo 的色彩管理系统迄今为止只被少数设备制造商采用。即使在谷歌 Pixel 2 上，一些用户也希望有更多的灵活性，而不是必须从自然、增强和饱和等颜色配置中进行选择。他们想要一种在更低水平的基础上调整显示饱和度的方法。

事实证明，[谷歌 Pixel/XL 和谷歌 Pixel 2/XL 的根用户事实上可以更灵活地改变显示饱和度](https://www.xda-developers.com/custom-saturation-level-google-pixel-2/),而不是只能从自然、增强或饱和的颜色中进行选择。可以使用终端命令来设置 0.0 和 2.0 之间的值，其中 0.0 将颜色设置为黑色和白色，而 2.0 将颜色设置为 100%饱和度。

接着，XDA 论坛版主[zachare 1](https://forum.xda-developers.com/member.php?u=7055541)开发了一款名为“Sa2ration”的开源 app，让用户可以轻松更改显示饱和度值。这消除了用户使用终端命令的需要。应该指出的是，该应用程序不会影响 gamma 值(用户可以刷新一个支持 KCAL 的自定义内核，如果它可用的话)。

我们为 Pixel 用户开发了这款应用，但 XDA 论坛上的用户开始报告说，它可以在基于 MIUI 的小米设备上工作，这些设备采用 Android 8.1 Oreo 和更高版本。我们能够确认它在根植的小米 Redmi Note 5 Pro 和根植的小米 Poco F1 上工作，这两款产品都是基于 Android 8.1 Oreo 之上的 MIUI 9。Redmi Note 5 Pro 和 Poco F1 已经配备了颜色配置文件(自动提供三种色温预设；对比度增加；以及通常以 sRGB 色域为目标的标准配置文件)，但 Sa2ration 应用程序在饱和度方面为用户提供了更细粒度的控制。

应该注意的是，将显示饱和度设置得太高或太低都会使手机的显示相对于 sRGB 色域不准确(值得注意的是，因为大多数小米手机上的标准颜色配置文件都是根据 sRGB 校准的)，但一些用户实际上*更喜欢*饱和色，这个应用程序也允许他们拥有他们想要的颜色。

Sa2ration 应用程序可以通过 XDA 实验室和谷歌 Play 商店下载。提醒一下，使用这个应用程序的唯一先决条件是用户**必须有根用户**。在小米手机上有 root 就是申请 bootloader 解锁，解锁 bootloader，然后闪 Magisk。它可能会也可能不会在每一个根 Android 8.1 或更新的设备上工作，例如，它不能在运行 Android Pie 的 OnePlus 6 上工作。