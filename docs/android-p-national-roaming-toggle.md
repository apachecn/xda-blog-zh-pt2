# 几年前的 Android 问题将最终通过国家漫游切换得到解决

> 原文：<https://www.xda-developers.com/android-p-national-roaming-toggle/>

Android 是一个功能丰富的移动操作系统，但这并不意味着它没有问题。相反，几年前发现的操作系统中的一些问题仍然没有得到解决，而新问题会在新版本中出现。一个众所周知的问题是缺乏对全国漫游的支持。

## 问题是

一些运营商和移动虚拟网络运营商(MVNO)要求启用数据漫游，以便在网络和设备之间进行任何数据传输。这是因为 Android 检测到设备正在漫游，而实际上它并没有。这是什么时候发生的？在极少数情况下，以 MCC 和 MNC 代码以及 IMSI 的形式存储在 Android 中的运营商数据会出现不匹配。

移动国家代码(MCC)与移动网络代码(MNC)结合使用来唯一地标识移动网络。另一方面，国际移动订户身份(IMSI)用于识别移动网络的*用户*，并且是与所有移动网络相关联的唯一标识。

一些 MVNOs 没有与母公司相同的 IMSI。因此，Android 将 MVNO 识别为一个独立的网络，不同的 imsi**让 Android 看起来好像设备正在漫游**，即使它不是。

结果是，用户打开数据漫游开关，让移动数据工作，认为他们不会被收费。然而，一旦他们出国旅行，他们手机的 SIM 卡就会锁定当地运营商的信号(如果有必要的漫游协议的话)。然后，用户因使用数据漫游而被收费，并且在许多情况下被收取过高的费用。

这是因为用户无意中启用了数据漫游开关。当在一个国家境内使用时，它不会产生费用，但一旦 SIM 卡在国际上使用，用户就必须支付漫游费，即使他们不想使用漫游 SIM 卡。

在欧盟，[国际漫游](https://europa.eu/youreurope/citizens/consumers/internet-telecoms/mobile-roaming-costs/index_en.htm)不收费，这一变化从 2017 年 6 月 15 日开始生效。(当然，这是有附加条件的，比如合理使用政策和有条件的数据限制。)这意味着当移动网络用户在欧盟范围内漫游时，没有漫游费。

用户因此可以启用数据漫游，并在旅行时忘记它，但这将是一个坏主意，因为无论何时他们在欧盟以外旅行，那么国际漫游费**将** **适用。** [谷歌问题追踪器](https://issuetracker.google.com/issues/65279063)上的用户也报告称，如果设备无法连接到任何国家网络，即使在欧盟境内也适用卫星漫游费——例如，在海上这是常见的情况。

## 解决方案

这里的解决方案是**全国漫游切换**。国家漫游开关将使用户能够在国内使用时保持漫游，但将确保未经用户同意，不会在用户的国家之外使用**漫游。这是[用户在近八年半前](https://issuetracker.google.com/issues/36908687)就已经向谷歌提出的问题，但这个问题没有任何进展。唯一的修正包括[安装一个暴露的模块](https://forum.xda-developers.com/xposed/modules/xposed-national-roaming-t2420249)以获得一个全国漫游选项，[修改 framework-res](https://forum.xda-developers.com/elephone-p8000/development/mod-remove-roaming-home-network-t3206004) (这只能在某些手机上完成)，或者安装某些定制的 rom。**

*运行 Android 8.1 Oreo 的谷歌 Pixel 2 XL 上的漫游设置*

这有望很快改变，因为索尼正在创作必要的承诺以增加对国内漫游的支持以及对 Android 中国内漫游 UI 的支持。当这个选项出现在 Android 中时(最有可能出现在 [Android P](https://www.xda-developers.com/android-p-signal-strength-carriers/) 中)，它将为国际旅行者带来巨大的好处，因为他们不必每次在前往国际旅行之前都记得关闭数据漫游。

* * *

**P.S.** 上图截图展示的是[赛的奥利奥黑暗主题](https://play.google.com/store/apps/details?id=baka.sai.oreo&hl=en)，使用 Substratum 安装。你可以按照这个步骤安装没有根[的黑暗主题。](https://www.xda-developers.com/install-dark-theme-android-oreo-without-root/)