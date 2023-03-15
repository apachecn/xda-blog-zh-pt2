# SuperSU 2.13 开始筹备 Android L 发布

> 原文：<https://www.xda-developers.com/supersu-2-13-android-l/>

# SuperSU 2.13 开始筹备 Android L 发布

SuperSU 获得了重大更新，现在已经为即将到来的 Android L 正式发布做好了准备。

自从上一个主要版本 T1 和几个小的测试版本以来，SuperSU 已经平静了几个月，最终在其稳定分支中获得了一个重要的更新。XDA 资深公认的开发者 [Chainfire](http://forum.xda-developers.com/member.php?u=631273) 添加了大量的错误修复、兼容性添加和只有精通技术的用户才会注意到的底层变化。

SuperSU 现在已经为 Android L 做好了充分准备，Android L 应该很快就会发布。Chainfire 花了很大力气让这个应用程序与 AOSP 兼容。因此，SuperSU 现在与根级应用程序更加兼容。对于 *boot.img* 是否必须更新才能获得 root 仍然有些担心，但我们应该保持乐观。

为了正常工作，SuperSU 需要将一些二进制文件推入到 */system* 分区中。从现在开始，SuperSU 应用程序将与针对所有 Android 变体的特定于架构的二进制文件一起发布。从 Android L 开始，官方支持 64 位版本，但是二进制文件还没有经过测试，因为我们还没有看到很多 64 位 Android 设备。

以下是 SuperSU 2.13 的完整更新日志:

> *   改进了对 Android TV 的支持(调整了图标，禁用了一些功能，默认使用设备默认主题，等等)
> *   如果系统无法将 UID 名称手动解析为数字，请执行此操作
> *   修复即使启用了“信任系统用户”,系统用户也无法获得 root 权限的问题
> *   如果在 init_shell 上下文中启动，则转换到 init 上下文(如果可能)
> *   调整加密设备的启动顺序
> *   支持-cn/ -上下文切换的 MCS
> *   对最新 AOSP/L 的大量审计保持沉默
> *   许多小的变化，以修复对最新的 AOSP/L 的支持
> *   次要用户不再能够更改信任系统或遵守 CM 设置
> *   添加了实验性 sppolicy 二进制文件
> *   启动时检查移除的应用程序，如果启用了重新验证，则忘记它们的设置
> *   亚马逊应用商店支持
> *   取消 APK 限制，仅安装到 ARM 和 X86 上(MIPS 问题)
> *   当需要隐藏覆盖时，通知感兴趣的应用程序(授予 root 权限)
> *   如果在内核上下文中启动，则转换到 init 上下文
> *   armeabi-v7a、arm64-v8a、x86-64、mips、mips64 的实验版本
> *   修复了可能导致 su 会话冻结的错误 fd 关闭
> *   修正了 sugote 中偶尔死机和错误的退出代码
> *   移除 TWRP/CWM 二进制更新程序中的 busybox 依赖项
> *   修复了备份脚本中丢失的 sugote-mksh
> *   修正了安装脚本清除 SuperSU Pro
> *   添加了禁用装载命名空间分隔的选项
> *   修正了授予默认访问权限仍然显示提示的错误
> *   二进制更新后在对话框中增加了重启按钮
> *   增加了点击保护-可能会导致屏幕变暗应用程序的问题！
> *   增加了移除团队毒液苏
> *   添加了新的 dalvik-cache 路径以在包维护时清除
> *   修复启用完整内容日志记录时 exitcode 有时会出错的问题
> *   修复自动 OTA 生存
> *   更新的语言文件

你可以在这篇 Google+文章的[中了解更多关于 CF-Auto-Root 的最新变化。你可以通过访问](https://plus.google.com/+Chainfire/posts/eshAgMtYfoX)[官方 SuperSU 应用线程](http://forum.xda-developers.com/showthread.php?t=1538053)获取最新版本的应用。你也可以等待 Play Store 或亚马逊的更新，但这可能会比通过你最喜欢的恢复显示最新的 ZIP 文件花费更长的时间。