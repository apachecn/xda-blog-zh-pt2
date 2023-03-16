# 一加 8 专业版解锁工具现已推出

> 原文：<https://www.xda-developers.com/oneplus-8-pro-unbrick-tool-now-available/>

# 一加 8 专业版解锁工具现已推出

如果你已经成功地把你闪亮的新一加 8 Pro 砌好了，有一个简单的方法可以用这个简单的工具把它拆开。请继续阅读，了解如何操作！

采用高通骁龙芯片组的设备具有一种称为**E**emergency**D**own**l**oad Mode(EDL)的替代引导模式，该模式严格用于 OEM 服务。通过特定型号的软件二进制文件(通常称为程序员)和 EDL 闪存工具的正确组合，有可能恢复失去快速启动访问的硬砖设备。例如，一加将他们的 EDL 闪存标签为“MsmDownloadTool”，客户支持代表使用它在您的设备上执行低级闪存以恢复出厂固件。该公司显然已经升级了他们的存储库，以支持新发布的[一加 8 系列](https://www.xda-developers.com/oneplus-8-pro-specifications-features-pricing-availability/)，因为用于[一加 8 Pro](https://www.xda-developers.com/oneplus-8-pro-review-never-settle-on-hardware/) 的 MsmDownloadTool 现在可供争夺。

**[一加 8 临 XDA 论坛](https://forum.xda-developers.com/oneplus-8-pro) || [一加 8 临 XDA 评论](https://www.xda-developers.com/oneplus-8-pro-review-never-settle-on-hardware/)**

除了取消绑定，EDL 软件包对于执行降级特别有用，因为 OxygenOS 的库存恢复和本地更新选项都不允许最终用户这样做。触发 EDL 启动模式非常简单——你需要做的就是关闭你的一加 8 Pro，然后按住音量增大和音量减小按钮，并将手机插入你的 PC。闪光器应该自动检测电话，否则，你需要安装正确的驱动程序链接在下面的线程。请记住，闪存工具将清除您的手机，并重新锁定引导加载程序。

**[MsmDownloadTool for the global and Indian 一加 8 Pro — XDA 线程](https://forum.xda-developers.com/oneplus-8-pro/how-to/op8pro-unbrick-tool-to-restore-device-t4084953/)**

由于设备存储的访问范围，EDL 模式经常被安全研究人员和修改社区利用。作为预防措施，像诺基亚和小米这样的公司已经对闪存程序实施了[服务器端锁定](https://www.xda-developers.com/xiaomi-edl-unbrick-authorized-mi-accounts/)。幸运的是，一加 8 的所有者不需要经历所有这些麻烦，MsmDownloadTool(基于 [OxygenOS 10.5.4](https://www.xda-developers.com/oneplus-8-series-update-adds-live-caption-bullets-wireless-z-integration-dolby-atmos/) )甚至允许在全局单元上交叉刷新印度固件(反之亦然)。仍然建议在交叉刷新之前备份“持久”分区，因为指纹扫描仪可能会在之后给出与某些注册问题相关的错误。