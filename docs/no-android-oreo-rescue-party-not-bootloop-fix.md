# 不，Android Oreo 的拯救派对不是你要找的 bootloop 补丁

> 原文：<https://www.xda-developers.com/no-android-oreo-rescue-party-not-bootloop-fix/>

在 XDA，我们一直在广泛报道谷歌最新发布的安卓操作系统:[安卓 8.0 奥利奥](https://www.xda-developers.com/android-8-0-oreo-google-released/)。Android Oreo 带来了大量新功能，但我们最感兴趣的是底层的变化。像 [Project Treble](https://www.xda-developers.com/project-treble-custom-rom-development/) 和[全系统定制主题支持](https://www.xda-developers.com/custom-themes-android-oreo-substratum/)是我们的读者感兴趣的 Android 奥利奥相关变化的两个例子。Android 爱好者一直期待看到的另一个功能是新的[救援队](https://www.xda-developers.com/android-oreo-rescue-party-bootloop/)功能。这个功能被很多人吹捧为可以保护你的设备不被引导，但是现实远比这令人失望。 **Rescue Party 不是你要找的 bootloop 补丁**。

事实上，救援队只在非常有限的情况下工作，这种情况对许多设备进入引导循环的用户来说不太可能有影响。对于我们论坛上几乎每一个遇到 bootloop 的用户来说尤其如此——救援方不会帮助你。不过，这不是救援队的错，因为它被夸大了，远远超过了它应该考虑的实际情况。

* * *

## 安卓奥利奥中的拯救党——它是如何工作的

让我们从如何触发救援队开始。首先，需要实施救援方，这不是原始设备制造商所要求的。在有救援方支持的设备上，发生的第一个检查是查看该功能是否被启用，如果设备在调试/工程构建上运行或者如果系统属性`persist.sys.disable_rescue`在 build.prop 中被设置为 true，则[可能不是这种情况](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r4/services/core/java/com/android/server/RescueParty.java#70)

在启动过程中启动了 Android OS 的[裸最小部分](https://android.googlesource.com/platform/frameworks/base/+/master/services/java/com/android/server/SystemServer.java#527)之后，系统确定是否需要派遣救援队。你可能已经读到过，每当[设备在 5 分钟内重启超过 5 次](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r4/services/core/java/com/android/server/RescueParty.java#269)或者[系统应用在 30 秒内崩溃超过 5 次](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r4/services/core/java/com/android/server/RescueParty.java#305)，就会派出救援队。救援队随后开始[递增](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r4/services/core/java/com/android/server/RescueParty.java#137)通过各种“救援级别”,试图修复重启循环。

以下是救援队可以采取的[步骤](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r4/services/core/java/com/android/server/RescueParty.java#178):

### 级别 1 -重置不受信任的默认值

第一救援方级别是*重置*对[设置的任何和所有更改。全局](https://developer.android.com/reference/android/provider/Settings.Global.html)或[设置。由不受信任的应用程序制作的安全](https://developer.android.com/reference/android/provider/Settings.Secure.html)偏好表。不受信任的应用程序是那些由用户安装的软件包。当调用此救援方级别时，第三方应用程序所做的任何更改都将被替换为其默认值(如果存在)。如果默认值不存在，则删除该设置。

不受信任的应用程序能够修改全局或安全设置值的唯一方式是该应用程序具有 root 访问权限或通过 ADB 被授予`WRITE_SECURE_SETTINGS`权限。不过，这种情况并不少见，因为我们自己的许多非根教程都严重依赖于以同样的方式修改这些设置数据库。

这种救援队级别的一个例子是，如果用户试图[在 Android Oreo](https://www.xda-developers.com/customise-the-navigation-bar-android-oreo/) 上定制他们的导航栏。这样做需要通过第三方应用程序修改`Settings.Secure.sysui_nav_bar`，比如[自定义导航栏](https://forum.xda-developers.com/android/apps-games/app-custom-navigation-bar-customize-t3590967)。现在，通过这种方法修改导航条不太可能导致引导循环，但如果导致了引导循环，那么这个救援方级别将重置您所做的任何更改，并将其替换为 sysui_nav_bar 的默认值`"left,back;home;recent,right"`。

### 级别 2 -重置不可信的更改

修复重启问题的第二个尝试是将级别 1 向前推进一步。它不是重置任何由不可信的软件包设置的值，而是将它们全部删除。

### 级别 3 -重置可信默认值

救援队提供的最后一道防线，第 3 级将重置对设置所做的任何更改。全局或设置。安全值是由可信的，即。系统、应用程序。它还尝试早期级别所做的更改，例如删除不受信任的包所做的更改。

### 4 级-工厂重置

如果所有其他方法都失败了，那么最后一次尝试修复你的设备就是启动恢复程序，然后[提示用户执行工厂重置](https://android.googlesource.com/platform/frameworks/base/+/android-8.0.0_r4/services/core/java/com/android/server/RescueParty.java#130)。虽然这一操作可能会解决引导环路问题(前提是引导环路不是由硬件问题引起的，如 [Nexus 5X](https://www.xda-developers.com/nexus-5x-bootloop-fix-boot-phone/) 或 [Nexus 6P](https://www.xda-developers.com/nexus-6p-bootloop-fix/) )，但显然这并不理想，因为这需要重新设置你的手机。

* * *

## 不适合您的 Bootloop 修复程序

那么我们来总结一下拯救党实际上是做什么的。本质上，它所做的只是试图修复用户或系统应用程序对设置所做的任何错误更改。全局或设置。安全首选项表。如果你的设备进入引导循环是因为你刷新了一个拙劣的音频模式，安装了错误的底层主题，启用了一个不适合你的 Magisk/Xposed 模块，进行了错误的 build.prop 编辑，或者做了任何一个根用户可以做的进入引导循环的事情，那么 **Rescue Party 不适合你**。

如果你[在开发者选项中修改了“模拟辅助显示器”](http://blog.jbit.net/2013/01/android-settings-reset-using-adb.html)这样的设置，不知何故陷入了重启循环，只有这样，Rescue Party 才会真正帮助你。但我推测，我们的绝大多数读者不太可能通过救援队解决他们的错误。不幸的是，处理盗号的最好方法是**定期备份你的数据**，这样你就不必处理手机上灾难性的数据丢失。**不要指望拯救党**成为你的救世主。