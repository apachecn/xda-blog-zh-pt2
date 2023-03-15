# 在 Windows 上快速签署 apk

> 原文：<https://www.xda-developers.com/quickly-sign-apks-on-windows/>

发布应用程序或自定义 ROM 时，您需要签署。apk 或者。带有使用私钥的证书的 zip 文件。Android 系统使用证书来识别应用程序的作者，并在应用程序之间建立信任关系。

XDA 论坛主持人 [andyharney](http://forum.xda-developers.com/member.php?u=797171) 发布了一个易于使用的工具，可以带签名或不带签名。apk 并重新签名，或者全部批量签名。放在输入文件夹中的 apk 文件。该应用程序包括创建您自己的签名所需的工具，以及所有必需的 Java 文件，因此不需要单独的 Java 安装代码。

如果你觉得有用，请给开发者留下你的评论。

> 最初由 **andyharney** 发布
> 
> 已经决定完全重写我以前的 Sign & Aligner 工具，我已经到了准备测试的阶段。
> 
> 版本 1.1 已发布
> 
> 将 JDK 7 安装路径添加到用户路径-临时更改，用户路径在关闭时恢复
> 
> 增加了对 JDK 安装的检测
> 
> 代码改进
> 
> 特征
> 
> 用测试密钥签名
> 
> 用私钥签名
> 
> 生成您自己的私钥
> 
> 调整您的 apk
> 
> 您可以生成自己的私钥集来签署自己的 apk。生成的密钥完全符合当前 Android 市场的要求。

继续进入[应用线程](http://forum.xda-developers.com/showthread.php?p=16367924#post16367924)了解更多信息。