# 面向印度的 Google Pay (Tez)准备增加黄金礼品选项

> 原文：<https://www.xda-developers.com/google-pay-tez-india-gold-gifting-option/>

[Google Pay](https://www.xda-developers.com/google-pay-tests-safetynet-status-protecting-online-purchases-pin/) 是谷歌的统一支付平台，但该公司也有一个名称相同但功能不同的应用程序供印度用户使用。这个[独有的 Google Pay 是以前的](https://www.xda-developers.com/google-for-india-event-announcements/) [Google Tez](https://www.xda-developers.com/google-tez-7-5-million-users-india/) 的更名，更名后该应用程序继续增加更多功能。该应用的材料主题重新设计正在进行中，现在谷歌正计划为支付应用添加黄金礼品选项。

面向印度的 Google Pay[于 2019 年 4 月](https://india.googleblog.com/2019/04/google-pay-launches-gold-buying-in.html)推出了购买黄金的选项。黄金在印度文化中占有特殊的地位，同样的情况也反映在印度是世界上第二大黄金消费国。谷歌与印度 MMTC-PAMP 公司合作，允许用户在谷歌支付(Google Pay)应用内购买 99.99%的 24k 黄金。用户可以购买任何价值的黄金，无论大小，这些黄金都以数字形式存储在 MMTC-PAMP 的黄金累积计划(GAP)中，并代表用户物理存储在安全的金库中。这些购买声称是 100%保险。

通过 Google Pay 帐户购买的黄金以数字形式出现在应用程序内的黄金金库中，这实质上是 GAP 帐户余额的可视化表示。已经购买的黄金可以随时在 Google Pay 中出售，价格据称每隔几分钟就会刷新一次。您也可以将您的[黄金实物交付给您](https://support.google.com/pay/india/answer/9380078?hl=en-GB&ref_topic=9181318)，尽管此功能仅在少数地方可用。

APK 拆卸通常可以预测应用程序未来更新中可能出现的功能，但我们在这里提到的任何功能都可能不会出现在未来的版本中。这是因为这些特性目前还没有在实时构建中实现，并且可能会被开发人员在未来的构建中随时引入。

[Google Pay(Tez)v 48 . 0 . 001 _ RC03](https://www.apkmirror.com/apk/google-inc/tez-a-new-payments-app-by-google/tez-a-new-payments-app-by-google-48-0-001_rc03-release/)包含新字符串，表明谷歌向前迈进了一步，允许用户互赠黄金。

```
 <string name="gold_gifting_description_hint">Add a personal note</string>
<string name="gold_gifting_gifting_subject">"Gift gold to %1$s"</string>
<string name="gold_gifting_milligram_quantity_symbol">%1$s mg</string>
<string name="gold_ui_gift_output_text">Worth %1$s based on current selling price.</string>
<string name="gold_ui_header_gift_title">How much gold to gift?</string> 
```

像往常一样，这一功能尚未在谷歌 Play 商店的最新版本的应用程序中上线。我们预计谷歌会在准备推出时正式宣布这项功能。虽然赠送黄金会变得更加容易，但请记住，赠送黄金在印度确实会产生税务影响。

* * *

*感谢 PNF 软件为我们提供了使用许可 [JEB Decompiler](https://www.pnfsoftware.com/?aid=xdadev) ，这是一款针对 Android 应用的专业级逆向工程工具。*