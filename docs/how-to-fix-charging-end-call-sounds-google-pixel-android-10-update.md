# Android 10 更新后如何修复谷歌 Pixel 上缺失的系统声音

> 原文：<https://www.xda-developers.com/how-to-fix-charging-end-call-sounds-google-pixel-android-10-update/>

**更新(美国东部时间 3/2/20 @下午 4:50):**Pixel 2 缺失充电/结束通话声音 bug 已在 2020 年 3 月更新中修复。

随着 [Android 10 更新](https://www.xda-developers.com/google-releases-stable-android-10-for-pixel-smartphones/)，一些第一代和第二代谷歌 Pixel 智能手机的用户注意到几个 UI 声音有所不同。例如，[一些用户注意到](https://www.reddit.com/r/GooglePixel/comments/ej0qq1/any_way_to_bring_back_the_call_end_sound/)结束通话和锁屏音消失，而[另一些用户注意到](https://issuetracker.google.com/issues/140447165)充电声音不同。如果你在更新到 Android 10 后注意到了你的 Pixel 上的这种奇怪行为，并想知道可能是什么原因，我们有答案和解决方案。

事实证明，罪魁祸首似乎是系统声音文件的重新定位。在 Android 9 Pie 及之前的版本中，Google 习惯将 UI‌声音如对接/非对接声音和锁屏声音存储在 */product/media/audio* 目录中。Android 10 改变了这一点，它将声音移到了一个新的位置:*/系统/媒体/音频*。问题是 Pixel 上的 Android 10 和 Pixel 2 认为 UI 声音还在旧目录里。因此，当系统试图从这个旧位置访问声音并且无法定位文件时，Android 会退回到嵌入在 framework-res 中的旧 UI 声音。

据 XDA 成员 [co4](https://forum.xda-developers.com/member.php?u=7913624) 称，你可以通过调整全局系统设置的偏好来轻松解决这个问题。为此[在你的 PC 上设置 ADB](https://www.xda-developers.com/install-adb-windows-macos-linux/) ，连接你的 Pixel 或 Pixel 2，从命令提示符或 Windows PowerShell 运行以下命令。

```
 adb shell settings put global car_dock_sound /system/media/audio/ui/Dock.ogg
adb shell settings put global car_undock_sound /system/media/audio/ui/Undock.ogg
adb shell settings put global desk_dock_sound /system/media/audio/ui/Dock.ogg
adb shell settings put global desk_undock_sound /system/media/audio/ui/Undock.ogg
adb shell settings put global lock_sound /system/media/audio/ui/Lock.ogg
adb shell settings put global low_battery_sound /system/media/audio/ui/LowBattery.ogg
adb shell settings put global trusted_sound /system/media/audio/ui/Trusted.ogg
adb shell settings put global unlock_sound /system/media/audio/ui/Unlock.ogg
adb shell settings put global wireless_charging_started_sound /system/media/audio/ui/ChargingStarted.ogg 

```

这些命令会将每个 UI‌声音的路径从*/产品/媒体/音频*更改为*/系统/媒体/音频*，确保系统现在在请求系统声音时处于正确的位置。

运行上述 ADB 命令后，无需重启设备。注意，这个问题应该不会影响谷歌 Pixel 3、Pixel 3a 或 Pixel 4，因为在这三个设备的固件中，UI 声音已经位于 */product/media/audio* 中。它只影响 Pixel 和 Pixel 2 的所有者，他们已经执行了 Android 10 的全新安装，即通过刷新 Android 10 系统映像。如果你用官方 OTA 从 Android Pie 更新到 Android 10，你应该没问题——只要你不执行出厂重置。

* * *

## 更新:已在三月更新中修复

今天早些时候发布的 2020 年 3 月更新修复了今年早些时候出现的一个奇怪问题。根据 Reddit 上几个用户的说法，丢失的锁定和解锁音效终于回来了。这是一个奇怪的错误，我们很高兴它最终得到了解决。

**Via:[Reddit](https://www.reddit.com/r/GooglePixel/comments/fci8ud/with_march_2020_update_google_has_finally_fixed/)**