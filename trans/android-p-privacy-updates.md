# P 代表隐私:Android P 将如何增强用户隐私

> 原文：<https://www.xda-developers.com/android-p-privacy-updates/>

当 Android 的新开发者预览版出来的时候，总是有一股寻找所有最新功能的热潮涌向 T2。尽管[的一些新增功能](https://www.xda-developers.com/android-p-blocks-custom-overlays-substratum-themes/)可能不如[的其他功能](https://www.xda-developers.com/android-p-screenshot-editor/)好，但你总是可以依靠迭代的 Android 更新来包含许多隐私和安全方面的改进。有时这是以牺牲用户自由为代价的，但这是谷歌进一步进入企业市场空间和保护用户的努力。安卓 P 也没什么不同。增加了许多附加功能，以增强用户隐私，并进一步保护 Android 设备所有者免受恶意应用程序和黑客的攻击。

* * *

## Android P 中的网络和云安全改进

### 应用程序中的默认 HTTPS

HTTPS 极其重要，尤其是在通过公共 WiFi 上网或在线处理敏感信息时。当数据被加密时，任何试图在路由器和您的设备之间拦截您的数据的人都将什么也看不见。因此，谷歌强制要求所有为安卓平台及以上平台构建的应用程序默认通过 HTTPS**传输所有数据。如果开发人员想要使用它，他们必须显式地启用常规的明文 HTTP。使用 HTTPS 不是必须的，但强烈建议使用。**

 **### 云备份需要密码才能在 Android P 上恢复

通过 Google Drive 进行云备份现在需要密码来恢复您的 Android P 设备。这是因为您的数据会在备份时通过使用设备生成加密密钥来加密。没有密码，您的数据将无法恢复。一旦你的数据被加密，任何人，甚至是谷歌，都不能访问你的数据。如果从 Android P 设备转移到 Android Oreo 或更低版本的设备，加密备份将如何处理还不清楚。这项功能在 Android P 中还没有，但在未来的开发者预览版中会有。

### 动态更改 MAC 地址

当您连接到网络时，网络所有者可以看到您的 MAC 地址(设备的唯一标识符)。这没什么大不了的，但理论上，你的行动可能会被多个网络所有者合谋跟踪。从 Android P 开始的 Android 设备将支持为新的 WiFi 网络创建新的 MAC 地址，目的是在具有每个唯一 MAC 地址的网络上保持一致。这个功能是实验性的，在 Android P 中是关闭的，但理论上是可以启用的。

* * *

## Android P 中的系统安全改进

### 支持 APK 签名方案 v3

[我们很久以前就看到了 APK 签名方案 v3 支持的到来](https://www.xda-developers.com/apk-signature-scheme-v3-key-rotation/)，这对开发者来说是个好消息。基本上，开发人员现在可以有多个密钥来编译针对 Android P 的 Android 应用程序。这与只有一个密钥相反，如果应用程序丢失，需要开发人员以不同的包名重新上传到 Play Store。这对于开发者来说比用户更重要，但仍然是一个很好的补充。

### 支持硬件安全模块

这里有一个对开发者和消费者都有利的补充:搭载 Android P 的手机将能够支持 StrongBox Keymaster。这是一个硬件模块，包含自己的 CPU、安全存储、真正的随机数生成器和额外的机制，以防止软件包篡改和未经授权的应用程序侧装。

### 设备保护-唯一序列号

每一部安卓手机都有一个独特的序列号，这个序列号可以在工厂重置后保持不变。这是另一种技术上可以被跟踪的方法。在 Android P 之前，设备上的任何应用程序都可以看到它。Android P 中的应用程序现在需要特殊许可才能看到你设备的序列号。

* * *

## Android P 中面向用户的安全增强

### 传感器使用时的持续通知

并非所有的安全改进都是隐藏的。使用像[麦克风](https://www.xda-developers.com/android-p-audio-recording-limitations-privacy/)或[摄像头](https://www.xda-developers.com/android-p-background-apps-camera/)这样的传感器的应用程序，如果不声明自己是前台服务，将不再能够这样做。他们必须显示一个持久的通知，列出应用程序正在运行和使用某些传感器。目前还不知道这对 Cerberus 这样的应用意味着什么，也有可能不适用于/系统安装的应用。

### 统一指纹认证对话框

应用程序已经可以利用设备上保存的指纹，但在 Android P 中，将有可能使用系统提供的代表应用程序的认证对话框。这意味着用户通过为所有指纹检查创建标准化的外观和感觉来知道指纹检查是合法的。

### 面向用户的过期 API 使用警告

旧的 API 可能相当于安全漏洞。随着 Android 新版本的出现，旧的 API 被弃用，最终将不再起作用。谷歌已经开始警告用户，当他们使用的应用程序有旧版本的 API 时，希望推动开发者使用更新、更安全的 API。今年夏天，新的或更新的应用程序将被要求使用更新的 API 级别，所以开发者最好尽快行动起来。

* * *

## Android P 的其他安全改进

### 一些密码上的变化

其他改进包括系统范围内的密码变化，旨在进一步增强用户隐私和安全。旧标准很好，但这些作为升级，只是为了让您的设备可以处于安全的前沿。

* * *

## Android P:隐私的福音

这些只是冰山一角。许多更复杂的变化也在酝酿中，比如对 SELinux 的改变和对未记录的 API 的限制。虽然后者遭到了厌恶，但谷歌声称“崩溃风险”是他们禁用这些 API 的原因。如果你有兴趣直接从谷歌上了解最新的安全和隐私变化，你可以看看下面的链接。

* * *

[**Android P 应用行为**](https://developer.android.com/preview/features/security-behav.html#p-apps)

[**数据输入隐私**](https://developer.android.com/preview/behavior-changes.html#input-data-privacy)

[**系统安全**](https://developer.android.com/preview/features/security.html)**