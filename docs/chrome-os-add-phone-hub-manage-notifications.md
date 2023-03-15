# Chrome OS 测试 Phone Hub 来管理通知和控制你的手机

> 原文：<https://www.xda-developers.com/chrome-os-add-phone-hub-manage-notifications/>

**更新 1 (09/11/2020 @美国东部时间下午 1:57):**Phone Hub 现在出现在 Chrome OS 的金丝雀频道。滚动到底部了解更多信息。下面保留了 2020 年 7 月 29 日发表的文章。

作为谷歌“ [Better Together](https://www.xda-developers.com/chrome-os-android-integration-sms/) ”功能套件的一部分，Chrome OS 已经提供了与你的 Android 手机的轻松集成，如[文本/RCS 消息](https://www.xda-developers.com/android-messages-integration-chromebooks-pixelbook/)，自动 Wi-Fi 热点和智能锁。现在，根据最近来自[9 to 5 Google的报道，谷歌正在努力通过一个新的“电话中枢”功能来扩展 Chrome OS 与 Android 设备的集成。](https://9to5google.com/2020/07/28/chrome-os-android-phone-hub/)

最近在 Chromiun Gerrit 上发现的一个[代码变化](https://redirect.viglink.com/?format=go&jsonp=vglnk_159600980077112&key=b8f771eed689587b82c4635131ce08d7&libId=kd71oupv01010l04000DAp5suqe0l&loc=https%3A%2F%2F9to5google.com%2F2020%2F07%2F28%2Fchrome-os-android-phone-hub%2F&v=1&out=https%3A%2F%2Fchromium-review.googlesource.com%2Fc%2Fchromium%2Fsrc%2F%2B%2F2309757&ref=https%3A%2F%2Fapp.asana.com%2F0%2F1179573953519059%2F1186599479413728&title=Chrome%20OS%20to%20gain%20Android%20Phone%20Hub%20w%2F%20notifications%2C%20more%20-%209to5Google&txt=new%20code%20change)指向即将到来的 Phone Hub 功能标志，该功能标志“为用户提供一个用户界面，以查看有关他们的 Android 手机的信息，并在 Chrome OS 内执行手机端操作。”该功能预计将在 Chrome OS 和 Android 设备之间提供更深层次的集成，因为目前用户唯一可用的信息和“手机端”操作是查看和回复文本/RCS 消息。

关于该功能的另一个[代码变化](https://redirect.viglink.com/?format=go&jsonp=vglnk_159600980778113&key=b8f771eed689587b82c4635131ce08d7&libId=kd71oupv01010l04000DAp5suqe0l&loc=https%3A%2F%2F9to5google.com%2F2020%2F07%2F28%2Fchrome-os-android-phone-hub%2F&v=1&out=https%3A%2F%2Fchromium-review.googlesource.com%2Fc%2Fchromium%2Fsrc%2F%2B%2F2315394&ref=https%3A%2F%2Fapp.asana.com%2F0%2F1179573953519059%2F1186599479413728&title=Chrome%20OS%20to%20gain%20Android%20Phone%20Hub%20w%2F%20notifications%2C%20more%20-%209to5Google&txt=another%20code%20change)显示，电话集线器将位于连接设备页面的一个新部分，就在即时共享、智能锁和消息的下方。该部分将包括三个新设置，即电话中心通知、电话中心通知徽章和电话中心任务继续。虽然代码的变化并没有强调任务继续功能到底会为用户提供什么，但 *9to5Google* 表示，该功能将让用户在 Chromebook 上无缝地从他们的 Android 设备上继续任务。

截至目前，还不清楚任务继续功能是否会让用户在设备之间移动 Chrome 标签，或者是否也允许用户继续 Chromebook 上的应用活动。由于 Phone Hub 仍处于早期开发阶段，我们目前只知道该功能将利用蓝牙将您的 Chrome OS 设备与您的 Android 设备连接起来。我们也不确定这项功能是否会要求用户在他们的 Android 设备上安装一个单独的应用程序。

值得注意的是， [Windows 10](https://www.xda-developers.com/tag/windows-10/) 提供了类似的[你的手机](https://www.xda-developers.com/tag/your-phone/)功能，允许用户在他们的 Android 设备上发送和接收短信，管理照片，[可以直接从他们的 Windows 10 机器上使用他们手机的媒体控制](https://www.xda-developers.com/your-phone-app-windows-10-controlling-music-playback/)。对于三星设备，你的手机功能还允许用户管理跨设备的剪贴板，并查看他们设备的屏幕。

## 更新 1:(非功能性)手机集线器出现在 Chrome OS 金丝雀

前几天，XDA 成员 Some_Random_Username 告诉我们，Chrome OS canary 版本 87.0.4258.0 中出现了新的电话中心功能的图标。现在，ChromeStory 的 Dinsan Francis 在 YouTube 上发布了一段视频，展示了 Phone Hub 的用户界面。在视频中，我们可以看到在连接的手机上切换热点和铃声的图标。我们还可以看到一个按钮来定位您的手机和一个图标显示电池寿命。Dinsan 说这个特性还没有发挥作用，但是我们可能会在未来的金丝雀版本中看到更多的调整。