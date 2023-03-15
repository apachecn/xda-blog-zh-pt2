# 如何在亚马逊 Fire 7、HD 8 或 HD 10 上禁用 Alexa 并获得“Ok Google”

> 原文：<https://www.xda-developers.com/replace-alexa-google-assistant-amazon-fire-7-hd-8-hd-10/>

和谷歌助手一样，Alexa 是一款基于云的语音助手，允许你使用自然语言识别与你的设备进行交互。这款助手为亚马逊的 Echo 系列、Fire TV 和 Fire 平板电脑等设备提供支持。如果你购买了亚马逊 Fire 设备，你可能会意识到该操作系统实际上是基于 Android 的，这意味着你可以在其上运行常规的 Android 应用程序。正因为如此，实际上可以禁用亚马逊 Alexa，并用谷歌助手取代它——嗯，至少是“Ok Google”检测部分！

## 背景

亚马逊设备运行的 [FireOS 是 Android](https://en.wikipedia.org/wiki/Fire_OS) 的大幅修改版本，最初基于 Lollipop 5.1.1。一些较新的亚马逊 Fire 设备可能运行 FireOS 版本，这也是 Android 的一个重大修改版本，但基于 Nougat 7.0。较老的设备，如 [Kindle 8.9，第二代](https://forum.xda-developers.com/kindle-fire-hd)，运行的是安卓系统的一个重大修改版本，冰激凌三明治 4.0。任何装有 5.1.1 版本的亚马逊设备都只能在“Ok Google”级别体验谷歌助手。这是谷歌而不是亚马逊设置的限制。

目前完整的谷歌助手仅支持部分运行棉花糖 6.0 的设备，但在大多数运行牛轧糖 7.0 及以上版本的设备上可用。谷歌有望在今年的某个时候推出棒棒糖设备的全面助手应用。

如果你拥有一台亚马逊平板电脑或设备，如 [Fire Phone](https://forum.xda-developers.com/fire-phone) 、 [Echo](https://forum.xda-developers.com/connected-home) 或 [Fire TV](https://forum.xda-developers.com/fire-tv) ，那么你可以使用本指南禁用 Alexa，并代之以“Ok Google”语音检测。

## 先决条件

要做到这一点，你至少需要安装谷歌应用程序，并能够将你的设备接入电脑，通过 ADB 运行命令。[本指南适用于亚马逊 Fire 7、HD 8 和 HD 10 平板电脑](https://forum.xda-developers.com/amazon-fire/general/how-to-install-google-play-store-fire-t3486603)。如果你的设备运行 Fire OS 5.6.0.0，你可以按照这个指南通过[获得 root 权限。如果你足够幸运，拥有一台 Kindle Fire HD 8.9，你将无法安装所需的 Play Store APKs，但你可以获得 root 访问权限，安装](https://forum.xda-developers.com/hd8-hd10/general/tut-fire-hd-10-7th-gen-2017-root-box-t3726443) [TWRP](https://twrp.me/about/) ，并闪存一个定制的 ROM。[跟随我的指导开始](https://forum.xda-developers.com/kindle-fire-hd/8-9-inch-help/guide-root-custom-recovery-roms-jem-t3696244)。

重要的是要一步一步地遵循特定于您的设备的指南。以下是安装 Play Store 所需的 Google APKs 的单独链接:

1.  [谷歌客户经理](https://www.apkmirror.com/apk/google-inc/google-account-manager/google-account-manager-5-1-1743759-release/google-account-manager-5-1-1743759-android-apk-download/)
2.  [谷歌服务框架](https://www.apkmirror.com/apk/google-inc/google-services-framework/google-services-framework-5-1-1743759-release/google-services-framework-5-1-1743759-android-apk-download/)
3.  [Google Play 服务](https://www.apkmirror.com/apk/google-inc/google-play-services/google-play-services-11-5-09-release/google-play-services-11-5-09-230-164803921-android-apk-download/) **(如果你拥有 HD 8 或 HD 10，2017 版，[你需要这个 APK](https://www.apkmirror.com/apk/google-inc/google-play-services/google-play-services-11-5-09-release/google-play-services-11-5-09-240-164803921-android-apk-download/) 。)**
4.  [谷歌 Play 商店](https://www.apkmirror.com/apk/google-inc/google-play-store/google-play-store-8-3-41-release/google-play-store-8-3-41-u-all-0-fp-170066753-android-apk-download/)

你不需要在这些设备上安装一个定制的启动器来成功完成本指南。

有一个特定的权限，当放在应用程序的清单文件中时，允许应用程序更改 Android 平台中的三类设置。这个被称为`WRITE_SECURE_SETTINGS`的许可允许应用程序[读取或写入安全系统设置。](https://developer.android.com/reference/android/Manifest.permission.html#WRITE_SECURE_SETTINGS)“这些设置也可以通过 Android 调试桥(ADB)进行编辑和修改。修改这些设置**不需要 root 权限**。

下面是在你的亚马逊 Fire 设备上启用“Ok Google”支持的详细指南。如果您更喜欢手动方式，请参阅一般指南下面的“使用 ADB 手动设置助理应用程序”。

* * *

## 如何在亚马逊 Fire 7、HD 8 和 HD 10 上启用“Ok Google”

1.一旦你设置好 Google APKs 并安装了 Google App，从 Play Store 下载并安装“设置数据库编辑器”。

2.将设备插入 PC，打开终端或命令提示符窗口。在下面键入以下命令。如果成功，您将不会看到任何文本:

```
 adb shell pm grant by4a.setedit22 android.permission.WRITE_SECURE_SETTINGS 
```

3.现在打开“设置数据库编辑器”并点击“安全”标签。在该选项卡中，找到以下代码行:

```
 voice_recognition_service 
```

该行右侧的值应为:

```
 com.google.android.googlequicksearchbox/com.google.android.com.google.android.voicesearch.serviceapi.GoogleRecognitionService 
```

4.现在我们要添加几行代码。在“设置数据库编辑器”中，滚动到“安全”选项卡的顶部。在顶部，点击“添加新设置”

5.在第一个框中键入:

```
 assistant 
```

6.在第二个框中键入:

```
 com.google.android.googlequicksearchbox/com.google.android.voiceinteraction.GsaVoiceInteractionService 
```

7.现在找到这行代码:

```
 alexa_enabled 
```

该行右边的值应该是**‘1’**。点击设置**用 **0** 替换 **1** 中的**，然后点击保存。这将**禁用 Alexa** 。参考:0 =禁用，1 =启用，2 =切换(尽管切换不太可能出现在您的设置菜单中。这是因为您的提供商和/或制造商禁止使用他们自己不添加的开关)。

 **8.停留在“安全”标签，向下滚动靠近底部。查找代码行:

```
 voice_interaction_service 
```

它右边的值应该为空。点击设置，添加以下文本行(无空格)并点击保存:

```
 com.google.android.googlequicksearchbox/com.google.android.voiceinteraction.GsaVoiceInteractionService 
```

9.确保您已登录谷歌，打开谷歌应用程序。如果您使用的是最新版本，请点击屏幕右下角的三个栏。轻按“设置”，然后轻按“语音”。在右边，点击“Ok Google detection ”如果可以的话，训练你的声音。您可能需要下载其他谷歌应用程序，如 Gmail 或地图，以便获得所有可用的语音选项。

10.一旦你完成了所有这些，回到你的主屏幕。如果激活，只需说“好的谷歌。”如果搜索栏变得栩栩如生，只需说出你的搜索查询。您的助手现在处于活动状态！

### 禁用亚马逊应用商店

为了让您的设备在推出棒棒糖设备时准备好接受完整的谷歌助手，您可以加入谷歌 Play 服务和谷歌应用程序测试计划。然而，为了做到这一点，你必须禁用亚马逊应用商店和 OTA 更新，但这[只能在 FireOS 版本](https://forum.xda-developers.com/amazon-fire/general/root-required-remove-amazon-bloatware-t3636797)[5 . 4 . 0 . 0 和更低版本](https://forum.xda-developers.com/amazon-fire/general/root-required-remove-amazon-bloatware-t3636797)上实现。以下步骤将指导您禁用亚马逊应用商店，但请注意，**您将无法重新启用它，除非您进行工厂重置**。

要禁用亚马逊应用商店，请将您的设备插入 PC，然后打开终端或命令提示符窗口。在下面键入命令。如果成功，您将在命令后看到“成功”:

```
 adb shell pm uninstall -k --user 0 com.amazon.venezia 
```

要禁用 OTA 更新，请运行以下命令:

```
 adb shell pm uninstall -k --user 0 com.amazon.device.software.ota
adb shell pm uninstall -k --user 0 com.amazon.kindle.otter.oobe.forced.ota 
```

完成后，[访问此链接加入 Google Play 服务测试计划](https://play.google.com/apps/testing/com.google.android.gms)和[访问此链接加入 Google App 测试计划。](https://play.google.com/apps/testing/com.google.android.googlequicksearchbox)

现在等几分钟，打开游戏商店。去谷歌应用页面看看你是否是一个测试者。如果你注册了该项目，你可能需要更新谷歌应用程序，但只有在你成功成为测试者后才能这样做。

或者，您可以使用 ADB 添加和修改这些设置，以及您在设置数据库编辑器应用程序的三个选项卡中看到的任何其他设置。请注意，如果您更改了任何设置，而您不知道这些设置的作用，您可能会将您的设备砖化。建议使用上述方法来实现这一目标。对于更加手动的方法，请遵循以下步骤。如果您习惯使用 ADB，请仅使用手动方法。

### **使用 ADB 手动设置助手应用**

将您的设备插入 PC，打开命令提示符/终端窗口，键入以下命令，并在每个命令后按 enter 键。如果成功，当命令提示符返回时，您将看不到任何文本:

```
 adb shell settings put secure assistant com.google.android.googlequicksearchbox/com.google.android.voiceinteraction.GsaVoiceInteractionService
adb shell settings put secure voice_interaction_service com.google.android.googlequicksearchbox/com.google.android.voiceinteraction.GsaVoiceInteractionService
adb shell settings put secure voice_recognition_service com.google.android.googlequicksearchbox/com.google.android.voicesearch.serviceapi.GoogleRecognitionService
adb shell settings put secure alexa_enabled 0 
```

有了这些设置，一旦 Google Assistant 部署到 Lollipop 设备上，您的设备就可以接收完整的 Google Assistant 了。在那之前，你可以用“Ok Google”语音命令享受同样多的乐趣。**