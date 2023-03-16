# 谷歌的 ML 工具包是一个新的 Firebase SDK，它解决了机器学习的难题

> 原文：<https://www.xda-developers.com/google-ml-kit-machine-learning/>

近年来，机器学习和人工智能迅速进入了我们的词汇，但很少有人真正理解这项技术是如何工作的，或者它们有什么能力。甚至谷歌自己的人工智能研究人员[也开玩笑说机器学习类似于炼金术](https://www.sciencemag.org/news/2018/05/ai-researchers-allege-machine-learning-alchemy)。作为一名忙碌的开发人员，你可能没有时间学习机器学习(ML)，但谷歌不希望这阻止你获得它的好处。出于这个原因，该公司今天宣布了 **ML Kit** :一个新的 SDK，它将谷歌多年来在机器学习方面的工作整合到一个 Firebase 包中，iOS 和 Android 上的移动应用程序开发者可以用它来增强他们的应用程序。

如果你[对机器学习](https://www.xda-developers.com/developers-survey-open-source-ai-machine-learning/)一无所知，那么不要苦恼:**你不需要任何先前背景的 ML 知识**。您可能熟悉该技术的一些现实应用，如人脸检测和图像识别。谷歌的 ML 工具包希望你的应用程序能够从 ML 的实际应用中受益，而不需要你理解算法是如何工作的。如果你了解 ML 或者愿意学习，你也可以利用 ML 工具包。

* * *

## 用 ML 工具包为初学者学习机器

Google 新推出的 Firebase SDK for ML 为移动设备上最常见的一些用例提供了五个 API:

*   文本识别
*   人脸检测
*   条形码扫描
*   图像标注
*   地标识别

您所需要做的就是将数据传递给 API，SDK 会返回一个响应。就这么简单。ML 使用的一些例子包括音乐应用程序，它解释您弹奏的音符并将回声/噪声消除应用到您的音乐中。另一个例子是光学字符识别(OCR ),用于卡路里计数应用程序的营养标签。

可用的基础 API 列表将在未来几个月内扩展，包括一个智能回复 API，就像 [Android P](https://www.xda-developers.com/android-p-developer-preview-1-google-pixel-xl-pixel-2-xl/) 和一个高密度人脸轮廓添加到人脸检测 API。

* * *

## 面向有经验用户的 ML 套件

如果您有一点背景知识，那么您也可以部署自己的定制 [TensorFlow Lite](https://www.tensorflow.org/mobile/tflite/) 模型。你所要做的就是将你的模型上传到 Firebase 控制台，这样你就不必担心将模型捆绑到你的 APK 中(从而减少文件大小)。)ML 工具包动态地服务于您的模型，因此您可以更新您的模型，而无需重新发布您的应用程序。

更好的是，谷歌会自动将完整的 TensorFlow 模型压缩成 TensorFlow Lite 模型，这可以减少文件大小，并确保更多有限数据连接的人可以享受你的应用程序。

* * *

## 设备上和云 API

ML Kit 提供了设备上和云 API。设备上的 API 在没有网络连接的情况下处理数据(如 [Android Oreo 的文本选择功能](https://www.xda-developers.com/android-oreo-smart-text-selection-stable-google-chrome/))，而云 API 使用谷歌云平台来处理数据，以获得更高的准确性。

ML Kit 在 Android 和 iOS 上都可以工作，特别是在 Android 上，它可以与运行像冰激凌三明治一样古老的 Android 版本的设备一起工作。如果用户运行的是 [Android 8.1 Oreo](https://www.xda-developers.com/android-8-1-oreo-final-release-imminent/) 和更高版本，那么 ML Kit 将提供更好的性能，这要归功于已经存在的神经网络 API。在拥有专用硬件芯片组的设备上，如[高通骁龙 845](https://www.xda-developers.com/qualcomm-snapdragon-845-hands-on-benchmarks-first-impressions/) ( [及其 Hexagon DSP](https://www.xda-developers.com/qualcomm-snapdragon-845-hexagon-685-dsp/) )或[海思麒麟 970](https://www.xda-developers.com/how-the-kirin-970-uses-ai-to-take-better-photos/) (及其神经处理单元)，设备上的处理将得到加速。谷歌表示，他们正在与 SoC 供应商合作，以提高设备上的识别能力。

* * *

## 结论

想要开始的开发者应该在 [Firebase 控制台](https://console.firebase.google.com)中寻找新的 SDK。你可以在[的 Firebase](https://groups.google.com/forum/#!forum/firebase-talk) 谷歌群中留下反馈。

有 ML 经验的开发人员如果想尝试谷歌压缩张量流模型的算法，可以在这里注册。最后，如果你想尝试多种定制模式，请查看 [Firebase 远程配置](https://firebase.google.com/docs/remote-config/)；它允许您动态地切换模型值，创建群体细分，并并行试验几个模型。