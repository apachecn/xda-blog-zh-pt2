# 谷歌 Pixelbook 可能支持启动微软 Windows

> 原文：<https://www.xda-developers.com/google-pixelbook-windows-support/>

[最近的一次提交表明](https://chromium-review.googlesource.com/c/chromiumos/overlays/chromiumos-overlay/+/1026378)谷歌 Pixelbook 可以获得从 USB 启动和安装 Windows 的支持，这一功能以前由于 Kaby Lake 和 Skylake 设备上的固件支持较差而不可用。

 <picture>![screenshot of the commit, ](img/c0c15f0619e30257392fc238b67e3661.png)</picture> 

It's pretty clear what functionality this code merge brings.

此次更新与之前关于 [Alt OS 功能](https://www.xda-developers.com/google-pixelbook-altos/)的报道有关，即[增加了一个 Alt OS[替代 OS]选择器屏幕](https://chromium-review.googlesource.com/c/chromiumos/platform/bmpblk/+/972762)，我们之前怀疑这可能与启动 Windows 或 Fuchsia 有关，但看起来证据支持前者是真的。

不幸的是，这些更新被合并到 Pixelbook 的一个独特的固件分支“eve-campfire”，这不同于正常的分支“eve”。campfire 分支还没有公开，正在由 Google 内部开发和测试，所以很难说我们是否会在野外看到 Alt OS 功能。

谷歌 Pixelbook 于 2017 年 10 月与谷歌 Pixel 2/2 XL Android 智能手机一起发布。这是一台运行操作系统的高端笔记本电脑，目前还没有提供利用其硬件的工具。随着 Chrome OS 引入 [Crostini，这种情况可能会很快改变，Chrome OS 允许在 Chromebooks 上运行 Linux 应用程序。将 Linux 应用程序引入 Chrome OS 是将更多专业人士引入生态系统的一个很好的方式，但仍然会有很多依赖微软 Windows 的顽固分子。](https://www.xda-developers.com/linux-apps-chrome-os-overview-crostini/)

不过，如果 Pixelbook 的公共版本中真的有这种功能，那么启动微软 Windows 是一回事，获得适合硬件的驱动程序是另一回事。Pixelbook 的所有者们，先别抱太大希望。

来源:Chromium code-review，Chromebox 先生[ [reddit](https://www.reddit.com/user/mrchromebox) ] [ [网站](https://mrchromebox.tech/) ]获取他的固件知识