# “智能转发”可能会成为未来版本的 Android

> 原文：<https://www.xda-developers.com/android-version-support-smart-forwarding-forward-calls-between-sims/>

# 未来的 Android 版本可能支持“智能转移”来转移 sim 之间的呼叫

未来版本的 Android 将允许当当前号码无法接通时，来电被自动转移到工作中的 SIM 卡上。

与竞争对手相比，Android 的开源特性可以说是其最大的优势。AOSP 允许第三方为他们自己的设备修改安卓系统，也使得他们的代码易于贡献。潜伏在 AOSP 精神中，我们偶尔会发现一些有趣的事情。虽然 Android Q 的稳定版本还没有发布，但谷歌已经在研究一些功能，这些功能将融入未来的 Android 版本。早些时候，我们发现了一个线索，Android R 可能支持 [DualShock 4 运动控制](https://www.xda-developers.com/android-may-support-dualshock-4-motion-controls-new-playstation-apps/)和安全地[存储数字驾照](https://www.xda-developers.com/google-android-digital-drivers-license/)。现在，我们发现了一些与连通性有关的东西。

你可能已经注意到了，最近双卡手机在北美越来越受欢迎。过去两三年的旗舰产品已经开始采用 eSIM 功能，至少支持 DSDS。例如，谷歌 Pixel 3 [上的 Android Q beta 支持 DSDS](https://www.xda-developers.com/android-q-dual-sim-dual-standby-support-pixel-3/) ，有迹象表明 [Pixel 4 也会支持 T3。由于 Pixels 越来越好地支持双 SIM 卡，我们注意到谷歌正在为 AOSP 添加功能，以使每个人的通话体验更容易。有时候你的一张 SIM 卡会停止服务(也许你在一个糟糕的区域或者运营商有一些问题)，而这正是新的“智能转发”将帮助你的地方。](https://www.xda-developers.com/google-pixel-4-dual-sim-rumor/)

Android 未来的新增功能将把你所有的来电从一个无法接通的号码转移到你设备上的工作号码。请记住，只有当您的手机中有两个 sim 卡，并且在接听电话时只有其中一个可用时，才会出现这种情况。你将能够从用户界面触发该功能(并且很可能切换模拟市民)。以下是来自[相关提交](https://android-review.googlesource.com/c/platform/frameworks/base/+/936876)的功能描述:

当插入多个 sim 时，将使用系统。

智能转发的电话配置可以在[这里](https://android-review.googlesource.com/c/platform/packages/services/Telephony/+/937196)找到。老实说，我甚至不知道这种功能可以在系统级实现。从表面上看，具体的运营商不需要添加任何支持，或者至少谷歌还没有提到这一点。提交还没有合并，但由于这些补丁是由谷歌提交的，我们相信它们在被验证不会与其他任何东西冲突后会被合并。如果我们在 AOSP 看到该功能的任何进展，我们将随时更新。