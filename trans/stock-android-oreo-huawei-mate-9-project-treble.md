# 由于 Project Treble，我在华为 Mate 9 上启动了 Android Oreo

> 原文：<https://www.xda-developers.com/stock-android-oreo-huawei-mate-9-project-treble/>

就在今年谷歌 I/O 的一周前，谷歌公布了对安卓操作系统框架最根本、最底层的改变之一: [Project Treble](https://www.xda-developers.com/googles-project-treble-modularize-android-so-oems-can-update-devices-faster/) 。Project Treble 将 Android OS 框架模块化，使其与供应商代码分离，允许原始设备制造商开发新的软件更新，而不必等待供应商(如高通)更新他们的代码。作为供应商测试套件(VTS)的一部分，所有支持三重功能的设备必须能够引导一个[原始、通用 AOSP 版本](https://www.xda-developers.com/project-treble-custom-rom-development/)。任何搭载 Android Oreo 的设备都需要 Project Treble 支持，因此，尽管有几款设备符合这一标准，但没有人测试过我们是否真的可以直接从源代码编译 ROM。但最终，由于 Project Treble 的支持，我能够在华为 Mate 9 上启动一个普通的 AOSP 制造的 Android 8.0 Oreo ROM(T4)。

你在上面看到的是 AOSP 安卓 8.0 奥利奥在华为 Mate 9 上运行的截图。华为 Mate 9 于去年[发布](https://www.xda-developers.com/android-oreo-emui-6-huawei-mate-9/)，搭载安卓 7.0 牛轧糖。特别是，它在顶层运行一个名为 Emotion UI 的自定义皮肤。与你可能在谷歌 Pixel 手机上找到的东西相比，它的软件非常不同。

目前，该设备还没有公开的 Android 8.0 Oreo 版本。我们上个月早些时候获得的一个泄露的 Android Oreo 版本显示，华为确实在努力满足 Project Treble 的要求，尽管它[没有推出 Android 8.0](https://www.xda-developers.com/project-treble-android-o-exist-flagship/) 。Mate 9 的软件与现有的 Android 有很大不同，这使得它成为测试 Project Treble 是否真的允许我们将现有的 Android Oreo 引导到任何支持 Treble 的设备上的完美候选。

## 在支持三重功能的设备上引导库存 Android Oreo

最近，我们的基本手机论坛[上的一个成员发了一个帖子](https://forum.xda-developers.com/essential-phone/development/dev-using-project-treble-to-boot-t3705253)来看看他们的手机是否能启动通用的 AOSP 奥利奥版本。Essential 手机本身刚刚在 Project Treble 的支持下获得了 Android 8.0 的第一个正式测试版，所以它看起来似乎是可信的。XDA 资深成员 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) ，因其在[开源超级用户分叉](https://forum.xda-developers.com/android/software-hacking/wip-selinux-capable-superuser-t3216394)上的工作而闻名，准备接受挑战。由于谷歌出于认证目的与原始设备制造商共享的原始 AOSP 构建并不公开，phhusson 不得不构建自己的通用 AOSP 映像，并找到测试人员在他们的设备上进行测试。

尽管取得了进展，但还没有人成功地将 AOSP 的版本安装到他们的基本手机上。我决定在我的华为 Mate 9 上试一试，它完全符合 Project Treble 的要求。由于 Android Oreo 在 Mate 9 上没有公开，我使用了 [FunkyHuawei.club](https://funkyhuawei.club/) 服务将 Mate 9 上的固件更新为 Oreo 的封闭测试版。

 <picture>![Huawei Mate 9 Project Treble](img/cde84182eb873b9188d371477abd7ede.png)</picture> 

Snippet from /vendor/manifest.xml on the Mate 9

在大量的用户数据分区擦除、系统映像刷新和日志转储之后，我们终于在 Mate 9 上启动了通用的 8.0 版本。我们**也没有做任何内核修改**来让它启动。这不仅是**第一次华为 Mate 9 设备启动 AOSP ROM** ，也是第一次有人在谷歌和原始设备制造商之外测试 Project Treble-enabled 设备是否真的可以启动通用 AOSP 版本。

不过，在你兴奋之前，这个构建还不完美。一堆应用程序现在崩溃了，可能是由于一些解密错误，但我相信经过一点工作就可以解决。事实上，AOSP 8.0 奥利奥在所有设备中的华为 Mate 9 上启动，这本身就是一个奇迹。一旦我们的新**项目 Treble Device Development forum**开放，我们将完善这项工作并寻求开发者的投入，因此如果你对这种开发感兴趣，请继续关注这方面的新闻。

## 结论

关于 Project Treble 将在多大程度上帮助加快智能手机的软件更新，有很多猜测。原始设备制造商推出软件更新的当前过程[相当漫长](https://www.xda-developers.com/how-android-software-update-sony/)，尽管 Treble 加快这一过程很好，但我们还没有看到这种情况发生。不过，这很有意义，因为只有少数设备支持 Project Treble，我们需要等到 Android P 发布后才能真正看到 Treble 对整个 Android 生态系统的好处。

但由于 Project Treble 的认证测试要求，设备制造商被要求发运可以启动通用 AOSP 版本的设备。直到今天，还没有人测试这在现有的高音设备上是否可行。然而，现在我们已经证明了这种可能性存在于华为 Mate 9 上，我们希望打开基于三重功能设备的定制 ROM 开发的闸门。

* * *

## 更新:视频演示几乎完全正常工作的奥利奥

我们发表了一篇后续文章，详细解释了什么是 Treble 项目，以及为什么它对定制 rom 如此重要。我们在视频中展示了一个 Android Oreo ROM，它在华为 Mate 9 上基本上功能齐全。我们还宣布了一个新项目 Treble forum 的开幕。点击此处查看[后续文章，了解所有细节](https://www.xda-developers.com/how-project-treble-revolutionizes-custom-roms-android-oreo/)。