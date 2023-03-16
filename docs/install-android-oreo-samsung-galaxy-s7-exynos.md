# 如何在三星 Galaxy S7/S7 Edge 上安装 Android Oreo(exy nos)

> 原文：<https://www.xda-developers.com/install-android-oreo-samsung-galaxy-s7-exynos/>

Exynos 三星 Galaxy S7 和 Galaxy S7 Edge 的官方 Android 奥利奥昨天开始推出。当三星发布设备更新时，他们通过 CSC(国家特定代码)发布更新。该更新已推出到 BTU CSC，这是英国解锁版本。XDA 论坛成员 Silver [King](https://forum.xda-developers.com/member.php?u=9008521) 制作了 TWRP 备份，这样任何人都可以在自己的设备上安装奥利奥。

这是适用于 Exynos 三星 Galaxy S7 设备的 Android 8.0 Oreo 的首次发布，它带来了一系列新功能和改进。除了 Android Oreo 带来的所有新功能，如[画中画模式](https://www.xda-developers.com/picture-in-picture-mode-desktop-google-chrome/)、[通知频道](https://www.xda-developers.com/notification-importance-controls-all-apps-android-oreo/)、[后台应用优化](https://www.xda-developers.com/android-oreo-oem-background-app-limitations/)、[通知休眠](https://www.xda-developers.com/customize-notification-snooze-duration-android-oreo/)等等，还有大量针对三星的变化[三星体验 9.0](https://www.xda-developers.com/samsung-experience-9-0-beta-android-oreo-features/) 。本次更新还包含了三星的 Bixby。

随着三星 Experience 9.0 的推出，新键盘内置了贴纸和 gif，三星 Galaxy Note 8 的应用程序对功能，此前仅适用于 S7 Edge，等等。该版本带有最新的四月安全补丁。此次更新还带来了对覆盖管理器服务(OMS)的本地支持，即底层背后的[主题框架。以前，](https://www.xda-developers.com/custom-themes-android-oreo-substratum/) [Sungstratum](https://www.xda-developers.com/sungstratum-samsung-substratum-touchwiz/) 插件是应用自定义主题所必需的，但现在你应该过渡到更稳定的仙女座插件。

如果您正在使用另一个 CSC 值，并希望此更新，您可以使用我们下面的指南安装它。这将需要一个解锁的引导加载程序和 TWRP。Galaxy S7 和 S7 Edge 发布已经两年多了，所以你可能不必担心保修失效，解锁引导程序就可以了。然而，请记住，**解锁引导程序将会触发 Knox** ，使 Samsung Pay 和 Secure Folder 等应用程序无法运行。

## 在 Exynos 三星 Galaxy S7/S7 Edge 上安装 Android Oreo

### 如何在手机上安装 TWRP:

1.  转到设置，然后转到关于设备。点击内部版本号 7 次以启用开发者选项。进入开发者选项，启用 USB 调试和 OEM 解锁设置。
2.  在你的 Windows PC 上，确保你已经先安装了的 [ADB。打开计算机上的命令提示符，键入命令`adb reboot bootloader`。](https://www.xda-developers.com/install-adb-windows-macos-linux/)
3.  为你的手机下载奥丁 3.12.7 和 TWRP 的图片。这是给 [Galaxy S7](https://dl.twrp.me/herolte) 的，这是给 [Galaxy S7 edge](https://dl.twrp.me/hero2lte) 的。使用列表中的最新版本。
4.  打开 Odin 并选择 AP 选项卡，然后为您的设备选择 TWRP 文件。
5.  单击开始。一旦您单击开始，您将无法撤消启动加载程序解锁。**这会使 Knox 出错，使 Samsung Pay 和 Secure Folder 无法工作。**
6.  你的手机将重新启动系统。

### 如何在装有 TWRP 的设备上安装 Android Oreo:

1.  下载下面链接的文件。您将需要提取系统的 zip 文件。对于 Magisk v16.4 和 no-verify-opt-encrypt-6.0 zip 文件，不要提取它们并将所有文件传输到您的手机。
2.  在电脑上打开 CMD，输入`adb reboot recovery`
3.  选择一旦 TWRP 打开，选择恢复，然后您提取到您的手机文件。
4.  一旦他们恢复，你将会想要回到 Odin 的主屏幕并且点击安装标签。
5.  S7 Edge 用户，忽略此步骤。S7 用户，刷新 S7oreoboot.zip、no-verify-opt-encrypt-6.0 和 Magisk v16.4。
6.  S7 Edge 用户闪存 no-verify-opt-encrypt-6.0 和 Magisk v16.4。
7.  当你刷新它们时，选择擦除缓存/dalvik。
8.  返回主屏幕，然后选择擦除。滑动底部写着“刷卡恢复出厂设置”的滚动条这将删除您的数据，但如果您不这样做，您的手机将无法正常启动。完成后，单击重启系统。
9.  在这之后，你将运行 Android Oreo，并以 Magisk v16.4 为根。

[**系统还原文件为 S7**](https://mega.nz/#!URswBJ5A!ThOBn4u7dZYQGEo6BueKCtL-BS1gqzsLgMWlSaYrJ-c) [**S7 奥利奥启动镜像**](https://mega.nz/#!IZ1AGapC!01Jtsp1_H05-aOvUWsWqYkiEUBjOYxE7uwHHhNR7tQM) [**系统还原文件为 S7 edge**](https://mega.nz/#!URswBJ5A!ThOBn4u7dZYQGEo6BueKCtL-BS1gqzsLgMWlSaYrJ-c)[**Magisk v 16.4**](https://forum.xda-developers.com/attachment.php?attachmentid=4490349&d=1525170444)[**no-verify-opt-encrypt-6.0 . zip**](https://forum.xda-developers.com/attachment.php?attachmentid=4490348&d=1525170444)