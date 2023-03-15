# 如何将第三方音乐应用添加到 EMUI 的音乐锁屏[Root]

> 原文：<https://www.xda-developers.com/how-to-add-third-party-music-apps-emui-lock-screen/>

像许多 OEM 皮肤一样，EMUI 修改了股票锁定屏幕以适应其主题，并加入了公司认为其用户需要快速访问的功能。

EMUI 的锁定屏幕提供的功能之一是能够以美丽的全屏专辑封面和大轨道控制按钮显示当前播放的音乐轨道，如功能图像所示。然而，该功能仅限于华为/Honor 选择的少数预定义应用。该列表*包括:

*可能有其他应用程序可以与 EMUI 的音乐锁屏配合使用。这个列表直接来自华为的应用白名单，我将在下面详细描述。

如果你不使用 EMUI 中某个被认可的应用，比如[留声机](https://play.google.com/store/apps/details?id=com.kabouzeid.gramophone)或者[安可](https://play.google.com/store/apps/details?id=com.fastbootmobile.encore.app)，会怎么样？如果你想展示美丽的艺术，并为一些播客应用程序(如[播客上瘾](https://play.google.com/store/apps/details?id=com.bambuna.podcastaddict))提供大的轨道控制按钮，该怎么办？在这些情况下，当您开始一个轨道或 podcast 时，您的锁定屏幕将如下所示:

大屏幕的华为/Honor 设备可能会觉得处理起来很烦人，因为按钮相对于整个屏幕来说太小了。这让你很难控制你的音乐，而且用这种方式展示你的音乐也很难看。幸运的是，有一种方法可以将你选择的应用程序加入白名单，这样音乐曲目就会像普通音乐播放器一样显示在锁定屏幕上。

* * *

## 将第三方音乐应用添加到 EMUI 的音乐锁定屏幕

有一个系统设置包含 EMUI 用来确定哪些应用程序获得特殊音乐锁屏待遇的软件包列表。如果您发送以下 ADB 命令，那么您可以看到自己的包列表:

```
 adb shell settings get system white_music_for_keyguard 
```

不幸的是，通过 ADB 命令修改这个列表没有任何作用。然而，当我开始研究如何解决这个问题时，我在我们自己的 XDA 论坛上发现了一个解决方案。

这一招[最初是由 XDA 资深会员](https://forum.xda-developers.com/mate-8/general/adding-apps-to-music-lockscreen-root-t3442538/page2) [superior8888](https://forum.xda-developers.com/member.php?u=4832449) 在华为 Mate 8 论坛上发现的，但这应该在大多数华为和 Honor 设备上都有这个功能。不幸的是，这种方法**要求你拥有 root 权限**，因为你需要修改一个系统偏好文件来将你最喜欢的音乐应用添加到白名单包列表中。

从 Play Store 下载一个根文件浏览器(任何 app 都可以)。如果您知道如何使用命令行，那么您也可以使用终端模拟器。在任何情况下，根据您的设备型号，您必须编辑 **hw_defaults.xml** ，它位于不同的目录中，这取决于您设备的区域设置。这是因为华为/Honor 根据您设备的区域设置使用不同的 EMUI 配置文件。

对于国际型号，您需要编辑的文件位于:

```
 /system/emui/oversea/xml/ 
```

对于中国模型，您需要编辑的文件位于:

```
 /system/emui/china/xml/ 
```

一旦你打开这个文件，你将需要编辑或添加某一行，以便将你的应用程序列入白名单。有一个你将要编辑/添加的字符串，叫做 **white_music_for_keyguard** ，它包含一个**包名**的**分号分隔列表**。因此，您需要知道想要加入白名单的应用程序的包名。

有多种方法可以找到应用程序的包名。您可以从 Play Store 下载 [App Inspector](https://play.google.com/store/apps/details?id=com.ubqsoft.sec01) ，通过选择您的应用并查看数据目录的名称来找到包名称。或者您可以查看 Play Store 列表的 URL 来查找包名，如下所示:

请注意，URL 的粗体部分是包名。一旦您获得了想要的包列表，我们现在就可以修改 hw_defaults.xml 了。

首先，对于国际车型:

### 编辑前

```

<resources>
<string settings.secure.default_input_method="com.nuance.swype.emui/com.nuance.swype.input.HuaweiIME"/>

<integer settings.secure.fingerprint_gallery_slide="0"/>

<string white_languages="en_US,ar_EG,de_DE,bs_BA,es_ES,uk_UA,fr_FR,pt_PT,ru_RU,zh_CN,zh_TW,zh_HK,es_US,cs_CZ,da_DK,el_GR,hu_HU,pt_BR,it_IT,ja_JP,lt_LT,lv_LV,bg_BG,nb_NO,pl_PL,ro_RO,et_EE,sk_SK,sr_Latn,sv_SE,tr_TR,th_TH,fi_FI,in_ID,mk_MK,sl_SI,ms_MY,vi_VN,hr_HR,nl_NL,ca_ES,hi_IN,ko_KR,en_GB,iw_IL,my_ZG,my_MM,eu_ES,gl_ES,ka_GE,az_AZ,uz_UZ,km_KH,si_LK,ur_PK,kk_KZ,lo_LA,be_BY,bn_BD,ne_NP,tl_PH,jv_Latn"/>

<string white_music_for_keyguard="deezer.android.app;com.maxmpz.audioplayer;com.qobuz.music;com.soundcloud.android;com.spotify.music"/>

<string hw_invert_txtclr_packages="google*;facebook*"/>

<integer hw_displayafterfirstring="0"/>

</resources>

```

### 编辑后

```

<resources>
<string settings.secure.default_input_method="com.nuance.swype.emui/com.nuance.swype.input.HuaweiIME"/>

<integer settings.secure.fingerprint_gallery_slide="0"/>

<string white_languages="en_US,ar_EG,de_DE,bs_BA,es_ES,uk_UA,fr_FR,pt_PT,ru_RU,zh_CN,zh_TW,zh_HK,es_US,cs_CZ,da_DK,el_GR,hu_HU,pt_BR,it_IT,ja_JP,lt_LT,lv_LV,bg_BG,nb_NO,pl_PL,ro_RO,et_EE,sk_SK,sr_Latn,sv_SE,tr_TR,th_TH,fi_FI,in_ID,mk_MK,sl_SI,ms_MY,vi_VN,hr_HR,nl_NL,ca_ES,hi_IN,ko_KR,en_GB,iw_IL,my_ZG,my_MM,eu_ES,gl_ES,ka_GE,az_AZ,uz_UZ,km_KH,si_LK,ur_PK,kk_KZ,lo_LA,be_BY,bn_BD,ne_NP,tl_PH,jv_Latn"/>

<string white_music_for_keyguard="deezer.android.app;com.maxmpz.audioplayer;com.qobuz.music;com.soundcloud.android;com.spotify.music;<strong>YOUR.MUSIC.PACKAGE.HERE</strong>"/>

<string hw_invert_txtclr_packages="google*;facebook*"/>

<integer hw_displayafterfirstring="0"/>

</resources>

```

对于中国车型:

### 编辑前

```
 <resources>
<string default_input_method="com.baidu.input_huawei/.ImeService"/>
<string custom_certify_picture="/system/emui/china/media/certify_infor.png"/>
<string white_languages="en_US,ar_EG,de_DE,bs_BA,es_ES,uk_UA,fr_FR,pt_PT,ru_RU,zh_CN,zh_TW,zh_HK,es_US,cs_CZ,da_DK,el_GR,hu_HU,pt_BR,it_IT,ja_JP,lt_LT,lv_LV,bg_BG,nb_NO,pl_PL,ro_RO,et_EE,sk_SK,sr_Latn,sv_SE,tr_TR,th_TH,fi_FI,in_ID,mk_MK,sl_SI,ms_MY,vi_VN,hr_HR,nl_NL,ca_ES,hi_IN,ko_KR,en_GB,iw_IL,eu_ES,gl_ES,bo_CN,ka_GE,az_AZ,uz_UZ,km_KH,si_LK,ur_PK,kk_KZ,lo_LA,be_BY,bn_BD,ne_NP,tl_PH,jv_Latn"/>
<string hw_theme_support_hw/>
<string hw_theme_support_pay="true"/>
<integer is_show_google="0"/>
</resources>

```

### 编辑后

```

<resources>
<string default_input_method="com.baidu.input_huawei/.ImeService"/>
<string custom_certify_picture="/system/emui/china/media/certify_infor.png"/>
<string white_languages="en_US,ar_EG,de_DE,bs_BA,es_ES,uk_UA,fr_FR,pt_PT,ru_RU,zh_CN,zh_TW,zh_HK,es_US,cs_CZ,da_DK,el_GR,hu_HU,pt_BR,it_IT,ja_JP,lt_LT,lv_LV,bg_BG,nb_NO,pl_PL,ro_RO,et_EE,sk_SK,sr_Latn,sv_SE,tr_TR,th_TH,fi_FI,in_ID,mk_MK,sl_SI,ms_MY,vi_VN,hr_HR,nl_NL,ca_ES,hi_IN,ko_KR,en_GB,iw_IL,eu_ES,gl_ES,bo_CN,ka_GE,az_AZ,uz_UZ,km_KH,si_LK,ur_PK,kk_KZ,lo_LA,be_BY,bn_BD,ne_NP,tl_PH,jv_Latn"/>
<string hw_theme_support_hw/>
<string hw_theme_support_pay="true"/>
<string white_music_for_keyguard="<strong>YOUR.LIST.OF.PACKAGES.SEPARATED.BY.SEMI.COLON.HERE</strong>"/>
<integer is_show_google="0"/>
</resources>

```

完成编辑后，重新启动您的设备。你应该很有希望在锁定屏幕上看到带有大音轨控制按钮的全屏专辑封面。然而，我不能保证这一调整将适用于所有的多媒体应用，但我相信它将适用于大多数应用。

* * *

**试试这个技巧，** **让我们知道它对你的荣誉/华为设备是否有效！**