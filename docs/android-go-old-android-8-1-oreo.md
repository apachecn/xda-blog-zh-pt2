# Android Go 如何帮助旧的 Android 手机运行 Android 8.1 Oreo

> 原文：<https://www.xda-developers.com/android-go-old-android-8-1-oreo/>

Android Go 是谷歌基于 Android 8.1 Oreo 的精简版 Android，它旨在成为针对 1gb 或更低 RAM 的低端设备的优化版 Android。它是在去年五月的谷歌 I/O 开发者大会上宣布的，最终更多的细节在当年的 12 月底被披露。据说这是为下一代入门级设备制造的，以确保发展中国家的人们仍然可以使用功能正常的智能手机来访问互联网和使用应用程序。

Go 有各种各样的性能优化和改进，包括比普通的 Android Oreo 安装少占用 50%的存储空间。由于 Android Runtime (ART)和内核优化，运行 Android Go 的设备平均比相同设备上安装的常规 Android Oreo 快 15%。这些优化是通过 Google 的一些专门构建配置实现的，我们将在后面解释。

Android Go 还受益于特殊的“Go”应用，如[文件 Go](https://www.xda-developers.com/google-go-smart-file-manager-leaked/) 、 [YouTube Go](https://www.xda-developers.com/google-announces-youtube-go-in-india-the-data-friendly-way-to-youtube/) 和[谷歌地图 Go](https://www.xda-developers.com/google-maps-go/) 。这些是谷歌开发的应用程序的轻量级版本，降低了运行效率的要求。这意味着，那些拥有 Android Go 设备的人也可以享受普通 Android Oreo 用户可以享受的大部分好处，使用谷歌的应用程序套件，而不必花很多钱购买旗舰或甚至略贵的廉价设备。

这都是为了谷歌扩大他们的市场。然而，它回避了一个问题，如果 Android Go 主要由一个构建配置和一套优化的谷歌应用程序组成，开发者可以制作自己的 Android Go 吗？简而言之，是的，我们可以。

## 一些 LineageOS 开发者已经在开发针对 Android Go 优化的定制 rom

我们已经看到一些定制 rom 开发人员对 Android Go 有所吸收，例如 XDA 知名开发人员 [AdrianDC](https://forum.xda-developers.com/member.php?u=2233641) ，他在 LineageOS 15.1 上的工作为[几款旧索尼手机](https://review.lineageos.org/#/q/%22Android+Go%22)构建了 Android Go 配置。有问题的设备是索尼 Xperia SP、索尼 Xperia T、索尼 Xperia V 和索尼 Xperia TX。这些设备都可以追溯到 2012 年和 2013 年，但它们将使用 Android Go 构建配置接收基于 Android 8.1 Oreo 的 LineageOS 15.1，这可能允许设备流畅地运行谷歌“Go”应用程序，如果 Android Go gapp 集最终发布的话。

任何单独的 LOS 维护者都应该能够引入一个 Android Go 配置的构建，它是一组构建配置和其他优化。这意味着，那些可能已经购买了索尼 Xperia T(例如，一款在发布时运行 Android 4.0.4 冰淇淋三明治的设备)的人，将能够在该设备上使用更优化的 Android 8.1 Oreo 版本，利用 YouTube Go 和谷歌地图 Go 等应用程序。它不会以旗舰级别的性能运行，但它应该**可用**——特别是对于一个可以追溯到 2012 年的设备。

* * *

## Android Go 如何帮助旧的 Android 手机运行 Android Oreo

Android 上的构建配置是一组参数，这些参数与 Android 系统的各个方面有关，在编译系统映像以便在设备上闪存时会应用这些参数。通常这些会改变系统的行为方式，Android Go 的主要优化来自于这些构建配置。

 <picture>![Android Go](img/9e00f1c8e1229a0af3f56ae0803b7984.png)</picture> 

The build configurations used for compiling Android Go.

我与 XDA 知名开发人员 joshuous 进行了交谈，他极大地帮助了我理解正在发生的变化——是什么真正让 Android Go 工作。其中一些构建配置在没有重新编译的情况下无法更改，并且是 ROM 本身蓝图的一部分。这些是全大写的标志。

然而，所有这些标志都与 Android 存储和内存使用的许多不同方面有关。其中包括[自动存储管理](https://github.com/aosp-mirror/platform_packages_apps_settings/commit/2156b26b2e38e1e92d33d1dba0a7c33fc2feeaea)，Android 的低内存杀手，dex ( **d** 阿尔维克 **ex** 可执行文件)优化器和运行应用程序的 RAM 限制。APK 文件由这些 DEX 文件组成，所以在某种程度上，可以把 APK 文件想象成一个包含大量。dex 文件，这实际上是 Android 执行一个应用程序时运行的文件。自动存储管理将改为由 Files Go 应用程序控制，而不是 Android 系统。

### Android Go 实用程序 Android 的低内存模式

在 Android 4.4 KitKat 中，谷歌推出了一个名为“[低 ram](https://source.android.com/devices/tech/perf/low-ram) 的新标志，旨在支持 512 MB RAM 的设备。它对系统进行了多项优化。这些变化对低 RAM 设备非常有益。

**改进的内存管理**

*   经验证的节省内存的内核配置:交换到 ZRAM。
*   如果要取消缓存并且太大，则终止缓存的进程。
*   不允许大服务把自己放回 A 服务(这样就不会导致启动器被杀)。
*   杀死在空闲维护中变得太大的进程(即使是通常无法杀死的进程，如当前的 IME 进程)。
*   序列化后台服务的启动。
*   调整低 RAM 设备的内存使用:更严格的内存不足(OOM)调整级别、更小的图形缓存等。

上述这些变化基本上确保了系统通过使用 ZRAM 确保尽可能使用压缩内存。ZRAM 基本上是一个 RAMdisk(一种使用 RAM 的存储介质，比在设备上使用常规存储快得多)作为交换文件。当 RAM 使用率很高并且应用程序仍然需要内存时，使用交换文件。这比 RAM 慢得多，应该尽可能避免使用。本质上，它只是压缩了内存的内容。

**减少系统内存**

*   微调 system_server 和 SystemUI 进程(节省了几 MB)。
*   在 Dalvik 中预加载 dex 缓存(节省了几兆字节)。
*   经过验证的 JIT-off 选项(每个进程最多节省 1.5MB)。
*   减少了每个进程的字体缓存开销。
*   引入了 ArrayMap/ArraySet，并在 framework 中作为 HashMap/HashSet 的轻量级替代广泛使用。

尽可能保守地说，这里主要发生的只是减少设备上运行的各种进程的内存消耗。基本的系统服务已经被剥离，以在后台使用尽可能少的内存，因为每兆字节的 RAM 都很重要。

### Android Go 使用修改后的低内存黑仔和 dex 优化

鉴于 Android Go 主要面向 1GB 或更低内存的设备，因此需要更积极的内存管理。Android Go 以几种不同的方式修改了低内存黑仔(LMK)。首先，当大量 RAM 用完时，低内存杀手进入“[临界压力](https://github.com/aosp-mirror/platform_system_core/commit/c47f2992b58bfcd1f5d75cd25dc8172eb4fb5cc9)状态。这是因为当内存使用率较高时，系统会因为不断尝试访问设备存储上的交换文件而变得缓慢。保持 RAM 清空将防止系统需要使用这个交换文件，并防止内存抖动。当设备的内存已满时，会发生内存抖动，并且必须不断地在设备的存储上分页交换文件，从而严重降低性能。

服务和 WiFi 服务被设置为“ [speed-profile](https://source.android.com/devices/tech/dalvik/configure) ”，这意味着这些服务中的选择方法是提前(AOT)编译的。(方法指的是一组代码，可以在任何时候通过名字调用。)这减少了 RAM 的使用和存储，因为 Android 系统将不需要不断地重新编译在设备上运行的基本服务。与此同时，共享 apk 被设置为“quicken”，旨在通过优化 dex 指令来获得更好的性能，从而提供额外的电池寿命和额外的 CPU 周期。

在 dex 优化方面，Android Go 做得相当多。首先，10 天后，如果一个应用程序没有被用来节省空间，它将[降级它。这里的降级不是指应用程序的实际版本号减少，而是指应用程序的 dalvik_cache 将被清除。Dalvik 缓存的使用使得设备不需要重新编译应用程序，而是只编译最必要的部分并缓存。其余部分在应用程序运行时使用实时(JIT)编译器进行编译。然而，如果应用程序 10 天没有被使用，那么预编译的应用程序的必要部分也被删除。这样做是为了释放尽可能多的空间。另一个简单的变化是不允许应用程序的内存使用超过 256MB，这样应用程序就不能使用设备上的所有内存。](https://github.com/aosp-mirror/platform_frameworks_base/commit/3aeca17aa911394e7a4d2c1536b28423cb135b53)

* * *

## Android Go 是低端设备上定制 ROM 开发的未来吗？

目前，我们不知道这个问题的答案，但在旧设备上开发定制 ROM 的前景看起来很光明。在设备上运行新版本的 Android 可能会有其他问题，但理论上，基于 Android Oreo *升级到更优化的 Android Go 应该会让旧的低端设备运行得更好。*