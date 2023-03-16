# 戴 OS 手表的脸现在可以使用硬件加速

> 原文：<https://www.xda-developers.com/hardware-acceleration-wear-os-watch-faces/>

# 开发人员现在可以为 Wear OS watch faces 启用硬件加速

Wear OS 最近的一项变化应该会使手表表面运行得更流畅，因为它们可以利用硬件加速。

谷歌的 Wear OS 平台没有得到与智能手机 Android 相同的喜爱，但它仍然得到了 T2 偶尔的更新，增加了新功能。这种缓慢的方式与我们每年看到的少量佩戴 OS [智能手表](https://www.xda-developers.com/ticwatch-c2-plus-1gb-ram-wear-os/)相匹配。内存小于 1GB 的 Wear OS 智能手表往往会在某些领域与 UI 性能斗争，但由于手表表面增加了硬件加速，开发人员应该能够让事情运行得更好一些。

手表面部硬件加速的优势是 GPU 可以以更高的帧速率加速渲染手表面部 UI 和动画/过渡。我注意到，Wear OS watch 的表盘有时会口吃，尤其是在显示器唤醒时。硬件加速有助于让表盘看起来更加光滑。

Wear OS *应用*已经能够利用硬件加速有一段时间了，但它还不能用于观看面部开发者。上个月，谷歌更新了可穿戴支持库(版本 2.7.0)，允许开发者请求硬件加速的画布。除此之外，通过在设置>开发者选项下启用调试 GPU 性能分析，还有更多 UI 性能数据。

这种变化带来了一些问题。首先，谷歌表示“硬件加速会大大降低设备的电池寿命。”如果手表表面有“长时间运行的动画”，情况尤其如此，谷歌建议不要实现这一点。第二个问题是，watch faces 的硬件加速仅适用于 Android 9 Pie 或更高版本的 Wear OS 设备。

像许多功能一样，这取决于开发人员在他们的 Wear OS 手表界面中实现这一点。希望很多人都这样做，我们会看到更平滑的手表表面。这项功能的增加不会是谷歌智能手表操作系统的一个可取之处，但它是朝着正确方向迈出的一小步。

* * *

**来源:[谷歌](https://developer.android.com/training/wearables/watch-faces/hardware-acceleration)| Via:[9 to 5 谷歌](https://9to5google.com/2020/06/21/wear-os-watch-faces/)**