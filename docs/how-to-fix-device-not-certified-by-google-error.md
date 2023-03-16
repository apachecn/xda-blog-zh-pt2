# 如何修复“设备未经谷歌认证”的错误

> 原文：<https://www.xda-developers.com/how-to-fix-device-not-certified-by-google-error/>

几天前，我们报道了谷歌开始[阻止未经认证的 Android 设备](https://www.xda-developers.com/google-blocks-gapps-uncertified-devices-custom-rom-whitelist/)访问 Google Play 应用和服务。这意味着任何未经谷歌认证的设备都将无法下载和使用 Gmail、谷歌地图、谷歌音乐、谷歌照片等应用。从亚马逊等知名品牌到知名度较低的中国品牌，没有自带谷歌应用程序的设备有着巨大的市场。如果你买了一个安卓设备，你看到“**设备未经谷歌**认证”的警告，你能做些什么？你没有太多的选择，但我们会运行可用选项的列表，这样你也许可以在未经认证的 Android 设备上解锁 Google apps。

**更新 3/28/18 @ 05:22PM CST** :注册豁免的网页已经更新，现在输入您的 Google Play Services Framework 设备 ID 即可。已更新说明以适应这些变化。

**更新 4/3/18 @ 01:05PM CST:** 谷歌[再次更新网页](https://www.xda-developers.com/google-removes-100-device-registration-limit-uncertified-device-page/)，这次取消了 100 个设备注册限制，现在允许十六进制格式的 GSF id 工作。

* * *

## 什么是未经认证的设备，为什么我的设备是其中之一？

Android 是一个开源的操作系统。这意味着任何公司都可以采用 Android，并按照他们的意愿修改它，以销售给他们的客户。Android 设备的软件体验可以大相径庭，从[谷歌 Pixel 2](https://www.xda-developers.com/google-pixel-2-xl-announced-price/) 到[三星 Galaxy S9](https://www.xda-developers.com/samsung-galaxy-s9-and-galaxy-s9-are-official-specifications-features-prices-and-availability/) 到[华为 P20](https://www.xda-developers.com/huawei-announces-huawei-p20-p20-pro-p20-lite/) 或[小米 Mix 2S](https://www.xda-developers.com/xiaomi-launches-xiaomi-mi-mix-2s-qualcomm-snapdragon-845/) 。谷歌希望公司采用 Android 并对其进行定制，但他们也希望确保 Android 设备之间至少有一些一致性。

这就是为什么他们创建了兼容性定义文档(CDD)，这是 Android 智能手机和平板电脑制造商必须遵循的要求和指南列表，以便他们的设备能够通过兼容性测试套件(CTS)。如果该公司希望被允许在其设备上预装谷歌应用程序和服务，则需要通过 CTS。如果设备没有通过 CTS，那么他们就不能在设备上预装谷歌 Play 商店或其他任何重要的谷歌应用程序。

然而，一些制造商一直忽视这一要求。一些设备没有通过谷歌认证的公司仍然为他们的客户提供下载和安装谷歌应用程序的方法。虽然这没有违反任何规则，但它绕过了谷歌的认证要求，因此谷歌肯定不高兴这种情况一直在发生。出于这个原因，谷歌正在通过阻止这些公司的设备从侧面加载谷歌应用和服务来打击这些公司。任何固件在 3 月 16 日之后生产的设备都将开始看到以下警告消息，告诉他们“他们的设备未经谷歌认证。”

*演职员表:XDA 资深成员[利亚姆 _ 达文波特](https://forum.xda-developers.com/member.php?u=5823687)*

该警告会在设置过程中弹出，阻止您登录您的 Google 帐户。您仍然可以完成设置，但如果没有 Google 帐户，您将无法使用谷歌 Play 商店。那么你有什么选择？

## 如何检查您的设备是否未经认证

首先，让我们验证您的设备是否未经认证。如果你已经看到上面的警告，那么你的设备肯定是未经认证的。如果你怀疑你的设备未经认证，但你不确定，这里有如何检查。

### 我已经有了那个可疑的装置

1.  打开谷歌 Play 商店
2.  从左侧拉起，打开侧边栏菜单
3.  点击设置
4.  向下滚动到“关于”部分。您设备的认证状态应显示在“设备认证”下

### 我没有问题中的设备，我很好奇

我们之前写过一篇关于如何检查你打算购买的设备是否是经过认证的 Android 设备的教程。[点击这里查看](https://www.xda-developers.com/check-phone-tablet-certified-android-before-buying/)。

## 如何在安卓设备上解锁谷歌应用

正如我们之前提到的，这一举措旨在阻止公司运送未经谷歌应用和服务认证的 Android 设备。谷歌不想通过阻止普通用户使用他们的应用来惩罚他们，所以这就是为什么他们开放了一个网页，你可以在那里申请豁免。该网页旨在为定制 ROM 用户，如那些在[line geos](https://www.xda-developers.com/lineageos-15-android-oreo-officially-announced/)上的用户，提供白名单，这样你仍然可以使用 [Gapps](https://www.xda-developers.com/open-gapps-now-supports-android-8-1-oreo-arm-arm64/) ，但它也可能被亚马逊 Fire 或其他设备的用户使用。

谷歌公关与我们联系，告知我们网页正在寻找 Google Play 服务框架 ID (GSF)。以下是如何正确解锁您的 Android 智能手机或平板电脑，以便您可以使用 Play Store！

在谷歌 Play 商店设置中，您的设备仍会显示未经认证。这很正常。这个修复只是将你未认证的设备列入白名单，这样你仍然可以使用谷歌应用和服务。

1.  查找您的设备的 GSF 设备 ID。Play Store 上有一个简单的应用程序，名为“[设备 ID](https://play.google.com/store/apps/details?id=com.evozi.deviceid) ”，但由于你显然无法访问 Play Store，我让[在这里镜像应用程序](https://www.androidfilehost.com/?fid=673956719939830832)。
2.  打开应用程序，复制第二行名为“谷歌服务框架(GSF)”的代码
3.  转到[这个网页](https://www.google.com/android/uncertified/)。
4.  在“Android ID”框中输入您的 GSF 设备 ID。
5.  点击“注册”后，您的注册 ID 应该会出现在页面上。

这个*应该*允许你使用 Google Play 应用程序，但我们不能对所有设备做出任何保证。如果出于任何原因将你的设备添加到白名单中没有帮助，那么不幸的是，你将不得不要么[离开谷歌应用](https://www.xda-developers.com/comparing-battery-life-with-and-without-google-services-a-week-of-minimal-idle-drain/)，联系制造你的手机的公司以说服他们获得认证，要么购买另一个设备。如果你至少想访问 Play Store 和一些基本的谷歌应用程序，对于那些不介意稍微修改一下的人来说，还有一个替代方案。

## 如果您仍然无法取消阻止 Google 企业应用套件，该怎么办

有些人可能不喜欢谷歌应用的专有性质。这就是为什么 LineageOS 等定制 rom 如此受欢迎的原因。你可以访问一堆第三方应用程序，这些应用程序为你提供你需要的基本功能。然而，有一个折中的解决方案叫做[微 G](https://forum.xda-developers.com/android/apps-games/app-microg-gmscore-floss-play-services-t3217616) 。使用需要一个[定制 ROM，但这是使用谷歌应用和服务的最佳方式，不会牺牲隐私或电池寿命。Play Store 的另一个替代方案是使用一个应用程序，如](https://www.xda-developers.com/unofficial-lineageos-built-in-microg-avoid-google-services/) [Galaxy](https://www.xda-developers.com/galaxy-material-design-yalp-store-google-play-alternative/) ，这是流行的 Yalp 商店的一个材料设计分支，用于抓取 Google Play 的应用程序。

如果阻止未经认证的设备访问游戏服务的计划有任何变化，我们将更新本文。