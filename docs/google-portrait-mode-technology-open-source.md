# 谷歌开源了一个工具，用于启用 Pixel 2 的人像模式功能

> 原文：<https://www.xda-developers.com/google-portrait-mode-technology-open-source/>

# 谷歌开源了一个工具，用于启用 Pixel 2 的人像模式功能

谷歌发布了 DeepLab-v3 的源代码，这是一项人工智能技术，可用于在谷歌相机上启用人像模式，允许开发者在自己的应用程序中使用相同的技术用于其他目的。

**更新 05:02PM CST** :谷歌已经澄清肖像模式技术本身没有开源，而是使其成为可能的技术——语义图像分割——现在是开源的。标题已修改，以反映这一更正。

大多数人都认为 Pixel 2 家族拥有目前所有智能手机中最好的相机。相机硬件本身很棒，但大部分的魔力发生在软件方面。例如，HDR+功能使[几乎任何相机在](https://www.xda-developers.com/pixel-2-google-camera-port-essential-phone/)[移植到其他手机](https://www.xda-developers.com/google-camera-mod-exynos-portrait-mode-galaxy-s8-s7-note-8/)时都更好。Pixel 2 的一项新软件功能是“肖像模式”。它能识别你的身份，并模糊背景，创造出一种很酷的效果。

摄像机使用语义图像分割来实现这一点。基本上，它用诸如“人”或“天空”的标签对每个像素进行分类这有助于相机区分前景中的人和背景中的天空。谷歌已经将这项技术开源，这意味着开发者可以在自己的应用中使用相同的技术。肖像模式只是这项技术应用的一个例子。开发者可以做更酷的东西。

> 该版本包括基于强大的卷积神经网络(CNN)主干架构[2，3]构建的 DeepLab-v3+模型，旨在获得最准确的结果，用于服务器端部署。作为此次发布的一部分，我们还分享了我们的 Tensorflow 模型训练和评估代码，以及已经在 Pascal VOC 2012 和 Cityscapes 基准语义分割任务上进行预训练的模型。

* * *

[**来源:谷歌研究**](https://research.googleblog.com/2018/03/semantic-image-segmentation-with.html?utm=1)