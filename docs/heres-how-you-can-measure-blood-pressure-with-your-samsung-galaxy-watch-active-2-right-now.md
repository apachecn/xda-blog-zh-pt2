# 使用您的三星 Galaxy Watch Active 2 测量血压

> 原文：<https://www.xda-developers.com/heres-how-you-can-measure-blood-pressure-with-your-samsung-galaxy-watch-active-2-right-now/>

# 以下是如何立即用三星 Galaxy Watch Active 2 测量血压的方法

三星为 Galaxy Watch Active 2 开发的血压应用程序和智能手机配套应用程序已经过修改，可以在全球单位上进行侧加载。请继续阅读！

三星尚未在 Galaxy Watch Active 2 上启用期待已久的[心电图支持，但该公司确实在几周前](https://www.xda-developers.com/samsung-galaxy-watch-active-2-still-working-ecg-support/)[宣布了使用可穿戴设备的](https://www.xda-developers.com/samsung-galaxy-watch-active-2-blood-pressure-monitoring-app-feature/)无袖带血压监测和跟踪。不过，有一个问题，因为整个功能以及配套应用程序(三星健康监测器)目前只在韩国获得批准。虽然三星计划在今年第三季度内进入全面上市阶段，但 XDA 高级成员 [adfree](https://forum.xda-developers.com/member.php?u=1030585) 和其他几位修补者已经找到了一种方法，通过禁用区域锁定机制，在你的 Galaxy Watch Active 2 上下载血压监测插件，并在你的手机上安装配套应用程序(即使是非三星型号)。

**免责声明:**Galaxy Watch Active 2 的这一特殊功能可能尚未获得当地政府的批准。**不要**试图将手表作为认可医疗设备的替代品。尝试自担风险！

Galaxy Watch Active 2 运行 Tizen OS，因此侧装过程与 Android 世界略有不同。请极其小心地按照下面列出的步骤激活手表上的血压测量功能:

*   从本帖的[下载修改后的应用程序。](https://forum.xda-developers.com/showpost.php?p=82502465)
*   在 Galaxy Watch Active 2 上启用调试和“开发者选项”，然后将手表与 Wi-Fi 连接。您的电脑和手表应该在同一个网络上。
*   下载并安装带有 IDE 的最新版本 [TizenStudio。](https://developer.tizen.org/development/tizen-studio/download)
*   启动 TizenStudio，你会看到一个写着“无目标”的框。点击下拉菜单并选择“启动远程设备管理器”。然后点击“扫描”，你就会找到你的手表。在这一阶段，你需要点击“开启连接”按钮，接受手表上的连接。

*   一旦连接上，您就可以使用[智能开发桥](https://developer.tizen.org/development/tizen-studio/web-tools/running-and-testing-your-app/sdb) (SDB)二进制文件安装 **TPK** 文件(例如手表的插件包)。侧装命令应该是`sdb install NAME_OF_THE_TPK.tpk`。
    *   如果你得到一个 SDB 服务器和客户端不匹配，你可以忽略它，只要你看到 install_percent 达到 100 应用程序将显示在你的手表上。
*   在你的手机上安装 **APK** 。只要你在手表上启动血压应用程序，它就会提示你从手机上继续。从那里，它们将自动链接并正常工作。

您可以访问[讨论主题](https://forum.xda-developers.com/smartwatch/galaxy-watch/ecg-bp-gwa2-t4051141)了解更多信息。我们再次提醒您，不要用 Galaxy Watch Active 2 替代任何经批准的医疗设备。请自行决定是否使用这种修改。

* * *

**图片来源:r/GalaxyWatch ( [1](https://www.reddit.com/r/GalaxyWatch/comments/gh9bda/i_successfully_installed_the_blood_pressure_app/) ， [2](https://www.reddit.com/r/GalaxyWatch/comments/ghjuo9/good_job_samsung_its_quite_close_i_hope_after/) )**