# 谷歌可能会拆分 Android 安全补丁级别，以加快安全更新

> 原文：<https://www.xda-developers.com/google-separate-vendor-security-patch-android-security-patch-level/>

在早期历史的很长一段时间里，由于苹果公司对应用程序的“围墙花园”方法，Android 一直有不如 iOS 安全的名声。过去的名声是否名副其实并不是我们要深入探讨的事情，但很明显，谷歌在保护 Android 免受漏洞攻击方面取得了长足的进步。该公司不仅在最新版本的 Android 中提供了新的安全功能，而且由于谷歌 Pixel 2/2 XL 中的硬件安全模块，他们还在他们的最新设备中提供了“T2”企业级安全功能。保持设备安全还需要持续更新，以修补所有最新的威胁，这也是为什么谷歌为所有设备制造商和供应商提供了[每月安全公告](https://www.xda-developers.com/essential-google-security-patches/)，以整合针对所有已知活跃和潜在漏洞的补丁。现在，该公司似乎正在对 Android 安全补丁系统进行更改，提供了一种方法来**区分 Android 框架补丁级别和供应商补丁级别**以及引导加载程序、内核等。或者划分安全补丁级别，以便 OEM 可以提供纯框架更新，或者更好地向用户标识他们正在运行的补丁级别。

* * *

## 每月 Android 安全补丁-入门

我们都知道安全补丁很重要，尤其是在去年下半年一系列备受瞩目的漏洞被公之于众之后。 [BlueBorne 漏洞](https://www.xda-developers.com/bluetooth-vulnerability-blueborne-impacts-android-ios-windows-and-linux-devices/)攻击蓝牙协议，在[2017 年 9 月月度补丁](https://www.xda-developers.com/android-security-bulletin-september/)中被修补， [KRACK](https://www.xda-developers.com/wpa2-wifi-protocol-vulnerability-krack/) 针对 Wi-Fi WPA2 中的一个漏洞，在[2017 年 12 月](https://www.xda-developers.com/google-announces-android-security-bulletin-december-2017/)被修补，Spectre/Meltdown 漏洞大多用【2018 年 1 月补丁修复。修补这样的漏洞通常需要与硬件供应商(如博通和高通)合作，因为漏洞涉及硬件组件，如 Wi-Fi 或蓝牙芯片或 CPU。另一方面，Android 操作系统中存在一些问题，例如这个 [toast 消息覆盖攻击](https://www.xda-developers.com/android-toast-message-overlay-attack/)，只需要更新 Android 框架就可以修复。

每当谷歌推出月度安全补丁时，设备制造商都必须修复该月安全公告中列出的所有漏洞，如果他们想说他们的设备在该月度补丁水平下是安全的。每个月，设备可以满足两个安全补丁级别:每月 1 日或 5 日的补丁级别。如果一个设备说它运行的是从每月 1 号开始的补丁级别(例如，4 月 1 号而不是 4 月 5 号)，那么这意味着构建包含了上个月发布的所有框架和供应商补丁以及最新安全公告中的所有框架补丁。另一方面，如果一个设备说它正在运行一个从本月 5 日(例如，4 月 5 日)开始的补丁级别，那么这意味着它包含了上个月和本月公告中的所有框架和供应商补丁。下表举例说明了每月修补程序级别之间的基本差异:

| 

每月安全补丁级别

 | 

4 月 1 日

 | 

4 月 5 日

 |
| --- | --- | --- |
| 包含四月框架补丁 | 是 | 是 |
| 包含四月份的供应商补丁 | 不 | 是 |
| 包含 March 框架补丁 | 是 | 是 |
| 包含三月份的供应商补丁 | 是 | 是 |

你可能很熟悉 Android 生态系统中安全补丁的情况有多糟糕。下图显示，谷歌和 Essential 提供了最快的月度安全补丁更新，而其他公司则落后了。OEM 厂商可能需要几个月的时间才能为设备带来最新的补丁，例如 [OnePlus 5 和 OnePlus 5T](https://www.xda-developers.com/oneplus-5-5t-oxygenos-open-beta-april/) 最近收到了[4 月份的安全补丁](https://www.xda-developers.com/nexus-pixel-security-april-2018-ota-factory-images/)，而它们之前是 12 月份的补丁。

截至 2018 年 2 月的 Android 安全补丁状态。来源:@ [SecX13](https://twitter.com/SecX13/status/968225118517452800)

提供 Android 安全补丁更新的问题不一定是原始设备制造商懒惰，因为有时这可能超出他们的控制。正如我们之前提到的，每月的安全补丁更新通常需要硬件供应商的合作，如果供应商无法跟上每月的安全补丁公告，这可能会导致延迟。为了解决这一问题，谷歌可能开始将 Android 框架安全补丁级别与供应商补丁级别(可能还有引导加载程序和内核级别)分开，以便在未来，原始设备制造商可能能够提供纯粹的 Android 框架安全更新。

* * *

## 更快的针对框架漏洞的 Android 安全补丁更新？

一个新的[提交](https://android-review.googlesource.com/#/c/platform/system/sepolicy/+/660840/)已经出现在 Android 开源项目(AOSP) gerrit 中，它暗示了一个“供应商安全补丁道具”，每当一个设备的新版本被创建时，该补丁将在 Android.mk 文件中被定义。该属性将被称为“`ro.vendor.build.security_patch`”，类似于当前存在于所有 Android 设备上的“`ro.build.version.security_patch`”，用于指定每月的 Android 安全补丁级别。

这个新属性将告诉我们设备的“`VENDOR_SECURITY_PATCH`”级别，它可能与 Android 框架安全补丁级别匹配，也可能不匹配。例如，设备可能运行最新的 2018 年 4 月框架补丁以及 2018 年 2 月供应商补丁。通过区分这两个安全补丁级别，谷歌有可能打算让原始设备制造商提供最新的 Android 操作系统安全补丁，即使供应商没有提供该每月补丁级别的更新补丁。

**或者**，谷歌**可能只显示两个补丁级别中最低的**(可能还有引导加载程序和内核补丁级别)，以便更准确地向用户显示他们的设备安装了什么安全补丁。我们还没有确认这个补丁背后的意图，但我们希望尽快找到更多。

 <picture>![](img/3b46e7fc5defca986fd4b886eccf4215.png)</picture> 

Google Pixel 2 XL on Android P Developer Preview 1 with March 2018 Security Patches

至少，这将对我们这些在[Project Treble](https://www.xda-developers.com/list-android-devices-project-treble-support/)[Generic System Images](https://www.xda-developers.com/flash-generic-system-image-project-treble-device/)(GSIs)和其他基于 AOSP 的定制 rom 有所帮助，因为定制 rom 通常只提供框架更新，而不修补每月安全公告中指定的所有供应商、引导加载程序和内核补丁，所以这种不匹配会在用户中造成混乱，因为他们认为他们正在运行最新的补丁，而实际上他们的设备只是针对最新的每月安全公告进行了部分修补。