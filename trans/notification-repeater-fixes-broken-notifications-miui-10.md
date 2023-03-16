# 通知重复器修复了小米 Mix 3 等一些 MIUI 10 设备上的坏通知

> 原文：<https://www.xda-developers.com/notification-repeater-fixes-broken-notifications-miui-10/>

# 通知重复器修复了小米 Mix 3 等一些 MIUI 10 设备上的坏通知

通知转发器应用程序修复了小米 Mi Mix 3 等 MIUI 10 设备上无法显示通知的问题。继续阅读，了解更多信息！

小米的 MIUI 因其对 Android 操作系统的广泛改变而闻名(或声名狼藉，取决于你的视角)。其中一个变化是积极的电池管理，它优先考虑设备的电池寿命，而有争议的副作用是在后台关闭应用程序。这确实会导致应用程序在向你的设备发送通知时偷懒，而在理想情况下，它们本应该发送通知的。

虽然 MIUI 的电池优化确实承担了这些跳过通知的大部分责任，但它们不是完全的原因。如果关闭电池优化不能解决通知丢失和损坏的问题，那么你的[问题可能与 Redditor](https://www.reddit.com/r/Xiaomi/comments/agh1ca/short_investigation_into_broken_notifications_on/) [FabioCZ](https://www.reddit.com/user/FabioCZ) 在 MIUI 10 上的小米 Mix 3 上遇到的问题相同。Discord 和 Google Voice 等应用的通知显然被立即删除，因为“ [*原因 _ 错误*](https://developer.android.com/reference/android/service/notification/NotificationListenerService#REASON_ERROR) ”，这是一个错误代码，基本上意味着 MIUI 无法显示通知中的一些内容，因此取消了通知的显示。

FabioCZ 随后转向解决这个问题，并为 MIUI 10 设备开发了[通知重复应用。该应用程序会监听因上述错误而被拒绝的通知，然后以基本的方式重复这些错过的通知，以确保它们确实显示在设备上。新通知只是原始通知的标题和内容的克隆，但是它去掉了样式以实现其目的。因此，不支持快速回复等功能。](https://www.reddit.com/r/Xiaomi/comments/ai46ke/update_miui_10_notification_repeater_new_version/)

开发者还对该应用进行了更新，包括启用通知的说明，触发测试通知的能力，以及允许振动，灯光和浮动通知功能现在可以工作。该应用程序也是[开源的](https://github.com/FabioCZ/NotificationRepeater)，所以你可以自己看一下该应用程序，以确保代码不会做任何邪恶的事情。

* * *

[**下载通知中继器**](https://github.com/FabioCZ/NotificationRepeater/releases/)

[**故事 Via:/r/小米**](https://www.reddit.com/r/Xiaomi/comments/ai46ke/update_miui_10_notification_repeater_new_version/)