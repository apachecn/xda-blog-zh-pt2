# 三星 Galaxy S10 可能无法使用 Swift 安装程序或 Substratum 中的自定义主题

> 原文：<https://www.xda-developers.com/samsung-galaxy-s10-custom-overlay-themes-swift-installer-substratum/>

三星的最新旗舰产品三星 Galaxy S10 将该公司在消费者就绪型硬件和软件方面取得的最佳成果整合到一款智能手机中，这将让竞争对手彻夜难眠。Galaxy S10 提供了迄今为止最好的三星体验，这是通过在这一领域的 10 年努力而实现的。

尽管三星 Galaxy S10 有很多优点，但人们一旦开始探索这款手机，就会发现它仍有一些痛处。事实证明，Galaxy S10 可能无法使用 Swift 安装程序或底层的自定义主题，[类似于三星 Galaxy S8 和三星 Galaxy Note 8 上的 One UI 更新](https://www.xda-developers.com/one-ui-blocks-substratum-swift-installer-samsung-galaxy-s8-galaxy-note-8/)所发生的情况。

我们的 YouTube 频道的 TK Bay 发现，美国解锁的 Galaxy S10+不允许使用第三方覆盖。这已经在三星 Galaxy S10+ SM-G975U1 上发现，这是解锁的骁龙变种，内部版本号为 PPR1.180610.011.G975U1UEU1ASAU，OneUI 版本为 1.1。

当 TK 试图安装并使用 XDA 公认的开发者[za chare 1](https://forum.xda-developers.com/member.php?u=7055541)的 One UI Tuner app 来[将状态栏时钟向右移动](https://www.xda-developers.com/move-status-bar-clock-right-samsung-one-ui/)时，原本要安装的覆盖图没有安装成功(见上图图库中的图 1)。然后，我们试图通过 ADB 安装覆盖，但这也导致了一个错误(图 2)。Swift 安装程序也存在同样的情况(图 3)。

然而，我们可以确认来自 Galaxy 商店的自定义主题继续工作，这可以在关于电话页面的截图中看到(图 4)。因此，初步看来，三星似乎正在阻止用户从 Substratum 和 Swift Installer 等应用程序安装自定义覆盖图，但对 Galaxy Store 的自定义主题没有任何限制。在 Android Pie 中，安装覆盖层的能力[仅限于平台签名的系统应用，这意味着你需要 root 才能安装它们。一些 One UI 测试版和稳定版允许安装没有平台签名的自定义主题，但 One UI 的新版本显然已经消除了这种行为。](https://www.xda-developers.com/rootless-custom-themes-android-p/)

目前为止的信息仅适用于美国未锁定的 Galaxy S10+。我们需要确认其他 Galaxy S10 型号是否有相同的限制，如果它们运行相同的版本，这是一种可能性。

[**三星 Galaxy S10 论坛**](https://www.xda-developers.com/samsung-galaxy-s10-forums-open/)