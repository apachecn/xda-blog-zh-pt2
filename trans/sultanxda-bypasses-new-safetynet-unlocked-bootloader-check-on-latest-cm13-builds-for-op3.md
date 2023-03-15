# Sultanxda 绕过新的 SafetyNet 解锁引导程序检查

> 原文：<https://www.xda-developers.com/sultanxda-bypasses-new-safetynet-unlocked-bootloader-check-on-latest-cm13-builds-for-op3/>

对于那些想使用 Android Pay 同时完全控制自己手机的人来说，谷歌的安全网是一个巨大的眼中钉。直到最近，它主要是关于禁用根 的 [设备上的 Android Pay，但几天前，谷歌更进了一步——他们甚至在带有](http://www.xda-developers.com/google-security-engineer-explains-issues-with-root-and-android-pay-in-the-xda-forums/) [解锁引导加载器](http://www.xda-developers.com/android-safetynet-now-reportedly-tripped-by-unlocked-bootloaders/) 的设备上触发安全网。

谢天谢地，就像 Chainfire 的 systemless Root 有 [暂时绕过了](http://www.xda-developers.com/android-pay-no-longer-working-with-systemless-root/)safety net a[施加的 Root 限制几次](http://www.xda-developers.com/xda-external-link/suhide-updated-to-bypass-safetynet-update/) (就像有 topjohnwu 的开源 [Magisk](http://www.xda-developers.com/magisk-updated-to-v7-now-completely-open-source/) ，一个用于 systemless modding 和 [Xposed](http://www.xda-developers.com/unoffical-systemless-xposed-is-now-available-otas-and-pay-unaffected/) 的接口)，Sultanxda 找到了一个 [临时](https://github.com/sultanxda/android_kernel_oneplus_msm8996/commit/abc05b16bbd33521c2fffaf491c5657a94bfcfc5)

它的工作原理是，SafetyNet 通常会通过使用 [验证引导](https://source.android.com/security/verifiedboot/) 来检查引导加载程序是否解锁，这是一个自 KitKat 以来仅在 Android 中出现的功能，但尚未被每个设备支持(这个功能在 Android 7.0 Nougat 中变得越来越激进[](http://www.xda-developers.com/strictly-enforced-verified-boot-with-error-correction-to-come-with-android-7-0-nougat/)，甚至 [在 Pixel 上阻止传统的根方法](http://www.xda-developers.com/pixel-phones-not-yet-rootable-with-current-methods/) 为了支持那些没有支持验证启动所需硬件的旧手机，如果安全网没有从验证启动测试中获得任何响应，它将不会变绿。

但俗话说，XDA 总能找到办法:

为了绕过这一点，Sultanxda 从他修改后的内核中移除了对验证引导标志的支持，从而阻止引导加载程序将标志传递给 SafetyNet。这使得 SafetyNet 得到了与不支持硬件级验证启动的设备相同的响应，因此 SafetyNet 允许设备通过测试。

虽然这不是一个永久的解决方案(之前也没有被证明是)，但它应该允许人们绕过 SafetyNet，直到谷歌找到修补这个安全漏洞的方法。令人欣慰的是，这个特殊的安全漏洞看起来可能需要谷歌花一段时间来修复，但对于我们的爱好者和开发者社区来说，谷歌首先采取这些措施是一种耻辱。

对于 Linux 和 macOS 世界来说，人们对自己的电脑拥有根支持是标准的(Windows 个人电脑的管理员访问权限也是如此，尽管这并不是完全相同的事情)，但谷歌认为我们不能信任我们对自己设备的控制(默认情况下不附带它，并采取措施防止人们使用它)。他们表现得好像这是一台由他们管理的设备，而不是从他们那里购买的设备。谢天谢地，像 Sultanxda、Chainfire 和 topjohnwu 这样的人今天在这里帮助恢复从我们这里夺走的特征，但未来会发生什么呢？

传播这个补丁，让其他人也能在他们的设备上享受它！