# LineageOS Changelog 23:这里是所有的新功能和变化

> 原文：<https://www.xda-developers.com/lineageos-changelog-23-features/>

LineageOS 于 2016 年底/2017 年初从 CyanogenMod 的灰烬中诞生，自其诞生以来，定制 Android 发行版已经发展到支持数十种设备，拥有数百万用户。回到 2019 年 2 月下旬，团队[宣布了基于 Android 9 Pie 的](https://www.xda-developers.com/lineageos-16-android-pie/) LineageOS 16，用于 24 款设备。在过去的几个月里，LineageOS 16 增加了对 OnePlus 6 和 Essential Phone 等更多设备的支持，但定制 ROM 也增加了大量新功能。为了让我们了解 LineageOS 16 首次发布以来的所有重大变化，LineageOS 背后的团队发布了一篇新的博客文章，概述了他们自 3 月份以来的进展。

变更日志很长，所以这里总结一下我最喜欢的新增功能。首先，切换夜灯[现在也可以切换](https://www.xda-developers.com/enable-android-p-dark-theme-night-light/)内置的黑暗主题。接下来，音量面板可以[现在展开](https://www.xda-developers.com/posp-latest-update-android-pie-oneplus-6t-poco-f1/)来显示所有的音量流，这样你就不用去声音设置了；此外，您可以将音量面板的默认位置移到屏幕的左侧。然后，[可膨胀速凝瓷砖](https://www.xda-developers.com/posp-v2-3-rgb-accent-picker-oreo-quick-settings/)又回来了；stock Android Pie 不再允许你从快速设置中更改 Wi-Fi 网络或蓝牙连接，但 LineageOS 又恢复了这一功能。有一个新的壁纸应用程序，有一些漂亮的默认壁纸，锁屏快捷方式支持，电池电量的著名圆形状态栏图标[又回来了，通知音量现在可以从铃声音量中分离出来。股票拨号器应用程序已更新为](https://www.xda-developers.com/circular-battery-status-for-android/)[支持合法地区的通话记录](https://www.xda-developers.com/future-android-version-call-recording/)，添加了蓝牙 SBC DualChannel HD(这值得单独撰写一篇文章，因此我们将很快对此进行更详细的介绍)，2019 年[4 月](https://www.xda-developers.com/april-2019-android-security-google-pixel-essential-phone/)、[5 月](https://www.xda-developers.com/may-2019-google-android-security-updates/)和[6 月](https://www.xda-developers.com/may-2019-android-security-patches/)的所有安全补丁已合并。

## **linea geos Changelog 23:2019 年 3 月 1 日以来的重大变化**

除非明确声明，否则所有的更改都是指当前分支，沿袭-16.0。

*   AOSP 的夜间显示器现在可以控制夜间模式(仅在最近的设备上，如 Snapdragon 820 或更高版本的设备)
*   live display 的所有其他功能仍然可用
*   现在可以扩展音量面板来控制所有不同的音量流
*   现在可以选择将音量面板重新定位到左侧
*   扩展的快速设置又回来了
    *   提供以下图块的详细视图:Wi-Fi、蓝牙、移动数据、位置、配置文件
*   新的默认壁纸和一个新的壁纸应用程序，有许多新的和旧的壁纸
    *   除了常见的自然、城市和抽象主题壁纸，单色和渐变壁纸现在都有了
*   隐私卫士现在支持工作档案中的应用程序
*   最多可以再添加两个锁屏快捷键
*   自从 LineageOS 13.0 以来，循环电池在丢失后又回来了
*   通知铃声级别可以与电话铃声级别分离
*   GPS 电池节省模式现在可以从设置中启用
*   Vim 已更新至 8.1 版(Nano 已更新至 4.2 版)
*   由于 Q 的后端口修复，修正了使用某些专用 DNS 导致设备崩溃的问题
*   更新了通话记录配置(15.1 和 16.0)
*   根据法律和/或法律先例，在某些国家/地区允许(不允许)通话录音。源代码中有带链接的信息。
    *   这些国家现在支持通话录音:阿尔巴尼亚、美属萨摩亚、阿根廷、亚美尼亚、阿鲁巴、白俄罗斯、博内尔岛、波斯尼亚和黑塞哥维那、巴西、加拿大、智利、克罗地亚、库拉索岛、塞浦路斯、爱沙尼亚、法罗群岛、法属圭亚那、法属波利尼西亚、格鲁吉亚、希腊、格陵兰岛、瓜德罗普岛、匈牙利、印度、爱尔兰、以色列、日本、科索沃、拉脱维亚、列支敦士登、立陶宛、卢森堡、马耳他、马提尼克岛、马约特岛、摩尔多瓦、黑山、摩洛哥、新喀里多尼亚、新西兰、北马其顿、秘鲁、俄罗斯、留尼汪岛、萨巴岛、圣巴特勒米岛
    *   这些国家被禁止通话录音:安道尔、冰岛、印度尼西亚、摩纳哥、瑞士、美利坚合众国及其部分领土-关岛、北马里亚纳群岛、波多黎各和美属维尔京群岛。
*   增加了对蓝牙 SBC 双通道 HD 的支持(15.1 和 16.0)
*   Eleven(音乐播放器应用程序)的性能改进(15.1 和 16.0)
*   4 月、5 月和 6 月的安全修补程序已合并(15.1 和 16.0)
*   WebView 已更新到 Chromium 74 . 0 . 3729 . 157(15.1 和 16.0)

* * *

## LineageOS 15.1 和 LineageOS 16 下载链接

我们在下面链接了所有目前安装了 LineageOS 16 或 LineageOS 15.1 版本的设备的下载页面。这取决于你是否遵循 wiki 页面中提到的安装说明，因为没有安装 LineageOS 的通用方法。不过，一般来说，你需要解锁引导程序，刷新自定义恢复，刷新 LineageOS，然后可选地刷新 Google apps 包。如果你的设备没有列在下面，一定要检查 XDA 论坛，看看是否有一个非官方的版本。

### LineageOS 16 (Android 9 Pie) -每夜发布

#### 贝克勒尔

#### 必要的

#### Fairphone

#### 谷歌

#### 荣誉/华为

#### LeEco

#### 联想（电脑的品牌名）

#### 水平规ˌ水准仪(Level Gauge)

#### 摩托罗拉

#### 下一位

#### 一加

#### OPPO

#### 三星电子

#### 索尼

#### 狡猾的狐狸

#### 小米

#### 禹

### LineageOS 15.1 (Android 8.1 奥利奥)-每周发布

*注意:一些设备同时具有官方 LineageOS 15.1 和官方 LineageOS 16 版本。*

#### 贝克勒尔

#### 谷歌

#### 荣耀

#### LeEco

#### 水平规ˌ水准仪(Level Gauge)

#### 下一位

#### 英伟达

#### 一加

#### 索尼

#### 小米

* * *

## 帮忙翻译！

如果你的语言不被 Android 支持，你可以通过贡献给 [Crowdin](https://crowdin.com/project/lineageos) 来帮助 LineageOS 增加对它的支持。该团队指出，由于社区翻译人员的贡献，Lineage 是第一个支持威尔士语(Cymraeg)的定制 Android 发行版。

* * *

## 支持项目！

LineageOS 是一项由社区主导的工作。它完全依赖于志愿者开发人员、翻译人员和测试人员的贡献。如果您希望支持团队的工作，您可以通过以下方式之一做出贡献:

**提交错误报告**

**捐赠给 LineageOS 以支付服务器成本**

**关注社交媒体上的 LineageOS，了解最新新闻**