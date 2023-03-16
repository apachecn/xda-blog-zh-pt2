# Chromebooks 可能会获得类似苹果 Boot Camp 的 Windows 10 双引导，带有“篝火”

> 原文：<https://www.xda-developers.com/chromebooks-chrome-os-windows-10-dual-boot-apple-boot-camp-campfire/>

我们所知道的关于 Campfire 的一切，这是谷歌让 Windows 10 在 Chromebooks 上运行的秘密项目。自从谷歌 Pixelbook 首次报道 Windows 10 功能以来，我们一直在密切跟踪发展，以了解谷歌背后发生的事情。我们后来发现证据表明，“篝火”可能是 Chromebook 相当于苹果的新兵训练营。

今年早些时候，Chromium Git 上出现了一个神秘的项目。Chrome OS 开发人员已经创建了 Google Pixelbook 的一个新固件分支，名为 eve-campfire，并且正在为这个分支开发一个新的“Alt OS 模式”。自从[证实这个 Alt OS 指的是微软 Windows 10](https://www.xda-developers.com/google-pixelbook-microsoft-windows-10/) 之后，我们发现证据表明它不仅仅是一个内部项目，而是打算公开发布。

距离我们的上一个专题已经过去几周了，我们有更多有趣的细节要分享。

## 谷歌 Pixelbook 不会是唯一一款支持篝火的 Chromebook

公平地说，Alt OS 和 Campfire 不会出现在数百台 Chromebooks 上，但如果这只是注定要出现在谷歌 Pixelbook 上，开发者的时间将会浪费。提到了多个“campfire 变体”、“T1”以及合并到主分支而不是特定于设备的分支的更改，这表明谷歌 Pixelbook 不会是唯一一个支持 Campfire 的 Chromebook。然而，鉴于这种支持意味着对设备进行额外的测试和配置，它可能仅限于选择 chrome book——可能只是新设备，甚至只是谷歌品牌的设备。现在说还为时过早。

## Campfire 不需要在 Chrome 操作系统中启用开发者模式

传统上，在 Chromebook 上双启动其他操作系统需要启用开发者模式，这是 Chrome 操作系统上一种不方便但功能强大的模式，每次启动时只需点击空格键即可使用 Chromebook。不幸的是，启用开发者模式也会禁用验证启动等功能，从而降低 Chromebook 的安全性。由于谷歌将直接支持 Chromebook 上的双启动，因此启用 Alt OS 模式并启动到微软 Windows 10 [将不需要开发者模式](https://chromium-review.googlesource.com/c/chromiumos/platform/depthcharge/+/1127904)。

## 将 Campfire 设置为双启动 Windows 10 是无缝的

开发人员重新设计了他们向 Chromebooks 上很少使用的 ROM 部分 RW_LEGACY 发布更新的方式。chrome book ROM 上的 RW_LEGACY 部分传统上为用户提供了双重引导至替代操作系统的能力，但这是生产过程中的事后想法，设备出厂后该部分很少更新。现在，有了 Campfire，谷歌将通过常规的自动更新过程将[签名的更新推送到 RW_LEGACY](https://chromium-review.googlesource.com/c/chromiumos/platform/depthcharge/+/1127904) 中，因此固件刷新将不会成为 Joe Public 的一个问题。最近，[通过 crosh](https://chromium-review.googlesource.com/c/chromiumos/platform2/+/1170675) 使用一个简单的[alt_os enable]命令启用 Alt OS，这表明从用户端来说，这将是一个相当容易的设置过程。

## 篝火比你想象的更接近释放

在这个阶段，Campfire 和 Alt OS 模式显然是不完整的，没有任何 UI 变化可言。然而，开发人员一直在努力争取尽早合并更改，这表明 Chrome 路线图的时间表很紧。谷歌的硬件盛会即将到来，有传言称[谷歌 Pixelbook v2 将与严重泄露的谷歌 Pixel 3 和谷歌 Pixel 3 XL 一起推出](https://www.xda-developers.com/google-pixelbook-2018-rumor-chromebook)。即使完整的功能还没有准备好，也有理由期待在这次活动中发布或演示。

## 篝火会占用你相当大的存储空间

如果你希望你的 2013 款宏碁 C720 能以某种方式获得支持，16GB 的存储空间不会削减它。最近的一条评论和 crosh 源代码表明，最低存储要求将是 40GB (30GB 用于 Windows，10GB 用于 Chrome OS)，这使得大多数带有焊接 eMMC 的 Chromebooks 不可能实现这一要求。

Campfire 为 Chrome OS 引入了一个我们从未见过的激动人心的新动态。如果一年前你建议在 Chrome 操作系统上安装谷歌支持的 Windows 10 双引导，你会被笑出房间。买了 Chromebook 不喜欢软件？运气不好，除非你想跳过许多技术难关，否则你会被它困住。考虑到苹果的新兵训练营，谷歌看起来很棘手。

无论你是否是 Chrome OS 的粉丝，安全和简单的双重启动对消费者来说都是一个明显的胜利——这是谷歌在上个月€50 亿美元反垄断罚款后迫切需要展示的。无痛双启动还将为用户提供一种方法，在谷歌任意设定的 6.5 年 EOL 里程碑之后继续安全地使用他们的设备——这比填埋功能完美的硬件要好。无论动机是什么，Google 激起了我们的兴趣，我们将继续在整个开发过程中关注 Campfire 和 Alt OS。