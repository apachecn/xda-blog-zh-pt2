# 谷歌 Pixel 3/2 的主动边缘挤压功能已经移植到定制的 rom 上

> 原文：<https://www.xda-developers.com/google-pixel-active-edge-squeeze-feature-custom-roms/>

# 谷歌 Pixel 3/2 的主动边缘挤压功能已经移植到定制的 rom 上

来自 Pixel 2 和 Pixel 3 手机的流行 Active Edge 的完全开源端口已经提供给定制 rom 社区。

由于 XDA 资深成员[杰特洛克](https://forum.xda-developers.com/member.php?u=4723245)和[肮脏独角兽](https://dirtyunicorns.com/) rom 开发团队的努力，来自 Pixel 2 和 Pixel 3 手机的流行 [Active Edge](https://www.xda-developers.com/google-pixel-2-active-edge-google-pixel-3/) 的完全开源端口首次向定制 ROM 社区开放。后者在 Twitter 上宣布了 Active Edge 的上市。

除了可以从肮脏的独角兽 [Gerrit](https://gerrit.dirtyunicorns.com/#/q/status:merged+topic:active_edge) 和 [Github](https://github.com/DirtyUnicorns/android_external_google) 链接中挑选，发布候选版本还可以用于 Pixel 2 XL ( [taimen](https://download.dirtyunicorns.com/?device=taimen#Rc) )、Pixel 3 ( [blueline](https://download.dirtyunicorns.com/?device=blueline#Rc) )和 Pixel 3 XL ( [crosshatch](https://download.dirtyunicorns.com/?device=crosshatch#Rc) )。只需点击 RC 选项卡后，按照您的设备的链接。注意:在刷新任何这些候选版本之前，为您支持的设备安装最新的供应商、引导加载程序和无线电映像非常重要。该团队没有正式支持常规的 Pixel 2 (walleye)，但对于有经验的定制 ROM 开发人员来说，挑选提交并包括必要的库应该没有问题。我闪现了 taimen 的构建，并在下面录制了一个 Active Edge 的演示。

正如在 Dirty Unicorns 中实现的那样，Active Edge 不仅仅是简单地触发谷歌助手相关的操作，就像它在股票 Pixel 手机上的专有对应物一样。它还可以用来拍照、切换手电筒、清除通知、显示音量面板、关闭屏幕、显示通知和显示快速设置面板。我个人希望 Jertlok 或任何使用他的作品的定制 ROM 开发者最终会添加一个动作，让谷歌助手说“哎哟！别这么用力挤我！”

首次开发这种主动 Edge 端口的开发者 Jertlok 不得不艰难地完成这项工作，因为这项功能从未推向 AOSP(毫无疑问，因为它的更大兄弟是 HTC 从 HTC U12 获得的专有 Edge Sense 功能，HTC 制造了 Pixel 2)。Jertlok 必须对 Active Edge 进行反编译和逆向工程，以使其可用于定制 rom，他在 Dirty Unicorns[Github](https://github.com/DirtyUnicorns/android_frameworks_base/commit/e0d49ebf2cf08593872733bbb01e40e694886d94)repo 中详细描述了这一过程。

* * *

[**来源:肮脏独角兽(推特)**](https://twitter.com/_DirtyUnicorns_/status/1095762148138074114)