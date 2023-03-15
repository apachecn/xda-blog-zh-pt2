# 谷歌准备将 Chrome 更新从 Chrome OS 更新中分离出来

> 原文：<https://www.xda-developers.com/google-prepares-decouple-chrome-updates-chrome-os-updates/>

# 谷歌准备将 Chrome 更新从 Chrome OS 更新中分离出来

谷歌正在进行一项名为 Lacros 的实验性计划，旨在将 Chrome 更新从 Chrome OS 更新中分离出来。

虽然谷歌向 Chrome OS 设备推送常规软件更新，但这些更新依赖于几个特定于设备的非谷歌硬件和软件。由于这个原因，许多旧的[Chrome book](https://www.xda-developers.com/tag/chromebooks/)不会无限期地接收 Chrome 浏览器更新，这使得它们在发布几年后就容易受到攻击。据报道，为了解决这个问题，谷歌正在进行一项代号为 Lacros 的实验计划，将 Chrome 更新与 Chrome OS 更新分离。

根据 Android Police 就此事的一份报告，Lacros 的目标是分离系统 UI(灰窗管理器、登录屏幕等)。)来自 Chrome OS 上的 Chrome 二进制。为此，Chrome 开发者将 Chrome OS 上现有的 Chrome 二进制文件重命名为 ash-Chrome，改动很小。开发人员随后将 linux-chrome 二进制文件重命名为 lacros-chrome，改进了它的 Wayland 支持，并使它像 chrome 操作系统上的 web 浏览器一样工作。实际上，这些变化将允许 Google 以一定的性能/资源成本独立发布两个独立的二进制文件。通过拥有两个不同的 Chrome 实例，谷歌将能够向停止接收 Chrome 操作系统更新的停产 Chromebooks 推送浏览器更新。

Chrome 更新与 Chrome OS 更新的分离预计将对使用旧硬件的 Chromebook 用户产生积极影响。通过 Lacros，用户将能够接收到谷歌 Chrome 的最新更新，即使他们的设备上没有运行最新版本的 Chrome OS。这不仅可以确保用户获得最新的 Chrome 功能，而且有望使报废的 Chromebooks 使用起来更安全。然而，这些变化仍处于早期发展阶段，我们没有任何进一步的信息表明谷歌计划在该功能最终进入稳定渠道时如何向用户推出这些变化。当我们从该公司获得更多信息时，我们将更新这个帖子。

* * *

**来源:[谷歌 Git](https://chromium.googlesource.com/chromium/src.git/+/master/docs/lacros.md)**

**Via: [安卓警察](https://www.androidpolice.com/2020/09/12/google-is-separating-chrome-from-chrome-os-its-a-big-deal-heres-what-you-need-to-know/)**