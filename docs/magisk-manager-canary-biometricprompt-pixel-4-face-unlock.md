# Magisk Manager Canary 为 Pixel 4 面部解锁添加了生物计量提示

> 原文：<https://www.xda-developers.com/magisk-manager-canary-biometricprompt-pixel-4-face-unlock/>

Magisk 基本上已经成为 Android 上 root 访问的代名词，这是因为它是最简单的获得 root 权限的方法，而无需直接修改系统分区。Magisk 的部分吸引力在于它的配套应用程序 Magisk Manager，它使管理超级用户访问和安装模块——打包了应用程序、脚本和其他文件的档案，可以系统地修改您的设备——变得超级简单。XDA 认可的开发者 topjohnwu，Magisk 的创造者，为他的超级用户工具和配套应用程序维护稳定、测试和金丝雀通道，他宣布了管理器应用程序的新功能:生物认证，特别是针对超级用户请求的面部解锁。

目前，当超级用户请求的“自动响应”设置为“提示”并且在“设置”中启用了“启用指纹验证”时，Magisk Manager 支持在指纹验证后锁定超级用户请求。每当应用程序请求超级用户访问时，该应用程序使用 FingerprintManager API 来显示自定义指纹验证对话框。这个 API 在 Android 9 Pie 中被弃用，取而代之的是 BiometricPrompt，这是一个更通用的 API，它提供了一个系统对话框，可以与任何已识别的安全生物认证硬件一起工作。

在 Android 10 中，安全面部识别硬件现在被认为是 BiometricPrompt 中的有效认证方法，因此使用该 API 的应用程序可以呈现面部认证对话框。由于新的 Pixel 4 没有指纹扫描仪，topjohnwu [需要更新管理器应用程序](https://www.xda-developers.com/google-pixel-4-users-wait-developers-add-face-unlock-support/)，以便[根 Pixel 4 设备](https://www.xda-developers.com/google-pixel-4-root-magisk/)可以对超级用户请求使用面部认证。如果你有 Pixel 4 并下载了最新的 Magisk Manager Canary 版本，你会注意到“启用指纹认证”已被“启用生物认证”设置所取代。打开这个，你就可以用你的脸来验证超级用户的请求。

如果你最喜欢的应用程序还没有更新到使用 BiometricPrompt，你可以使用 [Fingerface Xposed 模块](https://www.xda-developers.com/use-google-pixel-4-face-unlock-any-app/)在所有应用程序中强制支持面部解锁，作为权宜之计。

**[Magisk 经理金丝雀论坛线程](https://forum.xda-developers.com/apps/magisk/dev-magisk-canary-channel-bleeding-edge-t3839337/)**