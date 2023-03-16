# Apktool v2.3.2 带来了对 Android P、实验性 AAPT2 重建等的支持

> 原文：<https://www.xda-developers.com/apktool-android-p-aapt2-rebuilding/>

# Apktool v2.3.2 带来了对 Android P、实验性 AAPT2 重建等的支持

Apktool 是逆向工程 APK 文件最流行的工具之一。它最近进行了更新，以支持为 Android P 开发者预览版制作的反编译应用程序，并且它还添加了 aapt2 二进制文件的实验性重建。

对 Android 应用程序进行逆向工程是 XDA 论坛上的一个流行爱好。反编译和修改现有的应用程序是一种技能，已经被用来生产具有新主题、新功能等的非官方版本的应用程序，而可供修改者使用的最重要的工具之一是 Apktool。Apktool 是使用最广泛的免费工具，旨在对 Android 应用程序进行逆向工程。该项目于 2012 年由 XDA 知名开发者 [iBotPeaches](https://forum.xda-developers.com/member.php?u=3924617) 启动，直到今天仍在不断更新，[最近的一个](https://forum.xda-developers.com/showthread.php?p=76158353#post76158353)增加了对第一个 Android P 开发者预览版和实验性重建 AAPT2 应用程序的支持。

该工具的最新版本是 v2.3.2，它最终允许用户重新编译基于 API 级构建的应用程序。以前，你可以很容易地反编译为 P 发行版开发的应用程序，但那只对执行“ [APK 拆卸](https://www.xda-developers.com/tag/apk-teardown/)”有用，对实际修改文件没用。那些 Magisk 模块的粉丝会很高兴地知道，系统修改可能正在进行中，因为修改者可以反编译、修改和重新编译 Android P 系统文件。

此外，该工具还为使用 [AAPT2](https://android.googlesource.com/platform/frameworks/base/+/master/tools/aapt2/readme.md) 构建应用程序提供了实验性支持。AAPT2，或 Android 资产打包工具 2.0，是 Android Gradle 插件 3.0 的默认版本，它提供了一个比普通 AAPT 更好的[增强功能](https://developer.android.com/studio/build/gradle-plugin-3-0-0-migration.html#aapt2)。AAPT 获取应用程序的资源文件并编译它们。Apktool 能够逆转 AAPT，但直到现在它还不能逆转在用 AAPT2 构建的应用程序下执行的资源打包。

您可以在下面查看完整的更改日志。我们很高兴看到 Apktool 的更新版本可以为各地的修改者所用。它只是 modder 工具包中的许多工具之一，包括 JADX、vdexExtractor 等等，但它是用户学习使用的最重要的工具之一。

*   [ [#1742](https://github.com/iBotPeaches/Apktool/issues/1742) ] - Android P 预览支持
*   [ [#1689](https://github.com/iBotPeaches/Apktool/issues/1689) ] -最初支持使用 aapt2 二进制文件进行重建
*   [ [#1730](https://github.com/iBotPeaches/Apktool/issues/1730) ] -修复了带有空 resources.arsc 文件的应用程序的问题
*   [ [#1703](https://github.com/iBotPeaches/Apktool/issues/1703) ] -修复了根深度 kotlin 文件夹的问题
*   [ [#1741](https://github.com/iBotPeaches/Apktool/issues/1741) ] -固定窗口上的建筑 Apktool。
*   添加了发现非零类型应用程序时的警告。
*   更新至 baksmali v2.2.2
*   支持将附加的照片扩展视为 raw (m4a)
*   防止临时文件堵塞临时目录。