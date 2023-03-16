# Magisk 已更新，支持 Android P DP1 上的 Google Pixel/XL 和 Pixel 2/2 XL

> 原文：<https://www.xda-developers.com/magisk-google-pixel-xl-pixel-2-xl-android-p/>

# Magisk 已更新，支持 Android P DP1 上的 Google Pixel/XL 和 Pixel 2/2 XL

Android P Developer Preview 1 现在可用于 Google Pixel、Google Pixel XL、Google Pixel 2 和 Google Pixel 2 XL，由于 Magisk 的最新更新，root 访问权限不久后也将推出。

几天前，谷歌向我们发布了第一个 Android P 开发者预览版。该版本适用于第一代谷歌 Pixel 和 Pixel XL 以及第二代谷歌 Pixel 2 和 Pixel 2 XL。更新中有很多变化，从用户界面的修改到生活质量的提高。我们已经在[两篇](https://www.xda-developers.com/everything-new-android-p-developer-preview/) [独立的](https://www.xda-developers.com/android-p-dp1-google-pixel-xl-pixel-2-xl-minor-features/)文章中涵盖了几乎所有可见的变化，虽然我个人认为这是一个伟大的更新(除了[底层惨败](https://www.xda-developers.com/substratum-petition-google-custom-overlay-android-p/))，但你们中的一些人可能会发现它有所欠缺。幸运的是，Magisk 现在已经更新到支持第一个 P 开发者预览版，这将有望打开定制修改的闸门。

在宣布 Magisk v16 发布后，许多人担心 XDA 认可的开发者 [topjohnwu](https://forum.xda-developers.com/member.php?u=4470081) 的缺席会导致一段时间的安全网失败或延迟对 Android P 的支持。事实并非如此，因为开发者在其他人的帮助下，如 GitHub 上的 XDA 成员 [shakalaca](https://forum.xda-developers.com/member.php?u=1813976) 和 [worstperson](https://github.com/worstperson) ，已经找到了一些时间[在 Magisk](https://forum.xda-developers.com/showpost.php?p=75844810&postcount=40) 上工作——迅速将 root 访问权限带给渴望的谷歌 Pixel/Pixel XL 和 Pixel 2/Pixel 2 XL 用户。当然，SafetyNet 通过了这个版本，这意味着你应该能够在保留 root 访问权限的同时使用 Google Pay 等应用。

## 魔术 v16.1 (1610)变更日志

*魔法 v16.1 (1610)*

*   更新重置提示
*   更新几个 SELinux 的东西
*   添加缺少“make_ext4fs”的解决方法
*   修复 Android 6.0 及更低版本的 SELinux 问题

*Magisk Manager v5.6.2 (107)*

*   手动禁用 SQLite 的 WAL 模式，因为 Android P 很奇怪
*   改变隐藏管理器的路径，因为 Android P 增加了更多的限制
*   修复旧版本 Android 上的隐藏管理器

## 在 Android P 上为 Google Pixel/XL 和 Google Pixel 2/2 XL 安装 Magisk

一如既往，最新版本可在 XDA 论坛的官方发布线程上获得。

[**下载魔法 v 16.1(1610)**T3](https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445)

有了 root 权限，如果你有 Pixel 2，你就可以开始修改诸如 [Pixel Launcher Mod](https://www.xda-developers.com/google-pixel-launcher-mods-change-icon-packs-widget-sizes-labels/) 或[环境锁屏音乐](https://www.xda-developers.com/ambient-lock-screen-music-pixel-2/)应用程序。这仅仅是 root 访问的开始，所以一定要访问我们的论坛，为你的设备找到最好的插件。