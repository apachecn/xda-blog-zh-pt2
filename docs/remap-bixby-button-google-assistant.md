# 如何在三星 Galaxy S10、Note 9 和其他 One UI 设备上将 Bixby 重新映射到谷歌助手

> 原文：<https://www.xda-developers.com/remap-bixby-button-google-assistant/>

在三星 Unpacked 上，三星宣布了他们的新[三星 Galaxy S10 系列](https://www.xda-developers.com/samsung-galaxy-s10-s10-and-s10e-launch-with-the-snapdragon-855-ultrasonic-in-display-fingerprint-scanners-reverse-wireless-charging-and-a-whole-lot-more/)和 [Galaxy Fold](https://www.xda-developers.com/samsung-galaxy-fold-new-video/) 。在媒体发现 Bixby 中的一个新选项后，三星证实该按钮将是原生可重新映射的。随着今天在旧的 One UI 设备上发布的 Bixby 应用程序的[更新](https://www.xda-developers.com/samsung-galaxy-s10-plus-bixby-button-remapping-update/)，这终于成为可能。然而，这并不全是好消息。三星正在限制你可以通过该按钮启动的应用程序。这意味着 Bixby 按钮[无法原生启动谷歌助手](https://www.xda-developers.com/samsung-remap-bixby-button-google-assistant/)，但我们有一个解决方案。

三星将其他助手应用程序列入黑名单，禁止该按钮使用。这包括亚马逊 Alexa 和微软 Cortana 以及谷歌助手。我们可以通过使用 Tasker 脚本并将其导出为 APK 来解决这个问题。这意味着你需要做的就是安装应用程序，在设置中选择它，然后按下按钮选择谷歌。

这款应用也不仅仅支持谷歌助手。我们也能够推出 Cortana 应用程序，但它不能与亚马逊 Alexa 兼容。理论上，任何支持回答语音命令的 app 都可以用这种方法重新映射到按钮上。任何支持 Bixby 按钮重映射的手机，包括 Galaxy S10/S10+/S10e、Galaxy S9/S9+以及 Galaxy Note 9 和 Galaxy Note 8 [都将支持使用助手](https://www.xda-developers.com/samung-galaxy-note-9-bixby-remapping/)。

## 使用 Bixby 按钮助手重新映射 Bixby

1.  下载 [Bixby 按钮助手重新映射 APK](https://www.androidfilehost.com/?fid=1395089523397903362)
2.  安装应用程序
3.  打开 **Bixby 语音设置**
4.  选择 **Bixby 键**
5.  选择**双击打开 Bixby**
6.  选择**使用单按**
7.  打开并点击齿轮图标来选择一个应用程序
8.  找到 **Bixby 按钮助手重映射器**并选择它
9.  按下物理 Bixby 按钮并选择您想要使用的助手应用程序(点按“总是”,这样它就不会每次都询问)
10.  就是这样！

通过设置 Bixby 快速命令，也可以在没有所需应用程序的情况下做到这一点。你只需设置一个快捷命令“打开助手”不过，我会推荐 app 方法。在我对 quick command 的测试中，它没有那么快，而且只在大约 20%的时间里有效。其他用户报告了非常可靠的结果，因此您的里程可能会有所不同。

## 使用快捷命令将 Bixby 重新映射到谷歌助手

1.  打开 **Bixby 语音**
2.  转到 Bixby 下拉菜单中的**快速命令**
3.  创建一个新的**快速命令**并将其命名为“助手”
4.  将快速命令词或短语设置为**“助手”**
5.  选择**“键入命令”**
6.  在此设置中，**键入“打开助手”**
7.  保存这个**快速命令**
8.  转到 **Bixby 语音设置**
9.  选择 **Bixby 键**
10.  选择**双击打开 Bixby**
11.  选择**快速命令**
12.  进入**快捷命令选项，选择“助手”**
13.  就是这样！

很高兴三星终于允许用户在 Galaxy S10、Galaxy Note 9 和其他 One UI 设备上将按钮重新映射到其他东西。虽然你不能完全禁用 Bixby，但你可以将其降级为双击，并将你喜欢的应用程序放在最前面。希望三星未来不要做任何事情来打破这个变通办法。