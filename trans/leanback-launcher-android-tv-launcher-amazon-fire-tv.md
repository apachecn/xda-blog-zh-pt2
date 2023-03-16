# Leanback Launcher 是一款适用于亚马逊 Fire TV 的 Android 电视启动器

> 原文：<https://www.xda-developers.com/leanback-launcher-android-tv-launcher-amazon-fire-tv/>

# Leanback Launcher 是一款适用于亚马逊 Fire TV 的 Android 电视启动器

亚马逊 Fire TV 设备的 Leanback Launcher 是 Android TV launcher 的一个全功能端口，用于启动基于 OS 的机顶盒、电视和 HDMI 加密狗。

亚马逊在许多领域与谷歌竞争，从智能音箱到流媒体盒子。(它从前甚至有自己的智能手机。)但亚马逊 Fire 平板电脑和 Fire 电视机顶盒的核心操作系统是 Fire OS，它基于 Android。它甚至支持许多 Android 的核心功能，如侧装应用程序和在家用启动器之间切换的能力。

如果你是一个 Android 纯粹主义者，或者如果你只是不喜欢 Fire TV 的用户界面，你会很高兴知道你可以将启动器改为不同的东西。一个很好的选择是 XDA 成员的 lean back Launcher[rockon 999:](https://forum.xda-developers.com/member.php?u=6689035)这是一个用于亚马逊 Fire TV 设备的全功能安卓电视启动器。它像 Shield TV 和 Nexus Player 等 Android 电视机顶盒一样简单易用，安装后，最上面一行会显示你锁定的应用程序，向下滚动时，你会看到已安装的应用程序被组织到视频和音乐等类别中。

### 后倾发射器特征

-无需安装 stock launcher 即可打开蓝牙和 WiFi 设置。

-打开通知中心、通知设置，并显示当前未读通知的数量。

-可以在商店中显示亚马逊下载的应用程序，以便于更新和管理。

-可以打开单个应用程序的设置。

-收藏夹行

-剥夺了所有谷歌服务(以防止崩溃！)

导航很简单。Fire TV 遥控器上的 menu 按钮操作应用程序菜单，收藏夹行中的 **[+]** 磁贴可用于将应用程序添加到您的收藏夹行。

要在亚马逊 Fire TV 设备上安装 Leanback Launcher，你需要准备一台装有 ADB 的电脑。

1.  #### 使用命令**ADB install【path】**(用网络上目标 Fire TV 设备的位置替换“[path]”)。

2.  #### 下一步是可选的，但是如果想要启动程序的通知计数器工作，你需要执行这个命令:**ADB shell pm grant com . rockon 999 . Android . leanbackluncher Android . permission . write _ SECURE _ SETTINGS**。

3.  如果你使用的是 Fire OS 版本 5.2.6 或更低版本，你可以选择[禁用股票启动器](https://forum.xda-developers.com/fire-tv/general/disable-bloatware-2nd-gen-fire-tv-stick-t3674629)。你需要禁用空中更新功能，这样它就不会覆盖你新安装的启动器。
4.  开发者建议你安装[launcher hick v3](https://forum.xda-developers.com/amazon-fire/general/launcher-root-launcher-hijack-v2-t3561026)来获得一个全功能的 home 键。
5.  接下来，如果你想让搜索功能正常运行，你需要安装谷歌搜索[2 . x 版](https://www.apkmirror.com/apk/google-inc/google-app-for-android-tv-android-tv/google-app-for-android-tv-android-tv-2-2-2-0-138699360-release/google-app-for-android-tv-2-2-0-138699360-android-apk-download/download/)或更新版本。预先警告，如果试图使用启动器中的“麦克风”球与谷歌搜索互动，它可能会崩溃-使用键盘球代替。

后倾发射器并不完美。一些琐碎的问题包括通知计数器，它并不总是正常工作。开发者指出，有时你必须重启应用程序，WRITE_SECURE_SETTINGS 权限才能生效。尽管如此，在 Fire TV 设备上安装一个功能齐全的 Android 电视发射器仍是一个不小的成就——对电视迷来说也是一个福音。

* * *

[**在我们的消防电视论坛**](https://forum.xda-developers.com/fire-tv/development/app-leanback-launcher-fire-tv-t3750451) 查看后倾发射器