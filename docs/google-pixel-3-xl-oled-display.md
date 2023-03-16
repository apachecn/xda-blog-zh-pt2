# 谷歌 Pixel 3 XL 使用三星的有机发光二极管显示屏

> 原文：<https://www.xda-developers.com/google-pixel-3-xl-oled-display/>

三星在智能手机和电视的有机发光二极管面板制造领域占据主导地位，但最近，LG 缩小了两家韩国公司之间的差距。谷歌 Pixel 2 的显著特点是 LG 制造的 P-OLED 面板，我们在我们的评论中高度赞扬了[。三星、LG，甚至索尼都加大了努力，推出市场上最好的移动有机发光二极管显示器:三星推出了](https://www.xda-developers.com/pixel-2-xl-xda-display-analysis/) [Galaxy Note 9](https://www.xda-developers.com/samsung-galaxy-note-9-specs-pricing-availability-features/) ，LG 推出了 [V40 ThinQ](https://www.xda-developers.com/lg-v40-thinq-lg-watch-w7-announced/) ，索尼推出了 [Xperia XZ3](https://www.xda-developers.com/sony-xperia-xz3-specs-renders-pricing-availability/) 。随着谷歌 Pixel 3 XL 的发布，你可能会想知道谷歌是从哪家公司采购有机发光二极管面板的。原来，这是三星制造的面板。

在评估 Pixel 3 XL 时，我发现了一个名为`qdcm_calib_data_S6E3HA8_ 6.3_command_mode_panel.xml`的校准文件，它引用了三星 Galaxy S9 系列中使用的同一款三星 DDIC。文件名中的 6.3 与 Pixel 3 XL 上的 6.3 英寸显示屏相匹配。还有一个三星 S6SY761 触摸屏数字化仪的固件文件。

今年的谷歌 Pixel 3 与前两代相比有很大不同。谷歌 Pixel 的 ODM 是 HTC，用于常规和 XL 型号，而 Pixel 2 的 ODM 分别是 HTC 和 LG，用于常规和 XL 型号。在收购了为谷歌 Pixel 工作的 HTC 工程师后，谷歌决定完全在内部开发 Pixel 3 和 Pixel 3 XL [并利用富士康的工厂进行制造。有](https://www.xda-developers.com/google-pixel-3-xl-foxconn-dual-front-camera-lenses-verizon-exclusive/)[早期传言](https://www.xda-developers.com/google-pixel-3-xl-notched-oled-lg/)谷歌将从 LG Display 为 Pixel 3 XL 采购开槽有机发光二极管面板，但谷歌和 LG 都没有在发布时证实这一消息。感谢 *[iFixit 的](https://www.ifixit.com/Teardown/Google+Pixel+3+XL+Teardown/113656)* 彻底拆卸 Pixel 3 XL 的显示屏，我们现在可以肯定地确认，我们必须归功于三星制造了出色的显示屏(当然，谷歌工程师校准得如此之好！)

我们有望在不久的将来对 Pixel 3 XL 进行自己的显示分析。目前，我们可以分享一些我们对这款设备的亲身体验。

## 谷歌 Pixel 3 和 Pixel 3 XL 显示屏的初步印象

以下部分由我们的展示分析师 Dylan Raga 撰写。

相对于像素 2 XL，谷歌像素 3 和谷歌像素 3 XL 显示屏的改进令人印象深刻。纯色看起来明亮、墨色，不再像像素 2 XL 那样有颗粒状外观。没有纹理也有助于文本和曲线看起来更清晰和平滑。像素 2 XL 显示器的一个不太为人知的问题是，顶部玻璃感觉是中空的，显示器本身似乎凹陷了进去。在谷歌像素 3 和谷歌像素 3 XL 上，有机发光二极管的叠层现在更靠近顶部玻璃，当按下时，允许屏幕元素看起来更靠近您的指尖，并增强触摸屏幕的感觉。像素 3 家族也选择放弃像素 2 XL 的 3D 玻璃曲线，这可能会导致它的中空显示，因为他们缺乏使用实际弯曲的“3D 玻璃”的经验。像素 3 和像素 3 XL 的大部分单位的角度色移也有很大改善，属于旗舰有机发光二极管的可接受范围。较小的像素 2(通常被接受作为高级显示面板的外壳)未表现出上述任何问题。然而，就像去年一样，今年的谷歌像素 3 和谷歌像素 3 XL 在这两个显示面板之间似乎有不同的特点。

在亮度方面，Pixel 3 的全屏(100% APL)亮度与 Pixel 2 XL 的相似(因此比较小的 Pixel 2 更亮)，Pixel 3 XL 略微但明显地超过了两者。 [*Android Central*](https://www.androidcentral.com/google-pixel-3-addresses-pixel-2-display-woes) 声称，谷歌 Pixel 3 和谷歌 Pixel 3 XL 显示器的全屏图像最低达到 400 尼特，然而，[我们测量了 Pixel 2 和 Pixel 2 XL](https://www.xda-developers.com/pixel-2-xl-xda-display-analysis/) 的全屏图像，已经达到了更高的水平，因此 400 尼特的最低值并不值得大书特书。

显示校准是大部分显示差异出现的地方。从经验上看，自然屏幕颜色模式下的谷歌 Pixel 3 XL 显示器校准看起来非常出色，可以与苹果最新的 iPhone 显示器校准相媲美。Pixel 2 XL 显示器具有近乎完美的色度校准，但明显超过了其显示伽玛，导致色调过暗。谷歌 Pixel 3 XL 在显示屏伽玛上有了显著改善，伽玛似乎非常接近 2.20 的预期目标，颜色仍然非常准确。但是，像素 3 似乎没有得到同样的改善；色调看起来仍然有点太暗，显示器伽马视觉上在大约 2.40 附近，如 Pixel 2 XL (2.42)。

谷歌去年因其 2017 年旗舰手机的颜色配置文件以准确的颜色为目标而受到严厉批评，这是大多数 Android OEMs 厂商不再遵循的决定，也是苹果一直为其手机所做的决定。Pixel 2 XL 校准并不完美，但许多人认为颜色配置文件导致了劣质面板。许多 Android 用户习惯于 OEM 厂商随其显示器提供的强烈、过度饱和的颜色配置文件，三星手机就是最臭名昭著的例子，它提供了自适应显示器配置文件。对于 Pixel 3 和 Pixel 3 XL，谷歌屈服了，将 Pixel 3 和 Pixel 3 XL 的显示面板默认为新的自适应颜色模式，谷歌迄今为止尚未透露太多信息。一眼看去，两款手机的配置文件实际上是**不同的**。对于谷歌 Pixel 3 XL，配置文件似乎类似于三星的自适应显示屏模式。然而，较小的谷歌 Pixel 3 具有自适应配置文件，非常类似于谷歌 Pixel 2 XL 中的饱和屏幕模式。谷歌 Pixel 3 在这种模式下明显比其更大的版本更饱和。

该显示器的其他方面还有待评估。