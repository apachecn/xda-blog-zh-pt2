# 旧版 Chrome 操作系统设备支持 Linux 应用程序

> 原文：<https://www.xda-developers.com/linux-app-support-older-chrome-os-devices/>

Chrome 操作系统上的 Linux 应用是自 Android 应用以来操作系统最大的发展之一。此前有报道称，搭载特定内核版本的 Chromebooks 将被弃之不顾，但 Chrome OS 开发者的路线图上也有更老的设备。

当谷歌第一次[在 Linux 应用功能](https://www.xda-developers.com/chrome-os-linux-app-support-google-pixelbook/)上打破沉默时，人们知道，由于对更新的内核模块的依赖，Linux 内核 4.4 是运行应用所必需的。多亏了在 Chromium 的公共 bugtracker 上发现的[问题，我们已经确认容器将不会被限制在与内核 4.4 一起发布的少数 Chrome OS 设备上。](https://bugs.chromium.org/p/chromium/issues/detail?id=763970)

由于功能设计的方式，Linux 应用程序需要更新的内核模块才能工作。bugtracker 条目表明开发人员正在将这些内核模块(在这个特殊的例子中是 *vsock* )移植到旧的内核，以便旧的设备可以利用新的功能。错误报告提到 Samus([chrome book Pixel 2015](https://www.xda-developers.com/xda-external-link/play-store-apps-come-to-2015-chromebook-pixel-and-acer-r11/)的代号)在 Linux 应用支持范围内，这是一款随内核 3.14 一起发布的设备。虽然 Pixel 可能是新版本之外唯一获得支持的设备，但我们更有可能看到所有 3.14 设备都获得支持。

Chrome 上的 Linux 应用程序(其项目代号为 Crostini)使完整的桌面应用程序能够在 Chrome OS 上本地运行，这在以前只能通过“开发人员模式”实现，对于那些不想冒险丢失数据的人来说，这是一个可怕的前景。目前，新功能的目标是希望运行 Android Studio 等完整应用程序的开发人员，但有报道称，支持更广泛应用程序的工作正在进行中，包括进一步支持图形密集型应用程序。

Chrome OS 基于 Linux 内核。不像你家里的普通 Linux 机器，内核升级很少发布。虽然有在旧 Chromebooks 上升级内核版本的先例，但设备通常会在产品生命周期内坚持使用工厂发布的内核。这对于那些想要站在前沿的超级用户来说可能不太理想，但是它让开发者更容易保证平台的稳定性。

我们不知道反向移植将在多大程度上弥补旧设备的差距。也许一些内核模块或平台不会被淘汰，功能也不会如此广泛。尽管如此，这一消息意味着旧款 Chromebooks 还不会过早过时。