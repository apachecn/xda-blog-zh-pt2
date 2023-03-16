# 谷歌 Pixel 5 和骁龙 765 的更多证据浮出水面

> 原文：<https://www.xda-developers.com/google-pixel-5-snapdragon-765/>

随着谷歌在 T2 的发布会迅速临近 T3，谷歌 Pixel 4a 最近受到了很多关注。然而，在 Pixel 4a 公布后，谣言工厂将转移到谷歌 Pixel 5 上。目前还不太清楚这一设备系列，但自 1 月初以来，一直有传言称谷歌将退出“旗舰”市场。现在，我们相当有信心地说，谷歌 Pixel 5 确实不会是一款“旗舰”设备，因为它将拥有[高通骁龙 765](https://www.xda-developers.com/qualcomm-snapdragon-765-processor-specifications-features/) 而不是[高通骁龙 865](https://www.xda-developers.com/qualcomm-snapdragon-865-processor-specifications-features/) 。

早在一月份，我们是第一个报道三种可能的像素代号的人:太阳鱼、荆棘和红鳍。Sunfish 是由高通骁龙 730 驱动的设备，而 bramble 和 redfin 都是在高通骁龙 765 的基础上构建的。我们[很快证实了](https://www.xda-developers.com/google-pixel-4a-sunfish-qualcomm-snapdragon-730/)“太阳鱼”确实是 Pixel 4a，但迄今为止还没有确切的证据将黑莓和 redfin 的代号与任何特定的 Pixel 设备联系起来(到目前为止，仍然没有)。不过，我们一直怀疑这两个代号指的是谷歌 2020 年末的旗舰 Pixel 设备。早在三月份，XDA 资深成员 [cstark27](https://forum.xda-developers.com/member.php?u=2712580) 分析了[泄露的谷歌相机 7.4 APK](https://www.xda-developers.com/google-camera-7-4-leak-4k-60fps-video-recording/) 和[第一个发现【bramble 和 redfin 可能会使用 Pixel 2020 照片配置。](https://twitter.com/Cstark_27/status/1237802450284949506)

不过，我们并不放心仅仅基于代码分析就明确宣布 Pixel 5 将由高通骁龙 765 驱动。这是因为仍然只有一个证据将“荆棘”和“红鳍”与骁龙 765 联系起来——这是我们在 1 月份首次发现的代号。不过，现在我们有了另一项证据，将这两个代号与高通的骁龙 765 联系起来。

在 [Android 11 开发者预览版 4](https://www.xda-developers.com/google-android-11-beta-june-3-2020-developer-preview-4-live-release/) 中，XDA 资深会员 [cstark27](https://forum.xda-developers.com/member.php?u=2712580) 发现，预装的 EUICCGoogle APK 更新了一个新的参考谷歌即将推出的设备。在 APK 的参考资料中，他发现“modem_model_mappings_json”字符串现在包含了“g7250”调制解调器的新行，这很可能是谷歌对骁龙 765 的代号(尽管它也可以指骁龙 765G 或[骁龙 768G](https://www.xda-developers.com/qualcomm-announces-snapdragon-768g-mobile-platform/) ，因为这三者都是 pin 和软件兼容的)。g7250 调制解调器与一个散列名称配对(谷歌在这里是偷偷摸摸的)，所以 cstark27 必须修改谷歌相机 APK，以返回来自给定代码名称的散列。当他将自己的设备代号伪装成“redfin”和“bramble”时，logcat 输出返回的散列名称与 EUICCGoogle 资源中的名称相匹配。

 <picture>![](img/13baef32d7b1a217fbd976e5e9899357.png)</picture> 

On the left is the hashed names from the EUICCGoogle APK and on the right is output from a modified APK to return the hash from a given codename.

此外，今天早些时候，*[Android Police 的主编大卫·鲁多克通过他自己的消息来源](https://twitter.com/rdrv3/status/1262726642780139526?s=21)声称，Pixel 5 将由高通骁龙 765 SoC 驱动。因此，现在可以有把握地假设，谷歌将*而不是*在今年晚些时候发布一款与高通顶级骁龙 865 合作的设备。*

 *如前所述，自从我们在一月份首次发现以来，这种现象就一直在流传，尽管还没有确凿的证据浮出水面。事实上，仍然没有确切的证据证明这一点，但我们目前掌握的所有证据都表明了这一点。这一传言也与最近的[谷歌意见奖励调查](https://www.xda-developers.com/google-pixel-4a-pixel-5-prices-survery/)相吻合，该调查询问用户他们更喜欢 349 美元的 Pixel 还是 699 美元的“高级”Pixel 智能手机。699 美元的价格比以前的旗舰 Pixel 设备便宜，如果没有骁龙 865 ，[将是有意义的。](https://www.xda-developers.com/5g-push-unintentionally-killed-flagship-killer-this-year/)

除了处理器的传言，关于谷歌 Pixel 5 的其他信息并不多。上述意见奖励调查提到无线充电和防水是“优质”像素的特点。Android 11 代码[似乎也在暗示](https://www.xda-developers.com/android-11-battery-share-reverse-wireless-charging-pixel-5/)至少有一款 Pixel 5 设备(redfin)将支持*反向*无线充电。在可能于秋季推出之前，还有大量时间来了解更多关于该设备系列的信息。*