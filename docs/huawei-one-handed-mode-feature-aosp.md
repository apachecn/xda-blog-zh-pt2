# 华为的单手模式功能几乎进入了 AOSP

> 原文：<https://www.xda-developers.com/huawei-one-handed-mode-feature-aosp/>

**10/28/17**更新:如果你对一款能给任何设备带来单手模式功能的应用感兴趣(没有 root！)，那就来看看我们最新的 app: [单手模式](https://www.xda-developers.com/one-handed-mode-brings-apples-reachability-any-android-phone/)！

曾经有一段时间，4.7 英寸的显示屏被认为太大了。最初的三星 Galaxy Note 于 2011 年推出，许多消费者对这款“巨大”的 5.3 英寸设备的实用性持怀疑态度。今天，5.5 英寸显示器即使在预算价格范围内也很常见，5 英寸显示器的旗舰产品很难找到。

2017 年，随着 18:9 设备采用更高的显示屏纵横比，单手使用智能手机的问题变得更加严重。像 Galaxy S8、Galaxy S8+和 [Galaxy Note 8](https://www.xda-developers.com/galaxy-note-8-software-spen-apps/) 这样的手机和它们的前辈一样宽，但是要高得多。例如，Galaxy S8 的 5.8 英寸显示屏仅比 Galaxy S7 的 5.1 英寸显示屏略宽，但却高了很多。对于 LG V30、[小米 Mix 2](https://www.xda-developers.com/xiaomi-mi-mix-2-indian-launch-review/) 和谷歌 Pixel 2 XL 等 6 英寸 18:9 显示器，问题是你一只手无法够到显示器的顶部。虽然由于这些设备的宽度不变，在一些基本情况下单手使用是可能的，但这一点也不舒服。

这就是为什么原始设备制造商在他们的 rom 中增加了单手模式功能。三星从 2012 年开始在 TouchWiz / Samsung 体验中就有了单手模式。苹果在 2014 年为 iOS 添加了可达性。一些 LG 手机如 LG V20 也有单手模式。其他像小米、华为这样的 OEM 厂商也分别在 MIUI 和 EMUI 中加入了单手模式。

甚至谷歌也意识到了这个问题，这就是为什么它在新的 [Pixel Launcher](https://www.xda-developers.com/get-google-pixel-2-pixel-launcher-bottom-search-bar/) 上将持久搜索栏从主屏幕的顶部移到底部——但他们没有实现完整的单手模式功能。

单手模式并不局限于 Android 上的 OEM 皮肤。LineageOS 将他们对称为[“单手模式”](https://www.xda-developers.com/latest-lineageos-update-adds-single-hand-mode-and-more/)的特征的理解添加到定制 ROM 中。如果你想看它的动作，[看看这张 GIF](https://www.lineageos.org/Last-Week-in-LineageOS-4/) 。有趣的是，LineageOS 中的单手模式看起来和感觉都很像华为在 EMUI 中的单手模式。原因很简单:它实际上是基于华为的代码。更准确地说，**单手模式是基于华为试图贡献给 AOSP** 的开源代码。

华为[的一名员工负责编写提交](https://android-review.googlesource.com/#/q/huangbangbang%2540huawei.com)，这些提交[后来被合并到 linegeos 14.1](https://review.lineageos.org/#/q/status:merged+branch:cm-14.1+topic:oneHand)中。他在 2016 年 11 月和 12 月向 AOSP 上传了同样的提交。然而，在 2017 年 1 月，我们看到了关于 AOSP 代码审查的评论，这些评论表明该代码存在冲突，因此从未合并到 AOSP。具体来说，即使单手模式被禁用，当能够绘制其他应用程序的应用程序正在运行时，手动安装应用程序也是不可能的。在第二次提交上传后，一位评论者提请注意这个问题，即它不允许用户下载应用程序或接受某些应用程序的权限请求。

LineageOS 修改了代码，从而解决了问题，因此可以添加该功能。但对于 Android 的普通用户来说，很遗憾地知道，华为贡献给 AOSP 的代码从未被合并，也无法到达更多像谷歌 Pixel 2 XL 这样的设备。