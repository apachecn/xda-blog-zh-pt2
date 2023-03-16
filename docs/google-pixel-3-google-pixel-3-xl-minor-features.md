# 谷歌像素 3 花絮:你可能错过的一切！

> 原文：<https://www.xda-developers.com/google-pixel-3-google-pixel-3-xl-minor-features/>

谷歌 Pixel 3 和谷歌 Pixel 3 XL 于本周早些时候发布。最新的谷歌旗舰智能手机分别采用 5.5 英寸和 6.3 英寸有机发光二极管显示屏(后者有一个显示凹槽)，高通骁龙 845，4gb 内存，64 或 128GBs 存储空间，以及 Android Pie。谷歌在 Pixel 3 的发布会上重点介绍了该设备的新相机功能:顶部拍摄、夜视、照相亭和主题跟踪自动对焦。但是如果只看直播，有很多信息你是得不到的。我们在活动中花了一些时间使用该设备，并做了一些自己的研究，以帮助您跟上速度。

## 谷歌 Pixel 3 相机功能

我们已经知道谷歌相机应用的最新版本会带来很多用户界面的变化，但现在 Pixel 3 终于到了评测人员的手中，我们知道到底发生了什么变化。我们已经在上一篇文章的[中详细介绍了一些变化，但总而言之，新的谷歌相机应用程序允许你以 RAW 拍摄，以 h265/HEVC 录制，以在不牺牲质量的情况下实现更好的压缩，通过在每种模式之间滑动来简化设计，添加人像模式景深调整等等。还有一个谷歌 Pixel 3 独有的功能，以及我们被告知的一些我们认为值得讨论的变化。](https://www.xda-developers.com/google-camera-pixel-3-apk-download/)

### 自动 FPS 切换

首先，增加了一个在视频录制过程中自动切换 FPS 的新选项。据我们在活动中采访的一位产品经理说，人们在录制视频之前很难决定最佳帧速率。这项新功能可以让谷歌相机应用程序根据屏幕上的内容决定以何种帧速率录制——30 帧/秒或 60 帧/秒。该功能甚至可以在录制过程中切换帧速率。不过，它不适用于 4K 的视频。

### 像素视觉核心变化

接下来，一位产品经理向我们确认，Pixel 视觉核心[确实已经更新](https://www.xda-developers.com/google-pixel-3-xl-dual-front-camera-super-selfies/)。在该设备的内核源代码发布之前，我们不会确切知道 HAL 中添加了哪些新功能。然而，我们被告知，Pixel 视觉核心现在实际上被谷歌相机应用程序用于谷歌镜头建议、HDR+、Top Shot、运动自动对焦和 Photobooth。这很可能是为什么旧像素将获得夜视和游乐场的支持，但不会获得 Top Shot，运动自动对焦或 Photobooth 的支持-他们没有新的像素视觉核心。

当我们第一次听说谷歌 Pixel 2 [没有使用 HDR+](https://www.xda-developers.com/google-pixel-visual-core-instagram-snapchat-whatsapp/) 的 Pixel 视觉核心时，有点惊讶，因为我们不知道做出这一决定的确切原因，我们将避免猜测。我怀疑，由于 Pixel 3 上的许多新相机功能都依赖于 Pixel 视觉核心，它们将更难移植到其他设备上。一些开发人员已经在尝试引入一些功能，我已经看到一个开发人员成功地展示了新的“夜视”功能(尽管它还不能工作)。)

### 无 4K@60FPS

即使高通骁龙 845 中的 ISP 能够以 60 fps 处理 4K 分辨率的视频，Pixel 3 也不允许您以这种分辨率和帧速率组合进行实际录制。我们不确定为什么会这样，但我们会努力找出原因。使用的摄像头传感器可能是原因，但我们还不知道确切的摄像头传感器。

### 谷歌镜头

在演讲前几天，Pixel Tips 应用程序泄露的一段视频显示，谷歌镜头[在谷歌 Pixel 3 上的谷歌相机应用程序中实时工作](https://www.xda-developers.com/google-pixel-3-real-time-google-lens-google-camera/)。谷歌确实在 stage 上宣布了这项功能，但还有一些你可能错过的与谷歌镜头相关的新闻。

首先，谷歌镜头可以在 Pixel 3 上离线工作，但只能用于特定情况，如从图像中读取文本。其次，Google Lens 现在可以扫描专辑插图，并在 YouTube 音乐中播放结果。第三，谷歌镜头建议，以及我们之前讨论的其他相机功能，依赖于更新的 Pixel 视觉核心——这就是为什么它不会出现在谷歌 Pixel 或谷歌 Pixel 2 上。至少，不是正式的。

### 游乐场:不仅仅是品牌重塑

就在演示开始前不久，谷歌更新了 AR 贴纸应用程序和几个贴纸包，以新的品牌命名:游乐场。谷歌宣布了几个新的贴纸包，包括一个使用漫威人物的贴纸包，但你可能会想知道 Playground 与 AR 贴纸相比有什么不同。我们非常熟悉谷歌对重塑其产品品牌的偏好- [Google Feed to Discover](https://www.xda-developers.com/google-search-discover-lens-stories-activity-cards/) ，Google Keep to Google Keep Notes，等等。-但令人惊讶的是，游乐场真的不仅仅是一个品牌重塑。

在演示区，一名谷歌员工告诉我们，有几件事可以区分 Playground 和 AR 贴纸。首先，你放在屏幕上的角色现在可以互相交流，也可以和画面中的人交流。第二，现在有基于屏幕上当前内容的贴纸建议(可以显示关于人、物体或其他贴纸的建议)。第三，贴纸现在可以通过前置摄像头放置，并使用实时身体分割，可以看起来像是在视野中的主体后面。说到前置摄像头贴纸，该功能现在可以跟踪面部表情，贴纸可以做出相应的反应。最后，现在有来自 Gboard 的 2D 贴纸和新的贴纸可以表演的动画。

### 超分辨率变焦、计算 Raw、合成补光闪光灯、基于学习的人像模式和夜视

[*DPReview*](https://www.dpreview.com/articles/7921074499/five-ways-google-pixel-3-pushes-the-boundaries-of-computational-photography) 发表了一篇关于上述所有功能如何工作的深度文章，所以我们建议通读一遍(他们也有一堆样本照片)。但是如果你想要一个总结，这里是你应该带走的:

*   **超分辨率变焦**:“使用 HDR+连拍摄影来缓冲多达 15 张图像”，然后“采用超分辨率技术来提高图像的分辨率，超过传统传感器和镜头组合所能达到的分辨率。”它只能在 1.2 倍或更大变焦时激活。
*   **Computational Raw** :“与行业中的其他公司相比，有一个关键的区别。我们的 DNG 是对齐和合并[多达 15]多个帧的结果...这让它看起来更像是 DSLR 的结果。”-马克·莱沃伊，谷歌计算摄影主管
*   **合成补光闪光灯**:“合成补光闪光灯”给人类主体增加了一种光晕，就好像一个反光板举在他们面前一样。”
*   **基于学习的人像模式**:“我们过去从双像素计算立体，现在我们使用基于学习的流水线。它仍然利用了双像素，但它不是一种传统的算法，而是基于学习的”——谷歌计算摄影负责人 Marc Levoy。根据 *DPReview* 的说法，这意味着“改进的结果:更均匀的散焦背景和更少的深度图误差。”
*   **夜视**:“夜视”利用 HDR+连拍模式摄影，在非常黑暗的情况下拍摄可用的照片...在你按下快门按钮后，它希望你拿稳相机。当你这样做时，相机将合并多达 15 帧，每帧的快门速度低至 1/3 秒，以获得相当于 5 秒曝光的图像。”- *DPReview*

### 真正的立体声录音

*迪伦·拉格的作品*

对于视频录制，一个几乎没有被注意到的改进是 Pixel 3 现在可以录制真正的立体声音频。许多人对它在 Pixel 2 中的省略感到失望，Pixel 2 仅记录单声道。虽然分离的质量(和音频本身)未经测试，但这至少表明谷歌在音频录制的正确方向上迈出了一步。

### ![Google Pixel 3 XL Stereo Recording](img/87dfce5783924b71438e6fcf8befaa36.png)宽色彩捕捉？

*迪伦·拉格的作品*

早在 8 月，俄罗斯科技博客 Rozetked 设法泄露并提供了他们的预生产 Pixel 3 XL 的照片。从这些照片和视频中，我们设法发现 Pixel 3 能够进行立体声音频录制，并且前置摄像头具有自动对焦功能，[提前近两个月](https://www.xda-developers.com/google-pixel-3-xl-specs-features-pics-rumors/)。此外，我们还发现拍摄的照片具有嵌入式显示器 P3 颜色配置文件，这表明拍摄的照片将捕捉更大范围的颜色，不仅超过了其前辈，而且超过了所有其他 Android 智能手机相机——除了 iPhones(自 7 以来)之外，没有其他主要的智能手机相机捕捉宽彩色图像。这也与 [*Android Central*](https://www.androidcentral.com/google-pixel-3-review) 声称 Pixel 3 的传感器是“具有更好动态范围捕捉的新版本”不谋而合然而，在我们的审查单元上拍摄的照片没有嵌入式显示器 P3 色彩配置文件，而是典型的 sRGB 配置文件，所以看起来像谷歌拔掉了宽色彩捕捉的插头，至少现在是这样。

## 谷歌 Pixel 3 硬件

### IP68 防水等级

谷歌官方博客文章和来自@madebygoogle 账户的几条推文称，该设备的防护等级为 IP68。第一个数字代表颗粒阻力，而第二个数字代表水阻力。Pixel 3 应该在水下 1.5 米的最大深度防水长达 30 分钟，并提供保护免受有害颗粒的影响。

### FeliCa 支持

日本经常获得在国际上发布的相同智能手机的不同硬件版本。这是因为他们需要在设备中有一个 Osaifu-Keitai 兼容的安全元件，这样他们不仅可以读写 FeliCa 卡，还可以进行卡仿真。谷歌 Pixel 2 系列在设备中没有这样的安全元素，但今年，Pixel 3 有了。以下是 Pixel 3 和 Pixel 3 XL 的 4 种硬件变体:

*   G013A -国际像素 3
*   G013B -具有奥赛福-京泰兼容安全元件的像素 3
*   G013C -像素 3 XL 国际
*   G013D - Pixel 3 XL，带 Osaifu-Keitai 兼容安全元件

不同型号的波段支持也有所不同。日本的有 band 21，美国的没有。美国的有 71 和 32 频段，TDD 46，日本的没有。

### 没有通知 LED

我们可以谈论 Pixel 3 如何拥有一个始终显示的显示屏，可以向你显示你的通知，或者如何有像双击这样的手势来快速访问你的锁屏通知，但真的，很难说我们不会错过通知 LED。这是 Android 智能手机上一个非常常见的功能，我们不确定为什么 Pixel 3 上没有这个功能。如果没有通知 LED，当 Pixel 3 的屏幕不在你的视线范围内时，很难判断何时有新的通知。

## 谷歌 Pixel 3 软件功能

### 您可以隐藏 Pixel 3 XL 上的凹口...有点儿

“显示剪切块”开发者选项已经更新为一个新的“隐藏”选项。选中时，它会将状态栏向下推，直到它位于凹口区域的下方。这有效地将像素 3 XL 变成了像素 2 XL。看起来是这样的:

您也可以使用我们的 Nacho Notch 应用程序隐藏缺口。这并不是向下推动屏幕内容，而是使状态栏区域变暗。看起来是这样的:

### 手势是新的标准

在谷歌 I/O 期间，我们听说手势导航[将是](https://www.xda-developers.com/google-pixel-3-will-only-offer-gesture-navigation-and-not-standard-buttons/)在下一代谷歌 Pixel 设备上导航 UI 的唯一方式。谷歌后来澄清说，手势导航只会是 Pixel 3 的默认导航方式，他们无法确认手势是否是前进的唯一方式。现在 Pixel 3 在这里，我们可以确认没有关闭它们的选项。抱歉，伙计们，手势是不会变的。

 <picture>![Google Pixel 3 Gestures](img/2e1c4da42ce23eaf4612d5fad96d0f31.png)</picture> 

Swipe up to switch option is missing

有一种恢复标准导航键的方法，但是我会在以后的文章中详细介绍。

### 谷歌双工终于来了

未来的谷歌双工功能，可以代表你开始整个电话交谈，终于来了。谷歌最初在 I/O 上演示了这一点，但遭到了强烈反对，因为他们担心接收方会觉得受到了欺骗，因为他们没有被告知他们正在与机器人交谈。Google [通过在每个通过双工发起的呼叫开始时添加免责声明来解决这些问题。](https://www.xda-developers.com/google-duplex-roll-out-summer/)

现在，谷歌宣布，从下个月开始，纽约、旧金山湾区、凤凰城和亚特兰大的 Pixel、Pixel 2 和 Pixel 3 用户将可以使用 Duplex。这项服务将只在这些地区提供，至少在开始阶段，因为谷歌在推出这项服务之前必须与企业和城市合作。

### 驾驶模式在这里自动为你启动 Android Auto

在 Pixel 3 发布之前，我们[在 Google Play 服务中发现了](https://www.xda-developers.com/android-pie-driving-mode-android-auto-do-not-disturb/)一个隐藏的驾驶模式功能，后来[向少数用户推出了](https://www.xda-developers.com/automatic-do-not-disturb-driving-mode/)。谷歌 Pixel 2 推出的一项功能是，当你在移动的车辆中时，它可以检测到并自动启用请勿打扰模式，但新的驾驶模式也可以自动启动 Android Auto 并启用请勿打扰模式。谷歌 Pixel 3 在联网设备设置中提供了新的驾驶模式。

### 现在玩历史终于来了

Now Playing 是 Pixel 2 上首次推出的一项功能，它使用你设备的麦克风来记录音频片段，使用设备上的机器学习来构建音频指纹，并结合设备上的数据库和谷歌的海量云数据库来匹配音频指纹和一首已知歌曲。如果有匹配，Now Playing 将通过在始终显示/环境显示和/或作为通知显示歌曲标题，向您显示背景中正在播放的歌曲。然而，一旦你取消了通知或歌曲标题自动消失，就没有简单的内置方法来返回并查看你的手机以前识别的歌曲。随着谷歌 Pixel 3 的推出，这种情况正在发生变化。

谷歌终于将历史添加到了正在播放功能中。如果你进入声音设置中的“正在播放设置”页面，你现在可以访问一个新菜单，显示 Pixel 3 识别的最后几首歌曲。您也可以在主屏幕上添加一个快捷方式，引导您进入此页面。我们不确定为什么谷歌 Pixel 2 上还没有这个功能，因为几个月前我们在 Pixel Ambient Services 上首次发现了这个功能的证据。至少 Play Store 上已经有很多第三方应用程序使用一个简单的 NotificationListener 服务来记录你现在的播放历史，所以你现在不必等待更新来享受这个功能。

### Daydream VR 还能用

没错，谷歌 Daydream VR 依然在 Pixel 3 上工作，按照 [*之路走向 VR*](https://www.roadtovr.com/new-pixel-3-pixel-3-xl-daydream-ready-google-confirms/) 。Pixel 3 XL 的大小与 Pixel 2 XL 几乎相同，因此即使是相同的 Daydream View 耳机也应该很合适。鉴于来自 Oculus 的激烈竞争，我们不确定该平台的未来，但谷歌最近宣布了一些用于独立 Daydream VR 头戴设备的[非常漂亮的功能](https://www.xda-developers.com/daydream-vr-see-through-mode-2d-android-apps/)，因此他们可能仍在努力改善支持 Daydream 的智能手机的 VR 体验。

### 视觉快照中的新功能

今年早些时候，谷歌在谷歌助手中推出了[视觉快照 UI](https://www.xda-developers.com/google-assistant-google-now-cards/) 。视觉快照是一种向您显示重要信息的功能，如即将到来的日历事件、提醒、即将到来的账单、当前天气、当前上班交通等。视觉快照基本上是 Google Now 的精神继承者，只是涂上了一层新鲜的涂料。在谷歌制造的活动中，我们被告知下个月视觉快照将增加两个新功能:你推荐的活动和要记住的事情。

### 一个新的复活节彩蛋

Android Pie 带来了一个相当普通的发光 P 的复活节彩蛋，但 Pixel 3 上的 Android Pie 版本有一个合适的复活节彩蛋。点击原始复活节彩蛋中 P 的中间会打开一个绘图应用程序，你可以在里面画草图。

### 新的谷歌主页和谷歌像素启动器应用

谷歌主页应用程序进行了重大的重新设计，以使其更易于使用。你可以在这里了解更多信息，也可以下载 APK。Pixel Launcher 稍微有点新，因为它现在在搜索栏上有一个谷歌助手图标，并强制使用自适应图标。你可以在这里[看到它](https://www.xda-developers.com/download-google-pixel-launcher-pixel-3/)并在支持的设备上下载 APK。

## 谷歌 Pixel 3 配件

### 像素支架

新的谷歌 Pixel 支架不仅仅是一个无线充电底座。如果你愿意，你可以将新的谷歌 Pixel 3 坞接到任何 Qi 无线充电坞站，但将你的 Pixel 3 坞接到谷歌 Pixel 支架可以为你提供最快的无线充电速度(10W 对 5W)，还可以将谷歌助手集成到始终显示中。在舞台上，谷歌展示了当你将谷歌助手停靠在 Pixel 支架上时，你可以与谷歌助手进行的几个交互。例如，您可以快速进入“我的一天”程序，查看您的视觉快照，随着屏幕颜色的变化慢慢醒来，查看 Google 相册中的相册，等等。然而，有几个功能谷歌在舞台上没有详细介绍。

首先，当 Pixel Stand 向你展示谷歌相册中的照片时，它使用人工智能来裁剪照片，这样任何人都不会从图像中消失。第二，Pixel Stand UI 有 Nest 门铃集成。当一个人按下 Nest 的门铃时，Nest 的视频就会显示在“永远在线”显示屏的正上方——只要你的 Pixel 3 插在 Pixel 支架上，你就不需要解锁手机。

## 多方面的

### 回归 F2FS

凭借高通骁龙 845 芯片组、UFS 2.1 存储和 LPDDR4X RAM，我们预计 Pixel 3 和 Pixel 3 XL 将成为高速设备。真正让谷歌 Pixel 系列区别于大多数采用相同芯片组的设备的是 Pixel 性能团队的[软件优化](https://www.xda-developers.com/google-pixel-fastest-android-phone-eas/)。今年也不例外，谷歌正在尝试回归 F2FS——这是一个由三星开发的文件系统，最初是为了给基于闪存的存储带来高性能。

我们之前在本文和[中讨论了 F2Fs](https://twitter.com/t_murray/status/1049713921836253185) [的好处，根据 Pixel performance 团队的蒂姆·穆雷](https://www.xda-developers.com/f2fs-why-file-systems-matter-interview-stan-dmitriev-tuxera/)的说法，Pixel 3 使用 F2Fs 进行数据分区的原因是“它现在支持内嵌加密硬件”这不是第一款支持 F2FS 的谷歌设备 Nexus 9 以前支持它——但看到谷歌再次开始使用它很有趣。

### 第一个具有新控制流完整性保护的设备

在今年早些时候举行的 Linux 安全峰会上，谷歌工程师透露，下一代 Pixel 设备将是第一款在内核中搭载前沿控制流完整性(CFI)的设备。这是谷歌不断努力为 Android 设备强化 Linux 内核的一部分，今天，他们已经做出了这些新的改变[官方](https://android-developers.googleblog.com/2018/10/control-flow-integrity-in-android-kernel.html)。CFI 防御所谓的“代码重用攻击”，这种攻击劫持内核中的执行流来执行内核代码的任意部分，而不注入自己的代码。

CFI 在 4.9 和 4.14 版本的 Android 通用内核中可用，但这取决于设备供应商来集成这些变化。根据 Google 的说法，[在 Android Pie 中，媒体框架和安全关键组件(如 NFC 和蓝牙)默认启用 CFI。](https://android-developers.googleblog.com/2018/06/compiler-based-security-mitigations-in.html)

### 泰坦安全模块——我们仅有的几个细节

泰坦安全模块的完整文档目前还不可用，但一些谷歌工程师已经发布了推文，为我们提供了一些信息。首先，在对 TWRP 首席开发人员 Dees_Troy 的推特的[回复中，谷歌负责 Android 硬件支持的安全子系统的技术主管 Shawn Willden 表示，新的安全模块将不会用于运行时系统分析。这对 Magisk 用户来说很重要，因为硬件支持的运行时系统分析会使无系统根更加困难。然而，谷歌已经为可信执行环境(TEE)开放了一个 API，所以运行时系统分析仍然可能在未来发生(换句话说，对 Magisk 来说仍然可能有坏消息。)](https://twitter.com/Dees_Troy/status/1049774206487908352)

Chrome OS 安全工程师 Will Drewry 的另一条推文总结了 Titan 安全模块的用途。正如[CopperheadOS 前首席技术官丹尼尔·迈凯(Daniel Micay)解释的](https://twitter.com/DanielMicay/status/1049864087948185600)，泰坦安全模块提供了一个“替代硬件密钥库(而不是信任区)，并取代了用于 Pixel 2 安全芯片的 [Android 验证启动(AVB)状态](https://android.googlesource.com/platform/external/libese/+/master/apps/boot/)和 [Weaver](https://android.googlesource.com/platform/external/libese/+/master/apps/weaver/) 小程序。”根据 Daniel Micay 的说法，“Weaver 是 Pixel 2 安全芯片的主要用例:硬件强制的指数增长的密钥导出延迟。它在托管中保存派生每个配置文件的加密密钥所需的随机令牌，并且仅在获得正确的凭据派生的身份验证令牌时才提供它们。”

### 与项目高音，你会得到许多更新

自从 Project Treble 在 Android 8.0 Oreo 中首次推出以来，我们已经听到了很多关于它的信息，由于供应商测试套件和 GSI 上的 CTS 的引入，Project Treble 在 Android Pie 中已接近完成。我们被告知，搭载 Android Pie 的设备应该能够接收纯框架更新。Treble 是 Essential 能够如此迅速地推出月度安全补丁的重要原因。我们怀疑这也是谷歌能够提供 3 年担保 Android 平台升级的部分原因，从 Pixel 2 系列开始，现在也有 Pixel 3 系列。

注意:为了尊重谷歌的评论禁令，在我们全面审查之前，本文省略了一些细节。