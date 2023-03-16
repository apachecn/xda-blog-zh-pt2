# APKTool 2.4 现在可用于解码 Android 应用程序

> 原文：<https://www.xda-developers.com/apktool-2-4-release/>

# APKTool 2.4 现在可用于解码 Android 应用程序

APKTool 是反编译 Android APKs 最流行的逆向工程工具。该工具已经到了 2.4 版本，有许多错误修复和变化。

APKTool 是开发者 [ibotpeaches](https://forum.xda-developers.com/member.php?u=3924617) 提供的一个非常有用的逆向工程工具。它可以用来将大多数 Android 应用程序解码为 smali，然后可以转换为 Java 以便于分析。这是大多数想要修改应用程序或揭开秘密的独立开发者的首选工具。我们经常在[分析应用](https://xda-developers.com/tag/apk-teardown)的新功能时使用它。

该工具背后的开发者最近宣布了对[2.4 版](https://forum.xda-developers.com/showthread.php?p=79028225#post79028225)的更新，带来了许多错误修复和变化。其中一个修复解决了 PlatformBuildValue 被设置为意外值的问题，这对于许多试图重新编译应用程序的开发人员来说是一个巨大的痛苦。

**apk tool 2.4 版本变更日志**

*   将 baksmali/smali 更新至 v2.2.6
*   修复了非空 ids.xml 文件的新限制问题。(感谢 gino247)
*   修复了 PlatformBuildVersion 属性更改为意外值的问题。(感谢 gino247)
*   通过发布 4.10.2 版本，修正了 v5 升级的问题
*   通过新的参数- -nc | - no-crunch 增加了 no-crunch 支持。(感谢 Novex)
*   增加了 Windows 环境下的自动测试。
*   修正了解码时的问题。aapt1/aapt2 之间的 xsd 文件。
*   修正了解码带有畸形块头的应用程序的问题。(感谢塞布拉斯)
*   修正了 Mac 脚本窃取焦点的问题。
*   修复了阵列资源包项目类型错误的问题。(感谢 vbarthel-fr)
*   将 baksmali/smali 更新至 v2.2.6
*   修复了 9 个补丁图像缺少垂直或水平分割的问题。(感谢 IgorEisberg)
*   解决了引用非标准框架文件的问题。(感谢 IgorEisberg)
*   修复了解析被引用的 SDK 版本代码的问题。(感谢 IgorEisberg)
*   为 unix 添加了 32 位二进制文件，为 aapt1/aapt2 添加了 win。
*   增加了 api 等级传递给 smali 的能力。(感谢 IgorEisberg)

APKTool 是 XDA 社区的宝贵工具。多亏了它，我们可以为您带来来自谷歌、三星、华为、小米和其他公司的最新软件功能的新闻。开发人员在制作谷歌摄像头端口时也使用它。我们感谢 APKTool，感谢它带来的一切可能。

[**在安卓软件开发论坛**](https://forum.xda-developers.com/showthread.php?t=1755243) 阅读更多关于 APKTool 的内容