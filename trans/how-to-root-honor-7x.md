# 如何解锁 Bootloader 并 Root 荣誉 7X

> 原文：<https://www.xda-developers.com/how-to-root-honor-7x/>

# 如何解锁 Bootloader 并 Root 荣誉 7X

Honor 7X 采用 18:9 显示屏，分辨率为 1080 x 2160p。

在你可以根你的[荣誉 7X](http://www.hihonor.com/global/products/mobile-phones/honor7x/index.html?utm_source=forum7x&utm_medium=MediumBuy&utm_campaign=201712_honor7x_lauch&utm_term=ad) 或安装一个自定义恢复，你会想要解锁你的引导加载程序。在本教程中，我们将向您展示如何为您的设备获取解锁代码，以及如何使用 ADB 解锁您的引导加载程序。

首先备份你的数据。解锁引导加载程序将擦除你的荣誉 7 倍的数据。

## 获取您的解锁代码

*   转到这个网站并创建一个帐户
*   转到下载>解锁引导程序
*   用****IMEI****产品代码****型号** 填写表格**
***   您的解锁代码将显示在同一页，在表格的底部**

 **## 打开 USB 调试和 OEM 解锁

*   以你的名誉担保 7X:
*   前往设置>关于
*   轻击 **构建号** 七次
*   转到开发者选项
*   勾选 **启用 OEM 解锁**
*   检查 **USB 调试**

## 通过 ADB 解锁

如果你还没有安装 ADB，请看[这个](http://forum.xda-developers.com/showthread.php?t=2588979)线程的说明。

*   通过 USB 将手机插入电脑
*   键入命令 **' adb 重新启动引导加载程序 '** 并按回车键。
*   一旦进入引导模式，输入 **' 快速启动 oem 解锁【解锁代码】 '**
*   按照屏幕上的说明操作

 <picture>![](img/461a95414b6f929f038a2424f31652f7.png)</picture> 

This warning will show on your screen when booting your device, once your bootloader has been unlocked.

如果你在手机重启时看到这个警告，那么你已经做了所有正确的事情。

# 根你的荣誉 7X

在[的论坛上大声喊出来](https://forum.xda-developers.com/honor-7x/development/how-to-root-honor-7x-international-t3716056)。

## 下载 TWRP 和 SuperSU

*   在这里获得 7X TWRP [的荣誉](https://androidfilehost.com/?fid=962021903579497006)
*   在这里获得超 SU
*   将 TWRP 文件放入您的亚行文件夹中
*   将 SuperSU 文件放在您的 sd 卡上

## 通过 ADB 发送 Flash

*   重置后重新打开 USB 调试
*   通过 USB 将手机插入电脑
*   键入命令 **' adb 重新启动引导加载程序 '** 并按回车键。
*   一旦进入引导模式，输入 **' 快速启动快速恢复 twrp_Honor_7x.img '**
*   一旦完成，输入'**'**
***   重启后，拔掉你的手机并关机*   按住电源+音量以启动 TWRP*   滑动以允许修改*   转到安装>选择 SuperSU 文件*   滑动到闪光灯*   擦除 Dalvik 缓存，然后重新启动**

 **你现在扎根了。您可以使用根检查器应用程序来验证您已经正确完成了所有工作。

[第四段]

 <picture>![](img/5d68e374cc9fd52c63ab5975c9a68bb9.png)</picture> 

Get rid of ads with AdAway once your have root access on the Honor 7X

[/第四段][第四段]

 <picture>![](img/7ad39f0f81e432ce2dd60afd21dbf5d9.png)</picture> 

Remove bloatware and uninstall system apps

[/第四段][第四段]

 <picture>![](img/f143a126c34b63e59de8c49e69736999.png)</picture> 

Get custom themes with Substratum theme engine

[/第四段][第四段]

 <picture>![](img/a4af83fe0c735c93cddff6d12b38ae20.png)</picture> 

Use a root checker to verify root access

[/第四段]

XDA 正与麒麟开发者密切合作，为社区开发一些定制的 rom。Honor 最近发布了 7X 的内核源代码，这将加速该设备的开发。请继续关注更多的开发新闻，或者关注论坛的未来更新。

[***了解为什么 XDA 将 Honor 7X 评为 2017 年最佳经济型手机。***](https://www.xda-developers.com/best-budget-phone-of-2017/)

[**荣誉 7X 社区论坛**](https://forum.xda-developers.com/honor-7x)****