# 谷歌 Pixel 2 XL 充电速度功能上限为 10.5W

> 原文：<https://www.xda-developers.com/google-pixel-2-xl-charging-speed-functionally-capped/>

很长一段时间以来，消费者似乎认为随着智能手机电池容量的增加，充电时间自然也会增加。为了解决这个问题，许多公司研究了各种快速充电的方法。这些年来，我们已经看到了各种标准的兴起，例如 USB 电源传输、高通快速充电、三星的自适应快速充电、华为的 SuperCharge 和一加的 Dash 充电等等。

然而，不同智能手机的充电实现方式有所不同。手机 A 和手机 B 使用高通快充 3.0 并不意味着它们的充电速度相当。事实上，手机的充电时间取决于许多因素，除了使用充电标准。

[我们比较了不同的充电标准](https://www.xda-developers.com/charging-comparison-oneplus-huawei/)，发现一加手机上的 Dash 充电和华为手机上的 SuperCharge 在充电速度、热性能和效率方面表现最佳。在我们的比较中，我们注意到 Pixel XL 充电缓慢，充电速度与其他设备相比没有竞争力，尽管额定功率高达 18W。这不是因为 USB-PD 中的任何故障，而是因为电压已经被封顶的事实。

现在，在 [*内森·k .*](https://plus.google.com/102612254593917101378)的一份新报告中，人们发现新的 [Pixel 2 XL](https://www.xda-developers.com/google-pixel-2-xl-announced-price/) 也有类似的局限性。严格来说，这不是一个“问题”，但这绝对是不诚实的营销，[增加了设备的问题清单](https://www.xda-developers.com/google-pixel-2-xl-warranty-color-mode/)。

*Nathan K.* 对 Pixel 2 XL 进行了充电测试，并在 Google+上分享了他的结果。他的报告提到，谷歌 Pixel 2 XL 的充电速度比预期的慢。用户已经评论说，他们觉得他们的 Pixel 2 XL 设备充电速度不够快，他们的经历现在得到了证实。

Pixel 2 XL 配有一个墙上适配器，具有广告宣传的容量，可以用高达 18W 的电流为手机充电。但是在瓦数-温度图中，没有充电器消耗 18W 电流的情况。开始时瓦数约为 15W，但几分钟内就降到略高于 10W。Pixel 2 XL 继续以此速度充电，直到循环开始约 50 分钟，然后开始逐渐减速，直到循环结束，充满电(从 15%的电池)需要 2.5 小时。最高温度记录为 32.6 摄氏度。

*Nathan K.* 注意到第一代谷歌 Pixel 使用了多级锂离子快速充电:三级恒流，然后是最后的恒压级。然而，Pixel 2 XL 使用单级恒流，随后是恒压。

他认为，Pixel 2 XL 充电速度慢的原因是谷歌和 LG 试图避免给电池带来压力，以最大限度地延长电池寿命。制造商没有选择性能，而是“对充电电流和温度极其保守”。这样做可以避免 Nexus 6P 面临的电池退化问题。

最后，他指出，5 英寸的谷歌 Pixel 的最高充电功率也是 15 瓦，而不是宣传的 18 瓦。谷歌 Pixel 较小的电池(2770 毫安时)证明了这种瓦数差异的合理性。“有了 Pixel 2 XL，差别就大了很多。

目前，还不知道谷歌对这一新发展的回应是什么。

[**来源:Google+:内森 K.**](https://plus.google.com/102612254593917101378/posts/dnYcjUFxsg7)