# 在 Xperia Z2 和 Z3 上启用通话录音

> 原文：<https://www.xda-developers.com/call-recording-xperia-z2-z3/>

# 在 Xperia Z2 和 Z3 上启用通话录音

索尼在其固件中隐藏了通话录音功能。了解如何在根手机上恢复它。

虽然通话录音在世界各地都不合法，但在某些情况下却非常方便。一些原始设备制造商已经决定在他们的默认电话应用程序中实现电话录音，有时还隐藏它。如果该功能存在但被隐藏，可以通过 Xposed Framewok 模块或其他应用程序来启用它。

在较旧的固件上，如 4.4.2，索尼在 SemcPhone.apk 中有一个隐藏的通话记录功能。该功能被划分到多个应用程序中。XDA 资深会员 [AndroPlus](http://forum.xda-developers.com/member.php?u=5169444) 通过提取 ROM 的中文变体找到了恢复通话记录功能的方法。提取的 CallRecording.apk 可以使用一种流行的恢复方法刷新到设备上。

要使用此功能，您的设备必须是根用户。刷新存档后，可以在设置→通话设置→通话记录中找到该功能。在刷新这个应用程序之前，一定要检查通话录音在你的国家是否合法。你可以在这篇维基百科文章中找到相关规定[，但最好的办法可能是向当地政府部门核实。](http://en.wikipedia.org/wiki/Telephone_recording_laws)

您可以在[索尼 Xperia Z2](http://forum.xda-developers.com/xperia-z2) 和[索尼 Xperia Z3](http://forum.xda-developers.com/z3) 上启用通话录音功能。您也可以尝试其他模型，但建议这种方法可能行不通。你可以通过访问[在 Z3 和 Z2 23.x 固件论坛线程](http://forum.xda-developers.com/crossdevice-dev/sony/enable-call-recording-z3-z2-23-x-t2946588)上启用通话录音来了解更多方法。