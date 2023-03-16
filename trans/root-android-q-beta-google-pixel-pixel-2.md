# 谷歌 Pixel 和 Pixel 2 的 Android Q beta 现在可以根了

> 原文：<https://www.xda-developers.com/root-android-q-beta-google-pixel-pixel-2/>

在第一个 Android Q 测试版发布之前，XDA 认可的开发者 topjohnwu [宣布](https://twitter.com/topjohnwu/status/1102152024232263680)他已经扎根 Android Q。他完成这一壮举要感谢一个泄露的 Android Q 版本，[我们也获得了](https://www.xda-developers.com/android-q-dark-theme-desktop-mode-permission-revamp/)。当所有三条谷歌 Pixel 智能手机线的官方测试版都下降时，topjohnwu 再次投入工作，看看他是否能让 Magisk 工作。他很快[意识到](https://twitter.com/topjohnwu/status/1105947979679191041)让最新版本的安卓扎根比看起来更困难。然而，今天早些时候他[设法](https://twitter.com/topjohnwu/status/1106632329290764288)根 Android Q，但只适用于谷歌像素，像素 XL，像素 2 和像素 2 XL。可悲的是，谷歌 Pixel 3 和 Pixel 3 XL 还不能扎根。

[**像素论坛**](https://forum.xda-developers.com/pixel) [**像素论坛**](https://forum.xda-developers.com/pixel-xl)

[**像素 2 论坛**](https://forum.xda-developers.com/pixel-2) [**像素 2 XL 论坛**](https://forum.xda-developers.com/pixel-2-xl)

如果您有 Pixel、Pixel XL、Pixel 2 或 Pixel 2 XL，您可以通过切换到 Magisk 金丝雀频道来 root 您的手机。一旦你的手机有了根，我强烈建议你尝试的一件事是[启用全系统黑暗模式](https://www.xda-developers.com/android-q-toggle-dark-theme/)，但在第三方应用中禁用强制黑暗。启用黑暗模式可以在没有 root 用户的情况下完成，但在 Google Photos 等应用程序中禁用强制黑暗需要 root 用户更改系统属性。至于 Pixel 3 或 Pixel 3 XL 的所有者，你必须等待 topjohnwu 弄清楚如何让 Magisk 在这两款设备的最新更新上工作。

[**Magisk 金丝雀频道**](https://forum.xda-developers.com/apps/magisk/dev-magisk-canary-channel-bleeding-edge-t3839337)

那么是什么阻碍了 Pixel 3 对 Magisk 的支持呢？原因与逻辑分区和重叠有关。逻辑分区涉及一个真正的存储分区，分为可动态调整大小的分区，如系统、供应商、odm、oem、产品等。覆盖文件系统，基本上是将一个目录树的内容覆盖在另一个目录树的顶部。从概念上讲，它有点像 Magisk，尽管它的工作方式不同。逻辑分区和覆盖层都已经被实现，以使 Android Q 中的动态 Android 成为可能，尽管 XDA 公认的开发者 T2·胡森认为它们的用途不止于此。

谷歌 Pixel 3 和 Pixel 3 XL 有逻辑分区，而 Pixel、Pixel XL、Pixel 2 和 Pixel 2 XL 没有。topjohnwu 表示，Google Pixel 3 的逻辑系统分区不再被识别为 EXT4 映像，因此他以前的系统挂载方法不起作用。根据 topjohnwu 的说法，Magisk 劫持了所有东西的挂载，包括系统、供应商、产品、odm 等。，然后“将根目录从系统复制到 rootfs”，然后使用已挂载分区中的数据修补 sepolicy，最后修补 init 进程以加载修补的 sepolicy。他说他需要研究如何在早期引导阶段挂载逻辑分区，这包括学习设备映射器如何工作。

这就是 Magisk 目前在支持 Android Q 方面的情况。如果 topjohnwu 在支持 Pixel 3 运行测试版方面取得进展，我们会让大家知道。