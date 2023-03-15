# Magisk 模块无系统地启用 Miracast 和网络共享，并禁用 ADB 通知

> 原文：<https://www.xda-developers.com/magisk-module-to-systemlessly-enable-miracast-and-tethering-and-disable-adb-notify/>

Magisk 的优势之一是能够对您的设备进行无系统的修改，这反过来允许您保留通过 Android Pay 和其他服务的 SafetyNet 检查的能力。

XDA 成员 [VR25](https://forum.xda-developers.com/member.php?u=5228676) 组装了一个 Magisk 模块，允许您启用 Miracast 和网络共享以及禁用 ADB Notify。该模块通过修改 build.prop 并添加以下几行来实现这一点:

```
 net.tethering.noprovisioning=true
ro.hdmi.enable=true 
ro.hdmi.mirror.enable=true 
persist.debug.wfd.enable=1 
persist.adb.notify=0 
```

该模块会为您进行 build.prop 修改，因此您不必担心在不影响安全网的情况下自己修改它。

* * *

[**在我们的 Magisk 论坛中查看该模块！**](https://forum.xda-developers.com/apps/magisk/module-miracast-tethering-enabler-adb-t3611335)