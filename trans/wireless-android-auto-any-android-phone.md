# 如何让无线 Android Auto 在非像素手机上工作

> 原文：<https://www.xda-developers.com/wireless-android-auto-any-android-phone/>

如果你想买一辆新车，内置的主机/信息娱乐系统很有可能支持苹果的 CarPlay 或谷歌的 Android Auto。如果是的话，那太好了！由于与 iPhone 或 Android 设备的集成，您将可以访问各种应用程序和服务。苹果自 iOS 9 以来就支持无线 CarPlay，但无线 Android Auto [要求](https://support.google.com/androidauto/answer/6348019?hl=en)你特别拥有一部 Nexus 5X/6P 或 Pixel 智能手机，并且居住在美国、加拿大或墨西哥。然而，正如许多 Redditors 发现的那样，在过去的几周里，设备要求可能已经悄然发生了变化。

谷歌在 2018 年 4 月首次推出了新的无线 Android Auto，但它只适用于运行至少 Android 8.0 Oreo 的 Nexus 和 Pixel 智能手机。2018 年 5 月，肯伍德的一份新闻稿[暗示](https://www.xda-developers.com/wireless-android-auto-android-p/)无线 Android Auto 将通过 Android 9 Pie 更新提供给非谷歌设备，但新闻稿悄悄更新，称谷歌仍在努力为 Android Auto 无线带来更广泛的兼容性。一年多后，谷歌可能终于打开了开关，支持非谷歌智能手机。

在/r/[AndroidAuto](https://www.reddit.com/r/AndroidAuto/comments/cncu28/wireless_android_auto_on_nongoogle_phones/)subreddit 上，Redditor /u/ [dingonugget](https://www.reddit.com/user/dingonugget) 发现他能够将他的[一加 7 Pro](https://www.xda-developers.com/tag/oneplus-7pro/) 与他的 [Kenwood Excelon DMX905S](https://www.kenwood.com/usa/car/excelon/dmx905s/) 售后主机配对。

在分享了他的方法后，许多 Redditors 发现他们自己的非谷歌智能手机能够无线使用 Android Auto。拥有 Honor 9、三星 Galaxy Note 8、三星 Galaxy S10、LG V40 ThinQ 和一加 6T 等智能手机的 Redditors 报告了成功，许多人使用了不同制造商的售后主机。Reddit 线程的 OP 编译了设备和设备成功配对的主机的列表:

1.  一加 7 Pro 带建伍 Excellon DMX905S
2.  华为荣誉 9 w/先锋 W4400NEX
3.  三星 Galaxy Note 8 w/先锋 W4400NEX
4.  三星 Galaxy S10+w/Kenwood Excellon DMX 905s
5.  三星 Galaxy S8 w/Kenwood Excellon DMX 905s
6.  三星 Galaxy S10+ w/先锋 AVIC-W8400NEX
7.  LG V40 ThinQ 带先锋 AVIC-W8400NEX
8.  三星 Galaxy S10 w/先锋 W4400NEX
9.  三星 Galaxy S10+ w/先锋 W4400NEX
10.  三星 Galaxy S10 w/Kenwood Excellon ddx 9905s
11.  三星 Galaxy Note 9 w/Kenwood Excellon ddx 9705s
12.  三星 Galaxy S10 w/Kenwood Excellon DMX 905s
13.  三星 Galaxy Note 9 w/先锋 W4400NEX
14.  三星 Galaxy S9+ w/先锋 W4400NEX
15.  一加 6T 带 JVC KW-M845BW
16.  一加 6T 带先锋 W4400NEX(运行像素 ROM)
17.  三星 Galaxy S10 w/Kenwood Excellon ddx 9705s
18.  一加 6T 带建伍 Excellon DNX995S
19.  一加 6T 带 JVC KW-M855W
20.  三星 Galaxy S9 w/Kenwood Excellon ddx 9905s
21.  三星 Galaxy S10+ w/先锋 W8400NEX

如果你有兴趣自己尝试一下，以下是你必须做的事情。

## 在非像素智能手机上设置无线 Android Auto

**要求:**

*   您必须使用最新的 Google Play 服务测试版。你可以[加入测试程序](https://play.google.com/apps/testing/com.google.android.gms)并通过 Play Store 获取更新，或者你可以从像 [APKMirror](https://www.apkmirror.com/apk/google-inc/google-play-services/google-play-services-19-0-56-release/) 这样的网站下载最新的测试版 APK。如果你下载了这个应用程序，一定要下载与你的设备架构和 Android 版本相对应的版本。
*   你的智能手机至少要运行 Android 9 Pie。根据 Reddit 帖子的 OP，Android 8 Oreo 似乎不起作用，因为该方法在他儿子的 Moto Z2 Play 上不起作用。
*   您的主机必须支持无线 Android Auto。大多数内置头单元不支持它，但许多售后市场的支持。

**步骤:**

1.  在 Android Auto 应用程序中启用开发设置，方法是打开应用程序，轻按“设置”，向下滚动直到看到“版本”，然后轻按“版本”10 次。
2.  进入开发设置。
3.  选择“显示无线投影选项”
4.  重启你的手机。
5.  按照主机的说明无线连接主机。

这里有一个由/u/dingonugget 制作的屏幕记录，展示了步骤 1-3:

如果在尝试了这些步骤后，你仍然不能让它工作，或者你没有一个与 Android Auto wireless 兼容的主机，那么你可以尝试使用 XDA 知名开发商[的](https://forum.xda-developers.com/member.php?s=0ff3adc9062ca9a06d93ec0555679acf&u=842765) [AAGateWay](https://www.xda-developers.com/wireless-android-auto-head-unit-hack/) 来将你的有线主机用作无线主机。或者，您可以将任何 Android 兼容设备转换为无线 Android 自动主机，并重新加载[主机](https://forum.xda-developers.com/general/paid-software/android-4-1-headunit-reloaded-android-t3432348)。这个应用程序来自同一个开发者，但它更黑客一点。