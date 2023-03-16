# 谷歌 One 可能会为即将推出的手机提供 3 个月的 100GB 免费空间

> 原文：<https://www.xda-developers.com/google-one-1-42-upcoming-phone-free-3-month-100gb-plan/>

**更新 1(美国东部时间 9/11/19 @晚上 8:15):**虽然 HMD Global 的[新闻稿](https://www.hmdglobal.com/press-releases/introducing-new-nokia-smartphones-ifa)没有提到这一点，但似乎[诺基亚 6.2 和诺基亚 7.2](https://www.xda-developers.com/nokia-7-2-nokia-6-2-ia-2019/) 都附带了 3 个月免费的 Google One 云存储。

在去年的谷歌 I/O 大会上，谷歌宣布了一项一体化的云存储服务，将 Google Drive、Gmail 和 Google Photos 整合在一个屋檐下。名为谷歌一号(Google One)的订阅服务现在可以在全球几十个地区使用，包括欧洲、北美和 T2。我个人使用 20 美元/年的计划，这使我获得了 100GB 的云存储空间，这样我就可以继续向[谷歌照片](http://xda-developers.com/tag/google-photos)上传尽可能多的原始质量的照片。除了云存储的好处，谷歌还偶尔向其用户免费提供其他服务，如 YouTube Premium、Pixel 3 等硬件的折扣或免费设备。如果你正在寻找一款新的智能手机，而且你还不是 Google One 的订户，那么你可能想推迟购买订阅，因为看起来谷歌正准备将其云存储服务与即将推出的智能手机捆绑在一起。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

该应用的 1.42 版本今天早些时候在谷歌 Play 商店推出，它增加了如下所示的两个字符串。这些字符串表示“您的手机附带”一个 3 个月的会员计划，该计划授予您“访问 100GB 的存储空间、高级支持等”描述字符串奇怪地告诉用户在他们的手机上打开应用程序来开始他们的会员资格，即使这些字符串是应用程序本身的一部分。

```
 <string name="three_months_eft_description">You get access to 100GB of storage, premium support, and more. Open the Google One app on your phone to start your membership.</string>
<string name="three_months_eft_title">Your phone comes with a 3 month Google One membership</string> 
```

我们检查了 Google 相册、Google Drive 和 Gmail 的最新版本——这三种服务都是订阅的一部分——看看我们是否能找到这个字符串的引用。遗憾的是，我们没有达到目标。我们还检查了这个字符串会出现在应用程序本身的什么地方；我们只找到了一个名为 g1_education_fragment 的单一(新)布局文件，它引用了这两个字符串。

没有任何代码将这些字符串链接到任何特定的设备，所以我们不确定哪种智能手机将允许您获得 3 个月的免费订阅。不过，我希望是即将到来的谷歌 Pixel 4。我推测，如果 EFT 代表“早期现场试用”，那么这 3 个月的会员资格可能会作为预购奖金提供。谷歌[此前向当地导游提供了 3 个月的免费计划](https://www.reddit.com/r/LocalGuides/comments/9p11fo/3_months_of_free_google_one_for_being_a_local/)，但这些字符串没有明确提到任何关于当地导游的内容。

*更新:鉴于[最近发布的](https://www.nokia.com/phones/en_int/google-one#recommended-phones)诺基亚 6.2 和诺基亚 7.2 的促销活动，这些字符串可能适用于这两款诺基亚智能手机。*

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*