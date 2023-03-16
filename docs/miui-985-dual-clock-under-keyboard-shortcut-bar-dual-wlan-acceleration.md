# MIUI 9.8.5 增加了双时钟，并准备了键盘下快捷栏和“双 WLAN 加速”

> 原文：<https://www.xda-developers.com/miui-985-dual-clock-under-keyboard-shortcut-bar-dual-wlan-acceleration/>

小米使用 MIUI 测试版来测试即将推出的各种设备的功能，这些设备运行在他们基于 Android 的定制 UX 上。看到[未来](https://www.xda-developers.com/miui-always-on-display-xiaomi-redmi/)为用户准备了什么总是令人兴奋的，这些测试版让我们有机会观察[一些新的和即将到来的变化](https://www.xda-developers.com/xiaomi-mi-file-manager-updated-design-miui-beta/)。这些测试版也给了我们一些线索，让我们知道未来的设备会有什么样的功能，比如[反向无线充电功能](https://www.xda-developers.com/xiaomi-reverse-wireless-charging-miui-beta/)。最新的 MIUI 9.8.5 测试版透露，小米计划在屏幕键盘下方添加一个快捷栏，以及一个名为“双 WLAN 加速”的双 Wi-Fi 连接功能。最新的测试版还为其时钟小工具增加了双时钟功能。

## 双时钟

双时钟功能是小米自己通过他们的 [MIUI 微博账号](https://www.weibo.com/1786860821/I0PUS95ia)直接确认的。

在最新的测试版中，你可以通过设置>更多设置>日期和时间>双重时钟来为主屏幕时钟小工具启用双重时钟。拥有这个特性是很方便的，尤其是当你需要与世界上不同地方的人进行协调时。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些功能目前在 live build 中没有实现，可能会在未来的 build 中随时被小米拉出来。

## 键盘下的快捷栏

在 MIUI 9.8.5 中，我们还发现了表明小米正计划在键盘下方的快捷栏中添加的字符串。

```
 <string name="raise_bottom_height_of_keyboard">Enhanced</string>
<string name="raise_bottom_height_of_keyboard_sub_title">A bar with customizable shortcuts will appear under the keyboard if you switch to Enhanced mode</string>
<string name="raise_bottom_height_of_keyboard_title">Adjust keyboard to full screen display</string> 
```

快捷栏将增加一些快捷方式，每次虚拟键盘出现在屏幕上时，这些快捷方式都很容易访问。这些捷径是什么现在还不知道；但是可能的猜测包括剪切、复制和粘贴的快捷方式，以及其他基于文本编辑的操作。这些快捷方式也可以用于快速启动其他应用程序，但考虑到上下文，这样的选项似乎有点反直觉。

## 双 Wi-Fi /双 WLAN 加速

双 Wi-Fi 连接最近已经成为一个话题。[联发科 Helio G90 系列 SOC](https://www.xda-developers.com/mediatek-helio-g90-series-hyperengine-game-technology-launched/)将双 Wi-Fi 连接作为联发科超引擎游戏技术的一大亮点。Oppo 还[最近宣布双 Wi-Fi 连接](https://www.xda-developers.com/oppo-qualcomm-game-color-plus-dual-wi-fi-technology-mobile-gaming/)是 Oppo Reno 设备的一大亮点。最新测试版中的 Strings 表明小米也在研究类似的功能。

```
 <string name="slavewifi">Dual WLAN</string>
<string name="slavewifi_disconnect">Disconnect</string>
<string name="slavewifi_notification_title">Dual WLAN acceleration</string>
<string name="slavewifi_settings">Tap to modify configuration</string> 
```

根据我们的理解，双 WLAN 加速将允许智能手机同时连接到两个 Wi-Fi 波段或两个路由器。这将提升设备的整体连接速度，改善网络体验。这对于下载大文件和玩游戏特别有用。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*