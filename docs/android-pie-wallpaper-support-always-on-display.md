# Android Pie 源代码确认壁纸支持始终显示

> 原文：<https://www.xda-developers.com/android-pie-wallpaper-support-always-on-display/>

本周早些时候，谷歌[正式为谷歌 Pixel 和谷歌 Pixel 2 推出了](https://www.xda-developers.com/android-pie-google-pixel-google-pixel-2/) Android Pie。最新版本的 Android 为 Android 带来了大量的好东西，如手势导航、改进的材料设计主题、[数字福利](https://www.xda-developers.com/digital-wellbeing-google-pixel-xl-google-pixel-2-xl/)、[切片、应用动作](https://www.xda-developers.com/slices-app-actions-android-p-google-assistant/)等等。我们已经介绍了一些引擎盖下的新功能，如在用户意外退出时将 RAM 密集型游戏保存在内存中的新功能，蓝牙设备卷内存和强制回滚保护。现在，[源代码发布](https://www.xda-developers.com/android-pie-source-code-aosp/)证实了我们之前发现的一个特性:永远显示中的壁纸支持。

我们[在](https://www.xda-developers.com/google-pixel-2-always-on-display-wallpaper-android-p/) [Android P 开发者预览版 1](https://www.xda-developers.com/android-p-developer-preview-1-google-pixel-xl-pixel-2-xl/) 发布的谷歌 Pixel 2 中首次发现了该功能的线索。当时，我们的分析基于不完整的反编译代码，所以我们不确定我们发现的新类和新方法是否真的支持 Always on Display 中的壁纸。但是有了完整的源代码和提交历史，我们现在可以确认这个特性正在开发中。

根据第一次提交，对于要在始终显示中显示的壁纸，它必须在其 android.service.wallpaper 元数据中将“supportsAmbientMode”属性定义为“true”。你可以[在谷歌上传到 AOSP 的动态壁纸应用示例中](https://android.googlesource.com/platform/frameworks/base/+/7517b5dcce8dde3a22177857b8fff6439fd98d82/tests/Internal/res/xml/livewallpaper.xml#20)查看如何做到这一点的例子。第二次提交声明，默认情况下，总是显示的壁纸将在 1 分钟后隐藏。系统从壁纸背景过渡到黑色背景，带有持续 400 毫秒的[交叉淡入淡出动画。因此，谷歌对这一功能的采用看起来不会像三星那样强大，三星不仅支持静态壁纸已经有一段时间了，而且](https://android.googlesource.com/platform/frameworks/base/+/82aa1630962e712878301aa46333f1510dbe46a5/packages/SystemUI/src/com/android/systemui/doze/AlwaysOnDisplayPolicy.java#44)[甚至最近才开始支持几秒钟长的动画 gif](https://www.xda-developers.com/samsung-galaxy-s8-galaxy-note-8-always-on-display-gif/)。

我们不确定该功能是否会在现有的谷歌 Pixel 和谷歌 Pixel 2 XL 上可用，但我们希望开发者能够找到如何让他们在 Pixel 2 上工作的动态壁纸始终显示出来。有了[几个隐藏的 ADB 命令](https://www.xda-developers.com/customize-google-pixel-2-always-on-display-brightness/)，如果我们看到兼容的实时壁纸开始出现，也可以调整该功能的可见性和淡出超时。如果 Pixel 2 不支持该功能，那么谷歌计划何时推出它？

## 谷歌 Pixel 3 的壁纸支持一直显示？

以下所有内容纯属猜测，没有任何直接证据支持，所以不要全信。鉴于谷歌在谷歌 Pixel 设备上使用有机发光二极管面板的历史以及当前的行业报告，谷歌 Pixel 3 和谷歌 Pixel 3 XL 很有可能会采用有机发光二极管显示屏。我们还知道谷歌 Pixel 3 很有可能支持无线充电，因为过去两个月的多张真实照片都指向玻璃背面。六月份[的黑色](https://www.xda-developers.com/google-pixel-3-xl-prototype-display-notch/)[Pixel 3xl 在我们的论坛上泄露](https://www.xda-developers.com/google-pixel-3-xl-glass-back-display-notch/)，随后[的白色谷歌 Pixel 3 XL](https://www.xda-developers.com/google-pixel-3-xl-clearly-white-leak/) 也在 XDA 论坛上泄露。今天早些时候[另一组图片，甚至是一个 Pixel 3 XL 的拆箱视频](https://www.xda-developers.com/google-pixel-3-xl-unboxing-leak/)在网上泄露。三位泄密者都独立声明 Pixel 3 XL 有玻璃背面，尽管没有人能直接证实无线充电支持。

但玻璃背面并不是 Pixel 3 支持无线充电的唯一证据。我们首先报道了一组代号为“梦想飞机”的无线充电坞的存在，这可能正在进行中。随后在一次谷歌应用拆卸中出现了一个神秘的“[Pixel Stand](https://www.xda-developers.com/google-pixel-3-pixel-stand-wireless-charging-dock/)dock，我们认为这很可能是谷歌品牌的谷歌 Pixel 3 无线充电基座的名称。虽然我们还没有激活它，但我们相信一旦 Pixel 3 停靠在 Pixel 支架上，它将会有一个特殊的助手支持的用户界面。

那么壁纸在“永远展示”中支持什么呢？有可能只有当你将手机停靠在 Pixel 支架上时，才会显示壁纸。1 分钟后，壁纸逐渐消失，显示一个特殊的用户界面，可以“在手机锁定和 Pixel 支架上使用你的个人信息为你提出建议、回答问题和采取行动。”它可能不会以这种方式结束，但这就是我希望看到它工作的方式！