# Magisk 现在支持 Android Q 上的谷歌 Pixel 3 和 Pixel 3a

> 原文：<https://www.xda-developers.com/magisk-google-pixel-3-pixel-3a-android-q/>

谷歌在三月份发布了第一个 Android Q 测试版，谷歌 Pixel 和谷歌 Pixel 2 很快就可以通过 Magisk 进行 root 访问。然而，谷歌 Pixel 3 不能植根于 Android Q，因为 Magisk 的开发者 XDA 认识到开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 需要弄清楚如何使用新的逻辑分区布局。随着他在苹果公司的新实习，topjohnwu 在 Magisk 上工作的时间减少了，但这并没有阻止他在开发方面取得两项重大突破。在最新的 Canary 版本中，Magisk 现在支持 system-as-root，使应用程序更难检测 root 访问，并且还支持具有逻辑分区的设备，如 Android Q 上的 Pixel 3 和 Pixel 3a XL 系列。

[**谷歌 Pixel 3 论坛**](https://forum.xda-developers.com/pixel-3) **[谷歌 Pixel 3 XL 论坛](https://forum.xda-developers.com/pixel-3-xl)**

**[谷歌像素 3a 论坛](https://forum.xda-developers.com/pixel-3a) [谷歌像素 3a XL 论坛](https://forum.xda-developers.com/pixel-3a-xl)**

## Android Q 上的 Google Pixel 3 和 Pixel 3a 逻辑分区支持

为了帮助开发者在现有设备上测试 AOSP 版本的 Android，谷歌发布了通用系统映像(GSI)，可以在 Project Treble 兼容的设备上启动(任何使用 Android 9 Pie 或更高版本启动的设备)。)安装 GSI 需要解锁引导加载程序，这可能并非在所有设备上都可行，并且在擦除用户数据后在快速引导上刷新系统映像。在 Android Q 中，谷歌引入了一个名为[动态系统更新](https://www.xda-developers.com/android-q-dynamic-system-updates-project-treble/)的新功能，该功能允许开发者在不解锁引导加载程序或擦除数据的情况下启动 GSI。为了支持动态系统更新，设备需要具有可以动态调整大小的逻辑分区，以便为 GSI 安装腾出空间。谷歌 Pixel 3、谷歌 Pixel 3 XL、谷歌 Pixel 3a 和谷歌 Pixel 3a XL 在 Android Q betas 上有逻辑分区，尽管只有 Pixel 3 和 Pixel 3 XL 支持 DSU。尽管如此，正是由于分区结构的这种彻底改变，Magisk 才无法工作。

当 topjohnwu 下定决心，什么都不能阻止他实现 root 权限。就在前几天，他宣布他已经成功地将他的 Pixel 3 XL 植根于 Android Q beta 4。他的提交描述[这里](https://github.com/topjohnwu/Magisk/commit/f1112fdf3719c1ed2af7c2bc1d1d4dc3f67bf292)解释了他如何实现逻辑分区支持的技术细节，但重要的是 Magisk 现在可以安装在有或没有逻辑分区的设备上。

## 系统根支持

对于带有 [A/B 双分区](https://www.xda-developers.com/how-a-b-partitions-and-seamless-updates-affect-custom-development-on-xda/)的设备，系统分区被挂载为根目录(/)，但是没有 A/B 双分区的设备将系统分区挂载在/system。这使得纯系统 OTA 在非 A/B 设备上是不可能的，因为 ramdisk 中需要更新的文件位于引导分区中。这就是为什么，为了使 Android Pie 和更高版本中的纯系统 OTA 成为可能，Google 要求所有使用 Android Pie 的设备都支持 system-as-root 分区布局。在 system-as-root 布局中，ramdisk 映像被合并到系统映像中，系统映像作为 rootfs 挂载。

由于 Google 引入了 system-as-root，根设备的[解决方案](https://twitter.com/topjohnwu/status/1143799584801447937)是将 system-as-root 恢复到旧的分区“initramfs rootfs”布局。这种[在 Android 7.1 到 Android 9 Pie 上运行](https://twitter.com/topjohnwu/status/1143799588005928960)很好，因为 Android 有对这种旧布局的传统支持，但 Android Q 完全[取消了](https://twitter.com/topjohnwu/status/1143799588744073218)支持，因为 system-as-root 现在对所有设备都是强制性的，甚至对那些正在更新到 Android Q 的设备也是如此。Magisk 的以前版本仍然工作，这要感谢一些“非常讨厌的黑客”，但 topjohnwu 对那个解决方案不满意，所以为了正确支持 system-as-root，他[引入了](https://twitter.com/topjohnwu/status/1143799587024412672)“MagiskInit”

正确支持系统作为根分区布局的一个好的副作用是，根检测的一个潜在途径已经被压制。正如 topjohnwu 亲切地向我解释的那样，旧的“恢复到 initramfs rootfs”方法很容易被应用程序检测到，因为 Magisk 会将系统挂载到“/system_root”并将挂载“/system_root/system”绑定到“/system”应用程序要检测根的存在，只需检查“/system_root”是否存在，或者“/”是否为“rootfs”然而，目前还不清楚是否有任何应用程序真正利用这一点来检测 root。尽管如此，安全总比后悔好。

## 杂项变更

Android Q 为 Android 应用程序生命周期引入了对称为“[囊胚池](https://github.com/aosp-mirror/platform_frameworks_base/commit/cffbf1c9b4d6ea7fa58dba77073092f8f4571a00)的东西的支持。如果启用了新的“进程池”功能，MagiskHide】无法检测应用程序以隐藏 root 访问。最新的 Canary 版本现在支持这个特性。根据 topjohnwu 的说法:“为了正确地支持 Q 中引入的新的囊胚池优化，我重写了一大块用于进程监控的 ptracing 逻辑。”

* * *

如果你在 Android Q beta 上有 Pixel 3、Pixel 3 XL、Pixel 3a 或 Pixel 3a XL，请尝试最新的 Magisk Canary 版本，并让我们知道你是否成功地根化了你的设备。

[**Magisk 金丝雀频道**](https://forum.xda-developers.com/apps/magisk/dev-magisk-canary-channel-bleeding-edge-t3839337)