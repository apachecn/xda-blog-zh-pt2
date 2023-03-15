# 自动隐藏锁定屏幕上的快速设置磁贴[应用程序]

> 原文：<https://www.xda-developers.com/hide-quick-settings-tiles-lock-screen/>

谷歌在 Android 5.0 Lollipop 中引入了快速设置磁贴(尽管应该指出的是，在三星手机进入 AOSP 之前，该功能就已经在三星手机上提供了)。通过快速设置，用户可以访问许多有用的系统开关，如 WiFi、蓝牙、定位、GPS 或声音开关，而不必通过设置应用程序导航。并且通过 Android 7.0 Nougat 中引入的快速设置磁贴 API，开发者甚至可以[添加自己定制的磁贴](https://www.xda-developers.com/new-update-to-custom-quick-settings-app-brings-support-for-app-shortcuts-launch-activity-and-more/)。当创建一个新的磁贴时，开发者可以指定磁贴是否可以从锁定屏幕直接[切换，但是许多默认磁贴没有实现这个功能。如果你正在寻找一种方法让**禁用或隐藏锁屏**上的快速设置磁贴，我做了一个简单的**免费应用**，你可以用它来做到这一点。](https://developer.android.com/reference/android/service/quicksettings/TileService.html#unlockAndRun(java.lang.Runnable))

三星或华为等制造商的一些设备阻止用户在锁屏时切换某些磁贴。例如，运行 EMUI 的华为设备阻止用户在锁定屏幕上切换位置，除非他们解锁手机。但如果用户有飞行模式或 WiFi 磁贴，这些仍然可以切换，这使得位置磁贴保护无用。

虽然谷歌已经实施了工厂重置保护(FRP)来防止小偷偷走你的设备，然后工厂重置它，允许用户切换任何快速设置是一个潜在的安全问题。在锁定屏幕上隐藏快速设置磁贴是否真的有助于设备安全是另一个时间的争论，但显然有一个原因为什么某些 OEM 锁定某些磁贴而不解锁。由于这似乎是一个受欢迎的请求，我决定值得制作一个简单的应用程序来处理这项任务。

* * *

## 隐藏锁定屏幕上的快速设置磁贴

我用 [Tasker](https://play.google.com/store/apps/details?id=net.dinglisch.android.taskerm) 和它的 [Tasker App Factory](https://play.google.com/store/apps/details?id=net.dinglisch.android.appfactory) 插件做了一个超级简单的应用，在锁屏时隐藏快速设置磁贴。这绝不是一个漂亮的应用程序，但它完成了工作。该应用程序只是列出了状态栏中当前可用的快速设置磁贴，并让您选择想要从锁定屏幕中隐藏的磁贴。

快速设置图块列表取自[设置。安全](https://developer.android.com/reference/android/provider/Settings.Secure.html)首选项 sysui_qs_tiles。因此，应用程序需要被授予 [WRITE_SECURE_SETTINGS](https://developer.android.com/reference/android/Manifest.permission.html#WRITE_SECURE_SETTINGS) 权限(要么来自终端应用程序中的根 shell，如 XDA 初级成员 [yarolegovich](https://forum.xda-developers.com/member.php?u=6270589) 的 [Material Terminal](https://forum.xda-developers.com/android/apps-games/3-0-material-terminal-emulator-t3041056) ，要么通过 [ADB shell](https://www.xda-developers.com/google-releases-separate-adb-and-fastboot-binary-downloads/) )。授予权限后，应用程序可以写入 sysui_qs_tiles，这将立即更改可用快速设置的列表。

不幸的是，我还没有想出一种简单的方法来将 sysui_qs_tiles 首选项中的快速设置图块值转换为状态栏中显示的相同文本。不过，在我的测试中，这应该不是一个问题，因为显示的字符串很容易与它代表的图块相关联。此外，该应用程序显示字符串的顺序与它们在状态栏中显示的顺序相同，所以你没有理由找不到你想要隐藏的磁贴。

在任何情况下，一旦你选择了要在锁定屏幕上禁用的磁贴并启用了 display monitor 服务，该应用程序将检测屏幕何时被打开并活跃在锁定屏幕上。当在锁定屏幕上时，应用程序将修改保存当前快速设置磁贴的设置值，并从锁定屏幕中删除您想要隐藏的磁贴。然后当用户解锁手机时，应用程序将恢复你关闭屏幕时保存的快速设置磁贴。

我已经用了一个多星期了，没有出现任何问题，但是万一这个应用程序出错了，有一个“保存”和“恢复”按钮，可以让你在状态栏中保存当前的快速设置列表，以后再恢复它们。该应用程序可以隐藏和恢复您选择的任何快速设置磁贴，甚至是自定义的第三方磁贴——尽管来自 AutoNotification 等应用程序的第三方磁贴可能需要几秒钟才能重新初始化。

我希望我快速制作的这个应用程序能很好地为您服务。我绝不是一个开发人员，因为我在用 Tasker 制作这个应用程序时没有接触过一行代码，但我宁愿发布这个应用程序，让人们隐藏快速设置磁贴，而不是让人们继续等待别人可能会推出他们自己的应用程序。

[appbox xd a . hideqstiles]