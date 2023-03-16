# Flip to Shhh 是 Digital Wellbeing 在 Google Pixel 上的翻转静音手势

> 原文：<https://www.xda-developers.com/digital-wellbeing-flip-to-silence-google-pixel-2/>

睡觉前，用你的智能手机做一些最后一分钟的网络浏览真的很有诱惑力。这是很多人都有的坏习惯，所以谷歌和苹果今年都推出了一些功能来帮助你抑制对智能手机的依赖。在谷歌 I/O 2018 上，谷歌推出了[Digital wellness](https://www.xda-developers.com/android-p-beta-features/):一套减少你花在手机上的时间的功能。Digital Wellbeing 有一个仪表盘，可以显示你在 Reddit 等应用上花了多长时间，一个应用计时器可以限制你在你最喜欢的应用上花多长时间，还有一个放松模式，这样你就可以在晚上放下手机。随着 Android Pie 的正式发布，Pixel 2 和 Pixel 2 XL 的数字福利[进入了测试版](https://www.xda-developers.com/digital-wellbeing-google-pixel-xl-google-pixel-2-xl/)，但谷歌 I/O 期间被取笑的一个功能没有进入:通过翻转手机来启用勿扰模式的能力。

## 数字福利中已经存在的东西

作为总结，以下是谷歌 Pixel 2 和谷歌 Pixel 2 XL 目前在数字福利方面的所有功能:

*   概述您的应用使用情况，以及您在每个应用上花费的时间。
*   一个计数器，显示您解锁设备的次数。
*   您收到的通知总数的计数器。
*   一个应用程序计时器，用于限制您在所选应用程序中的使用。
*   Wind Down mode 可安排手机进入免打扰模式、开启夜灯和渐变至灰度模式的时间。
*   快速访问通知和勿扰模式设置。
*   [启动器快捷方式和灰度快速设置图块](https://www.xda-developers.com/digital-wellbeing-launcher-shortcut/)。

Google Pixel、Google Pixel XL、Google Pixel 2 和 Google Pixel 2 XL 正式提供数字福利。HMD Global [已经声明](https://www.hmdglobal.com/press/2018-09-28-nokia-smartphones-serves-first-slice-of-android-9-pie)诺基亚 7 Plus 将“从 2018 年秋季”获得支持，虽然有报道称一些用户获得了该功能(通过 [*NokiaPowerUser*](https://nokiapoweruser.com/all-nokia-7-plus-android-pie-beta-users-get-digital-wellbeing-via-a-playstore-update/) )，但我们无法确认该功能是否已经真正为 Android Pie 上的[诺基亚 7 Plus 用户推出。该功能也可以在任何使用 Magisk 模块的 Android Pie 设备](https://www.xda-developers.com/nokia-7-plus-android-pie-update/)上[启用，例如在这篇早期文章](https://www.xda-developers.com/get-google-pixel-digital-wellbeing-essential-phone-android-pie/)底部[链接的模块。](https://www.xda-developers.com/digital-wellbeing-launcher-shortcut/)

## 数字福祉即将到来

正如我们之前提到的，谷歌已经宣布，支持勿扰模式功能的翻转将进入数字福祉。我们不知道它将于何时推出——可能与谷歌 Pixel 3 事件一起或之后的某个时间——但我们知道，如果你有 root 权限，该功能在最新版本中已经可以使用。我们设法在一台运行 Android 9 Pie 的谷歌 Pixel 2 XL 和 Essential 手机上手动激活了该功能(在 XDA 知名开发者 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) 的少量帮助下)。一旦该功能上线，系统中会有一个新的设置- >手势，名为“翻转到嘘”，如下截图所示。

该功能的工作方式与所述完全相同。在平面上翻转我的 Pixel 2 XL 会立即启用请勿打扰模式，而拿起它会禁用它。既然这个功能看起来已经开始工作了，我们不确定为什么它还没有对用户开放。希望它能在几天内对所有用户开放。

### 我如何启用翻转到嘘

无聊之余，我利用 PNF 软件的 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) 在数字福利 APK 周围挖掘，看看是否有办法启用这一功能。幸运的是，它很容易启用——尽管除非您修改 APK 来硬编码该值，否则它会在一段时间后自动重置。无论如何，下面是你需要在手势设置中添加翻转到 Shhh 并启用它的步骤，至少是暂时的。这在 OnePlus 6 上不起作用，因为 OxygenOS 修改得太多了，所以翻转到 Shhh 菜单不会显示。

1.  下载最新版本的数字福利。
2.  输入以下 shell 命令:

    ```
     su
    pm enable "com.google.android.apps.wellbeing/com.google.android.apps.wellbeing.autodnd.ui.AutoDndGesturesSettingsActivity" 
    ```

3.  翻转到 Shhh 现在会出现在手势设置中，但是还不能启用。
4.  从我制作的名为`PhenotypePrefs.xml`的 [AndroidFileHost](https://www.androidfilehost.com/?fid=1322778262904020692) 下载这个文件，推送到`/data/data/com.google.android.apps.wellbeing/shared_prefs`。给它+660 权限。为此我使用了 MiXplorer，但是你也可以使用任何支持 root 的文件浏览器，比如 Solid Explorer 或者 FX File Explorer
5.  重启你的设备。
6.  重新启动后，您可能无法立即启用翻转到 Shhh。如果发生这种情况，请等待一分钟或只是重新启动。

希望您能够启用它。我不知道你为什么想这么做，因为它不会以这种方式永久启用，但尽管如此还是很酷。当我在谷歌 Pixel 2 XL 上启用它时，它保持了 8 个小时，直到我重新启动我的设备。对于 Max Weinbach 来说，在他的基本手机上启用它后，它在一个小时内重置。您的里程可能会有所不同。