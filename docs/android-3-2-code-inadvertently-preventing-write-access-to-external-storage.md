# Android 3.2+代码(无意中？)防止对外部存储器的写访问

> 原文：<https://www.xda-developers.com/android-3-2-code-inadvertently-preventing-write-access-to-external-storage/>

似乎谷歌在他们的 AOSP 代码中有一个错误，这个错误是在 Android 3.2 左右引入的，它影响了操作系统处理 USB 存储的方式，并可以阻止对 SD 卡和 USB 棒的写访问。XDA 精英公认的开发者、资深版主、[新闻撰稿人](http://www.xda-developers.com/android/google-announces-second-week-of-google-io-2012/)在他的[博客](http://www.chainfire.eu/articles/113/Is_Google_blocking_apps_writing_to_SD_cards_/)中总结了这个问题:

> 在过去，应用程序会请求“ *WRITE_EXTERNAL_STORAGE* 权限，这将授予对*所有*外部存储(用户/组“ *sdcard_rw* ”)的写访问权限。这显然已被更改为仅授予对*主*外部存储器的写访问权限。引入了第二个权限，称为“ *WRITE_MEDIA_STORAGE* ”，它将授予对其他外部存储的访问权限(用户/组“ *media_rw* ”)。
> 
> 问题是，第三方实际上不会被授予此权限，只有系统应用程序和设备制造商提供的应用程序通常会被授予此权限。也有例外，显然在一些设备上第三方应用程序会被授予这种权限，但根据 AOSP 的消息来源，他们当然不应该这样做。

在 Chainfire 调查这个问题时，他在 */system/vold/Volume.cpp* 中发现了一段代码，其中明确指出:

> if(primary storage){
> 
> //特殊情况下的**主 SD 卡**。
> 
> //为此我们授予对 SDCARD_RW 组的写权限。
> 
> GID = AID _ SD card _ RW；
> 
> } else {
> 
> //**对于二级外部存储我们把东西锁起来。**
> 
> GID = AID _ MEDIA _ RW；
> 
> }

在许多设备上，内部闪存被视为“主 SD 卡”然后，*真正的* SD 卡成为第二个外部存储器，并被锁定-由不可获得的“*写 _ 媒体 _ 存储*权限保护。

Chainfire 将他的问题提交给了 Android 开发者办公时间团队，他们于 4 月 11 日在 T2 的现场聚会上讨论了这个问题。不幸的是，在场的谷歌工程师无法提供任何真实的答案，因为这是一个复杂的问题，而且这个问题是在节目直播前一个小时才提出的。然而，他们已经承诺要弄清这个问题，并在晚些时候回复 Chainfire(和我们)。

此外，根据 Chainfire 的说法，这个问题实际上也存在于 SGS2 的 ICS 版本中，尽管三星“*使用非常丑陋的权限黑客*解决了这个问题:

你在这里看到的是三星*将 WRITE_MEDIA_STORAGE 权限搭载*到 WRITE_EXTERNAL_STORAGE 权限，因此应用程序不会遇到上述问题。

谷歌是否打算将连接的 SD 卡和 u 盘限制为第三方应用程序只读，还有待观察。然而，这确实产生了一个令人不安的想法:如果代码和附带的注释是谷歌对外部存储实施某种写保护的第一步，从而进一步限制我们的移动自由，会怎么样？我们只能希望这是一个真正的错误，因为自由是我们都避免黑暗面的原因之一。

【非常感谢 Chainfire 的提醒和帮助！]