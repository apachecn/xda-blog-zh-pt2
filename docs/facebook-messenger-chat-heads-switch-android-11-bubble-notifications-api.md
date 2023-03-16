# Facebook Messenger 聊天头切换到 Android 11 的 Bubbles API

> 原文：<https://www.xda-developers.com/facebook-messenger-chat-heads-switch-android-11-bubble-notifications-api/>

# Facebook Messenger 的聊天头切换到 Android 11 的气泡通知 API

Facebook Messenger 正在为运行 Android 11 的设备上的聊天头功能切换到气泡通知 API。

早在去年四月，谷歌就在 Android 10 Beta 2 中引入了新的 Bubbles API。该 API 最初是作为一个可供开发者选择的功能提供的，谷歌敦促他们在他们的应用程序中测试该 API，以便当该功能最终在未来的 Android 版本中推出时，支持的应用程序已经准备好了。正如所料，该功能在今年早些时候发布的 [Android 11 开发者预览版 1](https://www.xda-developers.com/android-11-developer-preview-changes/) 中默认启用。在[泄露的 Android 11 Beta](https://www.xda-developers.com/android-11-beta-1-rolled-out-early-some-google-pixel-4-users-whats-new-changes-features/) 中，气泡功能现在可以在通知设置中使用(而不是在开发者选项中)，然而，开发者仍然必须启用在气泡中显示通知的支持。到目前为止，我们只在 APK 拆除 Google Messages 应用的过程中看到了这一功能。但 Facebook Messenger 的最新更新也将应用程序切换到了 Bubbles API。

对于不知情的人来说，Facebook Messenger 长期以来一直有一个浮动通知气泡的功能，称为“聊天标题”。该功能利用了 Android 的系统提醒窗口 API，但在 Facebook Messenger 版本 268.0.0.3.118 中，如果设备运行 Android 11，该应用程序将切换到新的 Bubbles API。这项功能适用于我们的情报人员运行 Android 11 Beta 1 的 Pixel 4XL 和我们的主编米沙·拉赫曼运行 Android 11 DP4 的 Pixel 3a XL。

正如你在附带的截图中看到的，该功能在 Facebook Messenger 设置中显示为一个名为 Bubbles 的新选项。启用后，您可以选择是否希望在 Messenger 通知设置中看到所有对话、选定对话或无对话的气泡。虽然该功能利用了较新的 API，但它看起来仍然与旧的 Messenger 聊天工具没有什么不同。每当你收到一条新消息，它就会以聊天气泡的形式出现在你手机主屏幕的一侧。点击气泡会在一个浮动窗口中打开对话，您可以在其中快速回复信息。

您可以将气泡从一边移动到另一边，方法是点击并按住气泡，然后将其拖到另一边。您还可以选择在一个气泡中进行多个对话，只需点击顶部的加号图标并添加一个新联系人即可。要消除气泡，您可以点击并按住它，然后将它拖到靠近显示屏底部的 X 图标上。

* * *

*感谢 Hani Mohamed Bioud 的提示和截图！*