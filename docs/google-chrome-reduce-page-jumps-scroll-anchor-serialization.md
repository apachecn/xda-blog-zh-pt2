# 谷歌浏览器增加了一个功能，减少向前/向后导航时烦人的页面跳转

> 原文：<https://www.xda-developers.com/google-chrome-reduce-page-jumps-scroll-anchor-serialization/>

浏览网页并不总是美好的经历。在智能手机上市和智能手机占主导地位的这段时间里，功能不足的设备很难呈现以台式机为设计理念的网站。从那时起，移动网络已经随着响应式设计、优化框架(如[加速移动页面(AMP)](https://www.xda-developers.com/google-amp-url-canonical-cache-update/) )等东西而发展。就谷歌而言，它正在继续研究其在谷歌浏览器中实现的**滚动锚定**功能，以减少页面跳转。

回到 2016 年夏天，当[我们第一次写了谷歌工程师一直在测试的实验性 Chrome 功能](https://www.xda-developers.com/psa-enable-scroll-anchoring-in-google-chrome-to-prevent-annoying-page-jumps/):滚动锚定。它防止了谷歌 Chrome 浏览器加载屏幕外内容时出现的恼人的文本重排问题，这个问题让人们感到沮丧，因为它会导致广告、照片和链接的意外点击。

滚动锚定是实验性的，一直在积极开发中，直到 2017 年 4 月，[被推送到 Android 的 Chrome 稳定版本](https://www.xda-developers.com/google-officially-rolls-out-scroll-anchoring-to-fix-annoying-page-jumps/)。它极大地改善了 Chrome 的用户体验，但谷歌并没有就此止步。这家搜索巨头已经扩展了滚动锚定[，称之为滚动锚定序列化](https://groups.google.com/a/chromium.org/forum/m/#!topic/blink-dev/7NO-VxiozQs)，旨在减少当你在网站上前后导航时有时会发生的页面跳转。

挺聪明的。Chrome 的默认滚动行为恢复并保存像素偏移量的绝对值。相比之下，**通过滚动锚**恢复你的滚动位置，允许页面锚更早地建立，并防止在页面加载期间可能导致可见跳转的回流。

这个新特性需要通过一个 Chrome 标志来启用，这个新特性的提交可以在[这里找到](https://chromium-review.googlesource.com/c/chromium/src/+/878721/)。点击 Android 版 Chrome(目前是 Canary 和 nightly Chromium)中的[链接](chrome://flags/#enable-scroll-anchor-serialization)，你会直接进入 chrome://flags 页面中相应的**滚动锚定序列化**开关。要让它工作，启用标志并重启 Chrome 使其生效。