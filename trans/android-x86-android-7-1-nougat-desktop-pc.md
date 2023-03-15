# Android x86 7.1 R1 将 Android 7.1 牛轧糖带到桌面电脑上

> 原文：<https://www.xda-developers.com/android-x86-android-7-1-nougat-desktop-pc/>

Android x86 项目旨在将 Android 移植到基于 x86 的 Windows PCs 和 Mac 电脑上。它是 Android 的一个完整端口，而不是像其他解决方案一样更多的是一个应用播放器。Android x86 的上一个版本[在 2016 年 9 月带来了 Android 6.0 棉花糖](https://www.xda-developers.com/android-x86-project-releases-stable-version-of-android-6-0/)的稳定移植，让桌面用户体验谷歌 Play 商店，运行 Android 应用程序，与亚行合作，等等。现在，Android x86 项目的 7.1 R1 已经推出，它为 x86 计算机带来了完整的 Android 7.1 牛轧糖。

虽然 Android 7.1 牛轧糖早在 2016 年 10 月就发布了，但 Android x86 为 x86 用户开发操作系统的稳定端口还需要一段时间。6 月和 10 月发布了 Android x86 7.1 的发布候选，现在，开发者已经发布了 Android 7.1 牛轧糖的稳定端口。该端口以 ISO 和 rpm 格式提供，因此它可以作为虚拟机安装，也可以作为 x86 PC 上的完整安装。

以下是 Android x86 R1 与 10 月发布候选版本的变更日志:

> *   Android-x86 安装程序改进了很多，包括:
>     *   为 efibootmgr 创建 EFI 启动条目。
>     *   添加自动安装功能，这是有用的安装 Android-x86 作为唯一的操作系统。
>     *   提供有关磁盘和分区选择菜单的更多信息。
>     *   添加高级选项以提供更多启动选项。
>     *   保存 grub2 菜单中的最后一个选择。
> *   将内核更新到 LTS 内核 4.9.80，并添加更多来自 AOSP 的补丁。
> *   为 iio 型传感器添加新的 HAL。
> *   通过 ctrl-alt-del 显示关机菜单。
> *   修复了很多 bug。

尽管 Android x86 的最新稳定版本基于 Android 7.1 Nougat 而不是 Android Oreo，这似乎令人失望，但 Android Nougat 仍然是 Android 的一个相当新的版本，为 x86 PC 开发一个稳定的 it 端口满足了需要在 x86 PC 上使用 Android 的用户的需求。

由于它是一个稳定的端口，Play Store 等关键组件可以正常工作，对于那些需要在 x86 上使用完整版 Android 而不是应用播放器的人来说，Android x86 是一个很好的选择。据 *Android Police* 称，该版本甚至包括[任务栏作为启动器](https://www.xda-developers.com/android-nougats-freeform-window-mode-what-it-is-and-how-developers-can-utilize-it/)，由于[自由多窗口](https://www.xda-developers.com/praise-and-criticism-of-ns-multi-window-freeform-from-a-multi-window-fan/)的支持，这应该会使桌面体验更加甜美。

用户可以在源码链接下载 ISO 或 rpm 的 32 位和 64 位 PC 的 Android x86。开发人员建议对传统 BIOS 设备使用 32 位文件，对 UEFI 设备使用 64 位文件。

[**下载基于 Android 7.1 牛轧糖的 Android x86 预建镜像**](https://osdn.net/projects/android-x86/releases/67834)

* * *

[**来源:安卓 x86 发行说明**](http://www.android-x86.org/releases/releasenote-7-1-r1) [**Via:安卓警察**](http://www.androidpolice.com/2018/02/09/android-x86-7-1-r1-now-available-brings-nougat-pc/)