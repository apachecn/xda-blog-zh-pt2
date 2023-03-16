# 在大多数 Android 设备上下载最新的谷歌记录器应用程序

> 原文：<https://www.xda-developers.com/download-latest-google-recorder-app-android/>

谷歌最新的 Pixel 4 智能手机有很多吸引人的功能，如 90Hz 刷新率显示屏和谷歌最新的相机软件，但我们个人认为非常有用的功能之一是新的谷歌记录器应用程序。这个应用程序是一个完全离线的录音机，具有实时转录和音频搜索。谷歌的 Recorder 应用程序可能不完全是原创的，也不是功能最丰富的，但它确实做得很好。如果你拥有 Pixel 3a、Pixel 3 或 Pixel 2，那么只要你运行的是【2019 年 12 月发布的最新软件，这个应用[也可以为你](https://www.xda-developers.com/pixel-4-recorder-app-screen-attention-older-pixel/)使用。如果你有第一代 Pixel 或任何其他智能手机，那么你必须采取非常规手段下载并安装最新版本的谷歌记录器应用程序。

如果你是一名希望录制讲座的学生，或者如果你是一名希望录制采访的记者，这个应用程序真的很有用。我个人觉得快速记下我在想什么真的很有用；打开 Google Recorder 应用程序并开始交谈比在 Google Keep 这样的应用程序中输入我的想法要快得多。

目前唯一支持转录的语言是美国英语，所以如果英语不是您的主要语言，您可能很难让转录引擎识别您的语音。在我的 Pixel 4 上运行该应用程序时，即使在嘈杂的环境中，它也能转录我的声音，尽管在非官方支持的手机上，你的里程数可能会有所不同。最后，保存录音的音频质量不是很高，但谷歌正在研究让你以更高质量的 WAV 格式保存音频的方法。如果你认为你会发现这个应用程序很有用，那么下面是如何在大多数现代 Android 智能手机上安装它的方法。

## 下载最新的谷歌记录器应用程序

**要求**

1.  运行 Android 9 Pie 或 Android 10 的 Android 智能手机。该应用不是为早于 Android 9 Pie 的 Android 版本开发的。
2.  Android 软件，无需对 Android 框架中的 TextView 组件进行重大修改。似乎谷歌记录器应用程序在某些设备上无法正常工作，因为这些设备正在运行修改了 TextView 的软件。不过，如果不进行实际测试，就无法判断这款应用是否能在你的设备上运行，因此我们在一系列不同的手机上进行了测试，以省去你的麻烦:
    *   完全有效
        *   运行 Android 10 的谷歌 Pixel 和 Pixel XL
        *   运行 EMUI 9 (Android 9 Pie)或 EMUI 10 (Android 10)的华为和 Honor 手机
        *   运行 LG UX 8.0 的 LG 手机(安卓 9 派)
        *   运行 Android 9 的摩托罗拉手机
        *   运行 Android 9 的诺基亚手机
        *   运行一个 UI 1.0/1.5 (Android 9 Pie)或一个 UI 2.0 (Android 10)的三星 Galaxy 手机
        *   运行 Android 9 Pie 或 Android 10 的索尼 Xperia 手机
        *   任何运行基于 AOSP Android 9 Pie 或 Android 10 定制 ROM 的手机
    *   部分有效(录音有效，但保存后转录不可见)
        *   基于 Android 9 Pie 或 Android 10 运行 ROG UI 2.0/ZenUI 6.0 的华硕手机
        *   基于 Android 9 Pie 运行 ColorOS 6 的 OPPO 和 Realme 手机
        *   基于 Android 10 运行 OxygenOS 10 的一加手机
    *   不起作用
        *   运行 MIUI 10 或 MIUI 11 的小米手机

如果你想直接从谷歌下载谷歌记录器应用程序的官方未修改版本，只有一个版本可以在不支持的设备上运行:我找到并上传到 APKMirror 的[泄露的 APK。虽然这是一个旧版本的应用程序(版本 1.0.271)，但它仍然具有应用程序的关键功能，如实时转录和音频搜索。](https://www.xda-developers.com/google-recorder-app-pixel-4-update-transcriptions-audio-search/)

或者，如果你想要最新版本的应用程序(版本 1.1.284)，你可以下载我上传到 AndroidFileHost 的修改版本。它与原来的应用程序具有相同的包名，但由不同的签名密钥(我自己的)签名，所以它不会安装在正式版本的顶部。我在 app 里唯一改变的是要求有 PIXEL_2017_EXPERIENCE 特征标志；移除此标志后，应用程序不再会在不受支持的设备上立即关闭。

**下载 Google Recorder App** : [官方 1 . 0 . 271](https://www.apkmirror.com/apk/google-inc/google-recorder/google-recorder-1-0-271580629-release/google-recorder-1-0-271580629-android-apk-download/)| |[非官方 1.1.284](https://www.androidfilehost.com/?fid=4349826312261685031)

在我们试图让这款应用在更多设备上运行的过程中，我们发现，至少在应用不会立即崩溃的手机上(即除了小米之外的所有人)，转录*被保存*，即使应用程序在保存录音后无法显示它们。当我将谷歌记录器应用程序的数据文件夹从我的一加 6T 转移到我的 Pixel 2 XL 时，我认为没有保存在一加 6T 上的转录突然在 Pixel 2 XL 上可见。这一点，加上我们在 MIUI 上调试崩溃时保存的日志，让我们相信 OEM 软件是该应用程序在所有设备上无法正常工作的罪魁祸首。为了进一步证明这一点，我们证实这款应用可以在运行 AOSP 定制 rom 的一加和小米设备上完全运行。

因此，要么谷歌需要对他们的应用程序进行修改，要么原始设备制造商需要对他们的软件进行修改，以便应用程序可以在每台设备上运行。不过，我不怪谷歌将这款应用锁定在 Pixel 智能手机上，因为这是一个杀手级功能。这就是为什么 XDA 论坛在这里。