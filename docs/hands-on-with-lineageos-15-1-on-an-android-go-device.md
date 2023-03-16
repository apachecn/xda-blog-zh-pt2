# 在 Android Go 设备上实际操作 LineageOS 15.1

> 原文：<https://www.xda-developers.com/hands-on-with-lineageos-15-1-on-an-android-go-device/>

Project Treble 在定制 ROM 开发方面打开了许多大门，包括允许[晦涩、无内核的源设备运行 AOSP](https://www.xda-developers.com/obscure-mediatek-phone-kernel-source-android-oreo-project-treble/) 。所有你需要的是能够解锁引导加载程序，你可以在它上面启动一个 GSI。这正是我们对 [Blackview A20](https://www.xda-developers.com/blackview-a20-review-android-go/) Android Go 手机所做的。我们试用了由 XDA 知名开发商 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 移植的 linegeos Go[，结果令人惊讶。只要经过认证，一台设备应该可以很好地与 Project Treble 配合工作，但总会有一些问题需要解决。](https://www.xda-developers.com/unofficial-lineageos-15-1-android-go/)

## 基于 Android Go 的 LineageOS 15.1

首先也是最重要的，特性。正如你所料，一切都在这里。LineageOS 15.1 Android Go 版没有遗漏任何内容。我没有遇到任何附带功能的问题，*一切正常*。这对任何设备来说都是不可思议的。Android Go 是一个非常强大的操作系统，有许多 T2 的幕后优化让它在许多硬件上可行。[它的应用当然也能完成任务](https://www.xda-developers.com/android-go-apps-comparison/)。设备制造商[，至少现在](https://www.xda-developers.com/samsung-android-go-leaked-photos-ui/)，似乎坚持使用功能有点贫乏的安卓系统。这就是为什么 Android 通过一个通用的系统映像可以在你的手机上提供你需要的自由。

最让我感动的是一切都正常。相机工作，浏览工作，应用程序工作，所有 LineageOS 的功能工作。*几乎不存在任何问题*。如果你想知道你可以通过 LineageOS Go 访问哪些功能，你可以参考[这篇文章](https://www.xda-developers.com/lineageos-15-feature-list-overview-screenshots-video/)。总结最大的变化，有一些状态栏的调整，默认媒体音量控制，自定义强调颜色，等等。有很多定制选项，比现有的 Android 多得多。

但是性能呢？我们需要确保我们将获得的业绩至少与股票持平，因为这在很大程度上是一种承诺。很难找到一个股票系统映像，在安装了错误的 LineageOS Go 版本后，我不得不找到并使用它来拯救我的手机(稍后会详细介绍)。我运行了一个 Geekbench 4 基准测试，结果实际上令人惊讶。

现在，虽然与旗舰相比，结果可能很可怜，但这不是重点。这款手机由联发科 MT 6580M 驱动，这是一款在基准测试中一直得分很低的处理器。单核和多核分数实际上使这款设备成为采用该处理器的同类产品中的佼佼者。LineageOS 显然普遍承诺轻量级和快速的体验，但它能比现有的 Android Go 更轻量级吗？与其他设备相比，我对结果印象深刻，LineageOS 到目前为止看起来真的很好。但是实际的平滑度如何呢？

浏览 Aurora Store(Yalp 的一个 reskin)是一种有趣的体验。显然，对于这样的设备来说，它在图形方面非常沉重，但丢帧的数量令人震惊。谷歌 Chrome 的滚动功能还不错，设置和应用抽屉也不错。这不是最差的，也比库存好，但还是很差。

## 基于 Android Go 的 LineageOS 15.1 并非没有问题

我只遇到过一个问题，那就是关于 [Google Play 认证](https://www.xda-developers.com/how-to-fix-device-not-certified-by-google-error/)。这一变化是今年早些时候[推出的](https://www.xda-developers.com/google-blocks-gapps-uncertified-devices-custom-rom-whitelist/)，可能会让一些人感到头疼。我目前无法修复它，即使我提交了我的设备 ID。不过，我相信这只是一个奇怪的错误，在未来的版本中会得到修复。

*导航到为自定义 ROM 用户提供的 URL 需要一个 root 命令来获取设备 ID。*

据我所知，所有的硬件功能都工作得很好。有一些平滑的缺陷需要解决，但它肯定可以作为日常驱动程序使用。待机时间也很长，我也没有抱怨电池电量不足之类的问题。我确实对 phhusson 提供的 LineageOS Go (v5)的最新版本有问题，所以我使用了他的第一个版本(v4 ),效果很好。毫不夸张地说，他提供的第二个版本使我的手机成为我用过的最落后的手机。不管是什么原因，我不知道，但第一次构建运行良好。甚至屏幕亮度也可以改变，这是我在使用 Honor 9 Lite 时遇到的问题。然而，它缺乏自适应亮度。据我所知，其他一切都正常。

值得一提的是，它如此稳定的部分原因是 phhusson 使用了我现在用来移植 LineageOS Go 的相同设备。我们都在使用 Blackview A20，所以它在我的设备上运行良好并不奇怪。尽管如此，那些拥有其他 Android Go 手机的人(甚至那些只想从较低规格的手机中挤出性能的人)仍然可以使用它。应该不会有什么问题，它应该工作得很好。Project Treble 的整个想法是，rom 是通用的，所以如果制造商正确实施，它应该可以完美地工作。硬件特定的功能(如 OnePlus 6 的提醒滑块)将不起作用，但仅此而已。如果你想尝试一下，你可以在下面为你的 Android Go 智能手机下载 LineageOS Go！

* * *

[**LineageOS 15.1 安卓 Go**](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/lineage-phh-treble-t3767690)