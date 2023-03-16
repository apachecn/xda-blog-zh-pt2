# Android 11 开发者预览版-所有新的开发特性

> 原文：<https://www.xda-developers.com/android-11-developer-preview-new-development-features/>

今天，谷歌[在官方博客文章中宣布了](https://www.xda-developers.com/android-11-developer-preview-1-google-pixel)首个 Android 11 开发者预览版。该公司已经为任何有兴趣安装新 Android 操作系统的开发者发布了系统映像。我们建议您尽快安装它，以便根据 Android 11 中最新的行为变化和平台功能来测试您的应用程序。在你深入阅读这些文档之前，这里有一个在第一个 Android 11 开发者预览版中所有主要的以开发者为中心的新特性的总结。

## 新的网络/连接功能

5G 连接将在今年和明年风靡一时:三星正在通过 Galaxy S20 系列广泛提供支持 5G 的智能手机[，而](https://www.xda-developers.com/samsung-galaxy-s20-s20-plus-ultra-5g-us/)[高通继续提高 5G 智能手机连接的标准](https://www.xda-developers.com/qualcomm-snapdragon-x60-modem-5g-smartphones/)。在 Android 11 中，谷歌增加了两个新的 API，让开发者为 5G 连接的现实做好准备。不仅如此，其他基于连接的 API 也在不断完善。

**带宽估算器 API**

谷歌[正在更新 ConnectivityManager](https://developer.android.com/reference/android/net/ConnectivityManager) 以便更容易检查下行和上行带宽，而不需要轮询网络或需要开发者计算他们自己的估计。如果调制解调器不支持提供该数据，API 将基于现有的网络连接进行默认估计。

**动态计量 API**

该 API 允许开发者检查用户是否处于未计量的连接，如果是，则提供可能使用更多数据的更高分辨率或质量的媒体。随着 Android 11 的推出，这种 API 已经扩展到包括蜂窝网络，因此开发人员现在可以识别运营商在其 5G 网络上提供真正未计量数据服务的用户。

**来电过滤服务改进**

谷歌在 Android 10 中引入了“角色”的概念。它们有点类似于“默认应用程序”，因为授予应用程序一个角色允许它访问某些 API。例如，有一个[来电过滤角色](https://developer.android.com/reference/android/app/role/RoleManager.html?hl=en#ROLE_CALL_SCREENING)，它允许第三方应用在用户意识到来电之前阻止或识别来电。在 Android 11 中，来电筛选应用现在可以获得来电的[搅动/摇动](https://en.wikipedia.org/wiki/STIR/SHAKEN)验证状态，作为通话细节的一部分。然后，他们可以自定义系统提供的呼叫后屏幕，让用户执行诸如将呼叫标记为垃圾邮件或将呼叫者添加到联系人等操作。这将有助于来电筛选应用程序通过简化未知来电者的反应来为用户做更多的事情。

**Wi-Fi 建议 API 增强功能**

Wi-Fi 建议 API 现在将允许连接管理应用程序更好地管理自己的网络。例如，连接管理应用程序现在将能够通过删除网络建议来强制断开连接，管理 Passpoint 网络，接收有关连接网络质量的更多信息，等等。

**Passpoint 增强功能**

根据 Wi-Fi 联盟的说法，Wi-Fi Passpoint 是一种解决方案，它通过实现自动网络发现和选择、简化在线注册和无缝支持热点漫游来简化对 Wi-Fi 热点的网络访问。Android 11 将允许强制执行和通知 [Passpoint 配置文件](https://source.android.com/devices/tech/connect/wifi-passpoint)的到期日期，以及支持配置文件中的通用名称规范，并允许 Passpoint R1 配置文件的自签名 ca。如上所述，Wi-Fi 建议 API 还将允许连接应用程序管理 Passpoint 网络。

## 新的用户界面/UX 功能

**支持打孔和瀑布显示的 UI**

Android 智能手机原始设备制造商引领硬件领域的创新，最近我们看到的最显著的硬件变化之一是引入了显示屏剪切块。例如，三星 Galaxy S20 系列采用单中心打孔显示屏。打孔显示器，谷歌称之为针孔显示器，是一种显示器，它的整个边缘都被显示器像素包围着，就像有人在显示器上使用打孔器一样。另一项显示器创新是瀑布显示器:显示器在侧边有更明显的显示曲线，向下溢出到设备的两侧。

*左图:三星 Galaxy S20+采用单中心打孔显示屏。右图:采用曲面“瀑布”显示屏的华为 Mate 30 Pro 和 Vivo Nex 3 5G。*

Android 11 现在通过[显示剪切 API](https://developer.android.com/guide/topics/display-cutout) 扩展对打孔显示和瀑布显示的支持。如果开发人员愿意，API 还将允许他们构建可以使用包括边缘在内的整个瀑布屏幕的应用程序，并通过插入来帮助管理边缘附近的交互。

**通知中的专用对话部分**

我们很多人一天会收到大量通知，但并不是每个通知都同样重要。一般来说，来自消息应用的通知往往比来自其他应用的通知更重要。为此，Android 11 在通知阴影中引入了专门的对话部分。这将允许用户在他们最喜欢的应用程序中轻松找到他们正在与人进行的对话，并帮助开发人员创建更深入的对话体验。

**气泡 API**

去年，我们已经指出了 Android 10 中引入的 [Bubbles API 将如何在未来的 Android 版本中取代 overlay API。随着 Android 11 的推出，谷歌正在推动消息和聊天应用的开发者向气泡过渡，以便当用户在手机上进行多任务处理时，可以看到和访问对话。](https://www.xda-developers.com/android-q-system-alert-window-deprecate-bubbles/)

**在通知回复中插入图像**

Android 11 现在将允许支持复制/粘贴图像的应用程序让用户直接将这些图像插入通知的内嵌回复中，这意味着用户可以长按并在从通知阴影回复通知时使用粘贴上下文菜单选项。谷歌 Chrome 已经在努力支持将图片直接复制到安卓的剪贴板上，Gboard 正准备让用户直接将图片粘贴到社交媒体和消息应用上。谷歌现在提到这些功能将在 Android 11 开发者预览版 1 上提供。

## 图像和相机改进

**HEIF 动画绘画**

ImageDecoder API 现在将允许开发人员解码和渲染存储在 [HEIF(高效图像格式)](https://source.android.com/devices/camera/heif)文件中的图像序列动画。这将允许开发者利用高质量的资产，同时最小化对网络数据和 APK 大小的影响。与 gif 相比,, HEIF 图像序列提供了[大幅度的文件大小缩减，因此 HEIF 在基于移动的用例中处于一个更好的位置。开发人员将能够通过使用 HEIF 源调用 decodeDrawable 在他们的应用程序中显示 HEIF 图像序列。如果源包含图像序列，则返回 AnimatedImageDrawable。](https://nokiatech.github.io/heif/comparison.html)

**原生图像解码器**

Android 11 引入了新的 NDK API，允许应用程序从原生代码中解码和编码图像，用于图形或后期处理，同时保留较小的 APK 大小，因为不需要捆绑外部库。原生解码器还利用了 Android 的持续平台安全更新过程。

**相机拍摄期间静音**

当相机捕捉会话处于活动状态时，新的 API 允许应用程序将铃声、警报和通知的振动静音，因为这些振动可能会给录制带来震动，如果用户放大，这种震动可能会进一步放大。

**散景模式**

应用程序现在可以使用元数据标签在支持相机捕捉请求的设备上启用散景模式。

**低延迟视频解码**

应用程序现在可以使用新的 API 来[检查](https://developer.android.com/reference/android/media/MediaCodecInfo.CodecCapabilities#isFeatureSupported(java.lang.String))并为特定的编解码器配置低延迟播放。

低延迟视频对于实时视频流应用和服务(如 [Stadia](https://www.xda-developers.com/tag/google-stadia/) )至关重要。支持低延迟播放的视频编解码器在解码开始后尽快返回流的第一帧。

**HDMI 低延迟模式**

新的 API 现在允许应用程序检查和请求外部显示器和电视上的自动低延迟模式(也称为游戏模式)。在这种模式下，显示器或电视会禁用图形后处理，以最大限度地减少延迟。

## 其他新增和更新的 API

**神经网络 API 1.3**

神经网络 API (NNAPI)旨在为 Android 设备上的机器学习运行计算密集型操作。随着 Android 11 的推出，谷歌正在扩展该 API 下开发者可用的操作和控制:

*   服务质量 API 支持模型执行的优先级和超时。
*   内存域 API 减少了连续模型执行的内存复制和转换。
*   通过[带符号整数非对称量化](https://www.tensorflow.org/lite/performance/quantization_spec)扩展量化支持，其中带符号整数用于代替浮点数，以实现更小的模型和更快的推断。

**应用兼容性**

新的平台更新可能会给应用程序开发者带来潜在的应用程序兼容性问题，因此谷歌也在优先考虑应用程序兼容性方面开展工作。随着 Android 11 的推出，谷歌正在增加新的流程、开发工具和发布里程碑，旨在将平台更新的影响降至最低，从而将兼容性问题降至最低。

*   将行为变化的影响降至最低:谷歌有意识地努力将可能影响应用的行为变化降至最低。所有这些变化都与它们的影响一起受到了密切的审查，并试图让尽可能多的人选择加入，直到开发人员将其应用程序的 targetSdkVersion 设置为 Android 11。目前还不能发布针对 API level 30 的应用，但谷歌将在未来的 Android 11 开发者预览版中实现这一功能。
*   更容易的测试和调试:与我们上个月报道的一样，第一个 Android 11 开发者预览版带有一个[“应用兼容性”开发者选项，以帮助开发者测试新的平台变化](https://www.xda-developers.com/android-11-new-app-compatibility-developer-option-dev-test-new-platform-changes/)。Android 11 开发者预览版中引入的许多突破性变化已经可以切换——允许开发者从开发者选项或通过 ADB 单独强制启用或禁用这些变化。这应该有助于减轻测试应用程序兼容性时的痛苦，因为开发人员不需要为基本测试重新编译他们的应用程序或更改 targetSdkVersion。

*   更新灰名单:谷歌更新了[受限非 SDK 接口](https://www.xda-developers.com/google-undocumented-hidden-apis-android-p/)的名单。Android 11 开发者预览版也[移除了一些开发者正在使用的元反射解决方案](https://www.xda-developers.com/android-11-harden-hidden-api-restriction-meta-reflection/)。
*   动态资源加载器:开发者要求一个公共 API 来在运行时动态加载资源和资产，在 Android 11 中，Google 增加了一个资源加载器框架。
*   新的平台稳定性里程碑:在开发者预览/测试阶段，为早期兼容性准备应用程序对开发者来说是一个挑战，因为该版本平台的最终更改没有明确的日期。因此，在 Android 11 中，谷歌增加了一个新的发布里程碑，称为“平台稳定性”，谷歌预计将在 6 月初达到。这一里程碑式的发布不仅包括最终的 SDK 和 SDK and，还包括最终的内部 API 和其他可能影响应用的系统行为。关于发布时间表的更多信息可以在谷歌的开发者网站上找到。

* * *

如果您想测试新的 Android 11 开发者预览版，您可以将预构建的系统映像闪存到 Pixel 2、Pixel 2 XL、Pixel 3、Pixel 3 XL、Pixel 3a、Pixel 3a XL、Pixel 4 或 Pixel 4 XL 上。或者，您可以使用解锁的引导加载程序将预先构建的、谷歌签名的通用系统映像(GSI)闪存到任何 Project Treble 支持的设备上。如果你没有支持 Pixel 的手机或支持 Project Treble 的设备，并且没有解锁的引导加载程序，那么你可以在 Android Studio 中下载模拟器的最新系统映像。运行 Android 11 系统映像的 Android 模拟器具有在 64 位 x86 系统映像上运行 ARM 32 和 64 位二进制代码的实验支持。

除了设置 Android 模拟器，还可以在 Android Studio 内部下载 Android 11 开发者预览版 SDK 和 NDK。Google 建议您将 Android Studio 更新到最新的 Canary 版本,以利用 IDE 的最新功能。设置完成后，您可以通过查看 API 概述、API 参考和 API 差异报告，在 Android 11 开发者预览版中探索最新的平台功能和行为变化。如果你有任何反馈，你可以通过他们的任何官方渠道让谷歌知道。如果你在开发者预览版中发现了一个 bug，你可以在谷歌问题跟踪器上提交一份报告[。最后，请务必关注我们的新闻标签，了解 Android 11 的最新更新——我们发现有许多平台功能和行为变化是谷歌没有记录的！](https://issuetracker.google.com/issues?q=componentid:190602%2B%20created%3E%3D2020-02-19)

**[安卓 11 XDA 新闻](https://www.xda-developers.com/tag/android-11/)**