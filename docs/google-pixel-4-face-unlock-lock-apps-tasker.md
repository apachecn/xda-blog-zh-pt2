# 如何使用谷歌 Pixel 4 的面部解锁来锁定应用程序

> 原文：<https://www.xda-developers.com/google-pixel-4-face-unlock-lock-apps-tasker/>

# 如何使用谷歌 Pixel 4 的面部解锁来锁定应用程序

使用自动化应用 Tasker，你现在可以跳过等待，使用谷歌 Pixel 4 的面部解锁来保护你最喜欢的应用程序。

随着 Pixel 4 系列的[发布，谷歌已经采取了苹果的路线，从旗舰产品中放弃了指纹扫描仪。该公司现在青睐面部识别，并为此在其最新旗舰产品中添加了一系列传感器。然而，Pixel 4 用户可能不得不因为这一举动而处理一些问题。上周，我们了解到用户将不得不](https://www.xda-developers.com/google-pixel-4-specs-features-pricing-availability/)[等待开发者为他们的应用添加面部解锁支持](https://www.xda-developers.com/google-pixel-4-users-wait-developers-add-face-unlock-support/)。然而，我们现在发现了一种方法，让您可以跳过等待时间，使用面部解锁来保护您的应用程序。

**[像素 4 XDA 论坛](https://forum.xda-developers.com/pixel-4)**

使用自动化应用 Tasker，您现在可以为任何应用程序设置面部解锁，而无需等待开发人员使用 BiometricPrompt API 更新他们的应用程序。为此，您只需使用应用程序上下文创建一个配置文件，并选择您希望锁定的应用程序。然后，您可以添加一个任务来启动生物特征类型的身份验证对话框，并将结果存储在一个变量中。如果结果是成功的，那么你不需要进一步做任何事情。然而，如果失败，你将被送回主屏幕。请查看下面视频中的变通方法:

正如你所看到的，面部解锁提示需要一些时间才能弹出。但是你可以选择增加 Tasker 显示认证对话框的速度。为此，打开 Tasker 的设置并导航到监视器选项卡。在这里，减少“应用程序检查毫秒”值，就可以了。这个较低的值将使 Tasker 更快地检测应用程序何时打开，但值得注意的是，它会稍微增加功耗。如果你是 Tasker 的新手，不太知道如何设置个人资料，你可以从下面的链接导入我们的个人资料。同样值得注意的是，您至少需要 Tasker 版本 5.9.beta.5，以便此变通办法正常工作。

**[为任务者](https://taskernet.com/shares/?user=AS35m8kqHfc2QatEJk%2BqYTVVIBuiS1l%2BhCIZlNI5vIQ7E5PxFZMAB3LxyEzqDIBYxD2UAqq%2F&id=Profile%3AFace+Unlock+For+Apps)导入人脸解锁配置文件**