# 如何使用 Xposed 将一加人脸解锁与 App Lock 整合

> 原文：<https://www.xda-developers.com/oneplus-face-unlock-app-lock/>

# 如何使用 Xposed 将一加人脸解锁与 App Lock 整合

下面介绍如何将 OnePlus 3、OnePlus 3T、OnePlus 5 和 OnePlus 5T 的面部解锁功能与 OxygenOS 中的 App Lock 功能集成在一起。需要 root 访问权限和 Xposed 框架。

OnePlus 5T 最受欢迎的功能之一是面部解锁功能。该功能如此受欢迎，以至于用户的需求促使一加将其引入 [OnePlus 5](https://www.xda-developers.com/oneplus-5-face-unlock-oxygenos/) 以及后来的 [OnePlus 3/3T](https://www.xda-developers.com/oxygenos-open-beta-30-face-unlock-rolling-out-oneplus-3-3t/) 。

使用你的面部解锁最近的一加手机和安卓多年来一直拥有的可信面部功能之间的主要区别是，一加使用一种专有的软件算法，使其更快更方便，同时能够(在有限的程度上)区分真实的面部和照片。

虽然只通过面部就能快速解锁你的一加手机很棒，但快速的[谷歌搜索](https://www.google.com/search?q=oneplus+face+unlock+app+lock&oq=oneplus+face+unlock+app+lock)显示，许多人希望将这一功能扩展到 OxygenOS 的应用锁定功能。对于那些不知道的人来说，应用程序锁是一种在 pin/指纹扫描仪后面锁定特定应用程序的简单方法。这不是一个创新的功能，因为它的变体已经存在多年了，但内置它当然很好，因为这意味着你不必使用由[性能密集型辅助服务](https://www.xda-developers.com/working-as-intended-an-exploration-into-androids-accessibility-lag/)或 UsageStats API 构建的第三方应用程序。

多亏了一个新的[开源](https://github.com/Cyl18/OnePlus-5T-Applock-Tweaker)exposed 模块，你可以扩展一加的面部解锁功能，以配合应用程序锁定。你所需要做的就是使用 OnePlus 3、OnePlus 3T、OnePlus 5 或 OnePlus 5T，这些设备都是 OxygenOS 版本，包含面部解锁功能，[你是 rooted 用户](https://www.xda-developers.com/root/#oneplus)，并且你已经安装了 [Xposed 框架](https://www.xda-developers.com/xposed-framework-for-android-oreo-beta/)。如果您满足这些要求，您可以按照以下步骤启动并运行该模块:

* * *

## 将一加面部解锁与应用程序锁定功能集成在一起

1.  [下载](http://repo.xposed.info/module/com.cyl18.opapplocktweaker)并从 Xposed 库安装 Xposed 模块。
2.  重启你的手机。
3.  在模块中启用面部解锁。
4.  如果您还没有在 OxygenOS 设置中激活面部解锁。
5.  激活应用程序锁定功能，并选择要锁定的应用程序。

就是这样！享受在您的 OnePlus 3、OnePlus 3T、OnePlus 5 或 OnePlus 5T 上使用流行的面部解锁功能解锁特定应用程序的乐趣！