# 谷歌宣布 Android O，开发者预览版 1 可用于支持的设备

> 原文：<https://www.xda-developers.com/google-announces-android-o-developer-preview-1-available-for-supported-devices/>

厌倦了在智能手机上运行安卓牛轧糖？渴望了解世界上最受欢迎的移动操作系统的下一代产品的未来吗？谷歌今天为你做了报道，因为该公司刚刚宣布了 Android 牛轧糖之后的产品。

遇见**安卓 O** 。

按照谷歌的习惯，Android O 将是下一个操作系统版本的名称，直到它最终在 2017 年第三季度的某个时候向消费者推出。我们可以推测全名是什么，我们也有几个月的时间来这样做。

但是我们现在拥有的是一个完整的开发者预览版和 O 将会给 Android 带来的大量变化。谷歌已经列出了 Android O 中的[新功能](https://android-developers.googleblog.com/2017/03/first-preview-of-android-o.html)和[API](https://developer.android.com/preview/api-overview.html)，所以我们将在下面简要介绍其中几个。

[**查看我们的 Android O 全覆盖！**](https://www.xda-developers.com/tag/android-o/)

* * *

### 背景限制

电池寿命仍然是谷歌在 O 中优先考虑的问题。Android O 在以下三个主要领域对应用程序在后台可以做的事情进行了额外的自动限制:隐式广播、后台服务和位置更新。我们详细讨论了[谷歌如何在 Android Nougat 中为杀死流氓后台进程](https://www.xda-developers.com/how-android-n-will-improve-battery-and-memory-management/)奠定基础，但现在该公司正在进行额外的改变，以控制流氓应用程序消耗你的电池寿命。这些变化将使创建对用户电池寿命影响最小的应用变得更加容易，因此谷歌建议查看关于[后台执行限制](https://developer.android.com/preview/features/background.html)和[后台位置限制](https://developer.android.com/preview/features/background-location-limits.html)的文档以了解更多细节。

### 通知渠道

Android O 引入了[通知通道](https://developer.android.com/preview/features/notification-channels.html)来提供一个统一的系统，帮助用户使用应用程序定义的通知内容类别来管理通知。这将允许开发人员为他们需要发送的每种不同类型的通知创建一个通知通道，并反映应用程序用户的选择。例如，开发人员可以为消息应用程序中的每个会话组创建单独的通知通道。

用户还可以使用一致的系统用户界面管理与通知相关的大多数设置。发布到特定渠道的所有通知将表现相同。

Android O 也反对开发者设置单个通知的优先级。相反，用户现在可以在创建通知通道时设置推荐的重要性级别。一旦创建了通知通道，只有系统可以改变它的重要性，将权力交还给用户。

用户也可以**暂停通知**在以后重新出现。通知将以与第一次出现时相同的重要性级别重新出现。应用程序也可以删除或更新休眠通知，但更新休眠通知不会导致它重新出现。

此外，Android O 还为通知添加了新的视觉效果和分组，使用户在收到消息或浏览通知阴影时更容易看到发生了什么。对我们来说，这听起来很像旧版本 Android 上的通知栏，尽管我们必须确认这一点。

### Autofill APIs

Android O 通过包含一个自动填充 API，正式承认了密码管理器的作用。这种对自动填充的平台支持将使用户能够像选择键盘应用程序一样选择自动填充应用程序。谷歌正在添加新的 API 来实现自动填充服务。

### 手机的画中画和新的窗口功能

现在，手机和平板电脑都可以使用 PiP 显示屏，因此用户现在可以在回答聊天或任何其他类似任务时观看视频。开发人员可以指定纵横比和一组自定义交互，如暂停/播放。

其他新的窗口功能包括[新的应用程序覆盖窗口](https://developer.android.com/preview/behavior-changes.html?#cwt)供应用程序使用，而不是系统警告窗口，以及[多显示器支持](https://developer.android.com/preview/api-overview.html#mds)用于在远程显示器上启动活动。

### XML 中的字体资源

字体现在是 Android O 中完全支持的资源类型。应用程序现在可以在 XML 布局中使用字体，以及声明字体样式和字体文件的粗细。

### 适应性图标

Android O 还带来了[自适应图标](https://developer.android.com/preview/features/adaptive-icons.html)，现在可以在不同的设备和型号上显示各种形状。您可以在一台 OEM 设备上使用圆形来设置启动器图标，并在另一台设备上使用“squircle”。每个设备 OEM 将提供一个遮罩，然后系统使用该遮罩以相同的形状呈现所有图标。该系统还可以动画显示与图标的交互，并在快捷方式、设置应用程序、共享对话框和概览屏幕中使用图标。

### 应用程序的宽色域色彩

成像应用的开发者现在可以利用具有宽色域彩色显示的新设备。要显示宽色域图像，应用程序需要在每个活动的清单中启用一个标志，并加载嵌入了宽颜色配置文件的位图。我们已经为这个功能吵了几个月了，现在看来谷歌终于回应了我们的祈祷。

### 连通性

Android O 还支持高质量的蓝牙音频编解码器，如索尼的 [LDAC 编解码器](https://www.sony.net/Products/LDAC/)。 *Android Police* 通过谷歌的一份声明证实，此次更新带来了 [aptX 支持](http://www.androidpolice.com/2017/03/21/feature-spotlight-android-o-looks-like-it-will-add-support-for-aptx-bluetooth-streaming/)，这是一款来自高通的[高质量蓝牙编解码器](https://www.aptx.com/)。

新的 Wi-Fi 功能包括 [Wi-Fi 感知](https://developer.android.com/preview/features/wifi-aware.html)，也称为邻居感知网络(NAN)。在配备适当硬件的设备上，应用程序和附近的设备可以在没有互联网接入点的情况下通过 Wi-Fi 相互发现和通信。

谷歌还从电信框架中扩展了[connection service API](https://developer.android.com/reference/android/telecom/ConnectionService.html),使第三方呼叫应用程序能够与系统 UI 集成，并与其他音频应用程序无缝运行。例如，应用程序可以在不同类型的用户界面中显示和控制呼叫，如汽车主机。

### 键盘导航

Android O 致力于为“箭头”和“标签”导航建立一个更加可靠和可预测的模型。这是鉴于 Chrome OS 上 Android 应用的官方可用性，Chrome OS 的设备上有硬件键盘。您可以在此查看完整文档[。](https://developer.android.com/training/keyboard-input/navigation.html)

### 用于专业音频的 AAudio API

AAudio 是一种新的原生 API，专为需要高性能和低延迟音频的应用程序而设计。开发者预览版包含了这个 API 的早期版本，以获得开发者的反馈。

### WebView 增强功能

Android O 默认为 WebViews 启用多进程模式，并增加了一个 API，允许应用程序处理错误和崩溃。开发者还可以选择他们应用的 WebView 对象，通过谷歌安全浏览来验证网址。

### Java 8 语言 API

Android O 支持几个新的 Java 语言 API。此外，Android 运行时比以往任何时候都快，谷歌声称在一些应用程序基准测试中提高了 2 倍。

### 辅助功能:指纹手势

辅助功能服务还可以响应替代输入机制，如沿设备指纹传感器的方向滑动手势。这意味着**第三方开发者**可以正式利用指纹手势来执行他们自己的操作！

* * *

## 开发者预览

如果你真的真的很想试用 Android O，你可以试试谷歌为 Nexus 5X、Nexus 6P、Nexus Player、谷歌 Pixel、Pixel XL 和 Pixel C 设备提供的系统图像。此外，您还可以下载更新的 SDK，并在官方 Android 模拟器上试用 Android O。也有一个模拟器用于在 Android O 上测试 Android Wear 2.0。

谷歌极力坚持这个开发者预览版只面向开发者。它不是为日常和消费者使用而设计的(但这可能不会阻止 XDA 的读者)。因此，这些版本只能手动下载和刷新。一旦谷歌接近最终产品，Android Beta 计划将开放注册，因此 Android Beta 目前不适用于 Android O。在今年第三季度的最终发布之前，将有 3 个额外的开发者预览。下一个开发者预览版将会在五月中旬的某个时候发布，所以在谷歌给我们更多的好处之前，我们将有 2 个月的时间来玩这个新的更新。

#### 对于 Android O 开发者预览版 1 的下载链接和闪烁说明，[请点击这里](https://developer.android.com/preview/download.html)。

* * *

我们对 Android O 及其给 Android 生态系统带来的变化感到兴奋。这是更多开发者预览版中的第一个，所以我们可以肯定的是，这里介绍的特性将会在它们到达最终消费者手中时得到完善。

**你对 Android O 及其开发者预览版 1 有什么想法？请在下面的评论中告诉我们！**