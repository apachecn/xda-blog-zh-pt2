# 11 月的更新使 90Hz 平滑显示器在 Pixel 4 和 Pixel 4 XL 上的表现有所不同

> 原文：<https://www.xda-developers.com/november-update-makes-90hz-smooth-display-behave-differently-pixel-4-pixel-4-xl/>

# 11 月的更新使 90Hz 平滑显示器在 Pixel 4 和 Pixel 4 XL 上的表现有所不同

2019 年 11 月 Pixel 4 设备的安全更新包括对 90Hz 平滑显示器的更改，以提高在更多亮度条件下的性能。

上个月末，我们了解到 Pixel 4 的显示屏[会根据显示屏的亮度自动在 90Hz 和 60Hz 刷新率](https://www.xda-developers.com/google-pixel-4-90hz-display-only-works-at-high-brightnesses/)之间切换。我们的主编[米沙·拉赫曼](https://www.xda-developers.com/author/mishaalrahman/)证实，当亮度低于 77%时，Pixel 4 的 90Hz 平滑显示会自动调低至 60Hz。虽然我们确实找到了一种在开发人员选项中强制 90Hz 刷新率的方法，但这不是最理想的解决方案，因为它会影响电池寿命。披露后不久，谷歌发布了一份声明，声称它已经在进行更新，以在更多亮度条件下实现 90Hz 的刷新率。这些更新现在正与 2019 年 11 月的[安全补丁](https://www.xda-developers.com/november-2019-android-security-patches/)一起进入 Pixel 4 和 Pixel 4 XL。

更新之后，在更多情况下，这两款设备上的显示器将坚持 90Hz 的刷新率。然而，这两个设备将表现出不同的行为。每当显示器亮度高于 42%时，像素 4 将切换到 90Hz，并且环境亮度水平对刷新率没有影响。另一方面，像素 4 XL 将坚持 90Hz，而不管显示器或环境亮度如何。这种行为差异很可能可以归结为谷歌希望在较小的 Pixel 4 上节省电池寿命。但是，您仍然可以在开发者选项中启用“强制 90Hz”模式来避开显示器亮度触发。

值得注意的是，这些变化导致了 Pixel 4 XL 的另一个问题。由于该设备现在将在更多的情况下以 90Hz 运行，显示器伽马错误现在更加明显。因此，当您关闭和打开显示器时，它会应用错误的伽玛表，显示器看起来对比度很高，并向洋红色调偏移。