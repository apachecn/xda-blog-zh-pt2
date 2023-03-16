# 如何在 Realme X2 Pro 上的每个应用程序中强制 90Hz 模式[Root]

> 原文：<https://www.xda-developers.com/how-to-force-90hz-mode-in-every-app-on-the-realme-x2-pro-root/>

即使在 2020 年，Realme X2 Pro 无疑是你能买到的价格最好的旗舰级智能手机之一。这款手机由高通骁龙 855+ SoC 供电，提供令人印象深刻的四摄像头设置，疯狂快速的 50W 充电，以及 90Hz 的高刷新率显示。用户可以自由选择 60Hz 和 90Hz 的刷新率，但 90Hz 模式实际上仅限于少数第三方应用程序。我们自己的[图沙尔·梅塔](https://www.xda-developers.com/author/tusharmehta/)尝试了著名的 ADB 命令技巧，从一加 7 Pro/7T/7T Pro 到[在所有应用程序中随时解锁 90Hz 模式](https://www.xda-developers.com/oneplus-7-pro-true-90hz-display-mode/)，却发现[在 Realme X2 Pro 上不起作用](https://www.xda-developers.com/realme-x2-pro-xda-review/)。这显然是事实，因为 X2 Pro 不运行 OxygenOS，而是运行 ColorOS/Realme UI。

**[Realme X2 职业论坛](https://forum.xda-developers.com/realme-x2-pro)**

不过，好消息是，Realme 在 Realme X2 Pro 的固件中留有一个隐藏的命令，可以被用来解锁该设备上的一个持续 90Hz 模式。XDA 承认开发商 [phhusson](https://forum.xda-developers.com/member.php?u=1915408) 实际上在二月份就设法[发现了](https://github.com/phhusson/treble_experimentations/issues/1113#issuecomment-588467405)所需的参数。你需要摆弄一个名为 [SurfaceFlinger](https://source.android.com/devices/graphics) 的 Android 服务，尽管你必须从 ADB shell 或一个终端模拟器应用程序执行下面显示的命令。这个命令需要在每次启动时执行。

```
 su -c service call SurfaceFlinger 1035 i32 0 
```

如果你在你的 Realme X2 Pro 上运行 phhusson 的最近版本的[自定义 AOSP 项目高音 GSI](https://www.xda-developers.com/custom-aosp-project-treble-gsi-gets-updated-with-june-2020-security-patches-netflix-hd-support-for-the-xiaomi-mi-9-and-redmi-note-9s-and-more/) ，那么你可以在 phhusson 的高音设置应用程序的“杂项”设置中找到一个“强制 FPS”选项，它可以做上面提到的同样的事情。您可以单独[下载相关 app](https://treble.phh.me/treble-app-90fps.apk) ，但在现货 [Realme UI](https://www.xda-developers.com/realme-x2-pro-android-10-stable-update-realme-ui/) 下可能会起作用。

**[在 Realme X2 专业版——XDA 讨论帖](https://forum.xda-developers.com/realme-x2-pro/how-to/force-90hz-root-t4109761)** 上的每个应用中强制 90Hz 模式

如果你特别想让 Realme X2 Pro 上的 player unknown ' s BattleGrounds(PUBG)手机的刷新率达到 90Hz，XDA 资深会员 [rkmadotra](https://forum.xda-developers.com/member.php?u=5672720) 已经推出了一个方便的 Magisk 模块。检查内部结构后，似乎该模块只是用该文件的修改版本替换了`/system/etc/refresh_rate_config.xml`,将 PUBG Mobile 包设置为 90Hz 显示模式。

**[PUBG Mobile 全球 90Hz Enabler for the Realme X2 Pro—XDA 下载与讨论线程](https://forum.xda-developers.com/realme-x2-pro/themes/realme-ui-90-fps-enabler-pubg-mobile-t4112509)**

Realme UI 和 ColorOS 在智能手机上都有这种特殊的文件，其显示面板的刷新率高于 60Hz。操作系统检查该列表中的包，以决定以何种刷新率模式运行显示器。例如，这个文件确实存在于 [OPPO Find X2](https://www.xda-developers.com/oppo-find-x2-specifications-features-pricing-availability/) 和 [Realme X3 SuperZoom](https://www.xda-developers.com/realme-x3-superzoom-snapdragon-855-plus-120hz-refresh-rate-display/) 上，尽管这两款设备不能以 90Hz 运行，因为它们只有 60Hz 和 120Hz 显示模式。