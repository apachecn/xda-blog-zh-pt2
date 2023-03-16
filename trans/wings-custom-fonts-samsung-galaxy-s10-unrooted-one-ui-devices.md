# Wings 允许您在三星 Galaxy S10 和其他非 root One UI 设备上设置自定义字体

> 原文：<https://www.xda-developers.com/wings-custom-fonts-samsung-galaxy-s10-unrooted-one-ui-devices/>

随着 Galaxy S8 和 Galaxy Note 8 等三星旗舰产品系列设备的统一用户界面的发布，[三星悄悄地通过 Substratum 和 Swift Installer](https://www.xda-developers.com/one-ui-blocks-substratum-swift-installer-samsung-galaxy-s8-galaxy-note-8/) 禁用了叠加功能。这一变化继续影响到[的其他设备](https://www.xda-developers.com/samsung-galaxy-s10-custom-overlay-themes-swift-installer-substratum/)，这些设备正在接收基于 Android Pie 更新的单一用户界面，或者像 Galaxy S10 一样推出单一用户界面。在 Android Pie 中，安装覆盖层的能力[被限制在平台签名的系统应用上，这意味着你需要 root 才能安装它们。](https://www.xda-developers.com/rootless-custom-themes-android-p/)

但是，对于某些情况，可用的解决方法有限。例如， [Wings Samsung Fonts](https://forum.xda-developers.com/galaxy-s8+/themes/fonts-wings-samsung-fonts-1200-root-t3710688) 发布了其流行的字体改变应用程序的新更新，现在允许用户甚至在非 root One UI 设备上设置不同的字体。[正如向 *PiunikaWeb*](https://piunikaweb.com/2019/04/11/exclusive-samsung-galaxy-s10-custom-font-support-arrives-via-wings-font-installer/) 解释的那样，该项目的首席开发人员提到，启用自定义字体支持的技巧是在主题商店开放时通过 ADB 安装一个主题。这种变通方法也可以扩展到其他主题，但是在这方面有一些限制。

*诀窍是在主题商店开放的同时，由 adb 安装主题。没有更多的。但是错误很容易犯。所以我写了一个脚本来自动执行这些命令，以便有一个用户友好的安装方法。我们注意到，一旦成功安装，更新主题的工作很好，所以改变它不需要电脑。*

唯一的缺点是对注入主题的 10 分钟试用。但由于字体缓存在三星手机上，所以不需要一直使用主题，只在选择/更改字体时使用。所以我们还没考虑过什么试炼。目前的流程根本不需要其他东西，我们只使用 ADB。如果我们想要某种试用版破解程序，那么我们必须使用 ELM 许可证密钥。对我来说，这是一个低优先级，没有人每天都改变字体，所以没有必要让主题一直处于活动状态。

他们最新 3.1 版 RC1 更新的变更日志如下:

*   增加了对馅饼的无根支持！(OneUI)
    *   基于三星主题商店
    *   一键式 Windows Installer 应用
*   创建自定义字体包！
    *   导入多个。ttf 文件
    *   从 Wings 中选择字体
    *   直接用翅膀打开字体
*   新的闪屏和简介幻灯片
*   夜间模式同步(Pie)
*   恢复扫描(针对定制软件包)
*   错误修复:稳定版本

更新似乎还没有在[官方 XDA 线程](https://forum.xda-developers.com/galaxy-s8+/themes/fonts-wings-samsung-fonts-1200-root-t3710688/)中上线，据 *PiunikaWeb* 称，这是因为开发者希望进行另一轮测试。最新的 RC apk 可以在团队的 Telegram 组中获得，并由源网站镜像，因此您可以从那里下载。我们建议等待一段时间，让团队在线程上正式宣布，以防他们在发布之前遇到任何其他奇怪的事情。

[**翅膀三星字体- XDA 线程**](https://forum.xda-developers.com/galaxy-s8+/themes/fonts-wings-samsung-fonts-1200-root-t3710688/) [**故事 Via: Piunikaweb**](https://piunikaweb.com/2019/04/11/exclusive-samsung-galaxy-s10-custom-font-support-arrives-via-wings-font-installer/)