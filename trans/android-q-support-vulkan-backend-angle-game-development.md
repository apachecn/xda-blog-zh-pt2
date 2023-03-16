# Android Q 将支持角度的 Vulkan-backend，使 2D 游戏开发更容易

> 原文：<https://www.xda-developers.com/android-q-support-vulkan-backend-angle-game-development/>

在 Google I/O 2016 上，Android 牛轧糖[宣布支持 Android。提醒您一下，这个 API 可以帮助开发人员获得对底层硬件的更多控制。这种访问有助于他们更好地利用各自单元的处理和图形能力，并优化游戏以尽可能流畅地运行。毫不奇怪，正确的内存分配和线程管理对于任何类型的高能耗任务都很重要，比如运行游戏。这就是 Xbox One 和 PlayStation 4 等流行游戏机长期以来所做的事情——让开发者对设备内部的硬件进行低级别的控制。](https://www.xda-developers.com/google-io-2016-roundup-part-1-google-assistant-google-home-allo-duo-android-n/)

同样有趣的是，Vulkan 是一个跨平台的开放标准，面向跨平台的图形应用。今年早些时候，[我们发现了一条线索【Android Q 可能会通过 Vulkan API 渲染用户界面元素。这将是进一步提高系统流畅度的一个步骤。现在，我们收到信息，Android Q 肯定会支持角度，使 2D 游戏开发更容易。](https://www.xda-developers.com/google-android-q-vulkan-graphics-render-ui/)

## 什么是角度？

角度是一个缩写，它代表“几乎原生图形层引擎。”WebGL 的兴起使得支持渲染器的标准化解决方案成为必要。很长一段时间以来，OpenGL 驱动程序在 Windows 平台上一直不太稳定。因此，ANGLE 将 OpenGL 代码转换为 Direct3D，这是一种 Windows 原生支持的 API，将一切提升到了一个全新的水平。ANGLE 的主要目标是通过将 WebGL 和 OpenGL ES 内容转换为平台上可用的硬件支持的 API，使 OpenGL 可移植并可供所有人访问。使用相同的原理，ANGLE 将把 OpenGL 代码翻译成 Android 上的 Vulkan 代码，因为前者是操作系统上官方支持的硬件 API。你可能每天都在使用 ANGLE，却从未意识到这一点。谷歌 Chrome 和 Mozilla Firefox 的桌面网络浏览器内置了 ANGLE。它用于在 Windows 上的这些浏览器中呈现任何图形内容。

## OpenGL ES vs 火山

Khronos 小组正在努力使 ANGLE 成为 Vulkan 上 OpenGL 的主要渲染器。你们中的许多人可能看不到为了 Vulkan 而放弃 OpenGL 的必要性，但是肯定有改进的空间。在这一点上，OpenGL API 被认为是一种过时的技术。它最初发布于 1992 年，也就是 26 年前。26 年对你们中的一些人来说可能不算什么，但对于技术发展来说，这是一个天文数字。2016 年，全球引入 Vulkan——下一级图形 API。但是，更新并不意味着更好，对不对？我来解释一下为什么 Vulkan 比 OpenGL/OpenGL ES 好很多。

如果你曾经和 OpenGL ES 打过交道，你就会知道它是*巨大的*。这个 API 有超过 300 个扩展，一点也不容易使用。Vulkan 将一切都提升到了一个全新的水平，提供了一个更小的 API 和图形的直接控制。也更容易实现。虽然 Vulkan 在比 OpenGL ES 更低的层次上工作，但这意味着更大的控制能力。有了 Vulkan，线程和内存管理完全交给了游戏开发者，所以你可以充分利用资源。此外，Vulkan 的移动和桌面版本之间的差异非常小，因此移植游戏更加容易。简而言之，Vulkan 是一个底层驱动程序，可以让您释放特定设备上显卡的全部潜力。

## 为什么是角度？

ANGLE 的第一个优势是它是一个开放的标准平台。有很多方法可以为这个项目做贡献。你可以在你的设备上测试驱动程序，报告错误，修复错误，帮助开发者提出解决方案，发送建议，为开发捐赠一些钱，等等。所有这些都将加快发展速度。与 OpenGL ES 相比，下一个大优势是可移植性和跨平台支持。ANGLE 的特性使得平台和游戏开发者的工作更加容易。维护和实现 ANGLE 比早期的实现要容易得多。OpenGL 是如此的支离破碎，以至于追踪 bug 并在不同的设备上修复它们对开发者来说是一件痛苦的事情。将所有需要的驱动程序集中到 ANGLE 中意味着开发人员将更容易实现它们。ANGLE 开发者 Jamie Madill 向我们证实，在 Android 平台上，ANGLE 将通过谷歌 Play 商店接收定期更新。通过内置的第一方市场更新驱动程序是一个好主意，因为用户不必在每次驱动程序更新时更新整个系统。此外，开发人员不需要每次 ANGLE 改变一些东西时都修补代码。这里有一个关于 ANGLE 如何让 Android 游戏开发受益的视频。

正如你所看到的，ANGLE 在过时的 OpenGL ES 上有许多改进。Android Q 的第一个开发者预览版并没有走那么远，所以我们可以拭目以待 ANGLE 在实践中的效果。根据[这个提交](https://chromium-review.googlesource.com/c/angle/angle/+/1330315)，用户将能够从开发者选项角度强制所有应用程序工作。对渲染器的支持是[已经将](https://android-review.googlesource.com/q/branch:pie-angle-preview-dev+status:merged)合并到 Android Pie 分支中，供 OEM 厂商测试。你可以从网站和下面的 GitHub 库跟踪 ANGLE 的发展。

*感谢 XDA 资深会员 [XxPixX](https://forum.xda-developers.com/member.php?u=5015998) 的提示！*

[**角度网站**](https://opensource.google.com/projects/angle) [**GitHub 知识库**](https://github.com/google/angle)