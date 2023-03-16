# Android 开发人员的图形设计:创建理想的应用图标

> 原文：<https://www.xda-developers.com/graphic-design-for-android-developers-creating-the-ideal-app-icon/>

无论一个应用是通过什么样的市场或服务发布的，它的图标是潜在用户首先会注意到的。当试图吸引新用户时，第一印象至关重要，这意味着图标是任何应用程序的关键组成部分。此外，不管应用程序的意图是什么，创建一个漂亮的应用程序图标应该是每个应用程序开发阶段的重要组成部分。尽管许多技术应用程序的开发人员将图形留给了专门的设计师，但只要掌握了实验和分析的诀窍，任何人都可以理解设计的基本原理并加以应用。App 图标也不例外！

本指南介绍了如何使用开源软件为一个示例 Android 应用程序创建一个自适应图标。尽管最终结果可能不是您可能需要的格式，但是这里讨论的许多设计技巧将适用于多个平台。

* * *

# 安卓应用图标剖析

 <picture>![Android icon diagram](img/a1a4aa3a9dd3706e1cce11344bdf032d.png)</picture> 

A GIF from Google breaking down an adaptive icon into its constituent parts.

在 Android Oreo 发布“自适应图标”后，一个应用程序图标可以由三个基本层组成:一个**不透明背景层**、**一个带有**透明支持的前景层**和一个定义图标形状的**遮罩**。所有这些层的尺寸都是 108×108 DP，尽管用户只能看到内部的 72×72 DP；另一个区域，被顶部的遮罩切掉，用于 UI 中的特殊效果，使图标看起来动态。对于外行来说， *dp* 或*与显示器无关的像素*代表所有 Android 界面的测量单位，被定义为等于每英寸 160 点显示器上[一个像素的大小。)](https://developer.android.com/training/multiscreen/screendensities)**

来自谷歌的 Nick Butcher 谈到了图标中心的一个 66 dp 的圆圈,没有任何面具可以将其剪掉，称为“安全区”。这是我们图标设计的主要元素，当我们进入实际设计的时候。当图标上有形状遮罩时，超过 33 dp 半径的任何内容可能在图标中不可见。

# 弄脏你的手

由于 UI 缩放，图标最好是矢量图像，我们需要一个矢量图形编辑器来制作图标。Inkscape 是开源的，是更昂贵软件的一个很好的替代品，所以它将是我们在本教程中的选择。我还设计了一个项目文件[，这里有](https://drive.google.com/open?id=1iwKvFKKemGf-xtUj2JP269kTHh-yUcyU)标明了安全区域和谷歌自己的设计关键词，还有一个漂亮的图层蒙版，让我们预览图标的形状。

在 Inkscape 中打开项目文件，并打开**填充和描边** (Shift+Ctrl+F)、**导出 PNG 图像** (Shift+Ctrl+E)和**图层** (Shift+Ctrl+L)面板后，我们就可以开始了。图层面板是项目的核心所在，其中*前景*和*背景*图层用于放置它们的名义组件，而*指引线*和*蒙版*用于切换打开和关闭(通过点击它们旁边的小眼图标)以供参考。

 <picture>![Screenshot of Inkscape window](img/81c5119b9119f7db5d819a0b33d10615.png)</picture> 

Upon loading the file and setting up the panels, Inkscape should look something like this.

图标是一个应用程序身份的表达。因此，它必须结合应用程序的个性和特定平台的设计准则，就像 Android 的[材料设计语言必须提供的](https://material.io/design/iconography/product-icons.html#)。出于演示的目的，让我们假设我们正在开发一个使用物质元素的天气应用程序。我们可以使用经典的太阳和云主题来告知用户该应用程序的目的，并使用阴影和几何图形对这一基本设计进行一点旋转，使其与 Android 环境融为一体。

### 背景

 <picture>![Background layer](img/a5d3cf204b66ad1baed7ecf585309531.png)</picture> 

The background layer of the icon.

让我们从设置背景开始，背景将由蓝色的天空和中间的黄色太阳组成。将*蒙版*变为不可见，我选择*背景层*并使其可见，用**创建矩形和正方形**工具(F4)填充整个画布，并根据[材质调色板](https://material.io/design/color/the-color-system.html#tools-for-picking-colors)设置**填充和描边**中矩形的填充颜色为 64B5F6FF(浅蓝色)。然后，我选择**创建圆、省略号和圆弧** (F5)工具，按住 Shift 和 Ctrl，从关键线的中心到第二大的圆绘制一个圆，并将其颜色设置为 FFEE58FF，这给了我们一个温暖的小太阳。在任何类型的设计中，坚持基本几何学总是好的，尤其是 Android 的设计语言鼓励简单。为了符合材质指南，我也通过**滤镜→阴影和发光→阴影**给太阳一个微妙的阴影。

### 前景

 <picture>![Foreground layer](img/445c20193bdfb17a6cd8c9c1529cdfe1.png)</picture> 

The foreground layer of the icon.

来到*前景，*我通过从其他圆的圆周画圆来画一组围绕太阳的云，并给它们都赋予 EEEEEFF 的填充颜色。然后，我通过右击多个对象并选择**组**来适当地将圆分组，并在我最终获得的两个最终形状上运行阴影生成器。将*指南*变为不可见，并切换*前景*和*背景*或者，可以看到我们天气应用程序图标的组成层。如果应用程序的图标被拖过主屏幕，云会在静止的太阳上层叠！

### 结果

*遮罩*现在可以变得可见，并通过节点 (F2)使用**编辑路径进行调整，以尝试和模拟不同的形状遮罩。此外，这两个图层可以使用**导出 PNG 图像**面板单独导出，以便在 Android Studio 中使用[，也可以一起导出](https://developer.android.com/studio/write/image-asset-studio.html#create-adaptive) [Google Play 图标](https://developer.android.com/google-play/resources/icon-design-specifications/)。**

在创建一个产品图标的时候，尝试理解一个应用程序的目的，提炼出它最抽象的视觉形式，并用简单的几何图形表现出来，这是一个很好的实践。设计中的任何组件越简单，它通常工作得越好，越可靠，在平面设计中也是如此。在大多数情况下，前景中的对象形状和背景中的纯色或图案(反之亦然)就可以了，但就像在我们的示例中一样，如果需要，可以使用另一层对象；过多的堆叠或者使用阴影只会使图标的设计更加复杂。

 <picture>![Icon with adaptive shapes](img/a0a59153c291e64eabadad46089f0b3b.png)</picture> 

Both layers stacked, with the Mask layer being tweaked to preview the adaptive icon

你可以在官方[材料网站](https://material.io/design/iconography/product-icons.html#specs)上阅读更多关于材料界面中的图标设计，并从[同一网站](https://material.io/resources/icons/?style=baseline)上抓取免费系统图标用于图标设计。