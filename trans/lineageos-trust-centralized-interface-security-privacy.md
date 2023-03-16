# LineageOS 引入信任:安全和隐私的集中界面

> 原文：<https://www.xda-developers.com/lineageos-trust-centralized-interface-security-privacy/>

谷歌推出 Android 月度安全补丁是一个受欢迎且急需的举措。当时，Android 因其碎片化问题而臭名昭著，这对如何修补安全漏洞并迅速分发到设备产生了负面影响。每月的安全补丁为担心的用户提供了一个快速判断他们的设备到底有多“安全”和“最新”的方法。

不幸的是，尽管这一改变对最终用户来说可能是善意的，但一些原始设备制造商未能为他们的设备全面推出所有的安全补丁。每当谷歌推出月度安全补丁，原始设备制造商都被要求修复**该月安全公告中概述的所有**漏洞，如果他们想声称他们的设备安全达到该月度补丁水平。然而，研究人员发现，手机上报告的安全补丁级别与手机实际防护的漏洞之间存在明显的补丁差距。虽然大多数普通消费者似乎不会*关心这个问题，但不可否认的是，这是对原始设备制造商的背信弃义。诸如此类的问题促使谷歌[修改他们的 OEM 协议，纳入常规安全补丁的要求](https://www.xda-developers.com/google-require-oem-regular-security-patches/)。*

鉴于这些担忧，LineageOS 的开发人员引入了“ **[信任](https://lineageos.org/Trust-me/)”。**

## 信任

信任是 LineageOS ROMs(位于设置>安全和隐私)中的一个集中界面，现在将成为 LineageOS 所有安全功能的家园。在这里，您可以了解隐私保护等核心安全功能的概况，以及如何确保您的设备安全和数据隐私的说明。此外，作为用户体验改进的一部分，信任图标将在状态栏中可见，以通知用户正在进行的操作是安全的，并且不是由伪造的权限对话框、网络钓鱼企图和其他此类麻烦引起的。

信任与前面提到的 Google 的变化密切相关，因为它[将供应商安全补丁级别和框架补丁级别](https://www.xda-developers.com/google-separate-vendor-security-patch-android-security-patch-level/)分开。得益于 AOSP，LineageOS 能够修补 Android 框架，得益于 Linux 内核源代码，他们能够修补内核。但是开发者通常不得不依赖原始设备制造商来更新厂商的 Hal、bootloaders 等等。新的“供应商”安全补丁级别现在可以报告 BLOBs 上次更新的时间。这提供了更多的相关信息，正如在 Nextbit Robin 的案例中可以看到的，它将[显示 2017 年 4 月](https://review.lineageos.org/#/c/LineageOS/android_device_nextbit_ether/+/217183/2/device.mk)的供应商补丁级别，即使 Android 框架补丁级别可能是最新的。

当用户的设备不安全时，Trust 界面也会向用户发出警告，例如当 SELinux 被禁用、root 被启用或设备未加密时。当应用程序主动使用 root 访问权限时，信任也会在状态栏中显示一个图标，非常像隐私卫士。Trust 还包含控制应用程序短信限制的设置。

信任接口在本周的 [LineageOS 15.1](https://www.xda-developers.com/tag/lineageos-15/) 版本中上线。开发者承诺在未来提供更多的功能作为信任的一部分。