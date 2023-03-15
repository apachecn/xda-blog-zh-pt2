# 见见底层，主题化的未来将接管图层

> 原文：<https://www.xda-developers.com/layers-manager-is-being-deprecated-in-favor-of-substratum/>

Layers 已经看到[逐渐上升到 power](http://www.xda-developers.com/android-m-dev-preview-adds-functional-rro-framework/) ，成为 CyanogenMod 主题引擎的一个可行且有力的替代品。Layers 建立在索尼开发的 [RRO 框架之上，因为它允许更复杂的资源切换，并且比 RRO 最初做的更多元素主题化的可能性。](http://developer.sonymobile.com/2014/04/22/sony-contributes-runtime-resource-overlay-framework-to-android-code-example/)

为了进一步发展 RRO，索尼开发了 OMS(代表覆盖管理器服务)。顾名思义，OMS 是一个管理覆盖的客户端，允许提供商动态控制优先级和启用/禁用覆盖。这导致了一些与层的冲突，因为传统上这些功能是在主题的控制之下。

为了解决 OMS 提出的问题，并进一步增强层的功能，层管理器背后的开发人员合作创建了 Substratum，这是一个具有 OMS 功能的客户端。[用](https://plus.google.com/+SykoPompos/posts/YcmPDJESshB)[Syko pomps](https://plus.google.com/118195502410326243266)的的话说，蛋鸡养殖户背后的 dev:

> 随着底层的引入，覆盖图被下载、编译、签名和安装，就像第三方应用程序被安装到数据/应用程序一样。安装完成后，它们会创建一个 idmap 文件来创建链接，如果启用，它会告诉系统刷新其资源并加载新的资源。一个通知将通知用户一个新的主题可以被使用，并且这个包已经被安装(“Beltz 已经被安装”)

Substratum 试图将层功能与 CM 主题引擎的一些最佳部分合并，其中包括一个完整的设备上编译系统。叠加将不再相互重叠，以主题化单个元素。取而代之的是，这些元素将被一起注入以创建一个单独的覆盖层。设备上编译还使主题设计者能够保持向后兼容性(因为基础 API 设置为 API 版本 23)，并允许为 Marshmallow 制作的主题继续适用于 Android N。此外，您可以在移动中创建主题，在更改之间不需要重新启动，甚至可以在主题编译时使用其他应用程序。

此外，底层也将有利于设计者和使用者。当主题过时时，它会警告用户(例如，为旧的底层构建而构建)，如果他们真的想继续，只要他们认识到可能出现的不稳定问题，仍然会让他们继续。这也将鼓励 ROM 开发者提供新的底层版本，但是如果不是这样的话，仍然会给用户更多的权力。一个配置系统也正在开发中，它理论上可以让你保存整个设置并快速改变它们，使预设自动化在未来成为可能。

据报道，底层主题将更类似于为 CM 主题引擎构建的主题，这将减轻设计师在两个系统上共存的痛苦。对于主题设计者来说，一些更好的消息是，反盗版功能可以在 Substratum 中实现，这将使在一个设备上创建的覆盖图很难在另一个设备上重复使用，如果检测到这种情况，将会删除覆盖图。

* * *

到目前为止，层管理器运行良好，但很快就会被弃用，取而代之的是底层和设备上编译系统作为积极开发的重点。Substratum 虽然不支持预先制作的覆盖图，但开发者保证，对于主题设计者来说，转换成在设备上编译的主题是非常容易的，因为只需要一个明显的调整。

前往 [Google+公告帖子](https://plus.google.com/+SykoPompos/posts/YcmPDJESshB)了解更多关于底层的信息。