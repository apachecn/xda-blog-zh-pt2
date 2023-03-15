# 认识一下谷歌最新的操作系统甜点:安卓 8.0 奥利奥

> 原文：<https://www.xda-developers.com/android-8-0-oreo-google-released/>

在谷歌 I/O 大会上，谷歌通常会通过提供开发者预览版来揭开 Android 最新更新的面纱。但是 I/O 公告更侧重于开发者而不是最终用户，所以谷歌更喜欢对最新操作系统的名称和版本号保密，直到它准备好一个更完善和稳定的产品，可以交付给 Android 用户。今年，谷歌选择了美国多事之秋的日全食作为向我们展示最新美食的绝佳时机。遇见[安卓 8.0 奥利奥](https://www.android.com/versions/oreo-8-0/)。

Android 8.0 奥利奥遵循了谷歌为世界上最受欢迎的智能手机操作系统采用的甜点命名惯例。按照传统，安卓奥利奥雕像也在加州山景城的谷歌总部亮相。

日全食事件与奥利奥的营销惊人地契合，香草奶油中心和巧克力饼干威化象征着日食期间太阳和月亮之间的协同作用。除了按字母顺序和甜点灵感，命名方案背后通常没有太多隐藏的含义，但在这种情况下，谷歌看到了确保其最新发布的好处和补充日食的绝佳机会，并仍然是普通人的话题。

[button link = https://developer . ANDROID . com/about/versions/o/DOWNLOAD . html Icon = " Select a Icon " side = " left " target = " " color = " f 85050 " text color = " ffffff "]为您的 PIXEL 或 NEXUS 设备下载 **ANDROID** 8.0 **奥利奥**系统映像！[/button]

## Android 8.0 奥利奥有什么新功能？

Android Oreo 带来了许多新功能和对 Android Nougat 的改进。虽然最终用户不会立即看到所有这些功能，但它们肯定会为成熟智能手机操作系统的最终体验做出贡献。

### 重新设计的表情符号

Android Oreo 告别了我们在过去的 Android 版本中已经习惯的 blob 表情符号。取而代之的是一套重新设计的表情符号,比 blob 表情符号更圆，有更多的渐变和不同的设计语言。

### 背景限制

电池寿命仍然是谷歌在奥利奥的首要任务。Android 8.0 在这三个主要领域对应用程序在后台可以做的事情进行了额外的自动限制:隐式广播、后台服务和位置更新。我们详细讨论了[谷歌如何在 Android Nougat 中为杀死流氓后台进程](https://www.xda-developers.com/how-android-n-will-improve-battery-and-memory-management/)奠定基础，现在该公司正在进行额外的改变，以控制流氓应用程序消耗你的电池寿命。

### 通知渠道

Android Oreo 引入了[通知通道](https://developer.android.com/preview/features/notification-channels.html)来提供一个统一的系统，帮助用户使用应用程序定义的通知内容类别来管理通知。这将允许开发人员为他们需要发送的每种不同类型的通知创建一个通知通道，并反映应用程序用户的选择。用户还可以使用一致的系统用户界面管理与通知相关的大多数设置。一旦创建了通知通道，只有系统可以改变它的重要性，将权力交还给用户。用户还可以**推迟通知**在稍后的时间重新出现。通知将以与第一次出现时相同的重要性级别重新出现。

此外，Android Oreo 还为通知添加了新的视觉效果和分组，使用户在收到消息或浏览通知阴影时更容易看到发生了什么。

### Autofill APIs

Android Oreo 通过包含自动填充 API，正式承认了密码管理器的作用。这种对自动填充的平台支持将使用户能够像选择键盘应用程序一样选择自动填充应用程序。谷歌正在添加新的 API 来实现自动填充服务。

### 手机的画中画和新的窗口功能

现在，手机和平板电脑都可以使用 PiP 显示屏，因此用户现在可以在回答聊天或任何其他类似任务时观看视频。其他新的窗口功能包括供应用程序使用的[新应用程序覆盖窗口](https://developer.android.com/preview/behavior-changes.html?#cwt)，以及用于在远程显示器上启动活动的[多显示器支持](https://developer.android.com/preview/api-overview.html#mds)。

### XML 中的自适应图标和字体资源

Android Oreo 带来了[自适应图标](https://developer.android.com/preview/features/adaptive-icons.html)，现在可以在不同的设备和型号上显示各种形状。您可以在一台 OEM 设备上使用圆形来设置启动器图标，并在另一台设备上使用“squircle”。每个设备 OEM 将提供一个遮罩，然后系统使用该遮罩以相同的形状呈现所有图标。该系统还可以动画显示与图标的交互，并在快捷方式、设置应用程序、共享对话框和概览屏幕中使用图标。

字体现在是 Android Oreo 中完全支持的资源类型。应用程序现在可以在 XML 布局中使用字体，并声明字体样式和字体文件的粗细。

### 支持应用程序的宽色域色彩

成像应用的开发者现在可以利用具有宽色域彩色显示的新设备。要显示宽色域图像，应用程序需要在每个活动的清单中启用一个标志，并加载嵌入了宽颜色配置文件的位图。几个月来，我们一直在呼吁类似的功能，现在看来谷歌终于回应了我们的祈祷。

### 连通性

Android O 还支持高质量的蓝牙音频编解码器，如索尼的 [LDAC 编解码器](https://www.sony.net/Products/LDAC/)以及高通的[高质量蓝牙编解码器](https://www.aptx.com/)的 [aptX 支持](http://www.androidpolice.com/2017/03/21/feature-spotlight-android-o-looks-like-it-will-add-support-for-aptx-bluetooth-streaming/)。

新的 Wi-Fi 功能包括 [Wi-Fi 感知](https://developer.android.com/preview/features/wifi-aware.html)，也称为邻居感知网络(NAN)。在配备适当硬件的设备上，应用程序和附近的设备可以在没有互联网接入点的情况下通过 Wi-Fi 相互发现和通信。

还有新的蓝牙功能，如[蓝牙电池电量指示器](https://www.xda-developers.com/bluetooth-battery-level-indicators-android/)和[蓝牙带内铃声](https://www.xda-developers.com/bluetooth-in-band-ringtone-android-o/)。虽然它们在个体能力上有很小的改进，但是它们有助于操作系统的成熟。

### 辅助功能:指纹手势

辅助功能服务还可以响应替代输入机制，如沿设备指纹传感器的方向滑动手势。这意味着**第三方开发者**可以正式利用指纹手势来执行他们自己的操作！

* * *

今天，Android 8.0 Oreo 将被推送到 Android 开源项目(AOSP)供所有人访问。针对 Nexus 5X、Nexus 6P 和 Pixels 的更新版本已经进入运营商测试，谷歌预计将很快与 Pixel C 和 Nexus Player 一起分阶段推出。谷歌还与 Essential、General Mobile、HMD Global、华为、HTC、京瓷、LG、摩托罗拉、三星、夏普和索尼等 OEM 合作伙伴密切合作，以确保新设备要么采用 Android 8.0 Oreo，要么升级到最新的 sweet。此外，Android 测试程序中的设备也将收到这个最终版本。

我们迫不及待地想要得到最新的东西，只是想看看谷歌还藏着什么！

**你对 Android 8.0 奥利奥有什么想法？请在下面的评论中告诉我们！**