# Galaxy Note 20、Galaxy Fold 2 和 Project Zodiac 的内核代码提示

> 原文：<https://www.xda-developers.com/samsung-galaxy-s20-kernel-galaxy-note-20-galaxy-fold-2/>

在 Galaxy S20 系列的[发布](https://www.xda-developers.com/samsung-galaxy-s20-specs-features-pricing-availability/)几周后，三星发布了 Exynos 和骁龙 S20、S20+和 S20 Ultra 的[内核源代码](https://www.xda-developers.com/samsung-galaxy-s20-kernel-source-code-available-exynos-models/)。在骁龙 Galaxy S20 的内核源代码中，我们发现了我们认为是指三星 Galaxy Note 20 和采用骁龙 865 SoC 的 Galaxy Fold 2 的参考资料。我们还发现了一个神秘的新装置，叫做“十二宫杀手”项目。

我们能够在 Galaxy S20 内核源代码中找到五种不同设备和三个不同系列的文件。这些项目是“XYZ 项目”、“画布项目”和“赢家项目 2”Project XYZ 是 Galaxy S20 系列:Galaxy S20 是 x1，Galaxy S20+是 y2，S20 Ultra 是 z3。Project Canvas 很可能是即将发布的三星 Galaxy Note 20 系列，[正如 Ice Universe](https://twitter.com/UniverseIce/status/1235197069511364608?s=20) 所暗示的。我们能够找到“c2”，但很可能会有 2 个以上的设备，“c0”和“c1”，但我们现在不能确认这些存在。最后，还有项目赢家 2。鉴于第一个银河折叠是“项目赢家”，这很可能是银河折叠 2。 *[GalaxyClub](https://www.galaxyclub.nl/nieuws/codenaam-opvolger-samsung-galaxy-fold-is-een-open-deur-met-5g/)* 上个月也报道了这个代号。有传言称 Galaxy Fold 2 的代号为“ [champ](https://www.xda-developers.com/samsung-galaxy-fold-2-rumored-launch-under-screen-camera/) ”，但这可能是三星正在开发的一款不同的可折叠设备。

三星在三星 Galaxy Note 20 和 Galaxy Fold 2 中使用[高通骁龙 865](https://www.xda-developers.com/qualcomm-snapdragon-865-processor-specifications-features/) 的事实并不令人惊讶。三星已经在 Galaxy S20 系列手机中使用了骁龙 865，三星在 Galaxy Fold 继任者中使用它才有意义，因为第一款机型已经使用了骁龙 855。我们能够确认这些芯片的用途，因为“科纳”的代号指的是骁龙 865。我们可以在代码中看到,“winner2”和“canvas”都是基于“kona”也就是骁龙 865。

几个“Kconfig”文件详细描述了三星已经发布或将发布的骁龙 865 设备。它们包括“Kconfig.winner2”、“Kconfig.canvas”和“Kconfig.xyz”。这些文件中的每一个都存储特定设备和受支持区域的项目文件。比如 Galaxy S20 系列就存储在“Kconfig.xyz”文件中。在文件中，我们可以看到 Galaxy S20 的骁龙版本在韩国、美国、加拿大、中国和日本有售。对于“canvas”，该文件只显示了美国，这意味着骁龙 Galaxy Note 20 将只在美国上市。但请记住，这仍处于开发的早期阶段，因此我们预计这种情况会发生变化。对于“winner2”，我们只看到欧洲公开市场的配置。

与此同时，在三星 Galaxy Z Flip 的内核源代码中，我们发现了一款基于高通骁龙 855 的名为“十二宫计划”的新设备。该设备将在中国上市，因为这是唯一提到的地区。很可能“十二宫杀手计划”将是一款只面向中国的手机，但不幸的是，我们目前没有关于这款手机的更多信息。

这些泄漏让我们对今年晚些时候有所期待，假设没有因为正在进行的新冠肺炎疫情而出现重大延误。在接下来的几个月里，有很多设备准备推出，我非常兴奋。