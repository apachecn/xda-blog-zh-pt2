# 谷歌为 Project Treble 兼容设备发布官方 Android Q GSIs

> 原文：<https://www.xda-developers.com/android-q-gsi-project-treble/>

谷歌刚刚为所有三代谷歌 Pixel 智能手机推出了第二个 Android Q 测试版，但他们也发布了系统映像，允许任何 Project Treble 兼容的智能手机都可以使用 Android Q！是的，谷歌终于发布了最新安卓版本的通用系统映像。这意味着非像素智能手机也可以测试最新的安卓版本。

提醒一下，谷歌[宣布了与安卓 8.0 奥利奥一起的](https://www.xda-developers.com/googles-project-treble-modularize-android-so-oems-can-update-devices-faster/)项目 Treble。Treble 是对 Android 工作方式的一次大规模重构。它包括将 Android 模块化，以便原始设备制造商可以更快地推出软件更新。Treble 要求使用 Android Oreo 及更高版本的设备将 HALs 等供应商实现从 Android OS 框架中分离出来，HALs 是操作系统用来与底层硬件通信的软件。谷歌通过全面实施 VNDK(供应商原生开发套件)和引入 CTS-on-GSI(通用系统映像兼容性测试套件)测试，完善了 Treble 对 Android 8.1 Oreo 和 Android 9 Pie 的要求。任何使用 Android 9 Pie 启动的设备都被谷歌视为 Treble 兼容。

谷歌要求原始设备制造商验证其设备支持高音的方式是启动所谓的 [GSI](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/) 。GSI 是一个直接从 AOSP 编译的 Android 版本，没有经过任何供应商的修改。一个三重兼容设备必须能够成功地引导一个 GSI，它被刷新到系统分区上，而不需要修改供应商、引导或任何其他分区。我们论坛上的定制 ROM 开发者[已经利用了这一点，创建了他们自己的具有附加功能的 GSI，但谷歌也希望应用开发者尝试在他们自己的设备上闪存 GSI，以便他们可以在现有硬件上根据最新的 API 级别测试他们的应用。](https://forum.xda-developers.com/project-treble)

官方 Android Q beta GSIs 今天发布了 3 个版本:ARM64+GMS、ARM64 和 x86_64。你很可能想要 ARM64+GMS 版本，因为它包含 Google Play 应用程序和服务。以下是 Google 为所有 3 个版本提供的构建信息:

```
 Date: April 2019
Build: QPP2.190228.021-5411336
Build Type: experimental
Security patch level: 2019-04-05
Google Play Services: 16.0.88 
```

要在您的设备上安装 Android Q GSI，您需要满足以下要求:

*   您的设备与 Android 9 Pie 一起推出，符合 Treble 标准。
*   您有一个解锁的引导加载程序，因此您可以通过快速引导刷新系统和 vbmeta 映像。(谷歌[仍在研究](https://www.xda-developers.com/android-q-dynamic-android-aosp-gsi/)他们在不解锁引导程序的情况下安装 GSIs 的方法。)

请注意，这些 GSI 不保证所有硬件功能。Treble 的测试不会验证设备上的每个硬件组件都工作，所以不要指望一加 6T 或小米 9 的显示指纹扫描仪会工作。此外，GSI 没有通过 CTS，因此如果您的应用程序使用 SafetyNet 认证 API 来验证设备没有被篡改，那么它将无法工作。最后，Android Q 仍处于测试阶段，因此适用于 Google Pixels 发布的所有其他已知问题也将适用于此。除此之外，还有其他已知问题，如无法重新启动，无法在来电时听到音频，以及 Pixel 设备上的蓝牙连接问题。

要下载并安装 GSIs，请访问下面的链接。

[**安卓 Q GSI 二进制**](https://developer.android.com/preview/gsi-release-notes)