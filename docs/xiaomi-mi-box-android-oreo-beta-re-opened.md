# 在用户有大量问题后，小米盒子安卓奥利奥测试版重新开放

> 原文：<https://www.xda-developers.com/xiaomi-mi-box-android-oreo-beta-re-opened/>

# 在用户有大量问题后，小米盒子安卓奥利奥测试版重新开放

小米米盒子最近收到了安卓奥利奥的更新。由于用户遇到大量问题，OTA 已经停止，测试版重新开放。

小米盒子[最近收到了期待已久的安卓奥利奥更新](https://www.xda-developers.com/xiaomi-mi-box-android-oreo-update-2/)，此前该设备似乎被放弃了，因为[安卓牛轧糖更新从未到来](https://www.xda-developers.com/nearly-11-months-after-release-xiaomi-mi-box-owners-can-now-sideload-a-beta-build-of-android-nougat/)。虽然更新工作正常，但最终版本中存在的缺陷数量惊人。测试人员觉得他们没有被听到，关键功能被遗漏，这意味着一些小米 Mi Box 设备完全无法用于最初的目的。现在 xiaomi.eu 的创始人已经开始与小米合作，随着 Android Oreo beta 计划[重新开放](https://xiaomi.eu/community/threads/mi-box-3-oreo-internal-beta-test-program-submissions-temporarily-closed-30-member-test-group-reached.44778/)，该计划[已经取消](https://xiaomi.eu/community/threads/mi-box-3-oreo-public-ota-has-been-halted.44821/)。

所有用户将很快收到一个 OTA，它应该可以修复当前最重要的问题，如 HDCP 2.2 和 NTFS。HDCP 2.2 是用于 4k 视频的复制保护，而那些将 USB 硬盘连接到小米盒子的用户需要支持 NTFS 存储。接收此更新不需要申请测试版。其他需要修复的错误包括 Wi-Fi 速度慢，这是由一个被窃听的 Broadcom 驱动程序引起的，遥控器和麦克风间歇性地与 Mi Box 断开连接，以及一些 AAC 5.1 和杜比问题。这只是你可能在 Android Oreo 上发现的小米盒子的一些错误的一小部分。你可以在这里查看我们在下面添加的主要错误列表[。](https://xiaomi.eu/community/threads/mi-box-3-master-bug-list.44784/)

### 小米 mi 盒子安卓奥利奥更新 bug 列表截至北京标准时间 7 月 7 日晚 10:02

*   刷新率不起作用
*   自动分辨率切换不起作用
*   无法从 Aptoide 电视安装任何内容
*   谷歌 Android Oreo 操作系统的错误，启动后以太网似乎连接缓慢
*   双击主屏幕上的远程返回按钮不会像预期的那样快捷到 ATV Android 设置
*   OTA 电视去隔行(使用 AMLogic MediaCodec)仍然是半运动，如果与 Kodi Krypton/Leia PVR 的或 TvHeadend Live Channels 应用程序一起使用，mpeg2 图像质量是块状的
*   AAC 5.1 在 plex 上不工作(视频一点也不流畅！)(AC3 工作正常)
*   需要强制 dolby 在 plex 上获得部分通过
*   长时间待机后音频不起作用
*   长时间待机后，机箱无响应
*   配对的远程间歇性问题，包括麦克风
*   遥控器上的麦克风按钮仅触发全局搜索/助手，不能重新映射到应用程序搜索
*   未识别 NTFS 和 exFAT】【在 2018 年 7 月 6 日的内部测试版中部分修复】
*   爱可视媒体播放器、VLC 和 3.7.0 版 MrMC 应用程序似乎能够读取 NTFS 硬盘
*   与以前的棉花糖固件相比，一些用户报告了较慢的 WiFi 数据传输速率和 WiFi 掉线。**【博通驱动问题】**
*   交流 WiFi 速度慢**【BROADCOM 驱动程序问题】**
*   DD+网飞和其他应用程序，如 Kodi - bitstreaming 音频信号中断，尤其是在只使用 WiFi 的情况下。
*   没有 5.1 网飞音频如果您使用杜比数字只有 HDMI 连接的音频接收器，即使 MI 盒是杜比音频许可。
*   基于 ASIX & Realtek 芯片组的 USB3 >千兆位 LAN 适配器似乎只有在您的家用路由器上使用 DHCP 时才能工作。
*   错误报告提交:当应用程序崩溃时，Oreo 中报告错误或关闭应用程序的窗口丢失
*   蓝牙同步(与第三方外设的配对效果不佳，例如 MYMobile RKGAME4th 游戏手柄)
*   YouTube 应用程序，倒带视频导致应用程序崩溃和启动循环
*   白点神器([https://github . com/wrx tasy/libre elec . TV/blob/master/projects/od roid _ C2/initramfs/platform _ init # L35](https://github.com/wrxtasy/LibreELEC.tv/blob/master/projects/Odroid_C2/initramfs/platform_init#L35))([https://Xiaomi . eu/community/threads/Oreo-update-screen-artifacts-now-appearing-non-stop . 44745/](https://xiaomi.eu/community/threads/oreo-update-screen-artifacts-now-appearing-non-stop.44745/))([https://Xiaomi . eu/community/threads/odd-stick-DOT-of-the-left-the-the-of-the](https://xiaomi.eu/community/threads/weird-stuck-dot-left-of-the-screen.44730/)
*   网飞断断续续地断断续续回放着
*   DTS 声音与 Kodi 不兼容
*   Dolby 和 DTS 兼容接收机的 Kodi 问题消失了，现在唯一的选项是扬声器数量和直通(用于显示:支持杜比数字(AC3)的接收机；支持杜比数字加(E-AC3)的接收机；支持 DTS 的接收机；支持 TrueHD 的接收器；支持 DTS-HD 的 MM 接收器)
*   任何声音格式的声音解码仅在接收器上显示为 PCM(用于在 MM 上显示 Dolby、Dolby +、ProLogic II、DTS Sound、ATMOS)
*   从手机上断开 AndroidTV 远程应用程序后，屏幕键盘永远不会出现，除非盒子被重置
*   非官方的远程“确定”按钮在主屏幕上打开应用程序的上下文菜单，而不是直接打开应用程序
*   VLC 的 FLAC 文件，音乐播放器和 Google Play 音乐的声音抖动问题
*   创造性的 T30 无线扬声器的音量问题:只有 4 个较低的音量级别改变音量，在第 4 级，声音最大值已经在它的最大值。在第 4 级之后，有时会上升，然后回到上一级，但不会改变扬声器的有效音量。
*   android livechannel 中音频流(mp2)的解码问题
*   USB LAN 适配器无法识别/无法工作([https://Xiaomi . eu/community/threads/mi-box-Oreo-OTA-update-mi-USB-LAN-adaptor-stop-working . 44710/](https://xiaomi.eu/community/threads/mi-box-oreo-ota-update-mi-usb-lan-adaptor-stop-working.44710/))
*   Youtube -尽管音频正常，但所有视频都是绿屏[**升级到第一个内部测试版后发现问题]**

那么小米的下一步是什么？虽然我们可以期待在本周看到一个更新来修复两个更紧迫的问题，但在可预见的未来，那些使用 Plex 和 Kodi 的人将会有很多问题。我们只能希望修复很快到来，这次测试团队阻止小米发布另一个更新，这可能会使一些设备变得无用。不过，很大一部分功劳肯定要归功于小米论坛的马克胡克，因为没有他与小米自己一起讨论，就没有办法知道用户可能遭受了什么。

***感谢 XDA 会员 flipside101 的提示！***