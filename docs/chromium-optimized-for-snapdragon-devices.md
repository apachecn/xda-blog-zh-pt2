# 针对骁龙设备优化的铬

> 原文：<https://www.xda-developers.com/chromium-optimized-for-snapdragon-devices/>

# 针对骁龙设备优化的铬

Code Aurora 论坛上的开发者已经创建了一个针对骁龙设备优化的 Chromium 浏览器分支。

### CAF 到底是什么？

记得咖啡馆吗？当高通骁龙设备的内核开发人员维护他们工作的两个独立分支时，你可能在所有的论坛上都看到过这个名字。一个是基于谷歌 AOSP 的代码，另一个是基于 CAF 的。Code Aurora 论坛由 Linux 基金会维护，是高通发布各种平台参考资料的地方。大多数原始设备制造商基于高通提供的内核资源。另一方面，AOSP 为每一个 Android 软件迭代开发了一个咖啡馆，在此过程中为所有 Android 设备引入新功能。随着时间的推移，CAF 推出了专门针对骁龙设备的优化。

### Chromium 浏览器

[Chromium](https://www.chromium.org/Home) 是谷歌 Chrome 浏览器的开源版本。低调地，Code Aurora 论坛上的一组开发人员一直致力于为骁龙设备优化 Chromium。[你可以在他们的项目页面](https://www.codeaurora.org/projects/all-active-projects/chromium-browser-snapdragon)上关注他们的进展，在那里你也可以将源代码构建成 APK。一些用源代码构建了 APK 的用户报告说 Chromium 浏览器版本只有 v42，因此已经过时了。通常不建议运行过时的浏览器软件，因为每个版本之间会发现并及时修补许多安全缺陷。然而，似乎 Chromium 的最新稳定版本 v46 最近已经被[合并到项目源代码](https://www.codeaurora.org/cgit/quic/chrome4sdp/chromium/src/log/?h=m46)中，所以你应该很快就能运行最新版本了。

**特性**

维护 CAF 版本的开发人员不仅为骁龙设备优化了浏览器，还引入了许多关键特性，这些特性是我们论坛上的用户渴望从其他浏览器获得的。除了谷歌 Chrome 官方版本的所有功能外，骁龙优化版 Chrome 浏览器还包括:

1.  **夜间模式**
2.  **内置广告拦截器**
3.  **节能模式，限制处理器内核的数量并抑制内核速度以降低功耗**
4.  **改进了下载页面，可以选择保存每个文件的目录**
5.  **侧扫功能，允许您根据从哪边(分别是右/左)扫动来向前/向后移动**

**代码改进**

主观上，感觉 CAF 优化让浏览体验变得更快了。我在谷歌 Play 商店的 Chrome Dev 和 CAF 优化的 Chromium build 上运行了 SunSpider 浏览器基准测试，最终 Chrome Dev 的得分为 **996.7 毫秒+/- 17.5%** ，而 CAF 优化的版本的得分为**761.6 毫秒+/- 13.8%** 。对于对制作网络浏览器感兴趣的开发者来说，CAF [上的开发者已经提供了一个定制页面](https://www.codeaurora.org/xwiki/bin/Chromium+for+Snapdragon/Customization)，上面有添加诸如 URL 和 DOM(文档对象模型)操作器等功能以隐藏不想要的内容的说明。无论你是开发新浏览器的开发者，还是寻找 Chrome 更快替代品的普通用户，这款浏览器都绝对能满足你的需求。

Chrome 是你的默认浏览器吗？你试过这种铬合金吗？请在评论中告诉我们您的浏览器偏好！