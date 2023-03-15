# 在 Android 上保存 IMEI 号码的指南

> 原文：<https://www.xda-developers.com/guide-to-imei-numbers-and-preserving-them-on-android/>

你好奇 IMEI 代表什么吗？你想学习如何解释部分的 IMEI 号码，以了解更多的设备吗？XDA 资深会员 [xsenman](http://forum.xda-developers.com/member.php?u=4586061) 写了一本 IMEI 号码指南，旨在解释所有这些，以及如何在 ROM 闪存期间在你的手机上保存它们的细节。

IMEI 代表“国际移动设备身份”，是唯一标识每部移动电话的 15 位数字。因为它们是独一无二的，所以可以用来追踪被盗手机，或者阻止运营商访问任何设备。在大多数地区更改 IMEI 号码是非法的，因此保存您的 IMEI 号码极其重要。

虽然 IMEI 号码存储的区域在大多数手机上都是受保护的，但许多三星设备都将其保存在 EFS 分区中，这很容易通过根手机访问。这就是为什么有机会，而闪存到您的设备，你可能最终搞乱了 EFS 分区，从而失去了你的 IMEI 号码。

想了解更多关于 IMEI 号码的信息，关于它们的数字代表什么的完整描述，以及如何在你的手机上保存它们的细节，请前往[论坛主题](http://forum.xda-developers.com/showthread.php?t=1857054)。该线程还链接到验证器，用于检查 IMEI 号码是否有效或被列入黑名单，以及其他一些有用的线程，指导您修复可能影响您的 IMEI 号码的 EFS 相关问题。