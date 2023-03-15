# Chrome OS 85 极大地改善了一些 Chromebooks 的手写识别

> 原文：<https://www.xda-developers.com/chrome-os-85-vastly-improves-handwriting-recognition-for-some-chromebooks/>

# Chrome OS 85 极大地改善了一些 Chromebooks 的手写识别

Chrome OS 在其最新更新中获得了一个增强的人工智能手写识别模块，可以在本地工作。继续阅读，了解更多信息！

本月初，谷歌[开始通过稳定的渠道向兼容设备推出 Chrome OS 85](https://www.xda-developers.com/google-chrome-os-85-rolls-out-wi-fi-sync-simpler-settings-mic-slider-more/) 。此次更新带来了方便的 Wi-Fi 同步选项，相机应用程序中的视频录制暂停/恢复支持，以及许多其他改进。然而，事实证明，山景城巨人在这次更新中在一些 Chromebooks 上安装了一个增强的离线手写识别模块，尽管官方 changelog 中根本没有提到该功能。

据 [*安卓警察*](https://www.androidpolice.com/2020/09/11/chrome-os-85-significantly-improves-the-handwriting-keyboard-for-some-chromebooks/) 报道，新的人工智能手写识别组件完全离线工作。与之前基于云的机制不同，该模块的新版本利用了设备上的机器学习，精确度更高。手写图形数据被本地处理以编译一个相当精确的识别模型，该模型能够随着时间的推移而自我修正。

在引擎盖下，有一个名为[**libhandingbwriting . so**](https://source.chromium.org/chromiumos/chromiumos/codesearch/+/master:src/platform2/ml/handwriting.cc;bpv=1;l=21)的新库，负责管理 Chrome OS 中改版的手写识别系统的整个离线机器学习方面。只有在编译 Chrome OS 时在默认 makefile 中设置了`ondevice_handwriting`属性，才能加载该库。截至目前，谷歌正在分阶段推出，只有少数设备最初在其各自的 Chrome OS 85 版本中包含该属性。该功能可能严重依赖于处理器的神经处理能力，这就是为什么该公司试图限制选择 Chromebooks 的可能性。

以下是运行 Chrome OS 的设备列表，这些设备目前支持基于人工智能的本地离线手写识别:

*   《夏娃》:谷歌 Pixelbook
*   “sarien”:戴尔 Latitude 5300 二合一设备，Latitude 5400
*   “soraka”:惠普 Chromebook x2
*   “章鱼”:华硕、宏碁、惠普、联想、三星双子湖 Chromebooks 几款
*   「娜美」:宏碁 Chromebook 13 / Spin 13，戴尔 Inspiron 14 二合一型号 7486，联想 Chromebook C340-15，联想 Yoga Chromebook C630，
*   【rammus】:华硕 Chromebook Flip C434，华硕 Chromebook C425，华硕 Chromebook Flip C433TA
*   “鹦鹉螺”:三星 Chromebook Plus (V2)，三星 Chromebook Plus LTE
*   【孵化】:华硕 Chromebook Flip C436FA，宏碁 Chromebook 712，联想 IdeaPad Flex 5i，三星 Galaxy Chromebook
*   《夜曲》:[谷歌像素写字板](https://www.xda-developers.com/google-pixel-slate-detachable-chrome-os-tablet/)