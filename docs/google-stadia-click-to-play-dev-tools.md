# Google Stadia 增加了点击播放试用和新的开发移植工具

> 原文：<https://www.xda-developers.com/google-stadia-click-to-play-dev-tools/>

谷歌最近一直在扩大其 Stadia 游戏流媒体服务，支持更多智能电视和缓慢但稳定地推出更多游戏。然而，关于[谷歌的注意力从游戏服务转移到其他公司的白标流媒体技术的报道](https://www.xda-developers.com/google-stadia-google-stream/)抑制了体育场周围的兴奋。现在，对于 Stadia 玩家和游戏开发者来说，有一些好消息，有两个新功能宣布。

首先，谷歌试图通过引入“低变更移植”(LCP)让开发者更容易支持 Stadia。虽然 GeForce Now 和亚马逊 Luna 等其他流媒体服务都是由基于云的 Windows 虚拟机提供支持，但谷歌 Stadia 使用了一种基于 Linux 的定制架构，这种架构提高了游戏响应能力，但代价是开发人员增加了额外的工作。

LCP 是一组新的组件和工具，包括自动将 DirectX 调用翻译成 Vulkan 的库(大概类似于/基于 [Valve 的 Vkd3d 库](https://github.com/ValveSoftware/vkd3d))，改进的 Unity 和 Unreal 引擎支持，以及 play testing/质量保证的新工具。Mataboo 的*城市传奇*和 Milestone Srl 的 *MotoGP 21* 目前正在使用低变更移植，谷歌将在今年晚些时候向其他 Stadia 合作伙伴推出这些工具。

Stadia 的另一项改进是点击游戏试用，它允许任何人在游戏开发商确定的时间内立即玩游戏。Click to Play 不需要输入支付细节或创建 Stadia 帐户，游戏开发者也不必更新任何代码来激活它。这项技术已经在一些游戏中进行了测试，如 Jackbox Party Pack 8，但它将在 2022 年的某个时候向所有合作伙伴推出。

谷歌希望 LCP 和 Click to Play 都能改善 Stadia 的游戏库和玩家数量。该公司表示，其对点击播放的早期测试与传统的购买/索赔信息相比，点击率提高了 35%，与常规广告相比，玩家参与度提高了 70%。