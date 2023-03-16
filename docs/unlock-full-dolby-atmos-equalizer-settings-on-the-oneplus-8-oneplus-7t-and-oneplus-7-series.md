# 解锁一加 8、一加 7T 和一加 7 系列的杜比全景声均衡器设置

> 原文：<https://www.xda-developers.com/unlock-full-dolby-atmos-equalizer-settings-on-the-oneplus-8-oneplus-7t-and-oneplus-7-series/>

如今，智能手机制造商往往会提供某种数字音频优化，以增强其设备内置扬声器的性能。例如，一加与迪拉克研究公司合作，直到 T2 的一加 6T 的发布，但从一加 7 系列开始，他转向杜比全景声音频调谐。这些技术和解决方案中的大部分都是深入固件内部的，因此修改现有的预置通常需要 root 访问权限。然而，XDA 资深成员 [Rayekk](https://forum.xda-developers.com/member.php?u=6083771) 现在发现了一个简单的技巧(不需要 root 访问权限)来用一个功能更丰富的均衡器取代一加 7 Pro 上的准系统杜比全景声设置。我们已经在一加 8 和一加 8 Pro 上测试了该方法，没有任何问题，这一技巧也应该可以用于普通的一加 7 和一加 7T 系列手机。

**[一加七大论坛](https://forum.xda-developers.com/oneplus-7)| |[一加七大论坛](https://forum.xda-developers.com/oneplus-7-pro)|**

**[一加 7T 论坛](https://forum.xda-developers.com/oneplus-7t) ||| [一加 7T Pro 论坛](https://forum.xda-developers.com/7t-pro)**

**[一加八大论坛](https://forum.xda-developers.com/oneplus-8)| |[一加八大论坛](https://forum.xda-developers.com/oneplus-8-pro)|**

资深 OxygenOS 用户应该知道，一加只提供三种“基于场景的增强功能”，即“动态”、“电影”和“音乐”，作为这些手机中的杜比全景声均衡器预设。内置预置来自`com.oneplus.sound.tuner`包，它本身就是一个系统应用程序。你需要做的只是卸载当前用户的软件包，然后安装一个兼容的控制器应用程序，以释放手机的全部潜力。下面列出了这些步骤:

1.  按照[本指南](https://www.xda-developers.com/install-adb-windows-macos-linux/)设置 [ADB](https://www.xda-developers.com/install-adb-windows-macos-linux/) shell 访问。
2.  打开一加手机上的 USB 调试功能，并将其连接到 PC。
3.  执行以下 ADB 命令:

    ```
     <span >adb shell pm uninstall --user 0 com.oneplus.sound.tuner
    </span> 
    ```

4.  这将从主要用户配置文件中卸载纸张预设。现在你可以使用[这个链接](https://www.apkmirror.com/apk/razer-inc/dolby-atmos-4/dolby-atmos-4-dax2_2-6-0-28_r1-release/dolby-atmos-dax2_2-6-0-28_r1-android-apk-download/)下载从 Razer 手机的 Android 固件中提取的杜比 Atmos 均衡器。

与典型的第三方音频模块不同，新的均衡器与 OxygenOS 固件无缝集成。虽然您也可以使用此 ADB 命令恢复旧的预设:

```
 <span >adb shell cmd package install-existing com.oneplus.sound.tuner</span> 
```

...您应该事先移除其他 Dolby Atmos 应用程序，以避免潜在的冲突。

**[杜比全景声在运行 OxygenOS 的一加手机上解锁——XDA 讨论线程](https://forum.xda-developers.com/oneplus-7-pro/how-to/guide-dolby-atmos-control-how-to-real-t4103773)**

*特色图片演职员表:[杜比](https://www.youtube.com/watch?v=vkSN1F5EcVw)*