# 如何在美国电话电报公司三星 Galaxy S7 & S7 Edge 上安装预发布的 Android Oreo

> 原文：<https://www.xda-developers.com/how-to-install-pre-release-android-oreo-on-the-att-samsung-galaxy-s7-s7-edge/>

Android Oreo 在几个月前发布，但三星最终批准了[三星 Galaxy S8](https://forum.xda-developers.com/galaxy-s8) /S8+的[官方发布](https://www.xda-developers.com/samsung-galaxy-s8-android-oreo-project-treble/)。最近，Exynos 三星 Galaxy S7 Edge [的一个版本](https://www.xda-developers.com/samsung-galaxy-s7-edge-android-oreo-samsung-experience-9/) [Android Oreo](https://www.xda-developers.com/android-8-0-oreo-google-released/) 被泄露，可以作为定制 ROM 安装在我们的论坛上。现在，三星 Galaxy S7/S7 Edge 的 Android 8.0 版本已经推出。

这是骁龙三星 Galaxy 设备首次发布 Android 8.0，它带来了一系列新功能和改进。除了 Android Oreo 带来的所有新功能，如[画中画模式](https://www.xda-developers.com/picture-in-picture-mode-desktop-google-chrome/)、[通知频道](https://www.xda-developers.com/notification-importance-controls-all-apps-android-oreo/)、[后台应用优化](https://www.xda-developers.com/android-oreo-oem-background-app-limitations/)、[通知休眠](https://www.xda-developers.com/customize-notification-snooze-duration-android-oreo/)等等，还有许多三星特有的变化[三星体验 9.0](https://www.xda-developers.com/samsung-experience-9-0-beta-android-oreo-features/) 。本次更新还包含了三星的 Bixby。

随着三星 Experience 9.0 的推出，一个内置贴纸和 gif 的新键盘、三星 Galaxy Note8 的[应用对](https://www.xda-developers.com/galaxy-note-8-software-spen-apps/)功能(此前仅用于 S7 Edge)等等。该版本带有最新的[二月安全补丁](https://www.xda-developers.com/february-android-pixel-security-bulletins-factory-images-otas/)，因此所有最近披露的主要安全漏洞，如 [BlueBorne](https://www.xda-developers.com/bluetooth-vulnerability-blueborne-impacts-android-ios-windows-and-linux-devices/) 、 [KRACK](https://www.xda-developers.com/wpa2-wifi-protocol-vulnerability-krack/) 和 [Spectre/Meltdown](https://www.xda-developers.com/android-security-bulletin-january-2018-ota-factory-images/) 都已修复。此次更新还带来了对覆盖管理器服务(OMS)的本地支持，这是 Substratum 背后的主题引擎。之前， [Sungstratum](https://www.xda-developers.com/sungstratum-samsung-substratum-touchwiz/) 插件是应用自定义主题所必需的，但是现在你应该过渡到 [Andromeda 插件](https://www.xda-developers.com/andromeda-substratum-50-percent-sale/)了，它更加稳定。

想在你的 [AT & T 三星 Galaxy S7](https://forum.xda-developers.com/att-galaxy-s7) 或者 [S7 Edge](https://forum.xda-developers.com/att-s7-edge) 上安装这个更新？嗯，你很幸运，因为这个更新是从 ATT 的服务器上下载的，非常安全。此更新不是测试版，而是预发布版本，因此可能不稳定。目前，安装它的唯一方法是如果你有 Galaxy S7 或 S7 Edge 的最新更新。不幸的是，目前没有 Odin 版本可以闪现，所以这是唯一的方法。如果你觉得这个不稳定，想卸载，可以用 [Odin](https://drive.google.com/uc?authuser=0&id=1OU3pY0UC8aQxlCN1BLXCrl-ZOiVbFkS4&export=download) 里的这个文件给 [S7 edge](https://drive.google.com/uc?id=1L9QZvTvsUQIXGSgAHGDgsIxDTehtO15G&export=download) 用，这个给 [S7](https://androidfilehost.com/?fid=673791459329073619) 用。

## 如何在美国电话电报公司三星 Galaxy S7/S7 Edge 上安装带有三星体验 9.0 的 Android Oreo

1.检查你的手机型号。即使您可能知道您是否有 Galaxy S7 或 S7 edge，这也是为了确保这是您正在使用的美国电话电报公司型号，因此请转到“设置”,然后在“关于设备”和“型号”下确保它与 SM-G930A 或 SM-G935A 匹配。

2.如果你有 Galaxy S7，[下载这个文件](https://samsung.firmware.science/download?url=48782/1488/SS-G930AUCS4BRA1-to-U4CRB5-UP)。如果你有 Galaxy S7 edge，[下载这个文件](https://samsung.firmware.science/download?url=48775/1488/SS-G935AUCS4BRA1-to-U4CRB5-UP)。

3.如果您有 SD 卡，请继续下面的 SD 卡部分。如果您没有 SD 卡，请遵循无 SD 卡部分。

#### 带 SD 卡

4.将设备的 update.zip 文件传输到 SD 卡

5.按住音量键+主屏幕键+电源键进入恢复模式

6.选择“从 SD 卡应用更新”您可以使用音量摇杆进行导航，使用电源按钮进行选择。选择该选项后，找到名为“update.zip”的文件，并使用电源按钮选择它。

7.等待你的手机重新启动，然后它将运行 Android 奥利奥！

#### 不带 SD 卡

4.按住音量键+主屏幕键+电源键进入恢复模式

5.选择“应用来自 [ADB](https://www.xda-developers.com/install-adb-windows-macos-linux/) 的更新”您可以使用音量摇杆进行导航，使用电源按钮进行选择。

6.在你的电脑上，打开命令提示符并键入 adb sideload <file path="" to="" update.zip="">如果你还没有设置 adb，那么你可以按照[这些快速的指令集](https://www.xda-developers.com/install-adb-windows-macos-linux/)来加快速度。</file>

7.等待你的手机重新启动，然后它将运行 Android 奥利奥！