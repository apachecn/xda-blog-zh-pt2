# 如何在运行 Android 10 的索尼 Xperia 手机上启用隐藏像素主题

> 原文：<https://www.xda-developers.com/how-to-enable-hidden-pixel-themes-on-sony-xperia-phones-running-android-10/>

Pixel Themes 应用程序可以让你自定义图标形状、字体、强调颜色等。在运行 Android 10 的谷歌 Pixel 手机上。在谷歌推出第二个 Android Q 测试版后不久，我们[发现了](https://www.xda-developers.com/android-q-pixel-themes-google-pixel/)这款应用的存在，并设法在公开亮相前一个月左右获得了[其功能的早期预览](https://www.xda-developers.com/google-pixel-themes-customize-android-10/)。顾名思义，该应用程序不是为非像素设备设计的，但它切换的底层覆盖仍然可以在其他设备上找到。虽然运行 Android 10 的索尼 Xperia 手机上既没有成熟的 Pixel Themes 应用程序，也没有 [AOSP ThemePicker](https://android.googlesource.com/platform/packages/apps/ThemePicker/) ，但该公司留下了许多图标形状和强调颜色覆盖，可以通过`cmd overlay` shell 命令激活。

在摆弄他的全新索尼 Xperia 1 II T1 时，XDA 认出了开发者 T2 尼亚伯克 79 T3 T4 发现了 T5 这些覆盖层的存在。鉴于谷歌在索尼的覆盖管理器服务(OMS)之上设计了基于覆盖的主题化机制，Xperia 手机的 Android 10 固件中包含这些包并不令人惊讶。然而，没有面向用户的应用程序来控制这些覆盖，所以用户必须通过 ADB shell 手动切换它们。例如，您可以使用以下命令轻松更改强调颜色:

```
 cmd overlay enable com.android.theme.color.<COLOR_NAME> 
```

其中颜色名称可以是“紫色”、“黑色”、“肉桂色”、“绿色”、“海洋”、“兰花”或“空间”。

这里有三个基本的命令，你应该在玩叠加之前知道。将索尼 Xperia 智能手机连接到启用 USB 调试的 PC/Mac 后，您可以使用 Android Debug Bridge (ADB)输入它们。

最重要的是，这个技巧应该也适用于旧的 Xperia 设备，前提是它们收到了索尼官方的 Android 10 更新。这意味着, [Xperia 1/5](https://www.xda-developers.com/sony-xperia-1-xperia-5-receive-official-android-10-update/) 、 [Xperia XZ2/XZ3](https://www.xda-developers.com/sony-xperia-xz3-xz2-xz2-compact-xz2-premium-receive-official-android-10-update/) 和 [Xperia 10/10 Plus](https://www.xda-developers.com/sony-xperia-10-plus-official-android-10-update/) 的用户也可以在他们的手机上执行相同的命令行主题化魔法。