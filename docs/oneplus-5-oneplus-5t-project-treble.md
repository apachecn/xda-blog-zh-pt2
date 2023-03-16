# OnePlus 5 和 OnePlus 5T 非正式获得 Project Treble 支持

> 原文：<https://www.xda-developers.com/oneplus-5-oneplus-5t-project-treble/>

高音项目是近年来最令人兴奋的发展之一。Android 工作方式的低层次重新架构仍有许多变化(当完整的 Android P 发布时，我们会看到许多关于这方面的信息)，但它已经在基于 AOSP 的定制 ROM 开发中引发了某种形式的“T0”革命。这是因为高音支持允许设备[刷新基于 AOSP 的通用系统映像](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/) (GSI)，并且在未来将更容易升级到新版本的 Android。我们已经看到一些[设备非正式地获得高音支持](https://www.xda-developers.com/list-android-devices-project-treble-support/)，OnePlus 5 和 OnePlus 5T 是该列表中的最新产品。

此前，一加(和诺基亚)表示，他们[将无法更新他们现有的支持三重功能的智能手机阵容](https://www.xda-developers.com/why-current-oneplus-nokia-phones-wont-be-project-treble-certified/)。这是因为他们现有的设备缺乏专用的供应商分区，并且这些公司认为通过 OTA 更新进行重新分区不是他们想冒险做的事情。然而，在 OnePlus 5 和 OnePlus 5T 上实际上有一个未使用的 1.5GB 分区，名为“last_parti”，开发人员已经[测试了](https://review.lineageos.org/c/LineageOS/android_device_oneplus_msm8998-common/+/205186)，将它变成了一个临时的供应商分区(实际上你只需要重命名它。)现在，另一位开发者已经拿到了这个脚本，并完成了“tre 伯利兹”最新一加旗舰设备所需的其余工作。

这位名叫 XiNGRZ 的开发者是 Mokee ROM 团队的一员，他所做的[承诺](https://mokeedev.review/q/topic:%22op5-treblize%22+(status:open%20OR%20status:merged))展示了他是如何将 OnePlus 5 和 5T 进行 tre 伯利兹化的。正如[在他的 XDA 帖子](https://forum.xda-developers.com/project-treble/trebleenabled-device-development/discussion-guide-oneplus-5-5t-t3776358)中所解释的，他运行脚本从那个未使用的分区创建供应商分区，从/system/vendor 中移走所有 Hal，并且由于一加在最新的 OxygenOS Open Betas 中对所有 Hal 进行了 binderizing，他能够使设备三倍兼容。[做了这个](https://bbs.mokeedev.com/t/topic/5460)，他能够启动一个[复活混音 GSI](https://www.xda-developers.com/lineageos-15-1-resurrection-remix-available-project-treble/) ，正如他在他的[微博](https://m.weibo.cn/status/4227335836127198)账号上显示的。

由于这项工作，如果你为 OnePlus 5 ( [下载此处](https://download.mokeedev.com/?device=cheeseburger))或 OnePlus 5T ( [下载此处](https://download.mokeedev.com/?device=dumpling))闪存最新的夜间版本，你的设备将非正式地成为 Project Treble 兼容设备。在你这样做之后，你就可以选择[刷新任何目前可用的 GSI](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/) ，这包括 XDA 认可的开发者 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 的纯 AOSP，LineageOS 15.1，或者复活混音 rom(如上图)。我们论坛上的一位用户，XDA 资深会员 [Yousvel](https://forum.xda-developers.com/member.php?s=38383ed638623473652b3dadbc661b05&u=5684962) ，已经[展示了这一点](https://forum.xda-developers.com/oneplus-5/development/pure-aosp-booted-oneplus-5-via-phh-t3776392)。

**我们的观点:**这可能不会对现有的 OnePlus 5 和 5T 用户产生巨大影响。当一加公司宣布他们不会用三倍支持更新他们的设备时，引起了很多人的愤怒，然而，这些愤怒大部分是错误的。对于一加的设备，已经有一个健康的开发者社区围绕着他们，已经有多种基于 AOSP 的 rom 可供使用。

Treble 对定制 ROM 社区的好处在很少或没有开发者场景的设备上更容易看到，例如华为/Honor 手机或 Razer 手机等受众较少的手机。虽然很高兴在一加设备上看到这样的开发工作，但这并不意味着场景依赖于它。此外，随着对 Android P 的更改(完成版本化 VNDK 的工作)，在它面向未来之前，仍需要对这个三重“端口”进行工作。

最后，虽然高音支持可能会影响一加更新设备的速度，但不能保证一定会。这两款设备最近都更新了四月份的安全补丁，所以似乎决定这些设备更新速度的唯一因素就是一加本身。一旦 [Android P](https://www.xda-developers.com/android-p-developer-preview-1-google-pixel-xl-pixel-2-xl/) 更广泛可用，我们将看到高音支持是否会与[即将到来的 OnePlus 6](https://www.xda-developers.com/oneplus-6-name-confirmed-coming-with-256gb-storage-version-and-possibly-special-avengers-infinity-war-model/) 有所不同。