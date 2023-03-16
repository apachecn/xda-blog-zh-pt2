# DarQ 允许你在每个应用程序的基础上切换 Android Q 的强制黑暗模式

> 原文：<https://www.xda-developers.com/android-q-dark-mode-toggle-per-app/>

# DarQ 允许你在每个应用程序的基础上切换 Android Q 的强制黑暗模式

Android Q 有一个“覆盖强制黑暗”选项，让你在所有应用程序中强制黑暗模式。DarQ 是一款可以让你有选择地启用黑暗主题的应用。

当谷歌为 Pixel 设备推出 Android Q beta 3 时，他们包括了一个简洁的开发者选项，可以在任何应用程序中强制使用黑暗模式(尽管该选项在 Android Q beta 4 中被打破)。这个选项旨在为开发人员提供一种简单的方法来测试他们的应用程序的 UX，如果一个黑暗的主题被强加于其上，那么他们可以做出调整，为稳定的 Android Q 版本做准备。对于用户来说，这个新选项是一个在所有应用程序中获得全系统黑暗模式的简单方法，尽管它并不是在每个应用程序中都很好地工作。这也是一个要么全有要么全无的开关，这就是为什么 XDA 认可的开发者 [Quinny899](https://forum.xda-developers.com/member.php?u=3563640) 制作了这个新的 DarQ 应用。这个根应用程序让你有选择地强制黑暗模式只在你选择的应用程序中启用。

例如，我发现 DarQ 在 Instagram 中打开黑暗模式很有用，但在可视模式下却保持关闭。在使用 Android Q 中的 override force dark developer 选项时，Visible 应用程序出现了一些令人讨厌的 UI 冲突，使我无法看到我需要选择的一些 UI 元素。通过 DarQ，我可以选择 Instagram 强制进入黑暗模式。您可以自定义手机上的哪些应用程序要在黑暗模式下显示，哪些不显示。

DarQ 的另一个非常好的功能是在晚上自动开启黑暗模式。DarQ 可以检查手机上的时间，并在深夜打开黑暗模式，减少晚上使用手机时对眼睛的压力。Android Q beta 目前不支持这一功能，除非你使用 [Tasker](https://www.xda-developers.com/enable-android-p-dark-theme-night-light/) ，但其他 OEM 厂商如[三星](https://www.xda-developers.com/samsung-galaxy-note-9-night-mode-fov-selfies/)过去已经增加了对它的支持。这种自动切换也将适用于您专门为其启用黑暗模式的应用程序，以及系统 UI 和其他支持的应用程序。这款应用非常适合那些想在自己的设备上定制应用外观和感觉的人

DarQ 需要 root 才能运行下面的 shell 命令:`setprop persist.hwui.force_dark true`。它还需要一个辅助功能服务来切换每个应用程序的黑暗模式。多亏了[最新的 Magisk 更新](https://www.xda-developers.com/magisk-google-pixel-3-pixel-3a-android-q/)，所有 Android Q 设备，包括 Pixel 3 和 Pixel 3a 系列，都应该是可 root 的。如果你想下载这个应用，[可以在 XDA 实验室](https://labs.xda-developers.com/store/app/com.kieronquinn.app.darq)找到。它的源代码可以在[这里](https://github.com/KieronQuinn/DarQ)找到。

[**DarQ 论坛线程**](https://forum.xda-developers.com/android/apps-games/app-darq-app-selectable-force-dark-t3944356)