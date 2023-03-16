# 三星 Galaxy Tab S5 可能有高通骁龙 855

> 原文：<https://www.xda-developers.com/samsung-galaxy-tab-s5-snapdragon-855-leak/>

三星的可折叠智能手机三星 Galaxy Fold 将于下个月发布，该手机配备了一个 [Infinity Flex](https://www.xda-developers.com/samsung-foldable-phone-infinity-flex/) 显示屏。它有两个显示屏——一个覆盖显示屏用于基本的电话使用，另一个主显示屏可展开，为您提供平板电脑体验。这款设备的价格对大多数消费者来说将是[遥不可及的](https://www.xda-developers.com/samsung-galaxy-fold-specifications-pricing-availability/)，但是如果你正在寻找一款高端平板电脑，我们有一些令人兴奋的消息要分享。我们挖掘了即将发布的三星 Galaxy Fold 的固件转储，我们发现了一个我们认为可能是三星 Galaxy Tab S5 的引用。更好的是，它可能会推出旗舰高通骁龙 855 移动平台。

在三星 Galaxy S10 推出前几周，三星公布了[三星 Galaxy Tab S5e](https://www.xda-developers.com/samsung-galaxy-tab-s5e-amoled-tablet/) 。这是一款配有高通骁龙 670 的中档平板电脑，但三星给了它一个像样的 10.5 英寸 Super AMOLED 显示屏，四 AKG 调谐环绕声扬声器，一个基于 Android 9 Pie 的 UI，等等。这款设备被称为 Galaxy Tab S5 **e** ，因为与 Galaxy S10e 一样，它是一款以较低价格为消费者提供必需品的产品。足够好的显示屏、足够好的处理器、足够大的存储空间等等。

如果你认为 Galaxy Tab S5e 是 Galaxy Tab S4 的继任者，那么你可能会感到失望。三星在 Galaxy Note 9 发布前一周推出了 Galaxy Tab S4。Galaxy Tab S4 是三星最新的旗舰 Android 平板电脑，尽管对于 2018 年的旗舰 Android 平板电脑来说，它与 2017 年的旗舰移动平台高通骁龙 835 搭配令人失望。虽然[仍然是市场上最好的安卓平板电脑](https://www.xda-developers.com/samsung-galaxy-tab-s4-review/)，但许多人感到失望的是，最好的安卓平板电脑甚至没有当时市场上最好的 SoC。三星可能会通过 Galaxy Tab S5 来纠正这一点，因为我们发现的代码表明这款 2019 年的平板电脑将有一个 [2019 年旗舰 SoC](https://www.xda-developers.com/qualcomm-snapdragon-855-kryo-485-cpu-adreno-640-gpu-spectra-isp-cv/) 。

我们的消息来源从他们的三星 Galaxy 文件夹中提取了一个 Linux 内核配置文件 defconfig。该文件列出了许多不同的三星制造的高通骁龙 855 设备的代号。以下是每个代号的描述:

*   Beyond0QLTE -三星 Galaxy S10e(骁龙)
*   Beyond1QLTE -三星 Galaxy S10(骁龙)
*   Beyond2QLTE -三星 Galaxy S10+(骁龙)
*   WinnerLTE_USA_SINGLE -三星 Galaxy Fold(美国-运营商？)
*   WinnerLTE_USA_OPEN -三星 Galaxy Fold(美国-解锁？)
*   WinnerLTE_CAN_SINGLE -三星 Galaxy Fold(加拿大-运营商？)
*   winner LTE _ KOR _ SINGLE-Samsung Galaxy Fold(韩国)
*   WinnerLTE_CHNZC -三星 Galaxy Fold(中国大陆？)
*   WinnerLTE_CHNHK -三星 Galaxy Fold(香港)
*   WinnerLTE_DCM -三星 Galaxy Fold(日本- NTT Docomo)
*   KDI 温纳尔特-三星 Galaxy Fold(日本- KDDI)
*   WinnerLTE_EUR_OPEN -三星 Galaxy Fold(欧洲-解锁)。请注意，这一行没有被注释掉，因为我们的线人从欧洲 Galaxy Fold，SM-F900F 中提取了该文件，该文件的代号为 winnerlteeea，用于在欧洲经济区销售的 4g LTE Fold。
*   BoltQ5G - [5G 威瑞森调制解调器](https://www.xda-developers.com/samsungs-bolt-device-may-actually-be-a-5g-modem-for-verizon-powered-by-the-qualcomm-snapdragon-855/)
*   BeyondXQ - [5G 三星 Galaxy S10+](https://www.xda-developers.com/samsung-galaxy-s10-5g-verizon-europe/) (骁龙)
*   D2Q -未知的三星骁龙，但“d”很可能指的是“达芬奇”，这是三星 Galaxy Note 10 的代号。
*   5G model-5G 三星 Galaxy Fold

最后，还有“GTS5L”三星 Galaxy Tab S2 的代号是 GTS2，Galaxy Tab S3 的代号是 GTS3L，Galaxy Tab S4 的代号是 GTS4L。因此，三星 Galaxy Tab S5 的代号为“GTS5L”是有道理的。我们认为它可以在高通骁龙 855 上运行的原因是，我们拉的 defconfig 定义了内核配置，这个特定的配置适用于所有三星的骁龙 855 驱动的设备。三星所要做的就是取消 GTS5L 的注释行，并在为 Galaxy Tab S5 制作 defconfig 时选择其他参数。

虽然没有发布日期的传言，但如果去年的 Galaxy Tab S4 发布会是什么样的话，Galaxy Tab S5 应该比传闻中的无按钮三星 Galaxy Note 10(T1)早几周发布。

*特色图片:中端三星 Galaxy Tab S5e。*