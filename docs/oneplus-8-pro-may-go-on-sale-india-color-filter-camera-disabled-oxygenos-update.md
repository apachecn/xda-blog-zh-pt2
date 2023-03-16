# 一加 8 Pro 可能会在印度出售，但其彩色滤光片摄像头已被禁用

> 原文：<https://www.xda-developers.com/oneplus-8-pro-may-go-on-sale-india-color-filter-camera-disabled-oxygenos-update/>

出于一些原因，一加 8 Pro 上的彩色滤光片摄像头一直在新闻中出现。起初，[大多数评论](https://www.xda-developers.com/oneplus-8-pro-review-never-settle-on-hardware/)认为 500 万像素彩色滤光片相机及其存在只是一个噱头，使用案例非常有限，很多用户很快就会忘记。然后，一些用户发现，彩色滤光摄像头实际上可以[透过非常薄的塑料物体](https://www.xda-developers.com/oneplus-8-pro-color-filter-camera-see-through-some-plastic-objects/)和非常薄的衣服。[一加随后在一条微博](https://www.xda-developers.com/oneplus-8-pro-color-filter-x-ray-infrared-see-through-camera-temporarily-disabled-future-update/)中提到，他们将通过软件更新禁用摄像头，随后[澄清说这仅针对中国市场。令人惊讶的是，一家](https://www.xda-developers.com/oneplus-8-pro-color-filter-x-ray-infrared-see-through-camera-temporarily-disabled-future-update/) [OTA 向全球单位](https://www.xda-developers.com/oxygenos-10-5-9-disables-oneplus-8-pro-color-filter-camera-even-global-variant/)发出通知，最终禁用了摄像头，但一加出来澄清这是一次意外的首次亮相，此后不久就恢复了这一更改。

**[一加八大职业 XDA 论坛](https://forum.xda-developers.com/oneplus-8-pro)**

事实证明，在印度购买一加 8 Pro 的客户可能不会看到彩色滤光片相机，至少最初不会。我们有证据表明这种模式也会在印度单位上被禁用。

**[一加 8 Pro XDA 点评——从未看中硬件](https://www.xda-developers.com/oneplus-8-pro-review-never-settle-on-hardware/)**

在一加相机 4.0.267 中，我们发现了一些事情，这可以在为一加 8 Pro 推出的 [OxygenOS 10.5.10 中找到。一，](https://www.xda-developers.com/oneplus-8-8-pro-oxygenos-update-camera-system-network/)[这次更新增加了视频滤镜](https://www.xda-developers.com/oneplus-camera-4-0-267-on-the-oneplus-8-series-adds-video-filters-and-prepares-to-add-a-smart-scene-enhancement-toggle/?utm_content=buffer8cbef&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer)，并准备增加一个“智能场景增强”切换。除此之外，我们还发现了财产"*" InfraredCameraBuilder。ModelsToDisableInfraredCamera*被修改为包含型号名称“*2020*和“*2021*”。2020 年指的是中国的一加 8 Pro，而 2021 年是印度的一加 8 Pro。

我们反编译了应用程序，发现这个相机应用程序更新现在检查系统属性 *ro.product.model* 。如果此属性与 IN2020 或 IN2021 匹配，则滤色片相机和 Photochrom 模式被禁用。

我们没有印度一加 8 专业版来测试这一点。但是，我们可以在一个根一加 8 Pro 全球变型上通过将 *ro.product.model* 的值更改为 IN2021 来复制相同的结果(原始模型名称为 IN2025)。

我们可以确认，启用此属性将在相机应用程序更新中禁用彩色滤光片相机。

### 这对印度的客户意味着什么？

一加 8 Pro 已经在印度推出，但尚未在印度公开销售，因为该公司不得不因为新冠肺炎而处理生产问题。目前还没有宣布该设备的首次销售日期，所以实际上还没有消费者拿到这款设备。

一加很可能会在零售设备中预装这一软件更新，这意味着消费者将无法开箱即用彩色滤光片相机(请注意，其他相机和模式将保持功能)。即使他们没有预载更新，大多数用户也会接受手机上的 OTA 更新，特别是因为[更新确实有其他有意义的补充](https://www.xda-developers.com/oneplus-camera-4-0-267-on-the-oneplus-8-series-adds-video-filters-and-prepares-to-add-a-smart-scene-enhancement-toggle/?utm_content=buffer8cbef&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer)，这意味着该模式将在拆箱后不久通过更新被禁用。

我们的内部消息来源表明，禁用彩色滤光片摄像头是一项临时措施，一加已经在进行更新，将“修复”并重新启用摄像头，预计将于 2020 年 6 月底推出。

我们已经联系了印度一加公司就此事发表评论或声明。当我们收到他们的回复时，我们会更新我们的文章。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*