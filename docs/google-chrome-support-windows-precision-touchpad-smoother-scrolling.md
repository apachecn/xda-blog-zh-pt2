# 谷歌 Chrome 将最终支持 Windows Precision 触摸板，以实现更流畅的滚动

> 原文：<https://www.xda-developers.com/google-chrome-support-windows-precision-touchpad-smoother-scrolling/>

# 谷歌 Chrome 将最终支持 Windows Precision 触摸板，以实现更流畅的滚动

我们发现，谷歌 Chrome 将最终支持 Windows Precision 触摸板，以便在使用双指滚动手势时实现更平滑的滚动。

多年来，简单的触摸板已经从一个仅用于移动鼠标指针的设备发展到一个可以点击(或按下)来表示点击的设备，现在它们已经开始获得各种控制的手势。Windows Precision Touchpad 使人们能够使用触摸板的某些手势来执行各种任务，但它在 Chrome 上表现不佳，特别是双指滚动手势。然而，谷歌 Chrome 终于开始修复这些问题，并将支持 Windows Precision Touchpad 以实现更流畅的滚动。

关于谷歌 Chrome 如何处理微软精密触摸板计划的抱怨可以追溯到几年前。这些投诉往往在各种社区论坛上获得很高的票数，人们甚至去了谷歌自己的错误报告论坛，试图在 T2 揭示这个问题。如果我们在微软的 Edge 浏览器上使用这些手势，那么像用两个手指上下滚动这样的功能会使网站平滑滚动。然而，当这在 Chrome 中完成时，它是不可思议的，并且导致了糟糕的用户体验。

如果您幸运地找到了一个解决方法，那么您可能已经忘记了这个问题的存在。有一个实验性的 [Chrome 标志叫做 Enable Smooth Scrolling】据报道有助于解决这个问题，其他人发现](chrome://flags/#enable-smooth-scrolling)[安装 SmoothScroll Chrome 扩展](https://chrome.google.com/webstore/detail/smoothscroll/nbokbjkabcmbfdlbddjidfmibcpneigj?utm_source=chrome-app-launcher-info-dialog)有所帮助。不过值得庆幸的是，谷歌已经开始解决这些问题，谷歌 Chrome 最终将原生支持 Windows Precision Touchpad。

我们发现了一个承诺，表明[谷歌正在增加对直接操作](https://chromium-review.googlesource.com/c/chromium/src/+/653581/)的支持，这是让 Windows Precision Touchpad 工作所必需的。首先，另一个[提交显示了流行的缩放手势](https://chromium-review.googlesource.com/c/chromium/src/+/786348/)也被添加到谷歌浏览器中。虽然谷歌花了这么长时间来修复这个问题确实令人失望，但我们很高兴看到正在努力最终增加对这一功能的支持。