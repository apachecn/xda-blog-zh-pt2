# 启用双击唤醒某些华为和荣誉设备[Root]

> 原文：<https://www.xda-developers.com/enable-double-tap-to-wake-on-huawei-and-honor-devices/>

双击唤醒是你在真正拥有它之前不知道你需要的功能之一。

该功能在大屏幕设备中特别有用，因为它可以更容易地在桌子上打开屏幕，而不必摆弄按钮。虽然大多数 LG 设备都有双击唤醒功能(他们称之为“敲门”)，但你很难在其他制造商的设备上找到这一功能。

通过一个定制的内核，比如由 XDA 知名开发者 [flar2](https://forum.xda-developers.com/member.php?u=4684315) 开发的流行的 ElementalX，你可以使用双击来唤醒大量以前不支持的设备。如果你的设备没有定制的内核，有时你可以使用一个隐藏的开关来启用双击唤醒——前提是现有的内核支持它。对于某些华为/Honor 设备来说确实如此，如[华为 Mate 8](https://forum.xda-developers.com/mate-8) 和[华为 P9](https://forum.xda-developers.com/p9) 。使用 **root 访问**，您可以**启用华为禁用的原生双击唤醒功能。**

* * *

## 在某些华为/Honor 手机上双击唤醒

XDA 资深会员 [ajsmsg78](https://forum.xda-developers.com/member.php?u=1397125) 发现，你可以[在某些华为/Honor 手机上启用双击唤醒](https://forum.xda-developers.com/mate-8/general/enable-double-tap-to-wake-t3312676)，通过编辑你设备上的两个文件来支持该功能。

您需要编辑的第一个文件是位于 **/system 中的 **build.prop** 。**使用根浏览器应用程序(或 Play Store 中的 build.prop 编辑器)打开文件，将下面一行从

`ro.config.hw_easywakeup=false`

到

`ro.config.hw_easywakeup=true`

如果在 build.prop 中找不到这一行，只需手动将其添加到文件中。

接下来，我们将修改位于 **/system/emui/base/xml** 中的另一个名为**HW _ easywakeupmotion _ config . XML**的文件。同样，用一个根资源管理器应用程序打开这个文件，并将下面一行从

`<EasyWakeupMotion name="Double_Touch" support="1" value="0" flag="0" keycode="131" />`

到

`<EasyWakeupMotion name="Double_Touch" support="1" value="1" flag="0" keycode="131" />`

如果在 XML 文件中找不到这一行，那么就在靠近末尾的地方手动添加它。重启后，你会发现一个新的“**双击**功能，位于设置- >智能辅助- >运动控制。启用该功能，然后重新启动一次，你现在应该有双击唤醒！

或者，与其手动编辑这两个文件，你可以[在 XDA 资深成员](http://www.modaco.com/forums/topic/377614-update-zip-to-enable-dt2w-on-huawei-honor-devices/)[保罗布里安](https://forum.xda-developers.com/member.php?u=220328)制作的恢复中刷新这个 zip 文件。

我们论坛上的用户已经证实，这适用于华为 Mate 8 和华为 P9，但无法在华为 Mate 9 上使用。在您根深蒂固的华为/Honor 设备上试用一下，让我们知道它是否适合您！