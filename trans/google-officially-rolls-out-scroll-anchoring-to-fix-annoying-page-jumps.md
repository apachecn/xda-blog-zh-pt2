# 谷歌正式推出滚动锚定来修复恼人的页面跳转

> 原文：<https://www.xda-developers.com/google-officially-rolls-out-scroll-anchoring-to-fix-annoying-page-jumps/>

去年，我们[指出了一个修复](https://www.xda-developers.com/psa-enable-scroll-anchoring-in-google-chrome-to-prevent-annoying-page-jumps/)来防止谷歌 Chrome 浏览器中恼人的页面跳转导致你点击你不想点击的东西。这个修复被称为“滚动锚定”，它要求你在`chrome://flags`中启用一个实验标志。出现此问题的原因是由于网页内容的“渐进式加载”,它允许用户在网页完全加载之前与其进行交互。然而，这通常会导致在用户开始与网页交互后几秒钟就加载屏幕外的内容，从而下推当前屏幕上的内容，并经常导致误点击。现在，解决这个问题的功能，滚动锚定，终于从 Chrome 版本 56 开始对所有用户启用。

这个功能被称为滚动锚定，因为当启用时，Chrome 将锁定屏幕上元素的当前滚动位置，而屏幕外的内容继续加载，这应该可以防止意外的页面跳转。谷歌声称，自从实现了滚动锚定，这一功能就防止了“每次页面浏览大约三次页面跳转”，这已经是一个很大的进步。

然而，并不是所有的 web 元素都能很好地使用这个特性，正如我们中的许多人在去年启用了这个实验性特性后很快发现的那样。当用户启用滚动锚定时，一些网页内容会行为不端，但对于这些，Google 引入了一个新的 CSS 属性“溢出锚”，web 开发人员可以实现它来覆盖滚动锚定。

谷歌的新滚动锚定功能据说将在 Chrome 版本 56 及更高版本中推出，这意味着它应该在稳定、测试、开发和金丝雀频道中启用，但如果你没有注意到该功能，你可以通过将`chrome://flags/#enable-scroll-anchoring`粘贴到地址栏来仔细检查它是否启用。Google 设置的默认选项将启用该特性，但是在这里手动将其设置为 enabled 也没有坏处。

* * *

[**来源:铬博客**](https://blog.chromium.org/2017/04/scroll-anchoring-for-web-developers.html)