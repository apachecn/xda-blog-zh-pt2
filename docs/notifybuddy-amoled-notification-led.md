# NotifyBuddy 使用手机的 AMOLED 显示屏作为通知 LED

> 原文：<https://www.xda-developers.com/notifybuddy-amoled-notification-led/>

# NotifyBuddy 使用手机的 AMOLED 显示屏作为通知 LED

您的新智能手机缺少一个通知 LED？试试 NotifyBuddy。它使用手机的 AMOLED 显示屏的一部分作为临时的通知 LED。

当一加设计一加 6T 的时候，他们决定[去掉](https://www.xda-developers.com/oneplus-6t-notification-led-always-on-display-ip-rating/)的一个功能是通知 LED。一加 7 和一加 7 Pro 也缺少通知 led，但一加增加了一个[边缘照明效果](https://www.youtube.com/watch?v=-B9cJeF0x8Q)来补偿。我们已经见过[多个](https://www.xda-developers.com/miss-the-notification-led-on-the-pixel-3-and-oneplus-6t-try-pixel-pulse/) [第三方应用](https://www.xda-developers.com/plus-beat-notification-led-oneplus-6t/)在手机显示屏上显示通知，今天我们将重点介绍另一个。XDA 成员的 NotifyBuddy 是一个相当新的应用程序，上个月底在我们的论坛和 Google Play 上发布，已经获得了超过 10，000 次的下载。

该应用程序是为一加 6T 设计的，但它应该可以在大多数运行 Android Oreo 和更高版本的 Android 智能手机上工作。建议您在配有有机发光二极管显示屏的手机上使用此应用程序，这样通知灯光就不会照亮整个屏幕。如果您担心老化，开发人员通过偶尔移动通知照明出现的区域来实现老化保护。这里有一个视频，展示了这款应用在一加 6T 上的外观:

安装很简单。首先，从 Google Play 安装应用程序。接下来，禁用手机上的任何环境显示设置，将应用程序从 Doze 模式的电池优化设置中加入白名单，这样它就不会在后台被杀死，并启用应用程序的 NotificationListener 服务。最后，定制你想要显示临时通知 LED 的应用程序。

请注意，由于手机技术上不睡眠，你可能会遇到闲置电池消耗。XDA 线程中的一些用户报告最小的流失，而其他人报告很多。像这样的应用程序不应该导致太多的电池消耗，所以希望这些问题能为每个人解决。[访问 XDA 线程](https://forum.xda-developers.com/oneplus-6t/themes/app-amoled-notification-light-t3943715)直接给开发者反馈。