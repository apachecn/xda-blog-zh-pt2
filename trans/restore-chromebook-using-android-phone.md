# 【更新 2:返工】谷歌可以让你用安卓手机恢复 Chromebook

> 原文：<https://www.xda-developers.com/restore-chromebook-using-android-phone/>

**更新 2 (10/27/19 @ 12:05 PM ET):** 额外的代码提交显示谷歌仍在致力于这项功能。

**更新 1(美国东部时间 10/25/19 @下午 2:10):**谷歌似乎已经放弃了一项代码更改，这项更改原本可以让你使用 Android 手机恢复 Chromebook。

使用 Chromebook 最大的好处之一就是你的大部分文件都是在线备份的。这意味着在硬件出现故障的情况下，您可以放心，您的所有文件都可以轻松地再次下载。然而，如果 Chrome OS 由于某种原因停止工作，那么你就有了一个完全不同的问题。截至目前，恢复 Chrome OS 的唯一方法是在单独的设备上创建恢复介质，然后将其安装在 Chromebook 上。但现在，谷歌似乎正在研究一种方法，让你使用 Android 手机恢复 Chromebook。

根据 Chromium Gerrit 最近的承诺，Chromebook 用户将能够在恢复模式下使用 Ctrl+P 快捷键通过 Android 设备启动恢复。代码更改请求显示，由于 Android 恢复设备枚举对其他 USB 设备有潜在危险，因此添加了新的快捷方式。这就是为什么它应该只遵循明确的用户意图。

一旦该功能上线，Chromebook 用户将不再需要使用恢复介质来恢复他们的设备。目前，还没有关于这个功能的 Android 部分是什么样子的信息。然而，据推测，谷歌可能会在 Play Store 上发布新的 Chrome OS 恢复应用程序，允许用户为他们的设备下载正确的恢复文件。该功能似乎还处于开发的早期阶段，目前，谷歌还没有关于其正式推出的信息。我们希望在未来的金丝雀更新中了解更多的信息。

谷歌的开发人员一直在不知疲倦地为 Chrome OS 推出一系列新功能。最近，该平台的金丝雀版本获得了对 [Wi-Fi 网络同步](https://www.xda-developers.com/chrome-os-wi-fi-network-sync/)的支持，并让我们一瞥在锁屏上工作的[媒体控制。](https://www.xda-developers.com/chrome-os-79-media-controls-lock-screen/)

**来源:[Chrome Gerrit](https://chromium-review.googlesource.com/c/chromiumos/platform/vboot_reference/+/1832460)|****Via:[Chrome Story](https://www.chromestory.com/2019/10/chromebook-recovery-using-android-phone/)**

* * *

## 更新 1:废弃

嗯，就在它被首次发现的几个星期后，谷歌似乎已经放弃了一项代码更改，该更改原本可以让你使用 Android 手机恢复 Chromebook。在 Chromium Gerrit 页面的 changelog 中，所有者简单地写着“废弃”。抛弃这种改变……”该功能可能会被暂时搁置，并可能会回来。如果有，我们会更新这篇文章。

*感谢 XDA 会员 Some_Random_Username 的提示！*

**来源:[铬革里特](https://chromium-review.googlesource.com/c/chromiumos/platform/vboot_reference/+/1832460/1#message-01aa92619365edcb5d234bd8509beaecc47181dd)**

* * *

## 更新 2:仍在进行中

多个单独的[提交](https://chromium-review.googlesource.com/c/chromiumos/platform/depthcharge/+/1827841) [被](https://chromium-review.googlesource.com/c/chromiumos/platform/initramfs/+/1745186)合并，以将该功能添加到 Chrome OS 中。此外，[一个 bug 追踪器](https://bugs.chromium.org/p/chromium/issues/detail?id=972872)揭示了这个特性是如何工作的。谷歌正在使用 Android 中一个名为“[配件模式](https://source.android.com/devices/accessories/aoa)的功能，在 Chromebook 处于恢复模式时与它进行通信。目标是让最终用户和工厂都能使用这个工具。

*感谢@Shad0wKn1ght93 的提示！*