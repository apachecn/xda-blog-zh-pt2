# 使用三星的远程测试实验室在 Galaxy Z Fold 2 上测试您的应用程序

> 原文：<https://www.xda-developers.com/test-app-samsung-galaxy-z-fold-2-remote-test-lab/>

昨天，三星[公布了关于](https://www.xda-developers.com/samsung-galaxy-z-fold-2-foldable-smartphone-pricing-unveil-launch/) [Galaxy Z Fold 2](https://www.xda-developers.com/samsung-galaxy-z-fold-2/) 的更多细节，这款手机将于 9 月 18 日开始在美国销售，但现在[可以预订](https://www.xda-developers.com/best-galaxy-z-fold-2-deals/)。我们对这款设备的第一印象非常积极，但是 1999 美元的价格，并不是每个人都买得起。对于对可折叠外形优化应用感兴趣的开发人员来说，这可能会有问题，因为在实时硬件上测试应用总是更可取的。谢天谢地，三星在远程测试实验室有解决这个问题的方案。

三星周三发表了一篇简短的博客文章，介绍了如何开发创新的可折叠手机的一些一般细节。该公司提醒开发者该设备的灵活模式和应用连续性功能。[当可折叠部分折叠时，会触发灵活模式](https://developer.samsung.com/galaxy-z/flex-mode.html)，让应用程序利用拆分 UI 提供的扩展可用性。计划一旦设备进入灵活模式，你的应用会发生什么？看看 Jetpack 的[窗口管理器库](https://medium.com/androiddevelopers/support-new-form-factors-with-the-new-jetpack-windowmanager-library-4be98f5450da)。[应用连续性](https://developer.samsung.com/galaxy-z/app-continuity.html)另一方面，指的是当配置在折叠和展开之间改变时，应用无缝恢复其状态的能力，反之亦然。应用程序应该保存它们的用户界面状态，并支持优雅的配置更改，以便当前任务在转换后无缝地继续。

现在 Galaxy Z Fold 2 已经可以在三星的远程测试实验室中使用，任何开发者都可以用 Flex 模式和应用连续性来测试他们的应用程序的行为，而不仅仅是那些幸运地花了 2000 美元的人。三星的远程测试实验室通过将三星智能手机连接到云来工作，开发者可以远程控制云。该系统很有帮助，因为它允许开发人员在最新的硬件上测试他们的应用程序，即使他们无法实际访问这些设备。开发人员还可以远程安装 APK 文件，进行屏幕捕捉和录制，以及测试自动化脚本。遗憾的是，远程测试实验室不支持音频、附加外设、多点触控和摄像头。尽管有其局限性，但它对使发展变得更容易实现大有帮助。

今年早些时候，三星[曾将](https://www.xda-developers.com/developers-test-apps-samsung-galaxy-note-20-remote-test-lab/)Galaxy Note 20 与 Galaxy S20 系列和 Galaxy Z Flip 一起加入其远程测试实验室。

**[三星 Galaxy Z Fold 2 论坛](https://forum.xda-developers.com/samsung-galaxy-z-fold-2)| |****[远程测试实验室](https://developer.samsung.com/remotetestlab/galaxy/rtlDeviceList.action#481)**