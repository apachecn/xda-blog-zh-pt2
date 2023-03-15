# 新的 SuperSU 和 suhide 更新带来了小的错误修复

> 原文：<https://www.xda-developers.com/supersu-suhide-updates-bug-fixes/>

# 新的 SuperSU 和 suhide 更新带来了小的错误修复

Chainfire 推出了 SuperSU 和 suhide 的新更新，增加了对新版 TWRP 的兼容性，并隐藏了一些遗留问题。

当我们中的许多人在享受摆脱日常生活压力的周末时，Chainfire 正忙着为他的两个应用程序完成两个小的 bug 修复更新。我们不期待这些更新中有任何大的功能或变化，但 SuperSU 和 [suhide](https://www.xda-developers.com/experimental-suhide-mod-for-supersu-hides-su-binary-from-applications/) 都收到了新的更新，带来了一些小但重要的更新。这些更新现已向公众发布，SuperSU 升级到版本 2.82-SR5，suhide 升级到版本 1.09。

我们将从 SuperSU 更新开始，它现在是版本 2.82-SR5。此次更新的第一个变化与我们最近看到的谷歌像素和像素 XL TWRP 的变化有关。这个自定义恢复最近更新了对奥利奥的正确支持，但用旧版本的 SuperSU 更新新的 TWRP 图像最终打破了 TWRP。你可以启动 TWRP，然后闪存 SuperSU 很好，但如果你想在同一台设备上，然后你遇到了最后一个版本的问题。

除了修复之外，这个新版本的 SuperSU 还解决了一个与 Oreo 和基于文件的加密相关的问题。如果您有一台运行 Android 8.0 Oreo 的设备，并且它也使用基于文件的加密，那么如果/data 分区未加密，它将拒绝引导。到目前为止，Pixel 手机是唯一符合这一标准的设备，但可以肯定的是，随着时间的推移，这个问题会越来越多。所以这个新版本的 SuperSU 为这个问题增加了一个变通方法。

suhide 是 Chainfire 的另一个应用程序，本周末收到了一个更新。这个新的更新将它带到了 1.09 版本，它只是比以前隐藏了更多的“遗留问题”。这包括但不限于我们刚刚看到的添加到 SuperSU 新版本中的变化。你可以在我们的 SuperSU 论坛这里找到关于这两个更新的讨论。

*SuperSU*

- suinit:修复(刷新)Pixel (XL)上的 TWRP 3.1.1 兼容性

- FBE:允许 FBE 设备不加密启动(除非设置了 KEEPFORCEENCRYPT)

*苏希德*

-移除 ODM 和 OEM 安装

- Setpropex:设置多个属性

-清理:移除/启动

* * *

[**来源:+火链**](https://plus.google.com/+Chainfire/posts/BanQpQ1QPEg)