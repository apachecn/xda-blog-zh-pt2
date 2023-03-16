# 谷歌信息在 Android 10 中测试浮动对话气泡

> 原文：<https://www.xda-developers.com/googles-messages-tests-floating-conversation-bubbles-android-10/>

今年 4 月初，谷歌为 Pixel 设备推出了 Android 10 Beta 2，引入了新的气泡通知功能。该功能的工作原理非常类似于 Facebook Messenger 的聊天头，为正在进行的对话带来一个浮动的气泡。虽然该功能没有在 Android 10 的[稳定版本](https://www.xda-developers.com/google-releases-stable-android-10-for-pixel-smartphones/)中实现，但气泡通知系统有望在 Android 的未来版本中[完全取代覆盖 API](https://www.xda-developers.com/android-q-system-alert-window-deprecate-bubbles/) 。截至目前， [Bubbles API](https://developer.android.com/guide/topics/ui/bubbles) 正在开发中，Android 10 用户可以从开发者选项内手动启用(设置>开发者选项> Bubbles)。谷歌敦促开发者测试他们应用中的 API，以便在该功能启用时，支持的应用已经准备好，最有可能的是在 Android 11 中。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

为了给 Bubbles API 准备应用程序，谷歌也在它的消息应用程序上进行测试。今年 10 月早些时候，我们了解到该公司正在为新的气泡通知支持准备谷歌消息应用程序。现在，我们已经成功地在最新版本的应用程序中启用了它。我们的主编米莎尔·拉赫曼在“信息”应用中启用了气泡功能，这使得所有收到的短信都出现在一个气泡中。正如你在所附的截图中看到的，通知气泡出现在显示屏的边缘，带有联系人的照片、应用程序图标和消息预览。如果保持不变，预览会很快消失，取而代之的是一个通知点。

轻按通知气泡会在叠层中打开对话，允许您快速回复信息，而无需切换到“信息”应用程序。要消除聊天气泡，你可以点击并按住它，然后将其拖到底部出现的“x”图标上，就像你在手机主屏幕上使用小工具或应用程序图标一样。你甚至可以在应用程序设置中选择完全禁用应用程序的聊天气泡，你会发现一个新的气泡设置，可以切换打开或关闭应用程序的聊天气泡。

截至目前，谷歌还没有关于该功能正式发布的消息。但我们预计该公司会在该功能即将推出时透露更多细节。在此之前，如果你希望在你的设备上获得类似的功能，你可以下载 Tasker 并按照本教程中的说明为任何消息应用程序启用气泡通知。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*