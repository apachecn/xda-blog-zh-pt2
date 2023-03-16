# 高通骁龙 855 已获得 EAL4+认证

> 原文：<https://www.xda-developers.com/qualcomm-snapdragon-855-secure-processing-unit-eal4/>

当高通在 2017 年 12 月宣布骁龙 845 时，该公司宣传了 SoC 的新[安全处理单元](https://www.xda-developers.com/qualcomm-snapdragon-845-secure-processing-unit/) (SPU)。SPU 是一个片上安全元件，用于保护生物特征、支付信息和 SIM 数据。高通最新的旗舰 SoC,[骁龙 855](https://www.xda-developers.com/qualcomm-snapdragon-855-kryo-485-cpu-adreno-640-gpu-spectra-isp-cv/) 也有 SPU，但 6 个多月后，高通宣布 SPU 已获得 EAL4+认证。这意味着每一台配备高通最新芯片组的设备，即使是目前可用的智能手机，如[华硕 ZenFone 6](https://forum.xda-developers.com/zenfone-6-2019) 、[一加 7 Pro](https://forum.xda-developers.com/oneplus-7-pro) 、美国[三星 Galaxy S10](https://forum.xda-developers.com/galaxy-s10) 和[小米 Mi 9](https://forum.xda-developers.com/Mi-9) ，都将能够实现新的功能，尽管它们缺乏独立的安全模块。

## 通用标准和评估保证级别

[信息技术安全评估通用标准](https://www.commoncriteriaportal.org)，通常简称为 CC，提供了评估产品安全性的标准。CC 的[评估保证级别](https://www.commoncriteriaportal.org/files/ppfiles/pp0084a_pdf.pdf) (EAL)是产品可以获得的认证，以提供这些产品满足最低安全级别的有意义的保证。较高的 EAL 意味着产品接受了更高水平的审查，适合更安全的交易。虽然 EAL 升至 7 级，但第 4 级是“对现有产品线进行改造在经济上可能可行的最高级别”，也是大多数智能卡和嵌入式安全元件获得认证的级别。高通表示，通过获得 EAL4+安全认证，骁龙 855 是“首款移动 SoC”...以获得智能卡级别的安全保证。SPU 由一个独立的权威机构进行评估:德国[联邦信息安全办公室](https://www.bsi.bund.de/EN/Home/home_node.html)(德语，Bundesamt für sicher heit in der informations technik，或 BSI)。

## EAL4+认证和骁龙 855

获得 EAL4+认证的安全处理单元之所以重要，有两个原因:减少 OEM 的物料清单，以及未来新功能的机会。在前一种情况下，购买骁龙 855 的原始设备制造商可以通过不必集成单独的安全元件来节省资金，例如谷歌与 [Pixel 3 的 Titan M](https://www.xda-developers.com/google-pixel-3-titan-m-security/) 的情况。由于 SPU 现已通过 EAL4+认证，原始设备制造商可以放心，该 SoC 足够安全，可用于敏感交易，如[在 Android R](https://www.xda-developers.com/google-android-digital-drivers-license/) 中存储数字驾驶执照。此外，由于 SPU 是片上的，这意味着它采用相同的 TSMC 7 纳米工艺技术制造，与其他分立安全模块相比，SPU 具有较小的能效优势。

凭借 EAL4+认证，骁龙 855 的 SPU 可用于未来的额外安全交易。目前，SPU 参与了针对[Android strong box key master](https://developer.android.com/training/articles/keystore#HardwareSecurityModule)和[网守子系统](https://source.android.com/security/authentication/gatekeeper)的硬件支持的密钥认证。在 Android 9 Pie 中引入的 [StrongBox Keymaster](https://www.xda-developers.com/android-p-privacy-updates/) 实现允许安全交易，例如通过胰岛素泵验证胰岛素的管理。在上海世界移动通信大会上，高通将与数字安全公司[金雅拓](https://www.gemalto.com/)合作展示集成 SIM 卡(iSIM)。iSIM 将被集成到高通骁龙 855 SoC 中，它可以处理多个虚拟 SIM 卡配置文件之间的切换。

未来，我们可能会看到“离线支付、可信平台模块(TPM)功能、公交、电子身份证和加密钱包”等用例存储加密货币钱包是我们在[三星 Galaxy S10](https://www.xda-developers.com/samsung-galaxy-s10-blockchain-keystore-cryptocurrency-wallets/) 和 [HTC 的区块链手机](https://www.xda-developers.com/htc-5g-hub-second-gen-blockchain-phone/)上看到的一项功能，但由于 SPU 的 EAL4+认证，这项功能将有可能用于更多设备。电子身份证支持是谷歌[正在为下一版本的 Android](https://www.xda-developers.com/google-android-digital-drivers-license/)积极工作的东西，高通骁龙 855 的 SPU 应该满足这个 API 的要求，以安全地存储电子身份证。

 <picture>![](img/d43ba2ce0cf0045d9b35518d04325b52.png)</picture> 

A sample image of a digital driver's license accessed through the LA Wallet app. Source: Envoc

我向高通询问了对 IdentityCredential API 的支持，特别是 SPU 是否会支持“直接访问”模式，这种模式将允许用户在不完全启动 Android 的情况下调出电子 id，我收到了高通发言人的以下声明:

> #### “我们目前不支持在骁龙 855 的 SPU 上使用此 API，但我们正在考虑在未来支持它。”

因此，今天的公告只是未来的预览。EAL4+认证只是确保硬件能够抵御许多潜在的攻击和漏洞。原始设备制造商、谷歌和开发人员如何利用这种保证取决于他们自己。希望我们能看到这种安全的硬件在新的用例中得到利用，这些用例我们还没有在市场上看到过。许多医疗和金融服务可能会受益，但这些行业的参与需要时间。