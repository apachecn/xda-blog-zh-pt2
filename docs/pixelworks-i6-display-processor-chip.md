# Pixelworks 宣布 i6 芯片具有基于人工智能的视觉增强功能

> 原文：<https://www.xda-developers.com/pixelworks-i6-display-processor-chip/>

Pixelworks 是一家总部位于加州的公司，专门开发视频处理技术。在移动行业，Pixelworks 最著名的是其显示处理芯片和基于软件的图像质量增强产品，这些产品已用于 TCL、一加、OPPO、黑鲨、HMD Global、华硕和中兴的智能手机。今天，该公司发布了新的 i6 显示处理器，这是一种使用人工智能来提高移动设备图像质量的新芯片。

Pixelworks 开发并授权了两种视觉增强技术:其基于软件的“Pixelworks Pro 软件”及其显示处理芯片。显示芯片过去以“Iris”品牌上市。例如，[一加 8 Pro](https://www.xda-developers.com/oneplus-8-pro-specifications-features-pricing-availability/#gallery-5:~:text=Display,-OnePlus%E2%80%99) 和 [OPPO Find X2 Pro](https://www.xda-developers.com/oppo-find-x2-pro-pixelworks-iris-5-display-chip-goodix-new-voice-audio-technology/) 都采用了 Pixelworks 的 [Iris 5 芯片](https://www.xda-developers.com/pixelworks-iris-5-visual-processor-android-display-experience-oppo-find-x2/)。然而，根据 Pixelworks 的新产品组合，这个“Iris”品牌现在被取消了。相反，Pixelworks 的芯片将在新的“I”和“X”系列之间拆分。曾经被称为“Iris 5”的产品今后将被称为 X5，而 Iris 3 将被重命名为 i3。Pixelworks 表示,“X”系列针对高端智能手机，如[一加 8 Pro](https://forum.xda-developers.com/oneplus-8-pro) 和 [OPPO Find X2 Pro](https://forum.xda-developers.com/find-x2-pro) ，是目前他们唯一支持运动估计/运动补偿(MEMC)的芯片。另一方面,“I”系列芯片是为中低端和中高端手机设计的，不支持 MEMC。这些显示处理芯片可以与任何应用处理器(AP)配对，因为数据是通过 [MIPI](https://www.mipi.org/) 在芯片之间进行通信的。

另一方面，Pixelworks Pro 软件是基于软件的，因此完全在应用处理器(AP)上运行。这意味着 Pixelworks Pro 软件不能像专用的“I”或“X”显示处理器那样做，但它(很可能)会降低设备制造商的实施成本，并节省一点内部空间。例如，[新华硕 ZenFone 7 系列](https://www.xda-developers.com/asus-zenfone-7-pro-specs-features-pricing-availability/)采用 Pixelworks Pro 软件进行 DC 调光和 SDR 到 HDR 的上映射，而[一加 8 Pro](https://forum.xda-developers.com/oneplus-8-pro) 结合了 X5 芯片和 Pixelworks Pro 软件的全部功能，包括 MEMC、真实肤色、亮度平滑、色调自适应显示等。当设备以这种方式同时采用显示处理器和 Pro 软件解决方案时，Pixelworks 会添加一个“Pro”标志。例如，“X5 Pro”标志意味着设备同时使用 X5 显示处理器和 Pixelworks Pro 软件。同样，当一台设备使用新的 i6 芯片和 Pro 软件时，该设备据说会采用 Pixelworks 的“i6 Pro”解决方案。

那么 i6 芯片有什么新的地方呢？它到底提供了什么样的“人工智能显示处理”功能？

## Pixelworks i6 和 i6 Pro

新的 i6 显示处理芯片具有图像质量引擎模块和模糊逻辑推理模块，后者首次出现在 Pixelworks 显示处理器中。模糊逻辑推理引擎用于支持人工智能显示处理(自适应优化视觉质量)、始终开启的 HDR(人工智能辅助的实时 SDR 到 HDR 向上映射)、画质引擎(用于人工智能辅助的局部对比度和清晰度增强)、自动自适应显示(用于人工智能辅助的 6 模式自动亮度和色调)、肤色准确性(动态检测和保护肤色)和暗噪声抑制(动态降低低光视频和照片中的视觉背景噪声)。新芯片比其前身 Pixelworks i3 功耗低 40%。

我们要求该公司澄清在生产过程中哪些类型的数据通知了这些人工智能算法，以及采用了哪些人工智能技术。我们特别好奇，想了解更多关于人工智能辅助场景适应功能的信息，据说这是内容感知的。内容感知是基于图像统计还是实际场景？例如，如果有日落，向上映射是否会影响图像的颜色统计(黄色/橙色占优势)，或者更复杂的内容(日落)？

企业营销副总裁 Peter Carson 和产品与战略高级总监 Vikas Dhurka 告诉我们:

> #### "...由于新的 Pixelworks i6 系列处理器主要针对中高端手机，AI PQ[图片质量]引擎旨在平衡性能提升、能效和个性化，并利用专有的轻量级推理模块来增强我们的模糊逻辑 IP，并执行以下操作:
> 
> 1.  #### 从外部和内部来源获取输入，如环境亮度和色温、显示器类型、用户偏好、正在播放的内容等。
>     
>     
> 2.  #### 遵循基于 Pixelworks 知识库的视觉推理规则，该知识库利用了 20 多年的经验，包括最近来自好莱坞与我们的 TrueCut 平台密切合作的专业调色师和创意人员的意见。
>     
>     
> 3.  #### 动态调整显示管道，在各种内容和环境照明条件下，为移动设备创造卓越的视觉体验。
>     
>     
> 
> #### 上面提到的知识库(#2)会随着我们从 OEM 和好莱坞的内容专业人员那里学习和收集用户偏好信息而不断更新。值得注意的是，Pixelworks i6 处理器中 PQ 模块的架构已经升级为 2 层流水线，当应用于图像或视频的不同属性时，可以更好地控制处理。虽然这种 2 层能力不是特定于人工智能的，但我们的人工智能引擎允许 2 层管道比传统的 PQ 处理得到更充分的利用。
> 
> #### 例如，对于 i6 处理器，显示日落的决定不仅仅基于显示器上黄色/橙色阴影的准确性，而是基于考虑基于人工智能的场景检测/图像构成、显示器类型、环境亮度/色温等因素，使用户能够准确看到日落的决定。"

随着智能手机行业的竞争持续升温，越来越多的设备制造商转向 Pixelworks 等第三方供应商，以实现产品的差异化。i6 芯片提供的显示功能可以作为未来智能手机的一个卖点，尽管设备制造商通常不会提到这些功能背后的实际公司。

Pixelworks 表示，其新的 i6 芯片目前正在向客户提供样片，预计最早将于 2020 年第四季度在商业设备中推出。