# 华为 Mate 20 花絮:无线轻松投影、HiVision 等等

> 原文：<https://www.xda-developers.com/huawei-mate-20-wireless-easy-projection-hivision-details/>

在本月发布的近十几款智能手机中，泄露最多的两款是谷歌 Pixel 3 和华为 Mate 20。几乎每天都有关于这些智能手机的新信息。上周三，以色列科技网站*Girafa*T2 发布了一份基于该网站获得的营销幻灯片的报告。泄露的幻灯片已经被删除，显示了该设备的许多新软件功能。我决定再看看华为 Mate 20 的固件，看看我是否可以证实这个新信息和/或为自己找到更多的细节。我找到了无线轻松投影的证据、显示面板信息、电池容量、无线快速充电的存在、反向无线充电的存在，以及关于 HiVision 的更多细节——华为的谷歌镜头替代品。

*该信息基于 9 月 13 日华为 Mate 20 固件的转储，我们感谢 PNF 软件公司的[杰布反编译器](https://www.pnfsoftware.com/?aid=xdadev)对其进行了分析。同样的固件转储给了我们关于[可能的相机功能](https://www.xda-developers.com/possible-huawei-mate-20-camera-features/)、[壁纸、实时壁纸和主题](https://www.xda-developers.com/download-huawei-mate-20-wallpapers-live-wallpapers-themes/)以及该设备的[可能的运营商合作伙伴](https://www.xda-developers.com/huawei-mate-20-buy-carrier/)的信息。固件是由 [FunkyHuawei.club](https://funkyhuawei.club/) 提供给我们的，这是一项允许用户付费更新、 [unbrick](https://funkyhuawei.club/unbricking) 或[更名](https://funkyhuawei.club/rebranding)华为和 Honor 手机的服务。FunkyHuawei 计划全力支持即将到来的华为 Mate 20 系列，目前正在为 XDA 读者提供[销售。](https://funkyhuawei.club/xdaspecial)*

* * *

## 华为 Mate 20 上的无线轻松投影

去年，华为[在华为 Mate 10 上推出了一项名为 Easy Projection 的功能](https://www.xda-developers.com/huawei-mate-10-pro-porsche-official/)。轻松投影通过 USB Type-C 转 HDMI 转换器(如官方[华为 MateDock](https://consumer.huawei.com/at/accessories/huawei-matedock/) )将您的设备连接到支持的显示器，带来类似桌面的体验。桌面体验基于 [PhoenixOS](https://www.xda-developers.com/huawei-mate-10-easy-projection-phoenix-os/) ，它可以在支持 USB 3.1 的华为设备上工作，包括华为 Mate 10、华为 P20 和华为 P20 Pro。至少在[三星 Galaxy Note 9 发布之前，Easy Projection 比三星 DeX 有优势，因为除了适配器之外，它不需要使用额外的附件。](https://www.xda-developers.com/samsung-galaxy-note-9-specs-pricing-availability-features/)

*华为 Mate 10 上的有线轻松投影模式*

现在三星 DeX 在那方面已经赶上了 Easy Projection，看来华为要推出无线 Easy Projection 来夺回领先地位了。根据 *Girafa* 获得的信息，Easy Projection 将在 2.4GHz 或 5GHz Wi-Fi 连接上工作。该报告没有提供更多的细节，但我们在/product/app 中反编译了 HwPCExplorer 应用程序，以找到关于该功能的其他图像和文本。图像显示无线轻松投影可以通过快速设置互动程序启动。

字符串表示无线投影模式中有两种模式:桌面和电话模式。桌面模式允许您连接键盘和鼠标以获得类似桌面的体验，而电话模式只是投影您电话的现有内容。您还可以投影单个媒体文件，如照片、音乐和视频。无线投影适用于支持 Miracast、DLNA 或华为 Mirror 的显示器。支持 Miracast 的显示器支持桌面和电话模式。华为镜面显示器支持电话模式。支持 DLNA 的显示器仅支持单个多媒体文件的投影。要设置无线投影，您只需打开 Wi-Fi，在显示器上启用屏幕镜像，从快速设置磁贴中启用无线投影，然后选择要投影到的显示器。

### 华为 Mate 20 无线轻松投影弦

```
 <string name="wireless_first_case_tip_1">Wireless projection lets you project your phone screen onto a larger display.</string>
<string name="wireless_first_case_tip_2">In Desktop mode, you can connect a keyboard and mouse for a desktop-like experience. The display screen and phone can be used independently.</string>
<string name="wireless_first_case_tip_3">In Phone mode, your display screen will reflect what you do on your phone.</string>
<string name="wireless_first_case_tip_4">You can also project individual multimedia files such as photos, music, and videos.</string>
<string name="wireless_second_case">Which devices support Wireless projection?</string>
<string name="wireless_second_case_tip_1">You can use Wireless projection on any display screen (such as a TV) that supports Miracast, DLNA, or Huawei Mirror.</string>
<string name="wireless_second_case_tip_2">Miracast and Huawei Mirror devices support both Desktop and Phone modes.</string>
<string name="wireless_second_case_tip_3">DLNA devices only support the projection of multimedia files such as photos, music, and videos.</string>
<string name="wireless_third_case">How do I use Wireless projection?</string>
<string name="wireless_third_case_tip_1">Connect your device and external display to the same Wi-Fi network. The Miracast feature must be enabled manually.</string>
<string name="wireless_third_case_tip_2">You can enable Wireless projection from the notification panel or by going to Settings &gt; Device connection.</string>
<string name="wireless_third_case_tip_3">Wireless projection can also be enabled in the Gallery, Music, and Video apps.</string>
<string name="wireless_step_1_tip">On the external display: Make sure that the display's screen mirroring function is turned on (different brands have different names for this feature).</string>
<string name="wireless_step_2_tip">On the phone: Enable Wi-Fi, then slide down the notification panel and touch Wireless projection to search for your external display (or go to Settings &gt; Device connection &gt; Wireless projection).</string>
<string name="wireless_step_3_tip">Select the external display from the device list to start projecting.</string>
<string name="wireless_more_tip_1">Miracast devices: These support both Desktop and Phone mode. They include Miracast-enabled TVs and TV boxes.</string>
<string name="wireless_more_tip_2">DLNA devices: These only support the projection of multimedia files such as photos, music, and videos. They include DLNA-enabled TVs and TV boxes. You can start projecting multimedia files directly in Gallery, HUAWEI Music, and HUAWEI Video. When a supported device is available, touch the icon on the screen to start projection.</string>
<string name="wireless_more_tip_3">Huawei Mirror devices: These only support projection in Phone mode.</string>
<string name="wireless_more_tip_4">If connection fails, try restarting the projection feature on the external display.</string> 
```

## 华为 Mate 20 上的 HiVision

 <picture>![HiVision's App Launcher](img/bca96ae1f5cec72e1431a9705e024d60.png)</picture> 

HiVision's app icon.

除了华为 P20，华为还发布了 [HiAI 引擎](https://www.xda-developers.com/huawei-releases-hiai-engine-huawei-p20/)，以利用海思麒麟 970 中的 NPU。很明显，华为希望通过利用海思麒麟 980 上的[双 NPU 来继续大力营销其设备的人工智能能力的趋势，尽管我们不完全确定新芯片组将利用哪些功能。早在三月份，我们](https://www.xda-developers.com/hisilicon-kirin-980-honor-magic-2-huawei-mate-20-pro/)[就提供了华为 HiAssistant 和 HiVision 服务的首批细节](https://www.xda-developers.com/huawei-google-assistant-alexa-chinese-market/)。华为[宣布【HiVision 将用于运行 EMUI 9 的设备，尽管](https://consumer.huawei.com/en/press/news/2018/huawei-announces-android-pie-based-os-emui-9/)[第一套 EMUI 9 测试版](https://www.xda-developers.com/emui-9-beta-android-pie-huawei-honor/)不包括该功能。我们获得的华为 Mate 20 固件*确实*包含了最新的 HiVision APK，因此我们能够对其进行侧装和反编译，以了解更多关于其功能的信息。

### 食物识别

从 *Girafa* 得到的信息，我们知道 HiVision 是有能力识别食物的。食物识别显示 HiVision 可以确定某些食物的热量，[很像三星 Bixby](https://www.xda-developers.com/samsung-bixby-count-calories-food/) 。根据我们做的一个拆解，HiVision 使用 [Azumio 食物识别 API](https://www.azumio.com/) 来识别许多不同种类的食物。一个名为“kirinToCalorieMamaMap”的文件列出了一百多种食物，这些食物可能在当地得到认可，以便更快地得到结果。HwServerResultBean 类显示，该应用程序不仅可以显示卡路里含量，还可以显示来自 Azumio API 输出的钙、胆固醇、膳食纤维、铁、脂肪、碳水化合物、维生素含量等结果。

### 地标、绘画和旅行

我们还知道 HiVision 可以识别地标、绘画、二维码、文本、商品、车辆，并帮助您进行旅行。绘画识别功能的隐私政策规定，您的图片将被传输到 Artace Inc .进行识别。Artace 是谷歌 Play 商店 Magnus 应用程序背后的公司。除迪拜外，猫途鹰在世界各地都提供建筑标识，由迪拜旅游和商业营销公司处理。在迪拜，用户将获得一个特殊的商店标志识别功能，该功能只在城市步行区有效。该功能由猫途鹰和 Meraas 控股公司提供。最后，购物结果由 [ViSenze Pte](https://www.visenze.com/) 处理。

### 翻译

HiVision 将使用微软翻译器实时翻译文本。支持的语言有英语、中文、日语、韩语、西班牙语、法语、俄语、意大利语、德语和葡萄牙语。

在我运行 EMUI 9 测试版的华为 Mate 10 Pro 上运行的 HiVision，源自 Magisk，由 XDA 知名开发者 topjohnwu 提供。不幸的是，图像识别似乎在我的设备上不起作用。

## 收费详情

我们首次泄露的华为 Mate 20 显示了无线充电支持的[。另一个漏洞指向一个](https://www.xda-developers.com/huawei-mate-20-specifications-features-rumor/)[快速无线充电配件](https://www.xda-developers.com/huawei-mate-20-pro-cases-nm-card-wireless-charger/)。然后是 [Freebuds 2 Pro 无线耳塞](https://www.xda-developers.com/huawei-mate-20-pro-wirelessly-charge-freebuds-2-pro-wireless-earbuds/)，可能支持通过华为 Mate 20 Pro 无线充电。在 Mate 20 的 SystemUI APK 中，我们发现了手机支持的新充电模式的更新布尔，这证实了快速无线充电和反向无线充电的存在。BatteryStateInfo 类的一个片段可以在下面找到，在那里你会看到新的“IsWirelessQuickCharging”和“IsWirelessReverseCharging”布尔值。

## 电池容量和显示面板信息

我们最初的报告称，华为 Mate 20(普通，非专业)将有 6.3 英寸的 AMOLED 显示屏和 4200 毫安时电池。然而，我们看到的初始固件转储似乎包括 Mate 20 Pro 和普通 Mate 20 的共享文件。不过，随着常规 Mate 20 固件的更新，我们现在有了我们认为常规华为 Mate 20 的真正显示面板和电池容量。因此，我们现在认为我们之前报道的显示面板和电池容量信息是针对 Mate 20 Pro 而不是普通的 Mate 20。

常规的华为 Mate 20 将有 6.53 英寸的 1080x2244 的 TFT 凹口显示屏和 4,000mAh 的电池，如下面的截图所示。面板似乎来自 JDI 和夏普。电池容量被列为 4，000mAh，尽管这可能是典型容量，而额定容量为 3，900mAh。这一信息得到了吉拉法上周的报告的证实。

## RAM 和存储信息

随着这款手机接近发布，普通的华为 Mate 20、华为 Mate 20 Pro 和第三款传闻中的保时捷设计模型已经出现在中国认证网站 TENAA 上。认证揭示了以下 RAM 和存储变体:

*   华为 Mate 20 ( [HMA](http://www.tenaa.com.cn/WSFW/LicenceShow.aspx?code=3OjxvUZNGL9zfwy8EdfyQ6oOmXDsUCQ2m8mIZRN8VTCTVUTjKLw9u3VHlGxWV%2fu0) )
    *   4GB 内存+ 64GB 存储
    *   4GB 内存+ 128GB 存储空间
    *   4GB 内存+ 256GB 存储空间
    *   6GB 内存+ 128GB 存储空间
    *   6GB 内存+ 256GB 存储空间
    *   6GB 内存+ 512GB 存储空间
    *   8GB 内存+ 128GB 存储
    *   8GB 内存+ 256GB 存储空间
    *   8GB 内存+ 512GB 存储空间
*   华为 Mate 20 Pro ( [LYA](http://www.tenaa.com.cn/WSFW/LicenceShow.aspx?code=bhgJtRrjhkPJlEfNd1iKgTPMiuLErVDL%2bZeJItnBOwQjzxQLhttubVNNOWhkcAxO) )
    *   6GB 内存+ 128GB 存储空间
    *   6GB 内存+ 256GB 存储空间
    *   6GB 内存+ 512GB 存储空间
    *   8GB 内存+ 128GB 存储
    *   8GB 内存+ 256GB 存储空间
    *   8GB 内存+ 512GB 存储空间
*   华为 Mate 20 ( [EVR](http://www.tenaa.com.cn/WSFW/LicenceShow.aspx?code=EE%2b0Z5etCNsBM7dEam%2bXhu1Pxeg0K8Pi2JBIa2LwpZJJq%2fyma%2fpCk8baYDVYmIvL) -传闻中的保时捷设计模型)
    *   4GB 内存+ 128GB 存储空间
    *   4GB 内存+ 256GB 存储空间
    *   6GB 内存+ 256GB 存储空间
    *   6GB 内存+ 512GB 存储空间
    *   8GB 内存+ 128GB 存储
    *   8GB 内存+ 256GB 存储空间
    *   8GB 内存+ 512GB 存储空间

目前还不清楚这些 RAM 和存储型号将在每个市场推出。对于常规的华为 Mate 20，我们有一个可能的运营商合作伙伴列表，但我们不知道每个国家将会采用哪些 RAM 和存储版本。

## 其他详细信息

吉拉法的报告中还提到了其他一些我们无法证实的细节。据 *Girafa* 报道，华为将推出 SuperCharge 2.0，可在 30 分钟内为 70%的电池充电，仅在华为 Mate 20 Pro 中提供 3D 面部识别(这解释了为什么普通型号具有水滴凹口设计，而 Mate 20 Pro 具有更大的凹口)，在拥挤的区域更好地听到你的声音的“骨骼语音 ID”，以及 Pro 型号的 IP67 防水。

他们提供的其他一些信息我们已经谈过了，比如出现了 [NM 卡](https://www.xda-developers.com/huawei-mate-20-pro-cases-nm-card-wireless-charger/)、 [AI 影院、AI 变焦](https://www.xda-developers.com/possible-huawei-mate-20-camera-features/)。如果我们了解到更多关于即将推出的华为 Mate 20，华为 Mate 20 Pro，或传闻中的保时捷设计华为 Mate 20 的信息，我们会让你们都知道。