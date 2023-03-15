# Chainfire 发布 SuperSU v2.78 SR5，修复了一些牛轧糖 bug

> 原文：<https://www.xda-developers.com/chainfire-releases-supersu-v2-78-sr5-fixing-some-nougat-bugs/>

自 9 月起，XDA 认可的开发商 Chainfire [开始为 SuperSU](https://www.xda-developers.com/supersu-v2-78-sr1-released-with-su-binary-bugfixes-and-new-versioning-scheme/) 开发新的版本系统。这从 SuperSU 的 2.78 SR1 版本开始，到今天这个人已经发布了 2.78 SR5。他没有把它们标为 Beta，而是把它改成了一个服务发布命名方案。他认为这将是减少试图将测试版上传到非 Google Play 应用商店的人数的一个好方法，因为它将继续携带相同的版本号。

从那以后，Chainfire [开始着手让 SuperSU 兼容](https://www.xda-developers.com/supersu-is-updated-to-version-2-78-sr3-fixes-pixel-related-issue-and-more/) [Pixel](http://forum.xda-developers.com/pixel) 和 [Pixel XL](http://forum.xda-developers.com/pixel-xl) 的工作，同时消除一些与 Android 7.x 牛轧糖相关的错误。大多数错误修复都与 Android 7.0 和 Pixel 手机引入的 A/B 分区系统有关。但是有一些其他的东西，如 sukernel，supolicy，suinit，并确保 SuperSU 与 TWRP 并肩工作，因为他们有冲突，直到 SR4 发布。

今天，他发布了 SuperSU 的另一个更新，这次又聚焦于一些牛轧糖相关的错误。在 Google+的一篇帖子中，Chainfire 告诉我们，由于 SuperSU 对 SELinux 的一些修改以及 Nougat 中更严格的服务执行规则，一些脚本和服务无法执行。这并不是在所有的固件上都发生了，但这确实导致了 Wi-Fi、蜂窝和其他与调制解调器相关的功能在某些固件上无法工作(如三星 Nougat beta 和 CyanogenMod 14.1)。

通过这次更新，SuperSU GUI 现在提供了一种方法来禁用三星的 SecurityLogAgent 组件，作为禁用 KNOX 的一部分(以帮助删除人们遇到的一些弹出窗口)。Chainfire 还发布了一个定制包，用于获得对 [HTC 10](http://forum.xda-developers.com/htc-10) 新牛轧糖更新的 root 访问权限。这将通过 TWRP 或 CF-Auto-Root 替换为可闪存的 ZIP，当它变得可用时。

你可以在这里下载[新版 SuperSU，也请务必在 XDA](http://download.chainfire.eu/1014/SuperSU/SR5-SuperSU-v2.78-SR5-20161130091551.zip) 查看 [SuperSU 线程。](http://forum.xda-developers.com/apps/supersu/2014-09-02-supersu-v2-05-t2868133)

### 变更日志

*   修复可能无法在 7.x 固件上执行的基于外壳的脚本/服务
*   向 Samsung KNOX 检测添加 SecurityLogAgent
*   sukhernel:force sec label

[**来源:+火链**](https://plus.google.com/+Chainfire/posts/jpR76YEgaM9)