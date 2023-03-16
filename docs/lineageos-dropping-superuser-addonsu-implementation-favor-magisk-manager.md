# LineageOS 正在放弃自己的超级用户实现，使 Magisk 成为事实上的解决方案

> 原文：<https://www.xda-developers.com/lineageos-dropping-superuser-addonsu-implementation-favor-magisk-manager/>

LineageOS 是 Android 设备上最受欢迎的定制 ROM 之一，如果不是最受欢迎的定制 ROM 的话。这个定制的 ROM 采用了 Android 开源项目(AOSP)中的 Android，并在其上添加了自己的特色。许多定制 ROM 倾向于采用 LineageOS 作为自己的基础，因此 LineageOS 为自己进行的任何重大更改都倾向于在整个定制 ROM 社区中传播。LineageOS 背后的开发人员意识到了这种影响，并据此做出明智的决策。LineageOS 即将发布的版本极大地改变了根访问的处理方式，因为 ROM 放弃了对自己的 addonsu 二进制文件的支持，转而支持 Magisk。

LineageOS 的下一个主要版本将被称为 LineageOS 17，这里没有任何惊喜。自定义 ROM 正在基于 Android 10 的基础上重新开发。尽管是一个定制的 ROM，因此比 OEM UX 皮肤具有更大的灵活性，LineageOS 选择不预装根二进制文件——这意味着应用程序无法在全新安装的 ROM 上获得超级用户访问权限。为了让应用程序请求超级用户访问，用户必须有意识地安装超级用户二进制文件和超级用户管理器。大多数用户默认安装 Magisk 和 Magisk Manager，主要是因为 Magisk 针对 SafetyNet 检测提供了变通方法，以及 Magisk 模块的易用框架。

尽管是流行的选择，LineageOS 并没有正式推荐 Magisk 作为首选的生根解决方案。一些无知的用户最终在他们的设备上安装了不兼容的 Magisk 模块，然后向 ROM 维护人员大量报告错误行为——这对维护人员来说绝对是一个头疼的问题。相反，ROM 依靠自己的 [addonsu 包](https://www.xda-developers.com/addonsu-packages-lineageos-15-1/)来提供超级用户二进制文件和一个简单的超级用户管理器。

LineageOS 15.1 和 [LineageOS 16 版本](https://www.xda-developers.com/lineageos-16-android-pie/)中提供了这个 addonsu，但在官方 LineageOS 17、[中，将不再提供这个功能](https://review.lineageos.org/c/LineageOS/android_device_lineage_sepolicy/+/257100)。在这个版本中，[通过 ADB](https://review.lineageos.org/q/topic:%22ten-adbroot%22+(status:open%20OR%20status:merged) 的 root 访问将成为官方支持的用户在设备上处理重要文件的方式。如果用户想授予 apps 超级用户权限，那么他们必须安装 Magisk 和 Magisk Manager。虽然 LineageOS 仍然没有通过将 Magisk 合并到官方版本中来正式支持它，但 addonsu 的降级实质上提升了 Magisk 成为事实上受支持的解决方案。

但是为什么 LineageOS 要放弃 addonsu 呢？这是因为 addonsu 利用的 LineageOS 功能 PrivacyGuard 在 LineageOS 17 中也被删除了。PrivacyGuard 为用户提供了先进的权限管理控制，可以在现有的 Android 上实现。LineageOS 团队无法将 PrivacyGuard 框架移植到新的 Android 10 基础上，相反，该团队正在 Android 10 中利用谷歌自己的权限中心功能。这个权限中心功能是[相同的权限控制，我们在早期泄露的 Android Q 版本](https://www.xda-developers.com/android-q-dark-theme-desktop-mode-permission-revamp/)中看到过，但在公开版本中没有。谷歌没有在 Android 10 中发布这项功能，但它的代码仍然存在于 AOSP。LineageOS 已经将它分叉，并将它作为 PrivacyGuard 的替代方案。