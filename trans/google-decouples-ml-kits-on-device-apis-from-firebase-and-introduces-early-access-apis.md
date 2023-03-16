# Google 将 ML Kit 的设备上 API 从 Firebase 中分离出来

> 原文：<https://www.xda-developers.com/google-decouples-ml-kits-on-device-apis-from-firebase-and-introduces-early-access-apis/>

谷歌广泛使用人工智能来提供高度关联和准确的网络和图像搜索结果。除了网络平台上的搜索，谷歌的机器学习模型还为 Android 手机提供了各种人工智能应用，从谷歌镜头上的视觉搜索到像素设备闻名的 T2 计算摄影。除了自己的应用程序，谷歌还允许第三方开发者在 ML Kit 的帮助下，将机器学习功能无缝集成到他们的应用程序中，ML Kit 是一个 SDK(软件开发工具包)，是 Firebase 的一部分，Firebase 是其用于移动开发的在线管理和分析仪表板。截至今天，谷歌宣布了对 ML 工具包的重大改变，并将使设备上的 API 独立于 Firebase。

[ML Kit 在 Google I/O 2018](https://www.xda-developers.com/google-ml-kit-machine-learning/) 上公布，旨在简化向应用添加机器学习功能。在推出时，ML Kit 由文本识别、人脸检测、条形码扫描、图像标记和地标识别 API 组成。2019 年 4 月，谷歌以智能回复和语言识别的形式，向面向开发者的 SDK 推出了首个自然语言处理(NLP)API。一个月后，即在谷歌 I/O 2019 上，[谷歌推出了三个新的 ML API](https://www.xda-developers.com/firebase-3-new-capabilities-ml-kit-performance-monitoring-web-apps/)，用于设备上翻译、对象检测和跟踪，以及 [AutoML Vision Edge API](https://firebase.google.com/docs/ml/automl-image-labeling) ，用于使用视觉搜索识别特定对象，如花卉或食物的类型。

ML 工具包包括基于设备和基于云的 API。正如你所料，设备上的 API 使用保存在设备上的机器学习模型处理数据，而基于云的 API 将数据发送到谷歌云平台上的机器学习模型，并通过互联网连接接收解析的数据。由于设备上的 API 无需互联网就能运行，因此它们可以更快地解析信息，并且比基于云的 API 更安全。设备上的机器学习 API 也可以在运行 Android Oreo 8.1 和更高版本的 Android 设备上进行硬件加速，并运行谷歌的神经网络 API (NNAPI)，以及在高通、联发科、海思等最新芯片组上找到的特殊计算模块或 npu。

Google 最近发布了一篇博文,宣布 ML Kit 的设备上 API 现在将作为独立 SDK 的一部分提供。这意味着 ML 套件中的设备上 API–包括文本识别、条形码扫描、人脸检测、图像标记、对象检测和跟踪、语言识别、智能回复和设备上翻译–将在一个单独的 SDK 下提供，无需 Firebase 即可访问。然而，Google 确实推荐在 Firebase 中使用 ML Kit SDK 来[迁移他们现有的项目](https://developers.google.com/ml-kit/migration)到新的独立 SDK。一个新的[微型网站](https://developers.google.com/ml-kit/)已经发布，包含所有与 ML 套件相关的资源。

除了新的 SDK，谷歌还宣布了一些变化，使开发者更容易将机器学习模型集成到他们的应用程序中。首先，人脸检测/轮廓模型现在作为 Google Play 服务的一部分提供，因此开发人员不必为他们的应用程序单独克隆 API 和模型。这使得应用程序包的大小更小，并且能够在其他应用程序中更无缝地重用该模型。

其次，谷歌在所有 API 中加入了 [Android Jetpack 生命周期](https://developer.android.com/reference/androidx/lifecycle/Lifecycle)支持。这将有助于在应用程序经历屏幕旋转或被用户关闭时管理 API 的使用。此外，它还便于将 [CameraX Jetpack 库](https://www.xda-developers.com/google-camerax-android-api-third-party-apps-best-features-stock-camera/)集成到使用 ML 工具包的应用程序中。

第三，谷歌已经宣布了一个[早期访问计划](https://developers.google.com/ml-kit/early-access)，这样开发者可以在其他人之前获得即将到来的 API 和特性。该公司现在正在 ML 工具包中添加两个新的 API，供精选的开发人员预览并分享他们的反馈。这些 API 包括:

*   [实体提取](https://developers.google.com/ml-kit/early-access/entity-extraction)检测文本中的电话号码、地址、付款号码、跟踪号码和日期&时间，以及
*   [姿势检测](https://developers.google.com/ml-kit/early-access/pose-detection)用于 33 个骨骼点的低延迟检测，包括手和脚

最后，谷歌现在允许开发人员用来自 [TensorFlow Lite](https://www.xda-developers.com/tensorflow-lite-mobile-machine-learning/) 的定制机器学习模型来替换 ML 工具包中现有的图像标记以及对象检测和跟踪 API。该公司将很快宣布更多关于如何找到或克隆 TensorFlow Lite 模型并使用 ML Kit 或 Android Studio 新的 ML 集成功能训练它们的细节。