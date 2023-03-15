# [更新:即将推出 75 版本]谷歌 Chrome 将增加图片延迟加载功能，以加快手机页面加载速度

> 原文：<https://www.xda-developers.com/google-chrome-image-lazy-loading-speed-up-page-loading-mobile/>

# [更新:即将推出 75 版本]谷歌 Chrome 将增加图片延迟加载功能，以加快手机页面加载速度

谷歌 Android 版 Chrome 将增加延迟加载功能，以加快页面加载速度。延迟加载指的是只加载可见内容的概念。

**更新 2 (4/8/19):** Lazy-loading 终于要在下个月 75 版本中毕业到 Google Chrome 的稳定版了。

**更新 1(2018 年 8 月 14 日)**:延迟加载现在可以作为 Chrome Canary 的一个功能标志。更多信息如下。

每当您在网络浏览器上加载网页时，整个页面都会被下载。这在桌面设备或具有快速互联网连接的移动设备上不是问题，但谷歌一直在寻找方法来加速移动网络浏览，以便将下一代用户带到网络上。这里或那里的一些小的优化可以产生很大的不同，像[延迟加载](https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/czmmZUd4Vww/1-H6j-zdAwAJ)(通过 [*出血计算机*](https://www.bleepingcomputer.com/news/google/google-chrome-to-feature-built-in-image-lazy-loading/) )就是这种优化的一个典型例子。这里的想法是，一个网站将只在人们实际上可以看到的部分呈现图像和文本。因此，除非这个人向下滚动到底部，否则这些视图之外的图像和文本永远不会从服务器发送到您的浏览器。不是所有的网站都会因为这样或那样的原因实现这一点，但是看起来 Google Chrome 将会在未来的更新中为所有的网站实现这一点。

这是一个相当有趣的特性，因为统计数据已经证明，当开发人员在他们的网站上使用惰性加载脚本时，页面加载时间要快得多。平均测试表明，这可以提高 18%至 35%的页面加载速度，但当然，这将因网站而异。这完全取决于网站是如何设置的，以及从中加载了什么类型的内容。

谷歌已经表示，目前他们超过 50%的网络搜索查询来自移动设备，所以你可以看到这会产生多大的影响。对于发展中国家的用户来说，在谷歌 Android Chrome 浏览器中增加一个载入功能可能是一个很好的补充。这项功能需要做很多工作，因为谷歌需要重做一些现有的功能，包括“打印”或“另存为”，这样浏览器就可以在打印或保存网站之前加载整个页面。

* * *

## 更新 1:生活在桌面上的金丝雀

正如[*bleeding computer*](https://www.bleepingcomputer.com/news/google/built-in-lazy-loading-lands-in-google-chrome-canary/)所报道的，最新的 Chrome Canary 构建在桌面上，现在有了功能标志，当启用时，会带来延迟加载支持。

```
 chrome:
chrome: 
```

这些标志分别启用 image 和 iframe 延迟加载。还注意到谷歌正在与 W3C 合作创建一个 HTML 属性，网站可以用它来指定一个元素是否不应该被延迟加载。

## 更新 2:即将推出 Chrome 75

Chromium gerrit [上的一名谷歌开发者发布了](https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/jxiJvQc-gVg/wurng4zZBQAJ)他们打算在 Chrome 75 中发布惰性加载功能(通过 [Reddit](https://www.reddit.com/r/Android/comments/bat1ni/google_chrome_to_support_lazy_loading_by_default/) 和[TechDows](https://techdows.com/2019/04/chrome-lazy-load-images-and-iframes.html))。)