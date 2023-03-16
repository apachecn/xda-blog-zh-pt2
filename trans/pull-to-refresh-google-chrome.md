# Chromebooks 和 2 合 1 Windows 笔记本电脑的 Google Chrome 现在可以启用拉取刷新功能

> 原文：<https://www.xda-developers.com/pull-to-refresh-google-chrome/>

下拉刷新是一种向下滑动的手势，可以刷新应用内的内容，多年来已经出现在许多 Android 应用程序中。但这不是我们在 Chrome 上看到的东西。这种情况在本周发生了变化:Chrome OS 设备上的 Chrome 浏览器和 2 合 1 笔记本电脑上的 Windows 获得了一个刷新手势。

我们第一次听说 pull to refresh [将于 2017 年 7 月登陆 Chrome](https://chromeunboxed.com/chromebooks-pull-to-refresh-browser/) ，这要归功于 *Chrome Unboxed 的一篇文章。在 Chromium Gerrit 代码评审的一次合并提交中发现了这个问题。*

早在 7 月份，这个特性还没有实现，但是现在看起来已经改变了。Reddit 用户[卢卡斯班](https://www.reddit.com/user/lucasban)上传了一个短视频到[/r/ChromeOS](https://www.reddit.com/r/chromeos/)subredit，演示在谷歌 Pixelbook 上拉刷新。

它在 Chrome OS 和 Chrome for Windows 的开发者通道中可用，但默认情况下不启用。为了让它工作，你需要通过这里的隐藏标志来切换它:[chrome://flags/# pull-to-refresh](chrome://flags/#pull-to-refresh)。

有报道称，Chrome OS 版本 63 在稳定频道上显示了拉至刷新功能，但有些人在让它工作时遇到了一点麻烦。至少有一个三星 Chromebook Pro 用户在启用拉至刷新标志的情况下，幸运地将 over scroll history([chrome://flags/# over scroll-history-navigation](chrome://flags/#overscroll-history-navigation)设置为 **Simple** 。

说到 Chrome OS 上的多点触摸手势，拉至刷新并不是唯一的最新发展。今年 1 月，谷歌在 Chrome 中增加了对直接操作的支持，这为在配有精密触摸板的 Windows 笔记本电脑上实现更流畅的多点触摸手势奠定了基础。本周，我们发现了一项承诺，表明所有新的和现有的 Chromebooks 将很快获得触摸板缩放支持。

关于 Chrome 目前支持的多点触摸手势的完整列表，请查看谷歌的[支持页面](https://support.google.com/chromebook/answer/1047367?hl=en)。它充满了帮助你开始的提示。

* * *

[来源:Reddit 用户卢卡斯 T3](https://www.reddit.com/r/chromeos/comments/7z9wlu/pulltorefresh_flag_working_in_chrome_os_dev/)