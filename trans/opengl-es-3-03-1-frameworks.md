# Michael Leahy 发布 OpenGL ES 3.0/3.1 框架

> 原文：<https://www.xda-developers.com/opengl-es-3-03-1-frameworks/>

你可能知道 XDA 论坛成员迈克尔·莱格，又名迈克尔·莱希。Michael 因在 Android 上使用 OpenGL 而闻名。事实上，在 Android BBQ 2014 大会上，他发表了题为“ [OpenGL ES 3.1 / Android 扩展包](http://forum.xda-developers.com/member.php?u=4680981)”的演讲。今天，他以 [apache 许可框架演示](http://forum.xda-developers.com/tools/programming/library-modern-opengl-es-3-0-3-1-t2973316)的形式为开发者提供了更多信息。

作为一名开发人员，你很快就会发现的一件事是，我们可以说，使用图形是令人沮丧的。当您的图形类似于视频时，尤其如此。虽然有相当多的应用程序使用 OpenGL，但没有太多是开放的，开发者也没有分享他们自己的加速框架。在这种情况下，Michael 为您提供了利用 OpenGL 构建应用程序所需的一切。他还提供了指南和维基条目。

你可能会问自己，“这提供了 Android 本身所没有的什么？”好吧，你可以直接进入代码并找出答案，或者你可以直接从这个人那里听到:

> 从资产中轻松加载着色器代码的能力相当不错。AndroidGLESXXUtil 中的任何东西都可以真正减轻负担。OpenGL API 的工作方式是，您必须将数组或 IntBuffer 传递到方法调用中，以进行查询并获得返回值。所有这些都是通过 ThreadLocal 创建在内部管理的，所以它也是线程安全的。
> 
> 我用 EGL 1.4 重写了 GLSurfaceView -> GLSurfaceView2，删除了 1.0 版 Android SDK 中的所有遗留内容
> 
> AndroidGLES20Util 就是一个很好的例子。AndroidGLES30Util 中也有覆盖，可以更有效地加载纹理，并正确地使它们与计算着色器一起工作。Adreno 420 非常挑剔，但我发现了一种加载纹理的好方法，这种方法在 K1 for compute shader 上有效，但不会破坏它，但不会破坏 Adreno GPU 上的正常纹理支持。

虽然 Michael 目前正在运行一个 kickstarter，它将于今晚关闭，并且可能不会得到资助，但他分享这个内容的主要目标是找到对这个项目有类似兴趣的人，并为开发人员提供开源的 Apache 许可的标准。因此，如果你是一名开发人员，并且对 Android 上的 OpenGL 应用于电影感兴趣，请随时联系他。否则，检查这个 [OpenGL 演示](https://github.com/typhonrt/modern-java6-android-gldemos)项目以及[框架](https://github.com/typhonrt/modern-java6-android-glframework)。还有，别忘了[维基](https://github.com/typhonrt/modern-java6-android-gldemos/wiki/installation)！

如果你想看看这个框架能做些什么，而又不弄湿你的脚，那就去看看[演示](https://github.com/typhonrt/modern-java6-android-gldemos/blob/master/prebuilt-apk/ModernGL.apk?raw=true)。在依赖这个框架的 [kickstarter](http://kck.st/1xA3R61) 上有更多的例子。此外，别忘了看看[迈克尔·格雷格](http://forum.xda-developers.com/member.php?u=4680981)的 [XDA 论坛帖子](http://forum.xda-developers.com/tools/programming/library-modern-opengl-es-3-0-3-1-t2973316)。