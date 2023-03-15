# 在 Nexus 6P、OnePlus 3/3T 和小米 Mi 5 上启用谷歌像素 AR 贴纸

> 原文：<https://www.xda-developers.com/enable-google-pixel-ar-stickers-nexus-5x-nexus-6p-oneplus-3-xiaomi-mi-5/>

谷歌 Pixel 智能手机(第一代和第二代)昨天获得了一个令人敬畏的新功能:[增强现实贴纸](https://www.xda-developers.com/googles-ar-stickers-pixel-and-pixel-2/)。这些 AR 贴纸允许用户将 3D 数字对象放入智能手机的相机取景器中。第一批 AR 贴纸以《星球大战》和《奇异事物》系列中的人物为中心，玩起来很有趣。该功能是谷歌 Pixel 智能手机的官方专属，然而，这并不意味着它不能被带到其他智能手机上。今天，我们将向您展示如何在任何运行 Android 8.1 的根 Nexus 6P 上启用 Google Pixel AR 贴纸。我们还将向您展示如何在 OnePlus 3、OnePlus 3T 和小米 Mi 5 上运行它，这要归功于我们论坛上一位开发人员的工作。

*谷歌的 AR 贴纸演示*

* * *

## 在运行 Android 8.1 的根 Nexus 6P 上启用 AR 贴纸

这怎么可能呢？这是因为 AR 贴纸被编码为只能在谷歌 Pixel 手机上工作，但这些限制实际上很容易被欺骗。反编译 AR 标签的 APK 会在 AndroidManifest 中显示以下代码行:

```
 <meta-data android:name="com.android.device.restriction" android:value="brand=google, deviceName=marlin; brand=google, deviceName=sailfish; brand=google, deviceName=walleye; brand=google, deviceName=taimen" /> 
```

如你所见，除非设备的品牌是“Google ”,设备名称是 marlin、sailfish、walleye 或 taimen 之一，否则应用程序不会运行。分别指的是谷歌的 Pixel XL、Pixel、Pixel 2 和 Pixel 2 XL。接下来，该应用的最低 SDK 版本是 27，这意味着它需要 Android 8.1 才能运行。幸运的是，Android 8.1 是为谷歌 Nexus 6P 正式提供的。

因此，我们需要做的是修改我们的设备名称，以匹配白名单中的一个设备型号。这需要 root 访问权限，因为我们将修改位于/system 中的 build.prop 文件中的属性。如果您的设备是 rooted 用户，请按照以下步骤启用 AR 贴纸:

1.  下载并安装 [ARCore](https://www.androidfilehost.com/?fid=962021903579498014) app 和 [AR 贴纸](https://www.androidfilehost.com/?fid=962021903579498012) app。我已经将它们上传到 AndroidFileHost，因为谷歌 Play 商店会将它们标记为与 Nexus 6P 不兼容。
2.  从 Play Store 下载并安装 [BuildProp 编辑器](https://play.google.com/store/apps/details?id=com.jrummy.apps.build.prop.editor)。
3.  查找并更改“ro.build.product”、“ro.product.name”、“ro.product.device”和“ro.product.model”，使其等于“marlin”
4.  重启你的手机
5.  下载[更多快捷方式](https://play.google.com/store/apps/details?id=com.ss.moreshortcuts) app。我们将使用它创建一个快捷方式来启动 AR 贴纸活动。
6.  打开应用程序，选择“**活动**”
7.  向下滚动，找到 AR 贴纸。展开它并点击“**主活动**”
8.  将快捷方式添加到您的启动器中。
9.  回到你的启动器，点击快捷方式启动 AR 贴纸！

* * *

## 在 OnePlus 3/3T 或小米米 5 上启用 AR 贴纸

XDA 资深会员[阿诺娃 8G2](https://forum.xda-developers.com/member.php?u=4860033) [修改了](https://forum.xda-developers.com/showpost.php?p=74824785&postcount=1944)AR 贴纸、AR 核心和谷歌相机 apk，使其可以在其他非谷歌设备上运行。

按照这些步骤在 OnePlus 3、OnePlus 3T 或小米 Mi 5 上启用 AR 贴纸。我自己没有测试过这个，但上面的视频显示它在小米 Mi 5 上工作，我们论坛上的几个用户报告说它在他们的 OnePlus 3/3T 上工作。

1.  安装修改后的 [ARCore](https://drive.google.com/open?id=1d4SIq_gSE-bbIj9ObWPWYjn5WLVNGif6) 和 [AR 贴纸](https://drive.google.com/open?id=1Z1KgNE5OhkLhbwy-XrGWCzJc2AcK0Ocz) APKs。
2.  下载 [calibration_cad.xml](https://drive.google.com/open?id=1Bo6q60EsJQlSUJ-ljfqlHmaomtbORYfs)
3.  安装 [MiXplorer](https://forum.xda-developers.com/showthread.php?t=1523691) 或者使用任何其他支持根的文件浏览器。
4.  将 calibration_cad.xml 移动到/system/etc。
5.  从 Play Store 下载并安装 [BuildProp 编辑器](https://play.google.com/store/apps/details?id=com.jrummy.apps.build.prop.editor)。
6.  打开它并添加这一行:ro . config . calibration _ CAD =/system/etc/calibration _ CAD . XML
7.  从[这里](https://www.celsoazevedo.com/files/android/google-camera/)安装以下修改的谷歌相机 apk 之一:GCam5_5.1.018、MGC_5.1.018 或谷歌相机 _5.1.018。
8.  打开谷歌相机，在菜单中寻找 AR 贴纸。

* * *

## 结论

享受星球大战和陌生人的东西增强现实贴纸在您的根设备！这种方法可能适用于这里没有提到的其他设备，但是您需要一个专用于您的设备的 calibration_cad.xml 文件。检查您的设备的特定 XDA 论坛，看看是否有人已经让它在您的模型上工作！

如果有人愿意在他们的设备上尝试这些变通方法，请这样做，并让我们知道它是否有效。谷歌的 AR 核心已经在三星 Galaxy S8 上运行，因此 AR 贴纸可能会正式进入其他设备。在此之前，这种非官方的方法是我们知道的唯一能够在其他设备上启用该功能的方法。

* * *

*本文已更新，以反映此处描述的方法目前不适用于谷歌 Nexus 5X。*